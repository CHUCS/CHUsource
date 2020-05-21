---
title: Codeforces 176A
date: 2020-04-27 17:00:18
keywords: Codeforces 176A, Codeforces Trading Business
tags:
    - greedy
    - sortings
---
# Codeforces 176A - Trading Business
[Trading Business](https://codeforces.com/problemset/problem/176/A)


#### 題意:
給你n個星球及各自m種商品的買價、賣價及庫存數量，現在只能在一個星球採購一次，最多共k個商品，然後在一個星球賣掉，扣掉成本後問你最多可以賺多少？
<!-- more -->
#### 思路:
計算在i星球買到j星球賣的所有商品的價差，依利潤排序後根據庫存計算總利潤，跑完所有ij後輸出最高的。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/a091d508a0bf4212e112d56100d4c37b.js"></script>