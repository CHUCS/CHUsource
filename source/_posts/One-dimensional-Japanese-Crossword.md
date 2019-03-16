---
title: One-dimensional Japanese Crossword
date: 2019-03-09 18:42:21
tags:
    - CHU Training
    - CodeForces
---
Recently Adaltik discovered japanese crosswords. Japanese crossword is a picture, represented as a table sized a × b squares, and each square is colored white or black. There are integers to the left of the rows and to the top of the columns, encrypting the corresponding row or column. The number of integers represents how many groups of black squares there are in corresponding row or column, and the integers themselves represents the number of consecutive black squares in corresponding group (you can find more detailed explanation in Wikipedia https://en.wikipedia.org/wiki/Japanese_crossword).

Adaltik decided that the general case of japanese crossword is too complicated and drew a row consisting of n squares (e.g. japanese crossword sized 1 × n), which he wants to encrypt in the same way as in japanese crossword.
![A](A.PNG)
Help Adaltik find the numbers encrypting the row he drew.
<!-- more -->
#### Input:
The first line of the input contains a single integer n (1 ≤ n ≤ 100) — the length of the row. The second line of the input contains a single string consisting of n characters 'B' or 'W', ('B' corresponds to black square, 'W' — to white square in the row that Adaltik drew).

#### Output:
The first line should contain a single integer k — the number of integers encrypting the row, e.g. the number of groups of black squares in the row.

The second line should contain k integers, encrypting the row, e.g. corresponding to sizes of groups of consecutive black squares in the order from left to right.

#### 範例:
input:
```
3
BBW
```
output:
```
1
2 
```
input:
```
5
BWBWB
```
output:
```
3
1 1 1 
```
input:
```
4
WWWW
```
output:
```
0
```
input:
```
4
BBBB
```
output:
```
1
4 
```
input:
```
13
WBBBBWWBWBBBW
```
output:
```
3
4 1 3 
```

#### Note:
The last sample case correspond to the picture in the statement.

#### 題意:
這題簡單來說呢就是找出有多少個連續'B'的區間，第一行輸出總共這條字串有幾組連續'B'的區間，第二行則輸出每組區間'B'得數量。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/b18a15fe05325da585fab6348f062d1c.js"></script>

[題目網址](https://codeforces.com/problemset/problem/721/A)