---
title: Codeforces 165B
date: 2019-03-21 09:51:31
keywords: Codeforces 165B, Codeforces Burning Midnight Oil
categories: Codeforces
tags:
    - CodeForces
    - binary search
    - implementation
    - 普通
---
# Codeforces 165B - Burning Midnight Oil
[Burning Midnight Oil](https://codeforces.com/problemset/problem/165/B)

One day a highly important task was commissioned to Vasya — writing a program in a night. The program consists of n lines of code. Vasya is already exhausted, so he works like that: first he writes v lines of code, drinks a cup of tea, then he writes as much as ⌊v/k⌋ lines, drinks another cup of tea, then he writes ⌊v/k<sup>2</sup>⌋ lines and so on: ⌊v/k<sup>3</sup>⌋ , ⌊v/k<sup>4</sup>⌋ , ⌊v/k<sup>5</sup>⌋ , ...
<!-- more -->
The expression ⌊a/b⌋is regarded as the integral part from dividing number a by number b.

The moment the current value ⌊v/k<sup>p</sup>⌋ equals 0, Vasya immediately falls asleep and he wakes up only in the morning, when the program should already be finished.

Vasya is wondering, what minimum allowable value v can take to let him write not less than n lines of code before he falls asleep.

#### Input:
The input consists of two integers n and k, separated by spaces — the size of the program in lines and the productivity reduction coefficient, 1 ≤ n ≤ 10<sup>9</sup>, 2 ≤ k ≤ 10.

#### Output:
Print the only integer — the minimum value of v that lets Vasya write the program in one night.

#### 範例:

input:
```
7 2
```
output:
```
4
```
input:
```
59 9
```
output:
```
54
```
#### Note:
In the first sample the answer is v = 4. Vasya writes the code in the following portions: first 4 lines, then 2, then 1, and then Vasya falls asleep. Thus, he manages to write 4 + 2 + 1 = 7 lines in a night and complete the task.

In the second sample the answer is v = 54. Vasya writes the code in the following portions: 54, 6. The total sum is 54 + 6 = 60, that's even more than n = 59.

#### 題意:
他現在快睡著了，寫了v行程式碼之後就必須喝一杯茶，然後就能繼續寫⌊𝑣/𝑘⌋行程式碼；再喝一杯茶，能再寫⌊𝑣/𝑘<sup>2</sup>⌋行程式碼，當⌊𝑣/𝑘<sup>𝑝</sup>⌋等於0的時候就會立刻睡著。現在問你假如他必須寫出至少n行程式碼的話，v最少要是多少？

#### 思路:
需要n行，因此v=0時一定不行，v=n時一定可以，所以在0~n中做二分搜尋法必定可以找到答案。
● 若是v=mid時算出來的行數等於n，則mid就是最小值。
● 若是v=mid時算出來的行數大於n，則mid有可能是答案，將最小值記起來再減少上限找看看有沒有可能更小。
● 若是v=mid時算出來的行數小於n，則mid不可能是答案，增加下限找看看有沒有可能的答案。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/9316d78bd8016b0996ffd5fceeb75ffd.js"></script>


