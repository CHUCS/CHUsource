---
title: CodeForces 1324A
date: 2020-03-20 13:24:32
tags:
    - implementation
    - number theory
    - 簡單
---
# CodeForces 1324A - Yet Another Tetris Problem
[Yet Another Tetris Problem](https://codeforces.com/problemset/problem/1324/A)


#### 題意:
給你一個俄羅斯方塊現在每一排的高度，你只能使用高2寬1的方塊，且不能旋轉。問你是否能將所有方塊全部消除？
<!-- more -->
#### 思路:
因為不能旋轉，所以先記錄最高的排高度是多少，然後計算該排跟其他所有排的高度差，如果都能被2整除，那就輸出YES；否則輸出NO。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/42cc0cba34f5e3eb8bdf0709ec72f3d5.js"></script>