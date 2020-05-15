---
title: UVA 10929
date: 2019-11-17 11:05:18
tags:
- implementation
- math
---
# UVA 10929 - You can say 11
[You can say 11](https://onlinejudge.org/external/109/10929.pdf)


#### 題意:
檢查這數字是否是11的倍數。
<!-- more -->
#### 思路:
奇數項加起來A，偶數項加起來B，檢查abs(A - B) % 11 == 0。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/0f1f31a49fd5a25ee5e9988f57ee4910.js"></script>