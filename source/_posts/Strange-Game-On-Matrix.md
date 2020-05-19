---
title: Codeforces 873C
date: 2020-04-30 17:17:49
link: Strange-Game-On-Matrix
keywords: Codeforces 873C, Codeforces Strange Game On Matrix
tags:
    - greedy
    - two pointers
    - 普通
---
# Codeforces 873C - Strange Game On Matrix

[Strange Game On Matrix](https://codeforces.com/problemset/problem/873/C)


#### 題意:
給你一個n x m陣列，由0跟1組成。現在對每一個直行計算分數，算法是由上往下找1，找到後計算下面最多k個數字內有幾個1作為分數。現在你還可以花1次行動將任意1個數字從1換成0，問你最多可以得到幾分，和這個分數下最少的行動是幾次？
<!-- more -->
#### 思路:
對每一個直行計算區間高度k的分數，當第一個元素是1時實際計分，並且在脫離時將行動次數加1。跑完每一個直行後加總就是答案。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/6647f0ec1e751f77d1d389e3ea63a501.js"></script>