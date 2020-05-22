---
title: Codeforces 653A
date: 2019-03-14 10:02:47
keywords: Codeforces 653A, Codeforces Bear and Three Balls
categories: Codeforces
tags:
    - CodeForces
    - sortings
    - 簡單
---
# Codeforces 653A - Bear and Three Balls
[Bear and Three Balls](https://codeforces.com/problemset/problem/653/A)

Limak is a little polar bear. He has n balls, the i-th ball has size t<sub>i</sub>.
<!-- more -->
Limak wants to give one ball to each of his three friends. Giving gifts isn't easy — there are two rules Limak must obey to make friends happy:

● No two friends can get balls of the same size.
● No two friends can get balls of sizes that differ by more than 2.
For example, Limak can choose balls with sizes 4, 5 and 3, or balls with sizes 90, 91 and 92. But he can't choose balls with sizes 5, 5 and 6 (two friends would get balls of the same size), and he can't choose balls with sizes 30, 31 and 33 (because sizes 30 and 33 differ by more than 2).

Your task is to check whether Limak can choose three balls that satisfy conditions above.

#### Input:
The first line of the input contains one integer n (3 ≤ n ≤ 50) — the number of balls Limak has.

The second line contains n integers t<sub>1</sub>, t<sub>2</sub>, ..., t<sub>n</sub> (1 ≤ t<sub>i</sub> ≤ 1000) where ti denotes the size of the i-th ball.

#### Output:
Print "YES" (without quotes) if Limak can choose three balls of distinct sizes, such that any two of them differ by no more than 2. Otherwise, print "NO" (without quotes).

#### 範例:

input:
```
4
18 55 16 17
```
output:
```
YES
```
input:
```
6
40 41 43 44 44 44
```
output:
```
NO
```
input:
```
8
5 972 3 4 1 4 970 971
```
output:
```
YES
```
#### Note:
In the first sample, there are 4 balls and Limak is able to choose three of them to satisfy the rules. He must must choose balls with sizes 18, 16 and 17.

In the second sample, there is no way to give gifts to three friends without breaking the rules.

In the third sample, there is even more than one way to choose balls:

>>1. Choose balls with sizes 3, 4 and 5.
>>2. Choose balls with sizes 972, 970, 971.

#### 題意:
一隻熊要送他的三個朋友各一顆球，有兩個條件，(a)不能一樣大，(b)不能有兩個人的球的大小差距超過2。給你一些球，問你能不能挑出符合條件的三顆球？

#### 思路:
綜合兩個條件，唯一能符合的球的大小就是N，N+1，N+2，因此先小到大排序，然後從小的開始找有沒有出現三個連續大小的球。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/20b935d0b2db96a90f0c8265f25e0cfb.js"></script>

