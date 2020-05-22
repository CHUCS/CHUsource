---
title: AOJ ITP1_8_D
date: 2019-11-17 10:39:00
keywords: AOJ ITP1_8_D, AOJ Ring
categories: AOJ
tags:
    - implementation
---
# AOJ ITP1_8_D - Ring
[Ring](http://judge.u-aizu.ac.jp/onlinejudge/description.jsp?id=ITP1_8_D)


#### 題意:
幫他找出A字串在不再B字串裡面，需要連續的。
<!-- more -->
#### 思路:
先複製一個字串在源自串後面模仿一個環的樣子，然後逐一檢查一樣的話計數器加一，檢查完後檢查計數器的長度是否跟原自串一樣長，一樣就不檢查然後印答案。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/fa4b745d816d676bac397dcd0d05b2bd.js"></script>