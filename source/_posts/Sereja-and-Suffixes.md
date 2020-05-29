---
title: Codeforces 368B
keywords: Codeforces Sereja and Suffixes, Codeforces 368B
date: 2020-05-29 19:04:39
categories: Codeforces
tags:
    - Dynamic programming
    - dp
    - 動態規劃
---
# Codeforces 368B - Sereja and Suffixes
[題目網址](https://codeforces.com/problemset/problem/368/B)

#### 題意:
Sereja有個陣列a，有n個數字a1,a2,...,an，Sereja想要找m次，從陣列中某個位置到最後一個位置共有幾個不同的數字。
<!-- more -->
#### 思路:
用一個陣列來確認一個數字是否出現過，從陣列最後一個位置開始，每次遇到新數字就將答案+1後存成那個位置的答案，如果遇到舊數字就不用+1並且儲存答案。
#### 程式碼:
<script src="https://gist.github.com/zxzxcc112/ef4c2bf6e76a5ada12fb3d4f203b0cd2.js"></script>