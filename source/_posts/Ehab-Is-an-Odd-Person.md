---
title: CodeForces 1174B
date: 2020-04-07 13:48:18
tags:
    - sortings
    - 普通
---
[Ehab Is an Odd Person](https://codeforces.com/problemset/problem/1174/B)


#### 題意:
給你一個數列，當其中的兩個數奇偶不同的時候，可以將其交換。問你這個數列最小的字典順序為何？
<!-- more -->
#### 思路:
觀察後可以發現，當整個陣列都是奇數或都是偶數時完全無法交換，因此可以直接輸出；另外的情況其實跟可以任意交換是一樣的，因此直接排序後輸出。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/8a048f0981d076ff0257de1ffde0972f.js"></script>