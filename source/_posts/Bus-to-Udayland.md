---
title: Bus to Udayland
date: 2020-03-11 13:23:40
tags:
    - brute force
    - implementation
    - 簡單
---
[CodeForces 711A](https://codeforces.com/problemset/problem/711/A)
<!-- more -->

#### 題意:
輸入巴士的座位表，O表示空位；X表示已有人。現在問你是否有兩個不跨走道且相鄰的座位？有的話將輸出YES並將目標改為+輸出座位表，沒有的話輸出NO。

#### 思路:
邊輸入邊判斷有沒有連續的兩個O，沒有就輸出NO；有的話將內容改成+，輸出YES後輸出座位表。
#### 程式碼:
<script src="https://gist.github.com/Daviswww/be44b870a1a38cef36ab17aa4baaba14.js"></script>