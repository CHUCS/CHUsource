---
title: Functions again
date: 2019-11-30 08:53:25
tags:
    - 普通
    - two pointers
    - dp
---
[CodeForces 788A](http://codeforces.com/problemset/problem/788/A)
<!-- more -->

#### 題意:
輸入N及N個數字，求依照公式時最大的區段和是多少？

#### 思路:
觀察公式後，得知在區段中每一項差的絕對值會由+-+-+-…的規律加起來，因此除了第一個，要取的話就一次取兩個，不然只取-的會變小。先將所有的差的絕對值存起來，接著對偶數起點和奇數起點都做一次跨度為2的子區段最大和，最後得到的最大值就是答案。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/5ea9f2ecdcafdc4a7fdb8dc98a590879.js"></script>