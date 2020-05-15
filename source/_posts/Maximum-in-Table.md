---
title: CodeForces 509A
date: 2020-03-11 13:23:56
tags:
    - brute force
    - implementation
    - 簡單
---
# CodeForces 509A - Maximum in Table
[Maximum in Table](https://codeforces.com/problemset/problem/509/A)


#### 題意:
給你一個矩陣，最上面及最左邊的元素都是1，剩下的元素會等於該元素上面和左邊元素的和。問你這矩陣中最大的元素是多少？
<!-- more -->
#### 思路:
依照此種加法，最大的元素一定出在最右下，因此依照順序從上到下、左到右實際加一遍後，輸出右下的元素就是答案。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/06980227327d9159c2d37e937923aa78.js"></script>