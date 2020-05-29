---
title: Codeforces 580A
keywords: Codeforces Kefa and First Steps, Codeforces 580A
date: 2020-05-29 00:56:37
categories: Codeforces
tags:
    - Dynamic programming
    - dp
    - Brute force
    - 動態規劃
    - 暴力
    - 簡單
---
# Codeforces 580A - Kefa and First Steps
[題目網址](https://codeforces.com/problemset/problem/580/A)

#### 題意:
輸入數量為n的數字序列，請問此序列中非降序連續片段的最長長度是多少?<!-- more -->
非降序序列:a[0] <= a[1] <= a[2] <= a[3]...。
#### 思路:
每次輸入一個新數字就跟上一個數字比較，如果新數字比較小，紀錄起點到上一個數字的長度並比較此長度與答案，將最長的存為答案，之後重新設定起點，重複以上動作到結束。
#### 程式碼:
<script src="https://gist.github.com/zxzxcc112/48cc1a379a795ade9753108910ee212e.js"></script>