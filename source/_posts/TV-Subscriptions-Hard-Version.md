---
title: TV Subscriptions (Hard Version)
date: 2020-04-27 17:01:54
tags:
    - implementation
    - two pointers
---
[Codeforces 1225B2](https://codeforces.com/problemset/problem/1225/B2)
<!-- more -->

#### 題意:
輸入接下來n天預訂撥放的k種節目，問你在某一個連續的d天中，最少會看到幾種節目？

#### 思路:
先看開始的d天，紀錄所有節目出現的次數及種類，接著往右移動區間，紀錄新增及減少的節目次數及種類，區間移動結束後輸出答案。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/23a9e2ddb3244b70ae1670235a68745c.js"></script>