---
title: AOJ ALDS1_2_A
keywords: ALDS1 Bubble Sort
date: 2020-07-10 14:38:45
categories: AOJ
tags:
    - sortings
---
# AOJ ALDS1_2_A - Bubble Sort
[題目網址](https://onlinejudge.u-aizu.ac.jp/courses/lesson/1/ALDS1/all/ALDS1_2_A)

#### 題意:
利用泡沫排序排序，將結果與交換次數輸出。
<!-- more -->
#### 思路:
```
BubbleSort(A)
    for i = 0 to A.length-1
        for j = A.length-1 downto i+1
            if A[j] < A[j-1]
                swap A[j] and A[j-1]
```
一邊比較一邊交換。
#### 程式碼:
<script src="https://gist.github.com/Daviswww/d75e8bdad871d3b66348390c03f6f3d5.js"></script>