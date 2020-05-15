---
title: Codeforces 588B
date: 2019-10-26 11:28:10
tags:
    - math
---
# Codeforces 588B - Duff in Love
[Duff in Love](https://codeforces.com/contest/588/problem/B)

Duff is in love with lovely numbers! A positive integer x is called lovely if and only if there is no such positive integer a > 1 such that a2 is a divisor of x.
<!-- more -->

Malek has a number store! In his store, he has only divisors of positive integer n (and he has all of them). As a birthday present, Malek wants to give her a lovely number from his store. He wants this number to be as big as possible.

Malek always had issues in math, so he asked for your help. Please tell him what is the biggest lovely number in his store.

#### Input:
The first and only line of input contains one integer, n (1 ≤ n ≤ 10<sup>12</sup>).

#### Output:
Print the answer in one line.

#### 範例:
input:
```
10
```
output:
```
10
```
input:
```
12
```
output:
```
6
```


#### Note:
In first sample case, there are numbers 1, 2, 5 and 10 in the shop. 10 isn't divisible by any perfect square, so 10 is lovely.

In second sample case, there are numbers 1, 2, 3, 4, 6 and 12 in the shop. 12 is divisible by 4 = 2<sup>2</sup>, so 12 is not lovely, while 6 is indeed lovely.

#### 題意:
輸入它給你一個數字n，它因數分解的集合的因數分解不希望有任何可以被開根號的因數。如果有，希望你能把他丟棄，然後再組成新的數。

#### 思路:
n做出質因數分解，把重複出現的數去除，再把集合裡的數相乘，這樣就不會有可以被開根號的因數了。

#### 程式碼:

<script src="https://gist.github.com/89snnfk561/fc37c058fd2adfcffbd5b71e68747a2e.js"></script>


