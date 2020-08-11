---
title: AOJ ALDS1_6_C - Quick Sort
keywords: AOJ ALDS1 6 C Quick Sort
date: 2020-07-15 14:36:48
categories: AOJ
tags:
    - implementation
---
# 快速排序
[題目網址](https://onlinejudge.u-aizu.ac.jp/courses/lesson/1/ALDS1/all/ALDS1_6_C)

#### 題意:
快速排序有三個步驟：
1.挑選基準值：從數列中挑出一個元素，稱為「基準」（pivot)。

2.分割：重新排序數列，所有比基準值小的元素擺放在基準前面，所有比基準值大的元素擺在基準後面（與基準值相等的數可以到任何一邊）。在這個分割結束之後，對基準值的排序就已經完成。

3.遞迴排序子序列：遞迴地將小於基準值元素的子序列和大於基準值元素的子序列排序。

完成排序後檢查出現順序是否依照順序，例如先輸入"D 1"、"H 1"，輸出時若為"D 1"、"H 1"就輸出"Stable"，否則輸出"Not stable"。

<!-- more -->
#### 思路:
按照上面快速排序的步驟編寫。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/b1de01e5346182490fa59fec396ecd2c.js"></script>