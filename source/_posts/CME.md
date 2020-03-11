---
title: CME
date: 2020-01-14 15:51:33
tags:
    - math
---
[CodeForces 1223A](https://codeforces.com/problemset/problem/1223/A)
<!-- more -->

#### 題意:
現在要用火柴棒拼出正確的A+B=C式子，3個數字都大於0。現在輸入火柴棒的數量，為你需要在買多少火柴棒才能滿足這個條件？

#### 思路:
因為要拚出A+B=C的式子，所以需要的是A+B+C=2C根火柴棒，且C>=1，因此需要的是4根以上的偶數火柴棒，不到4就補到4；其他的偶數補0；奇數補1。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/4549203f9d56ce600024c12727f712de.js"></script>

