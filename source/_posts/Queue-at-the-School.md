---
title: Codeforces 266B
keywords: Codeforces Queue at the School, Codeforces 266B
date: 2020-06-11 00:53:18
categories: Codeforces
tags:
    - constructive algorithms
    - graph matchings
    - implementation
    - shortest paths
    - 800
---
# Codeforces 266B - Queue at the School
[題目網址](https://codeforces.com/problemset/problem/266/B)

#### 題意:
學校裡有男女生在排隊，過一段時間，男生覺得排在女生前面會覺得尷尬，所以決定讓位給女生，每隔一段時間所有排在女生前面的男生就會讓位給後面的女生，請問過了t段時間，隊伍會變成什麼樣子?
<!-- more -->
#### 思路:
直接模擬排隊情況，每次時間都改變一次字串。
#### 程式碼:
<script src="https://gist.github.com/zxzxcc112/1746167ba5e59709cd8f3b265f51b49d.js"></script>