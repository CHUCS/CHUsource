---
title: Lucky Division
date: 2019-03-09 18:48:00
tags:
    - CHU Training
    - CodeForces
    - implementation
    - math
    - 新手
---
Petya loves lucky numbers. Everybody knows that lucky numbers are positive integers whose decimal representation contains only the lucky digits 4 and 7. For example, numbers 47, 744, 4 are lucky and 5, 17, 467 are not.

Petya calls a number almost lucky if it could be evenly divided by some lucky number. Help him find out if the given number n is almost lucky.
<!-- more -->
#### Input:
The single line contains an integer n (1 ≤ n ≤ 1000) — the number that needs to be checked.

#### Output:
In the only line print "YES" (without the quotes), if number n is almost lucky. Otherwise, print "NO" (without the quotes).

#### 範例:
input:
```
47
```
output:
```
YES
```
input:
```
16
```
output:
```
YES
```
input:
```
78
```
output:
```
NO
```
#### Note:
Note that all lucky numbers are almost lucky as any number is evenly divisible by itself.

In the first sample 47 is a lucky number. In the second sample 16 is divisible by 4.

#### 題意:
找出信幸運數字。

#### 思路:
這題再找一個幸運的數字，因為N小於1000所以我們直接把1000以內幸運數字存在陣列裡面，題目也說道如果有數字可以被幸運數字整除，那麼它也是幸運數字。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/79c825a14fee509b9061b7d4fae97c74.js"></script>


[題目網址](https://codeforces.com/problemset/problem/122/A)