---
title: CodeForces 1256A
date: 2019-11-26 15:35:02
tags:
    - math
    - 新手
---
# CodeForces 1256A - Payment Without Change
[Payment Without Change](http://codeforces.com/problemset/problem/1256/A)


#### 題意:
給你4個輸入a, n, b, s，他有a個硬幣幣值為n，b個硬幣幣值為1，題目問你可不可以湊出S這個數字。
<!-- more -->
#### 思路:
先算出S/N看看有A沒有超過最大的換硬幣數量，如果有就把他的最大直設為A，接著再檢查減掉後的數有沒有超過B，沒有超過就代表可以換出來S。
#### 程式碼:
<script src="https://gist.github.com/Daviswww/4bda315b7e12083def4362b3d4eb7b03.js"></script>