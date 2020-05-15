---
title: Codeforces 476A
date: 2020-04-30 17:12:17
tags:
    - implementation
    - math
    - 簡單
---
[Dreamoon and Stairs](https://codeforces.com/problemset/problem/476/A)


#### 題意:
n個台階，1次能爬1~2階，現在希望爬的次數是m的倍數且最小，請你輸出最小的可能次數，不能就輸出-1？
<!-- more -->
#### 思路:
先計算最少的步數(a)跟最多的步數(b)，如果a可以，輸出a；如果b&lt;m，輸出-1；否則輸出(a/m+1)*m。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/bb6f37bf8be31dcf5e87553e9d731e2e.js"></script>