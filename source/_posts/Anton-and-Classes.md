---
title: Codeforces 785B
date: 2020-04-15 13:17:44
tags:
    - greedy
    - sortings
    - 普通
---
[Anton and Classes](https://codeforces.com/problemset/problem/785/B)


#### 題意:
現在有n個A課程的開始及結束時間，m個B課程的開始及結束時間。現在要在A跟B課程中各挑1個，讓他們中間的間隔時間愈長愈好，問你最長可以是多少？
<!-- more -->
#### 思路:
所以是結束到開始中間的時間愈長愈好，因此輸入時就順便記錄AB各自最大的開始時間跟最小的結束時間，然後看A開始減B結束跟B開始減A結束哪個大就輸出哪個，都是負數就輸出0。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/30e597d386bca33013ab7b1a210d1c36.js"></script>