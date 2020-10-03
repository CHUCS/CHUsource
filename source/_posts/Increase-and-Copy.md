---
title: Codeforces 1426C
keywords: Codeforces Increase and Copy, Codeforces 1426C
date: 2020-10-03 15:10:14
categories: Codeforces
tags:
    - binary search
    - constructive algorithms
    - math
    - 1100
---
# Codeforces 1426C - Increase and Copy
[題目網址](https://codeforces.com/problemset/problem/1426/C)

#### 題意:
你有一陣列a，一開始只有一個元素1(a = [1])，每次動作你能做以下一種事:
1.對a中其中一個元素+1
2.對a中其中一個元素做複製，並放在陣列最後面
你要找出「最小」次數的動作讓陣列a裡的元素總和至少為n。
<!-- more -->
#### 思路:
要次數最小，所以一次動作加越多數字越好，因此應該是先+1到某個數字後在做複製，根據數學可以知道某數的平方數字最大(算幾)，也會發現執行動作次數最少，所以要加到sqrt(n)之後作複製到超過n所需的次數。
#### 程式碼:
<script src="https://gist.github.com/zxzxcc112/6e6e6cc5ae4c3bd72ddfc6b89c8d648b.js"></script>