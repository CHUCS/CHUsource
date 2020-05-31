---
title: Codeforces 727A
keywords: 'Codeforces Transformation: from A to B, Codeforces 727A'
date: 2020-05-31 17:16:30
categories: Codeforces
tags:
    - brute force
    - dfs and similar
    - math
    - 1000
---
# Codeforces 727A - Transformation: from A to B
[題目網址](https://codeforces.com/problemset/problem/727/A)


#### 題意:
輸入起始數字a與目標數字b(a ≤ b)，你能進行兩種操作:
1.將現在的數字 x 2      (x = 2x)
2.將現在的數字 x 10 + 1 (x = 10x + 1)
請問，a能不能通過以上操作變成b，如果可以要把過程數字變化印出。
<!-- more -->
#### 思路:
a每次都有兩種變化可以選，但b每次只有一種變化，因此將兩種操作反向操作，看b能不能變成a。
因為必為整數，所以:
1.除2前必須是偶數
2.減1後除十前數字的個位數必須是1
#### 程式碼:
<script src="https://gist.github.com/zxzxcc112/b711a2d526c39455320d783d844d0f56.js"></script>