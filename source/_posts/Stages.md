---
title: CodeForces 1011A
date: 2020-04-07 13:48:08
keywords: Codeforces 1011A, Codeforces Stages
tags:
    - sortings
    - implementation
    - greedy
    - 普通
---
# CodeForces 1011A - Stages
[Stages](https://codeforces.com/problemset/problem/1011/A)


#### 題意:
現在需要組一個由k段構造構成的火箭，每一段的構造都用一個小寫英文字母代表，重量等同他在英文字母中的順序。每一段構造必須從輕的挑起，且一旦被挑過，下一段構造一定要至少比這一段重2以上。現在輸入可以用的段數量、需要的段數以及每一段的編號，問你這火箭最低的總重量是多少，組不出來則輸出-1？
<!-- more -->
#### 思路:
將所有編號排序，從小的開始依規則挑，能挑出k段則輸出答案，不能就輸出-1。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/4f04d5a5ff3b7ab57d56696801f16ba2.js"></script>