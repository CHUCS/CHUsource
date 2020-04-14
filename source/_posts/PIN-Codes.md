---
title: PIN Codes
date: 2020-04-14 13:04:43
tags:
    - greedy
    - implementation
    - 普通
---
[Codeforces 1263B](https://codeforces.com/problemset/problem/1263/B)
<!-- more -->

#### 題意:
有許多張卡，每張卡的密碼都是4位數字，現在想要將每張卡的密碼都改成不一樣的，請問最少要改幾個位數的數字？

#### 思路:
因為最多只有10張卡，所以其實只需要針對一個位數做變化就能保證全部不一樣了，這邊挑個位數。先針對個位數將用過的0~9記錄下來，然後比對陣列中同樣的密碼，將其中一邊的個位數改成沒用過的數字，記錄下有幾個數字需要改，輸出答案。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/b59af905ca283d646dbe25d93f73d09b.js"></script>