---
title: Colorful Field
date: 2020-04-14 13:06:18
tags:
    - implementation
    - sortings
    - 普通
---
[Codeforces 79B](https://codeforces.com/problemset/problem/79/B)
<!-- more -->

#### 題意:
給你一塊地及一些浪費的座標位置，其餘的座標從上到下左到右依序種紅蘿蔔、奇異果及葡萄，現在問你某個特定座標是被浪費了還是種了什麼作物？

#### 思路:
將所有浪費的座標上到下左到右排序，之後輸入每個查詢座標時去找它前面有幾個浪費的座標，若本身就是浪費的點就不用繼續了，直接輸出；否則先記錄下來，將現在的座標轉為上到下左到右順序的順序數後減去記錄下來的數字，可以得到這座標是第幾個沒被浪費的點，對3取餘數就能知道會種什麼東西。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/b0afbe68ce22d745f75b50eb1b16cc6b.js"></script>