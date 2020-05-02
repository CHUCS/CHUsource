---
title: Codeforces 677A Vanya and Fence
date: 2020-04-12 16:30:45
tags:
    - implementation
    - 新手
---
[Codeforces 677A](https://codeforces.com/contest/677/problem/A)
<!-- more -->

#### 題意:
輸入n和h分別是有幾個人和圍牆高度，為了不被警衛發現所以人的高度比圍牆高就要彎腰。
舉例：
3 7
4 5 14
圍牆高度7所以4, 5不需彎腰所以是1，14要彎所以是2，答案就是1+1+2=4。

#### 思路:
逐一比較如果h大於等於身高ans+1，其他ans+2。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/bf2ade7ddbf3787c47b6d7bc0ad4f112.js"></script>