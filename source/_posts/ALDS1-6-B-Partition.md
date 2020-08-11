---
title: AOJ ALDS1_6_B - Partition
keywords: ALDS1 6 B Partition
date: 2020-07-15 14:26:38
categories: AOJ
tags:
    - implementation
---
# 快速排序劃分
[題目網址](https://onlinejudge.u-aizu.ac.jp/courses/lesson/1/ALDS1/all/ALDS1_6_B)

#### 題意:

快速排序有三個步驟：
1.挑選基準值：從數列中挑出一個元素，稱為「基準」（pivot）。

2.分割：重新排序數列，所有比基準值小的元素擺放在基準前面，所有比基準值大的元素擺在基準後面（與基準值相等的數可以到任何一邊）。在這個分割結束之後，對基準值的排序就已經完成。

3.遞迴排序子序列：遞迴地將小於基準值元素的子序列和大於基準值元素的子序列排序。

而這題要做的就是分割這個動作。

<!-- more -->
#### 思路:
如果(a[j] <= x)我們就交換，最後我們將最後一個切割點輸出。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/2b61bf149936044aab2d398c8496b1b3.js"></script>    