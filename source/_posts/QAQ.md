---
title: Codeforces 894A
keywords: Codeforces QAQ, Codeforces 894A
date: 2020-05-29 00:56:16
categories: Codeforces
tags:
    - Brute force
    - 暴力
    - 簡單
---
# Codeforces 894A - QAQ
[題目網址](https://codeforces.com/problemset/problem/894/A)

#### 題意:
輸入一個字串，請問能找到幾組"QAQ"的子字串?
<!-- more -->
子字串是指完整的字串刪除幾個元素後形成的字串，例如:"QAQAQYSYIOIWIN"的子字串可以是"Q","QAQ","AYS","WIN","QAQAQ","QAQAQYSYIOIWIN"等。
#### 思路:
找出字串中的字元'A'，從這個A的位置向左右尋找各有幾個Q，將左右兩邊的數量相乘，重複以上動作直到把所有A跑過一次，將每次相乘的結果相加就是所有能形成QAQ的數量。
#### 程式碼:
<script src="https://gist.github.com/zxzxcc112/fdac775e8b16a25fb488b7b77aa24341.js"></script>