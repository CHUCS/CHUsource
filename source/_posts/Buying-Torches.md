---
title: CodeForces 1418A
keywords: CodeForces 1418A, CodeForces Buying Torches
date: 2020-09-22 22:51:35
categories: Codeforces
tags:
    - math
    - 1000
---
# CodeForces 1418A - Buying Torches
[題目網址](https://codeforces.com/problemset/problem/1418/A)

#### 題意:
你玩遊戲想要製作k個火把，每個火把需要一根棒子和一個煤炭，一開始你只有一根棒子,你能跟商人做兩種交易:
    1.用一根棒子交換x根棒子
    2.用y根棒子交換一個煤炭
每次只能做其中一種交易，請問你需要k個火把「最少」需要幾次交易? (測資必存在解答)
<!-- more -->
#### 思路:
數學問題，幾個煤炭就需要交易幾次，並且煤炭等於y根棒子，所以交易次數=到達所需棒子量的交易次數+換煤炭的次數。
#### 程式碼:
<script src="https://gist.github.com/zxzxcc112/fce4c025b50df9f1982acbd833a09d91.js"></script>