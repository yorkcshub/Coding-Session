# Sorting Technique

### Counting Sort
The algorithm loops over the items, computing the number of times each key occurs within the input collection.

```python
for x in input:
    count[key(x)] += 1

# calculate the starting index for each key:
total = 0
for i in range(k):   # i = 0, 1, ... k-1
    oldCount = count[i]
    count[i] = total
    total += oldCount

# copy to output array, preserving order of inputs with equal keys:
for x in input:
    output[count[key(x)]] = x
    count[key(x)] += 1

return output
```

## Type of problems that involve sorting
- Greedy problem (choosing k items which give the highest value in n items).
- Searching problem/determine the position of a desired item
- Related to the frequency of each item in an array of integers (counting sort).
- Etc

## Some practice problems

[Gravity Flip - Very Easy](http://codeforces.com/problemset/problem/405/A)

[Sale - Very Easy](http://codeforces.com/problemset/problem/34/B)

Once Bob got to a sale of old TV sets. There were n TV sets at that sale. TV set with index i costs ai bellars. Some TV sets have a negative price — their owners are ready to pay Bob if he buys their useless apparatus. Bob can «buy» any TV sets he wants. Though he's very strong, Bob can carry at most m TV sets, and he has no desire to go to the sale for the second time. Please, help Bob find out the maximum sum of money that he can earn.

__Input:__ The first line contains two space-separated integers n and m (1 ≤ m ≤ n ≤ 100) — amount of TV sets at the sale, and amount of TV sets that Bob can carry. The following line contains n space-separated integers ai (-1000 ≤ ai ≤ 1000) — prices of the TV sets.

__Output:__ Output the only number — the maximum sum of money that Bob can earn, given that he can carry at most m TV sets.

__Sample Input 1:__
```
5 3
-6 0 35 -2 4
```
__Sample Output 1:__
```
8
```
__Sample Input 2:__
```
4 2
7 0 0 -7
```
__Sample Output 2:__
```
7
```

[Game - Easy](http://codeforces.com/problemset/problem/984/A)

Two players play a game.

Initially there are n integers a1, a2, …, an written on the board. Each turn a player selects one number and erases it from the board. This continues until there is only one number left on the board, i. e. n−1 turns are made. The first player makes the first move, then players alternate turns.

The first player wants to minimize the last number that would be left on the board, while the second player wants to maximize it.

You want to know what number will be left on the board after n−1 turns if both players make optimal moves.

__Input:__
The first line contains one integer n (1 ≤ n ≤ 1000) — the number of numbers on the board.

The second line contains n integers a1, a2, …, an (1 ≤ ai ≤106).

__Output:__
Print one number that will be left on the board.

__Sample Input 1:__
```
3
2 1 3
```
__Sample Output 1:__
```
2
```
__Sample Input 2:__
```
3
2 2 2
```
__Sample Output 2:__
```
2
```

[Twins - Easy](http://codeforces.com/problemset/problem/160/A)

Imagine that you have a twin brother or sister. Having another person that looks exactly like you seems very unusual. It's hard to say if having something of an alter ego is good or bad. And if you do have a twin, then you very well know what it's like.

Now let's imagine a typical morning in your family. You haven't woken up yet, and Mom is already going to work. She has been so hasty that she has nearly forgotten to leave the two of her darling children some money to buy lunches in the school cafeteria. She fished in the purse and found some number of coins, or to be exact, n coins of arbitrary values a1, a2, ..., an. But as Mom was running out of time, she didn't split the coins for you two. So she scribbled a note asking you to split the money equally.

As you woke up, you found Mom's coins and read her note. "But why split the money equally?" — you thought. After all, your twin is sleeping and he won't know anything. So you decided to act like that: pick for yourself some subset of coins so that the sum of values of your coins is strictly larger than the sum of values of the remaining coins that your twin will have. However, you correctly thought that if you take too many coins, the twin will suspect the deception. So, you've decided to stick to the following strategy to avoid suspicions: you take the minimum number of coins, whose sum of values is strictly more than the sum of values of the remaining coins. On this basis, determine what minimum number of coins you need to take to divide them in the described manner.

__Input:__ The first line contains integer n (1 ≤ n ≤ 100) — the number of coins. The second line contains a sequence of n integers a1, a2, ..., an (1 ≤ ai ≤ 100) — the coins' values. All numbers are separated with spaces.

__Output:__ In the single line print the single number — the minimum needed number of coins.

__Sample Input 1:__
```
2
3 3
```
__Sample Output 1:__
```
2
```
__Sample Input 2:__
```
3
2 1 2
```
__Sample Output 2:__
```
2
```

[DVDs - Medium](https://open.kattis.com/problems/dvds)

Dezider is very unhappy as he just discovered that his DVDs got unsorted. Dezider is (occasionally) very organized and during one of his get-organized spells he numbered the DVDs __from 1 to n__. He keeps the DVDs in a tall stack and he wants to have them sorted in increasing order by their number, with 1 at the bottom and n at the top of the stack. The trouble is that his space allows him to perform only one type of sorting operation: take a DVD, pull it out of the stack while the DVDs above it fall down by one position, then place it at the top of the stack. What is the smallest number of such operations he needs to do to sort the DVD stack?

__Input:__
The first line contains k, the number of input instances. Each input instance is described on two lines. The first line contains 1 ≤ n ≤ 1000000. The second line lists the DVDs in the initial order on the stack, from the bottom to the top.

__Output:__
The output contains k lines. The i-th line corresponds to the i-th input. It contains the smallest number of operations needed to sort the stack.

__Note:__
In the first sample input it suffices to take DVD 4 and move it to the top of the stack; then the stack is sorted. In the second sample input one can first move DVD 4 and then DVD 5 to get a sorted stack.

__Sample Input:__
```
2
4
1 4 2 3
5
5 1 2 4 3
```

__Sample OutputL__
```
1
2
```

_This problem appeared in York University 2018 First ACM Contest._

