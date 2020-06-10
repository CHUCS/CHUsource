---
title: Codeforces 59A
keywords: Codeforces Word, Codeforces 59A
date: 2020-06-11 00:55:48
categories: Codeforces
tags:
    - implementation
    - strings
    - 800
---
# Codeforces 59A - Word
[題目網址](https://codeforces.com/problemset/problem/59/A)


#### 題意:
Vasya很難過，網絡上的許多人都將一個大寫字母和小寫字母混在一起。因此Vasya想要寫個程式把單字的大寫小血都轉成統一的，但要讓程式轉換字母的次數最少。
<!-- more -->
#### 思路:
計算大寫小寫個多少，哪邊多就轉換成哪邊。
(根據ASCII，'a' = 97 , 'A' = 65，可對字元進行數字加減做大小寫轉換)
#### 程式碼:
<script src="https://gist.github.com/zxzxcc112/40bedb712d029bb7f89949065a394418.js"></script>