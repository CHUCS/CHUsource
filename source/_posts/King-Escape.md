---
title: Codeforces 1033A
keywords: Codeforces King Escape, Codeforces 1033A
date: 2020-05-30 20:49:23
categories: Codeforces
tags:
    - dfs and similar
    - graphs
    - implementation
    - 1000
---
# Codeforces 1033A - King Escape
[題目網址](https://codeforces.com/problemset/problem/1033/a)

#### 題意:
有一個nxn的西洋棋盤，棋盤上只有一個皇后與一個國王各在棋盤上的一個位置，國王不會在皇后的移動範圍內，現在希望國王有個目的地，國王能不斷的移而皇后只能移動一次，請問國王能不能到達目的地?
(國王與皇后的移動範圍與西洋棋相同)
<!-- more -->
#### 思路:
皇后的移動範圍會將棋盤切成四塊區域，只要看國王與目的地是不是在相同區塊跟注意皇后周圍的位置(棋盤最小3x3)就知道可不可以了。
#### 程式碼:
<script src="https://gist.github.com/zxzxcc112/f869f29d6765dc6fed1899262adc2dfc.js"></script>