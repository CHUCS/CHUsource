---
title: CodeForces 1051D
date: 2020-01-17 13:17:54
link: Bicolorings
keywords: Codeforces 1051D, Codeforces Bicolorings
tags:
    - bitmasks
    - dp
---
# CodeForces 1051D - Bicolorings
[Bicolorings](https://codeforces.com/problemset/problem/1051/D)


#### 題意:
給你一個2xN的網格，每一個只能塗成黑色或白色，所有相鄰的同色都視為同一個元件。現在輸入N及K，問你2xN的網格有正好K個元件時有幾種可能的塗法？
<!-- more -->
#### 思路:
建兩個陣列，紀錄現在最右邊的兩個不同色(A)以及同色(B)時，有x個元件時的塗法。因此當總列數n=1時A[1]=2，其他的A都等於0；B[2]=2，其他的B都等於0。新增一列時，A[i]=A[i]+A[i-1]+2*B[i]，B[i]=B[i]+B[i-2]+2*A[i-1]，增加到N列後A[K]+B[K]就是答案。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/33e0bd925d84247f7daa6d6d20291ebc.js"></script>