---
title: Codeforces 988B
date: 2020-04-14 13:05:04
keywords: Codeforces 988B, Codeforces Substrings Sort
tags:
    - 普通
    - sortings
    - strings
---
# Codeforces 988B - Substrings Sort
[Substrings Sort](https://codeforces.com/problemset/problem/988/B)


#### 題意:
給你一些字串，問你這些字串能否重新排列成，所以前面的字串都是此字串的子字串。
<!-- more -->
#### 思路:
記錄下每個字串有幾個子字串，依照這個數字從小排到大，然後檢查是否每個字串的子字串數量都大於等於目前前面的字串數量，是的話就OK，否則輸出NO。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/1c28cc0e18778558f044237db1d4d574.js"></script>