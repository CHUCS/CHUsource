---
title: AOJ ALDS1_5_B - Merge Sort
keywords: ALDS1 5 B Merge Sort
date: 2020-07-15 12:39:23
categories: AOJ
tags:
    - implementation
---
# 合併排序
[題目網址](https://onlinejudge.u-aizu.ac.jp/courses/lesson/1/ALDS1/all/ALDS1_5_B)

#### 題意:
給你N個整數序列S創建一個程序，根據上面的虛擬碼通過合併排序由小到大進行排序。另外，請報告合併中的比較總數。
<!-- more -->
#### 思路:
先拆開然後檢查左邊和右邊誰大誰小，小的放左邊大的放右邊合併，重複這個動作到結束。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/86ace3aedb574bee48d1a7869cca847c.js"></script>