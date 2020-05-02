---
title: CodeForces 450A Jzzhu and Children
date: 2020-04-07 13:45:07
tags:
    - implementation
    - 普通
---
[CodeForces 450A](https://codeforces.com/problemset/problem/450/A)
<!-- more -->

#### 題意:
發糖果，孩子會排隊領取固定顆數的糖果，如果還沒拿到該孩子要拿的顆數，他會再回去排隊；已經達到的話就會直接回家。現在輸入人數、每一次發幾顆糖及每個孩子要拿的顆數，問你最後一個拿到糖的孩子的編號？

#### 思路:
邊輸入邊計算每個孩子要排幾次隊，紀錄數字最高且最後一次出現的人的編號，輸出。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/e01c3757ac81898aca72950dec9326d9.js"></script>