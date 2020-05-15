---
title: CodeForces 1326B
date: 2020-04-02 15:35:17
tags:
    - implementation
    - math
    - 簡單
---
# CodeForces 1326B - Maximums
[Maximums](https://codeforces.com/problemset/problem/1326/B)


#### 題意:
給一個a陣列，創建一個x陣列x_i項是a陣列前i-1項中的最大值，再創建一個b陣列，b_i項是a_i-x_i。現在給你陣列長度n及b陣列的所有內容，問你a陣列的內容為何？
<!-- more -->
#### 思路:
依據給的公式可以推出x_0=0，b_0=a_0-x_0 => a_0 = b_0。在知道a_0之後就能知道x_1 = a_0，知道x_1及b_1後可以推出a_1；然後依序推出x_2、a_2、x_2、a_3…，將a記錄起來就是答案。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/62b5e39b9129cdfe55d19ecc3a5208a9.js"></script>