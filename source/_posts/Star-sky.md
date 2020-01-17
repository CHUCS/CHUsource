---
title: Star sky
date: 2020-01-17 13:14:16
tags:
    - implementation
    - dp
---

[CodeForces 835C](https://codeforces.com/problemset/problem/835/C)
<!-- more -->

#### 題意:
天上有n個星星座標各自為(xi, yi)，初始亮度為si；還有全部星星共通的最大亮度c。在t時的亮度為x的星星，若x+1&lt;c，在t+1時的亮度為x+1，否則為0。現在你要觀察天空q次，分別在ti時觀察從(x1, y1)到(x2, y2)之間的星星，問這區間的總亮度是多少？

#### 思路:
用積分圖(integral image)的方式記錄整個天空的初始亮度跟每個亮度的星星數量，之後快速得到輸入區間每個亮度的星星數量後計算指定時間的亮度後加總就是答案。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/8c1b2ffefb29bec87901d412f5db84e8.js"></script>