---
title: AOJ ALDS1_2_C
keywords: ALDS1 Stable Sort
date: 2020-07-12 13:24:05
categories: AOJ
tags:
    - sortings
---
# AOJ ALDS1_2_C - Stable Sort
[題目網址](https://onlinejudge.u-aizu.ac.jp/courses/lesson/1/ALDS1/all/ALDS1_2_C)

#### 題意:
讓我們安排一副紙牌。總共有36張卡，四個狀態（S，H，C，D）和9個值（1、2，... 9）。
請將他們由小到大排序，並檢查排序結果是否有按照出現順序排序。例如：輸入 "D1 S2 H2"，排序結果為"D1 H2 S2"，而在輸入時S2比H2前面因此輸出"Not stable"，若排序結果為"D1 S2 H2"，那麼輸出"Stable"。

<!-- more -->
#### 思路:
先宣告一個結構儲存三個狀態分別為，狀態、數字和輸入順序，利用此結構進行選擇排序與泡沫排序，排序完後檢查陣列，如果數字一樣而且前面順序大於後面那就代表不穩定。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/78500fcd44526355e664551e4333f5aa.js"></script>