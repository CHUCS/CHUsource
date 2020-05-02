---
title: CodeForces 913C Party Lemonade
date: 2020-01-17 13:17:36
tags:
    - bitmasks
    - greedy
    - dp
---
[CodeForces 913C](https://codeforces.com/problemset/problem/913/C)
<!-- more -->

#### 題意:
輸入n，表示接下來會有n個瓶子，容量是2^(i-1)，價錢是ci。問現在至少需要總容量為L的瓶子，最少需要花多少錢？

#### 思路:
每個尺寸最低的價錢就是上一個尺寸的兩倍價錢以及這個尺寸輸入的價錢中較低的那個，先記錄所有尺寸最便宜的價錢。超出最大尺寸的部分直接用最大尺寸的最低價購買，剩下的部分則嘗試所有可能。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/ad4326a9423e9f8e9d836c8b607616cd.js"></script>