---
title: Codeforces 976B
date: 2019-04-20 18:50:14
link: Lara-Croft-and-the-New-Game
keywords: CodeForces 976B, CodeForces Lara Croft and the New Game
tags:
    - implementation
    - math
    - 簡單
---
# Codeforces 976B - Lara Croft and the New Game
[Lara Croft and the New Game](https://codeforces.com/problemset/problem/976/B)

You might have heard about the next game in Lara Croft series coming out this year. You also might have watched its trailer. Though you definitely missed the main idea about its plot, so let me lift the veil of secrecy.
<!-- more -->
Lara is going to explore yet another dangerous dungeon. Game designers decided to use good old 2D environment. The dungeon can be represented as a rectangle matrix of n rows and m columns. Cell (x, y) is the cell in the x-th row in the y-th column. Lara can move between the neighbouring by side cells in all four directions.

Moreover, she has even chosen the path for herself to avoid all the traps. She enters the dungeon in cell (1, 1), that is top left corner of the matrix. Then she goes down all the way to cell (n, 1) — the bottom left corner. Then she starts moving in the snake fashion — all the way to the right, one cell up, then to the left to the cell in 2-nd column, one cell up. She moves until she runs out of non-visited cells. n and m given are such that she always end up in cell (1, 2).

Lara has already moved to a neighbouring cell k times. Can you determine her current position?

#### Input:
The only line contains three integers n, m and k (2 ≤ n, m ≤ 10<sup>9</sup>, n is always even, 0 ≤ k < n·m). Note that k doesn't fit into 32-bit integer type!

#### Output:
Print the cell (the row and the column where the cell is situated) where Lara ends up after she moves k times.

#### 範例:
input:
```
4 3 0
```
output:
```
1 1
```
input:
```
4 3 11
```
output:
```
1 2
```
input:
```
4 3 11
```
output:
```
1 2
```
#### Note:
Here is her path on matrix 4 by 3:
![A](A.PNG)
#### 題意:
給你一個矩形棋盤，走法是先走最左邊一排，再蛇行往上。問你在第k步時的座標是多少？

#### 思路:
先計算是不是在最左邊那排，不是的話再計算他從最下面往上走了幾排又幾格。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/86b71f83f8144585dee9e5ae223c527b.js"></script>

