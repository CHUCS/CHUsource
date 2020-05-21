---
title: Codeforces 652B
date: 2020-04-30 17:16:49
keywords: Codeforces 652B, Codeforces z-sort
tags:
    - sortings
    - 普通
---
# Codeforces 652B - z-sort
[z-sort](https://codeforces.com/problemset/problem/652/B)

#### 題意:
給你一個數列，現在希望排成a[0]&lt;a[1]>a[2]&lt;a[3]……的格式，問你有沒有可能？可以的話輸出排序後陣列，不能就輸出Impossible。
<!-- more -->

#### 思路:
陣列排序，分成兩半，前半較小，用在小的部分；後半較大，用在大的部分。兩邊都從頭開始取，依照規則填入，可以的話輸出排序後陣列，不能就輸出Impossible。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/126107d2a5707324d18cb1d5b60592a1.js"></script>