---
title: Codeforces 38A
date: 2019-04-20 18:50:00
tags:
    - implementation
    - 新手
---
[Army](https://codeforces.com/problemset/problem/38/A)

The Berland Armed Forces System consists of n ranks that are numbered using natural numbers from 1 to n, where 1 is the lowest rank and n is the highest rank.
<!-- more -->
One needs exactly di years to rise from rank i to rank i + 1. Reaching a certain rank i having not reached all the previous i - 1 ranks is impossible.

Vasya has just reached a new rank of a, but he dreams of holding the rank of b. Find for how many more years Vasya should serve in the army until he can finally realize his dream.

#### Input:
The first input line contains an integer n (2 ≤ n ≤ 100). The second line contains n - 1 integers d<sub>i</sub> (1 ≤ d<sub>i</sub> ≤ 100). The third input line contains two integers a and b (1 ≤ a < b ≤ n). The numbers on the lines are space-separated.

#### Output:
Print the single number which is the number of years that Vasya needs to rise from rank a to rank b.

#### 範例:
input:
```
3
5 6
1 2
```
output:
```
5
```
input:
```
3
5 6
1 3
```
output:
```
11
```
#### 題意:
給你所有階級升級的需要年數，問你從a階升到b階要多少年？

#### 思路:
直接累加。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/c83a93cdf39d598e109761dbb0bd09f1.js"></script>
