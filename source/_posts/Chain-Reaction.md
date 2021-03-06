---
title: CodeForces 607A
date: 2019-12-22 15:10:04
keywords: CodeForces 1220A, CodeForces Chain Reaction
categories: Codeforces
tags:
    - 一般
    - binary search
    - dp
---
# CodeForces 607A - Chain Reaction
[Chain Reaction](http://codeforces.com/problemset/problem/607/A)


#### 題意:
在同一橫軸上有一些信標，功率b的信標a啟動後會將左邊距離b以內的信標都摧毀，現在給你N個信標的座標跟功率，並允許你在最右邊的信標右邊再增加一個信標，功率隨意，問從右邊開始逐個啟動所有未被摧毀的信標，最後最少會有幾個信標被摧毀？
<!-- more -->
#### 思路:
創一個陣列des紀錄所有信標在[0].右邊信標全數被摧毀(除了額外增加的信標)且當前信標被摧毀的狀況下被毀的最少總信標數，和[1]右邊信標全數被摧毀(除了額外增加的信標)且當前信標被啟動的狀況下被毀的最少總信標數。des[i][0] = min(des[i-1][0],des[i][1])，因為當前信標已毀，所以不影響未摧毀的總數及左邊的狀態，直接對左邊的取最小值；des[i][1] = des[s][1] – 1，由於當前信標未毀，所以會啟動將左邊當前功率內的信標摧毀，然後啟動左邊的信標，因此用二分搜尋找未被摧毀的最右邊信標s，然後將其最少被摧毀的信標數減1(因為當前信標未毀)。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/615f27ffbce7ae56571b5d648e092ae4.js"></script>