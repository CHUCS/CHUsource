---
title: Codeforces 1315A
date: 2020-02-26 13:54:52
tags:
    - implementation
    - 簡單
---
[Dead Pixel](https://codeforces.com/contest/1315/problem/A)


#### 題意:
在一個網格上放一個壞點，問你如果不覆蓋壞點的矩形最大是多少
<!-- more -->
#### 思路:
先找出最小面積後，把全部面積減去最小面積就可以得到答案了，而r與e要加一的原因是要去掉那一排有壞點的，而max((q*w)- tmp, 1)是因為在只有兩格的情況會變成沒面積所以兩格的話直接輸出1

#### 程式碼:
<script src="https://gist.github.com/Daviswww/652b04d1e317e2d9a9517f9078aee60f.js"></script>