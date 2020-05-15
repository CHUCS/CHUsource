---
title: Codeforces 977A v1
date: 2019-03-07 18:41:32
tags:
    - CHU Training
    - CodeForces
    - implementation
    - 新手
---
[Wrong Subtraction](https://codeforces.com/problemset/problem/977/A)

Little girl Tanya is learning how to decrease a number by one, but she does it wrong with a number consisting of two or more digits. Tanya subtracts one from a number by the following algorithm:
<!-- more -->
● if the last digit of the number is non-zero, she decreases the number by one;
● if the last digit of the number is zero, she divides the number by 10 (i.e. removes the last digit).

You are given an integer number n. Tanya will subtract one from it k times. Your task is to print the result after all k subtractions.

It is guaranteed that the result will be positive integer number.

#### Input:
The first line of the input contains two integer numbers n and k (2≤n≤10<sup>9</sup>, 1≤k≤50) — the number from which Tanya will subtract and the number of subtractions correspondingly.

#### Output:
Print one integer number — the result of the decreasing n by one k times.

It is guaranteed that the result will be positive integer number.

#### 範例:
input:
```
512 4
```
output:
```
50
```
input:
```
1000000000 9
```
output:
```
1
```
#### Note:
The first example corresponds to the following sequence: 512→511→510→51→50.
#### 題意:
N為一個整數，K為減少的次數。
這題的規則是:
  1.如果該數字的最後一位數字不為零，則將該數字減少一個。
  2.如果數字的最後一位為零，則將數字除以10（即刪除最後一位數字）。
#### 思路:
按照規則走。

#### 程式碼:

<script src="https://gist.github.com/Daviswww/4d41d72d84689b5e9c0a91dd551393fe.js"></script>

