---
title: ALDS1 6 A Counting Sort
keywords: ALDS1 6 A Counting Sort
date: 2020-07-15 13:33:29
categories: AOJ
tags:
    - implementation
---
# AOJ ALDS1_6_A - Counting Sort
[題目網址](https://onlinejudge.u-aizu.ac.jp/courses/lesson/1/ALDS1/all/ALDS1_6_A)

#### 題意:
計數排序可用於對數組中的元素進行排序，用一個陣列來計算元素有幾個，而他的index就是原本的數字裡面存的是出現次數。請利用計數排序排序下列數列。

<!-- more -->
#### 思路:
將每個數字都放進Ｃ陣列內計數(c[a[i]]++)，處理完後從0跑到K並根據C陣列內的計數，將所有的數字輸出一遍。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/245397223969f64944326fb98f0b1e80.js"></script>