---
title: Codeforces 992A
date: 2019-04-12 22:54:38
tags:
    - CHU Training
    - CodeForces
    - sortings
    - 簡單
---
# Codeforces 992A - Nastya and an Array
[Nastya and an Array](https://codeforces.com/problemset/problem/992/A)

Nastya owns too many arrays now, so she wants to delete the least important of them. However, she discovered that this array is magic! Nastya now knows that the array has the following properties:
<!-- more -->
In one second we can add an arbitrary (possibly negative) integer to all elements of the array that are not equal to zero.
When all elements of the array become equal to zero, the array explodes.
Nastya is always busy, so she wants to explode the array as fast as possible. Compute the minimum time in which the array can be exploded.

#### Input:
The first line contains a single integer n (1 ≤ n ≤ 10<sup>5</sup>) — the size of the array.

The second line contains n integers a<sub>1</sub>, a<sub>2</sub>, ..., a<sub>n</sub> ( - 10<sup>5</sup> ≤ a<sub>i<sub> ≤ 10<sup>5</sup>) — the elements of the array.

#### Output:
Print a single integer — the minimum number of seconds needed to make all elements of the array equal to zero.

#### 範例:
input:
```
5
1 1 1 1 1
```
output:
```
1
```
input:
```
3
2 0 -1
```
output:
```
2
```
input:
```
4
5 -6 -5 1
```
output:
```
4
```
#### Note:
In the first example you can add  - 1 to all non-zero elements in one second and make them equal to zero.

In the second example you can add  - 2 on the first second, then the array becomes equal to [0, 0,  - 3]. On the second second you can add 3 to the third (the only non-zero) element.

#### 題意:
現在一次行動可以將一個陣列的非0數字都加上某個數字，問你需要幾次行動才能將陣列全部歸0？

#### 思路:
題目等於是判斷現在陣列裡面有幾種數字，因此將陣列排序後，判斷非0的數字有幾種。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/7560d8637db8515e9a9320738b5bcace.js"></script>

