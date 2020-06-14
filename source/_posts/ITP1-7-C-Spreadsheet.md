---
title: AOJ ITP1_7_C
keywords: ITP1_7_C Spreadsheet
date: 2020-06-14 12:19:29
categories: AOJ
tags:
    - implementation
---
# AOJ ITP1_7_C - Spreadsheet
[題目網址](https://onlinejudge.u-aizu.ac.jp/courses/lesson/2/ITP1/all/ITP1_7_C)

#### 題意:
輸數一個矩陣將每一列的加起來的數字算出來放在最後，再將每一行的答案加起來放在最後接著輸出。
<!-- more -->
#### 思路:
在輸入每一列時將答案計算並放在a[i+1]內，最後跑一次行的然後輸出。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/ea47218d893d0d5e531a9dbc5b274126.js"></script>