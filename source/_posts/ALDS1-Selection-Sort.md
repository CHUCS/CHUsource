---
title: AOJ ALDS1_2_B
keywords: ALDS1 Selection Sort
date: 2020-07-10 15:13:36
categories: AOJ
tags:
    - sortings
---
# AOJ ALDS1_2_B - Selection Sort
[題目網址](https://onlinejudge.u-aizu.ac.jp/courses/lesson/1/ALDS1/all/ALDS1_2_B)

#### 題意:
利用選擇排序排序，當i不等於mini時才交換，請把結果與交換次數輸出。
<!-- more -->
#### 思路:
```
SelectionSort(A)
    for i = 0 to A.length-1
        mini = i
        for j = i to A.length-1
            if A[j] < A[mini]
                mini = j
        swap A[i] and A[mini]
```
先將一個數字的位置記住後逐一比較，如果比他大就將mini取代新的index，全部比較完後在進行交換。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/687c3ee75d3561997469a9830b92b038.js"></script>