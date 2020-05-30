---
title: Codeforces 948A
keywords: Codeforces Protect Sheep, Codeforces 948A
date: 2020-05-30 20:49:05
categories: Codeforces
tags:
    - brute force
    - dfs and similar
    - graphs
    - implementation
    - 900
---
# Codeforces 948A - Protect Sheep
[題目網址](https://codeforces.com/problemset/problem/948/A)

#### 題意:
Bob是位農民，他有RxC的牧場，每個空間可以有一隻羊、一隻狗或一隻狼，Bob想要保護所有的羊，所以要放狗進牧場中，羊與狗都不會動，而狼可以上下左右移動，狗可以擋住狼不經過那個位置，Bob有很多狗所以不用在意狗的數量，請問Bob有辦法保護所有羊不被狼吃掉嗎，如果可以，請印出最後牧場的動物分布。
<!-- more -->
#### 思路:
將空地全部填滿狗，記錄所有狼的位置，之後看狼的四個方向有沒有羊就知道可不可以了。
#### 程式碼:
<script src="https://gist.github.com/zxzxcc112/60375b3b23a494af098727cdf5497dcc.js"></script>