---
title: AOJ ALDS1_3_B
keywords: ALDS1 Queue
date: 2020-07-12 17:29:26
categories: AOJ
tags:
    - implementation
---
# AOJ ALDS1_3_B - Queue
[題目網址](https://onlinejudge.u-aizu.ac.jp/courses/lesson/1/ALDS1/all/ALDS1_3_B)

#### 題意:
在稱為循環調度的處理方法中，CPU按順序處理進程。每個過程最多處理ms(也就輸入中的q)。如果已經完成q毫秒，但是該過程尚未完成，則移至該行的末尾，並將CPU分配給下一個過程。如果這個進程結束了那就輸出花費時間。
<!-- more -->
#### 思路:
利用queue先進先出的規則把所有的進程排隊，然後依照順序扣除執行的時間，並設一個變數存取累計時間，直到所有進程結束。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/c107bef46c7fcda613c6628d2849004c.js"></script>