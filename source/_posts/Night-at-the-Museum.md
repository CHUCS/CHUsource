---
title: CodeForces 731A
date: 2020-04-07 13:44:09
keywords: Codeforces 731A, Codeforces Night at the Museum
tags:
    - implementation
    - strings
    - 簡單
---
# CodeForces 731A - Night at the Museum
[Night at the Museum](https://codeforces.com/problemset/problem/731/A)


#### 題意:
給你一個轉盤式的密碼鎖以及密碼，問你最少需要轉幾個刻度才能輸入完密碼(輸入每個字後不會強制回到a) ？
<!-- more -->
#### 思路:
每次旋轉都挑正反兩個方向中次數少的那邊。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/fabe31e27089cdced4c29c309941d198.js"></script>