---
title: Codeforces 706B
keywords: Codeforces Interesting drink, Codeforces 706B
date: 2020-05-29 19:04:10
categories: Codeforces
tags:
    - implementation
    - dp
    - binary search
    - 1100
---
# Codeforces 706B - Interesting drink
[題目網址](https://codeforces.com/problemset/problem/706/B)

#### 題意:
Vasiliy喜歡喝Beecola(一種飲料)，在他生活的城市中有n家店有賣，每家價格為x1,x2,...,xn，Vasiliy有q天，每天賺m1,m2,...,mq，請問Vasiliy每天所鑽到的錢可以到其中幾家店買到飲料(每天賺的錢是分開的)?
<!-- more -->
#### 思路:
將店家依價格小到大排序，每天的金額為目標，找出第一個價格大於今天賺到的錢的店家，在此店家前的店家數就是答案。
#### 程式碼:
<script src="https://gist.github.com/zxzxcc112/c69780f25b64001ce647a44fdd46c13c.js"></script>