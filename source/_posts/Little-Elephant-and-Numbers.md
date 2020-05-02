---
title: Codeforces 221B Little Elephant and Numbers
date: 2019-10-15 13:25:56
tags:
    - 新手 
    - implementation
---
[Codeforces 221B](https://codeforces.com/problemset/problem/221/B)
<!-- more -->
The Little Elephant loves numbers.

He has a positive integer x. The Little Elephant wants to find the number of positive integers d, such that d is the divisor of x, and x and d have at least one common (the same) digit in their decimal representations.

Help the Little Elephant to find the described number.
<!-- more -->
#### Input:
A single line contains a single integer x (1 ≤ x ≤ 10<sup>9</sup>).
#### Output:
In a single line print an integer — the answer to the problem.
#### 範例:
input:
```
1
```
output:
```
1
```
input:
```
10
```
output:
```
2
```

#### 題意:
輸入N，問你所有N的因數中，有幾個因數有使用到N本身使用過的數字。

#### 思路:
找因數只需要找到平方根就好。另一邊的因數可以用除的得知。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/572bf3a7c7b6f81a7a57a5831208c312.js"></script>

