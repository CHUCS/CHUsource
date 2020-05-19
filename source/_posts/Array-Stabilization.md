---
title: Codeforces 1095B
date: 2020-04-15 13:17:15
link: Array-Stabilization
keywords: Codeforces 1095B, Codeforces Array Stabilization
tags:
    - implementation
    - sortings
    - 簡單
---
# Codeforces 1095B - Array Stabilization
[Array Stabilization](https://codeforces.com/problemset/problem/1095/B)


#### 題意:
給你一個數列，問你從中挑出一個刪掉後，剩下的最大值減最小值的差最少可以是多少？
<!-- more -->
#### 思路:
排序，然後比較減去最大值跟最小值後的差，輸出少的。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/c9bd065b6f08ba5c4596fcf80971236b.js"></script>