---
title: AOJ ITP1_11_A
date: 2019-11-26 15:35:25
link: Dice-I
keywords: AOJ ITP1_11_A, AOJ Dice I
tags:
    - implementation
    - 簡單
---
# AOJ ITP1_11_A - Dice I
[Dice I](http://judge.u-aizu.ac.jp/onlinejudge/description.jsp?id=ITP1_11_A)


#### 題意:
給你一顆骰子，然後翻轉骰子後，問你朝上的那面數字為多少。
<!-- more -->
#### 思路:
先建一個東南西北轉完結果的"位子表"，將骰子骰完後的結果存到新的骰子，再將原本色子覆蓋掉重複地做。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/fdd20a2347cfacc7bcc6f8fa78818726.js"></script>