---
title: Maximum Profit
keywords:  ALDS1_1_D ,  Maximum Profit
date: 2020-05-30 17:14:50
categories: Algorithms and Data Structures
tags:
    - implementation
---
# ALDS1_1_D - Maximum Profit
[題目網址](https://onlinejudge.u-aizu.ac.jp/courses/lesson/1/ALDS1/1/ALDS1_1_D)
<!-- more -->

#### 題意:
他希望利用換匯率獲得最大的利潤，例如: 1塊買5塊賣可以賺4塊，輸出4塊，而輸入的順序是代表時間軸。

#### 思路:
先將第一個數作為最小值，然後與下一個相減看有沒有大於現在的利潤，接著把現在的數字與最小值比較，以確保最小數為值前的。
#### 程式碼:
<script src="https://gist.github.com/Daviswww/b456634867aba083d9230d0180c34acc.js"></script>