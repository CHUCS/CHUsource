---
title: AOJ ALDS1_1_C
keywords: ALDS1_1_C , Prime Numbers
date: 2020-05-30 17:00:04
categories: AOJ
tags:
    - implementation
---
# 質數
[題目網址](https://onlinejudge.u-aizu.ac.jp/courses/lesson/1/ALDS1/1/ALDS1_1_C)

#### 題意:
編寫一個程序，該程序讀取N個整數的，最後輸出共有幾個質數。

<!-- more -->
#### 思路:
先刪除二的倍數後，再以每次加二的方式除x如果可以整除代表不是質數。
#### 程式碼:
<script src="https://gist.github.com/Daviswww/294c4a0563b9993a1c4a798e8cfc7ced.js"></script>