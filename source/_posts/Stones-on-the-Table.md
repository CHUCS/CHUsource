---
title: Stones on the Table
date: 2020-04-14 13:03:49
tags:
    - implementation
    - 簡單
---
[Codeforces 266A](https://codeforces.com/problemset/problem/266/A)
<!-- more -->

#### 題意:
桌上有3個顏色(RGB)的石頭排成一列，現在希望每個石頭的隔壁都是不同顏色的石頭，在不改變順序只挑除一些石頭的情況下，請問最少挑出幾個石頭就能達到要求？

#### 思路:
從第2個石頭開始，遇到跟前一個一樣顏色的石頭就挑掉。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/d9d3881c3007f9e1b2d49a954758a357.js"></script>