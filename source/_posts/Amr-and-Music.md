---
title: Codeforces 507A
date: 2019-03-21 09:51:53
keywords: Codeforces 507A, Codeforces Amr and Music
categories: Codeforces
tags:
    - CodeForces
    - sortings
    - greedy
    - 簡單
---
# Codeforces 507A - Amr and Music
[Amr and Music](https://codeforces.com/problemset/problem/507/A)

Amr is a young coder who likes music a lot. He always wanted to learn how to play music but he was busy coding so he got an idea.
<!-- more -->
Amr has n instruments, it takes a<sub>i</sub> days to learn i-th instrument. Being busy, Amr dedicated k days to learn how to play the maximum possible number of instruments.

Amr asked for your help to distribute his free days between instruments so that he can achieve his goal.

#### Input:
The first line contains two numbers n, k (1 ≤ n ≤ 100, 0 ≤ k ≤ 10 000), the number of instruments and number of days respectively.

The second line contains n integers ai (1 ≤ a<sub>i</sub> ≤ 100), representing number of days required to learn the i-th instrument.

#### Output:
In the first line output one integer m representing the maximum number of instruments Amr can learn.

In the second line output m space-separated integers: the indices of instruments to be learnt. You may output indices in any order.

if there are multiple optimal solutions output any. It is not necessary to use all days for studying.

#### 範例:

input:
```
4 10
4 3 1 2
```
output:
```
4
1 2 3 4
```
input:
```
5 6
4 3 1 1 2
```
output:
```
3
1 3 4
```
input:
```
1 3
4
```
output:
```
0
```

#### Note:
In the first test Amr can learn all 4 instruments.

In the second test other possible solutions are: {2, 3, 5} or {3, 4, 5}.

In the third test Amr doesn't have enough time to learn the only presented instrument.

#### 題意:
現在有k天的時間，他想要盡量學一些樂器，學第i種樂器的時間需要a<sub>i</sub>天，請問最多可以學幾種樂器，分別是哪幾種？

#### 思路:
因為需要印出是哪幾種，所以不能直接排序，新建一個struct，存編號跟天數，然後再依據天數由小排到大。然後一直減k，直到沒得減了或k小於0了為止，最後輸出答案。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/9f680592a720d787b000254aefbb2d03.js"></script>

