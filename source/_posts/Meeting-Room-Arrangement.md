---
title: UVA 12694
date: 2019-12-22 15:26:15
tags:
    - 簡單
    - greedy
---
[Meeting Room Arrangement](https://onlinejudge.org/external/126/12694.pdf)


#### 題意:
幫他牌時程表，他希望裡面牌的會議越多越好。
第一個輸入代表有幾筆，之後開始輸入會議的區間S和F，直到輸入為"0 0"就輸出。
<!-- more -->
#### 思路:
將區間的F由小到大排序，接著檢查右邊會議結束時間有沒有小於等於下一個的開始時間，如果有就把左邊改為它的會議結束時間。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/76dc64ecd51fcede83e0d4edb89eb876.js"></script>