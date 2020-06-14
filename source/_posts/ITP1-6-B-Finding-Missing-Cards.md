---
title: AOJ ITP1_6_B
keywords: ITP1_6_B Finding Missing Cards
categories: AOJ
tags:
  - implementation
date: 2020-06-14 09:10:53
---
# AOJ ITP1_6_B - Finding Missing Cards
[題目網址](https://onlinejudge.u-aizu.ac.jp/courses/lesson/2/ITP1/all/ITP1_6_B)

#### 題意:
輸入這副牌有的花色和數字，請找出遺失的牌(沒輸入的牌)。
<!-- more -->
#### 思路:
用index的方式計算每一個花色的牌，最後判斷哪張牌是0代表沒有出現過。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/7d87751075a82cac1f7cc18dda00648f.js"></script>