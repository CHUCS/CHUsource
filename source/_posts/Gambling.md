---
title: Codeforces 1038C
date: 2020-04-30 17:17:19
keywords: Codeforces 1038C, Codeforces Gambling
categories: Codeforces
tags:
    - greedy
    - sortings
    - 普通
---
# Codeforces 1038C - Gambling
[Gambling](https://codeforces.com/problemset/problem/1038/C)


#### 題意:
兩個人各持n張牌，在各自的回合都可以做1)拿一張自己的牌算分數；2)移除對手的一張牌，的其中一個動作。假設兩個人都會做當下最自己最有利的一步，問最後a-b的分數是多少？
<!-- more -->
#### 思路:
將兩人的牌都排序，比對雙方最大的牌，自己的大於等於對方的，就自己算分；否則就移除對方的牌。重覆到所有牌用完輸出答案。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/84aac07557a00f6523dd318516a8b796.js"></script>