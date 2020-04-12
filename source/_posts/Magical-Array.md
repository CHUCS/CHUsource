---
title: Magical Array
date: 2020-04-12 16:28:28
tags:
    - combinatorics
    - implementation
    - 一般
---
[Codeforces 84B](https://codeforces.com/contest/84/problem/B)
<!-- more -->

#### 題意:
給你一條數列問你所有連續的子空間為多少，如下列範例：
4
2 1 1 4
可以看到兩個連續的1其他都只有一個
1的位置: [1;1], [3;3], [2;3]
其他: [2;2], [4;4]

#### 思路:
可以由上面1的例子得到2一樣的數字為1+2個可能，如果3個一樣的話就是1+2+3，所以我們可以先建一個一加到十萬的表，如果數字一樣我們就把計數器加一如果不一樣就查表。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/e9f132ec324b04cf79d2285e8ff962a3.js"></script>