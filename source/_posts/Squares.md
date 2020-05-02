---
title: Codeforces 263B Squares
date: 2019-03-14 10:02:24
tags:
    - CHU Training
    - CodeForces
    - sortings
    - math
    - 簡單
---
[Codeforces 263B](https://codeforces.com/problemset/problem/263/B)
<!-- more -->
Vasya has found a piece of paper with a coordinate system written on it. There are n distinct squares drawn in this coordinate system. Let's number the squares with integers from 1 to n. It turned out that points with coordinates (0, 0) and (ai, ai) are the opposite corners of the i-th square.

Vasya wants to find such integer point (with integer coordinates) of the plane, that belongs to exactly k drawn squares. We'll say that a point belongs to a square, if the point is located either inside the square, or on its boundary.

Help Vasya find a point that would meet the described limits.


#### Input:
The first line contains two space-separated integers n, k (1 ≤ n, k ≤ 50). The second line contains space-separated integers a<sub>1</sub>, a<sub>2</sub>, ..., a<sub>n</sub> (1 ≤ a<sub>i</sub>≤ 10<sup>9</sup>).
#### Output:
In a single line print two space-separated integers x and y (0 ≤ x, y ≤ 10<sup>9</sup>) — the coordinates of the point that belongs to exactly k squares. If there are multiple answers, you are allowed to print any of them.

If there is no answer, print "-1" (without the quotes).

#### 範例:

input:
``` 
4 3
5 1 3 4
```
output:
```
2 1
```
input:
```
3 1
2 4 1
```
output:
```
4 0
```
input:
```
4 50
5 1 10 2
```
output:
```
-1
```
#### 題意:
在平面上有N個正方形，左下點都對齊(0, 0)，請你找一個點，這個點剛好在K個正方形內，邊長保證都不會重複。

#### 思路:
因為左下角都對齊了，而且是正方型又不會重複，所以只要從大的開始往小的找K個，假設他的邊長為L，則(L, 0)就是答案。
![A](A.PNG)
#### 程式碼:
<script src="https://gist.github.com/Daviswww/a765b492ae4bf0e41cceabef430761ea.js"></script>

