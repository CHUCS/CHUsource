---
title: Codeforces 363B
keywords: Codeforces Fence, Codeforces 363B
date: 2020-05-29 00:57:08
categories: Codeforces
tags:
    - Dynamic programming
    - dp
    - Brute force
    - 動態規劃
    - 暴力
    - 簡單
---
# Codeforces 363B - Fence
[題目網址](https://codeforces.com/problemset/problem/363/B)

#### 題意:
Polycarpus家門前有個圍欄，由n個寬度相同的木板組成，第i個木板高度為h，Polycarpus買了一台寬度為k的鋼琴，他希望他希望拆掉連續k個木板使鋼琴能搬到家裡，而越高的木板拆除越費力，所以他希望找出最省力位置移除木板，也就是說找出某個木板的位置，向右k-1個木板高度相加會是「最小」的。
(圍欄是一個面，而不是環繞的; 木板的位置是1~n)
<!-- more -->
#### 思路:
從第一個位置開始將k個木板的高度加總，紀錄高度與位置，每下一個位置，減去上個位置的木板加上下個木板，比較高度，較低的一方紀錄高度與位置，重複到n-k-1的位置，印出被記錄的位置就是答案。
#### 程式碼:
<script src="https://gist.github.com/zxzxcc112/45797becf15b6e30f58e326843714188.js"></script>