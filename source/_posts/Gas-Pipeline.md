---
title: CodeForces 1207C
date: 2019-12-13 16:52:32
keywords: Codeforces 1207C, Codeforces Gas Pipeline
categories: Codeforces
tags:
    - 一般
    - greedy
    - dp
---
# CodeForces 1207C - Gas Pipeline
[Gas Pipeline](http://codeforces.com/problemset/problem/1207/C)


#### 題意:
用0/1表示一條街道的一個區段不是/是路口，在路口時管線必須立在離地兩單位高的柱上供路口通行，非路口時則沒有限制。現在輸入N、A、B，表示道路的區段數量、一單位長的管線的成本、一單位高的柱子成本，保證頭尾的區段都是非路口，問在道路頭尾的柱子都是1單位高時花費的最低成本是多少？
<!-- more -->
#### 思路:
用柱子來看，前一根柱子到這一根柱子的成本有四種，高度1到1、高度1到2、高度2到1、高度2到2四種，因此知道前一根柱子的高度1和2的最低成本，就可以算出這根柱子高度1和2時的最低成本。加上第一根根最後一根柱子高度限制為1的條件後，從第一根柱子開始推算就可以得出最後的最低成本。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/f150287a1b3ee14609c68fcfe3aa0131.js"></script>