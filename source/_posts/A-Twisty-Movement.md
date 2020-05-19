---
title: CodeForces 933A
date: 2019-11-17 16:12:07
link: A-Twisty-Movement
keywords: CodeForces A Twisty Movement, CodeForces 933A
tags:
    - dp
---
# CodeForces 933A - A Twisty Movement
[A Twisty Movement](https://codeforces.com/problemset/problem/933/A)

#### 題意:
輸入一串由1和2組成的數列，可以左右翻轉任意的範圍一次，問最長的非遞減子序列是多長？
<!-- more -->
#### 思路:
觀察後得知，題目是在求將數列分成4段之後(每一段的長度可以是0)，第1段1的數量+第2段2的數量+第3段1的數量+第4段2的數量的最大值是多少。因此創個陣列邊輸入邊維持最大值，[1]紀錄只有第1段時的最大值、[2]紀錄只有第1段及第2段時的最大值、[3]跟[4]同理，因次跑完後輸出[4]就是答案。

#### 程式碼:
<script src="https://gist.github.com/89snnfk561/7ed0e505140cd7796ab9db94fe515dec.js"></script>


