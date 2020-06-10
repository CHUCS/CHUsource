---
title: Codeforces 110A
keywords: Codeforces Nearly Lucky Number, Codeforces 110A
date: 2020-06-11 00:54:38
categories: Codeforces
tags:
    - implementation
    - 800
---
# Codeforces 110A - Nearly Lucky Number
[題目網址](https://codeforces.com/problemset/problem/110/A)


#### 題意:
Petya喜歡幸運數字(數字裡只有4或7)，而Petya想要找出「接近幸運的數字」(數字裡的幸運數字的數量是幸運數字)，請幫Petya判斷是不是「接近幸運的數字」。
<!-- more -->
#### 思路:
用字串輸入，計算4跟7的數量，判斷數量是否為幸運數字，因為最常是18位數，所以18內的幸運數字只有4跟7。
#### 程式碼:
<script src="https://gist.github.com/zxzxcc112/a2c82cd42402980c86793a0ea09d37d1.js"></script>