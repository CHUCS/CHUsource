---
title: CodeForces 1313A
date: 2020-03-04 08:20:38
tags:
    - brute force
    - greedy
    - implementation
    - 簡單
---
[Fast Food Restaurant](https://codeforces.com/problemset/problem/1313/A)


#### 題意:
輸入3種餐點的數量，依據每個人至少分到1份餐點、每種餐點不能分超過1份、所有人都要分到不一樣的組合，這3個條件。問這些餐點能分給幾個人？
<!-- more -->
#### 思路:
總共只有7種分配方式，先紀錄起來，然後將這7種分配方式的所有分配可能(有128種)全部跑一次，將可能的方式中可以分給最多人的次數記錄起來輸出。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/5d01eeb4d2d5ca796a5387d25f4c133e.js"></script>