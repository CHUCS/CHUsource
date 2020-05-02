---
title: Codeforces 1028C Rectangles
date: 2019-09-30 20:11:22
tags:
    - 普通
    - geometry
    - implementation
    - sortings
---
[Codeforces 1028C](https://codeforces.com/problemset/problem/1028/C)
<!-- more -->
You are given n rectangles on a plane with coordinates of their bottom left and upper right points. Some (n−1) of the given n rectangles have some common point. A point belongs to a rectangle if this point is strictly inside the rectangle or belongs to its boundary.

Find any point with integer coordinates that belongs to at least (n−1) given rectangles.

#### Input:
The first line contains a single integer n (2≤n≤132674) — the number of given rectangles.

Each the next n lines contains four integers x1, y1, x2 and y2 (−10<sup>9</sup>≤x1<x2≤10<sup>9</sup>, −10<sup>9</sup>≤y1<y2≤10<sup>9</sup>) — the coordinates of the bottom left and upper right corners of a rectangle.
#### Output:
Print two integers x and y — the coordinates of any point that belongs to at least (n−1) given rectangles.
#### 範例:
input:
```
3
0 0 1 1
1 1 2 2
3 0 4 1
```
output:
```
1 1
```
input:
```
3
0 0 1 1
0 1 1 2
1 0 2 1
```
output:
```
1 1
```
input:
```
4
0 0 5 5
0 0 4 4
1 1 4 4
1 1 4 4
```
output:
```
1 1
```
input:
```
5
0 0 10 8
1 2 6 7
2 3 5 6
3 4 4 5
8 1 9 2
```
output:
```
3 4
```
#### Note:
The picture below shows the rectangles in the first and second samples. The possible answers are highlighted.
![A](A.PNG)
The picture below shows the rectangles in the third and fourth samples.
![B](B.PNG)
#### 題意:
提供n個矩形，其坐標分別為左下角和右上角。 給定的n個矩形中的某些（n-1）個具有一些公共點。 如果某點嚴格位於矩形內或屬於其邊界，則該點屬於矩形。

找具有至少屬於（n-1）個給定矩形的整數坐標的任何點。
#### 思路:
要在N−1個矩形中，因此只要一個一個刪去後，判斷剩下的N−1 個矩形有沒有套在一起就可以了。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/9bd6c597f308d42107b1326c4e318330.js"></script>

