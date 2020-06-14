---
title: ITP1_8_B Sum of Numbers
keywords: ITP1_8_B Sum of Numbers
date: 2020-06-14 12:44:41
categories: AOJ
tags:
    - implementation
---
# AOJ ITP1_8_B - Sum of Numbers
[題目網址](https://chucs.github.io/site/)

#### 題意:
給你一個1000位以內的數字問你全部數字加起來是多少，例如123加起來是6因為1+2+3=6。

<!-- more -->
#### 思路:
由於int只能到9位數所以我們必須要用字串的放式處理。而我們可以利用ASCII的相減算出原本的數字，例如'0'對應48，'1'對應49所以我們都把他們減'0'就可以得到數字的值。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/add998f9189cec2f734a4d0e9d1fa6c0.js"></script>