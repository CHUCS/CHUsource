---
title: AOJ ITP1_11_B Dice II
keywords: ITP1_11_B Dice II
date: 2020-06-15 12:40:09
categories: AOJ
tags:
    - implementation
---
# AOJ ITP1_11_B - Dice II
[題目網址](https://onlinejudge.u-aizu.ac.jp/courses/lesson/2/ITP1/all/ITP1_11_B)

#### 題意:
輸入一顆骰子，然後輸入骰子的兩面上面和正面，問你右邊那面數字是什麼。

<!-- more -->
#### 思路:
先將上下左右的翻轉寫好，然後一條字串把所有面翻過一次找到正面和上面，然後就可以知道右邊那面是多少。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/25b5cd60d4468c874ff485d94323684c.js"></script>