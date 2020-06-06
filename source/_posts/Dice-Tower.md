---
title: Codeforces 225A
keywords: Codeforces Dice Tower, Codeforces 225A
date: 2020-06-07 02:48:36
categories: Codeforces
tags:
    - constructive algorithms
    - greedy
    - 1100
---
# Codeforces 225A - Dice Tower
[題目網址](https://codeforces.com/problemset/problem/225/A)


#### 題意:
骰子由1~6的數字組成，兩個相面對面的數字加起來都是7，共有兩種旋轉方向的骰子，依題目所有骰子皆使用同一種骰子。
Alice和Bob在玩骰子，Alice利用n個骰子疊成骰子塔，骰子與骰子的連接面不能是相同的數字，Bob只能在不移動的情況下看骰子，Bob只會看見骰子塔每個骰子的兩面及頂端的數字，請問Bob能猜出他看不見的所有數字嗎?
<!-- more -->
#### 思路:
可以發現，從頂端數第二個骰子，如果用跟頂端骰子上下不同的數字，那第二個骰子上下用哪一面都可以，因此要猜出看不見的所有數字就必須每一個骰子上下面都是同一組數字。
#### 程式碼:
<script src="https://gist.github.com/zxzxcc112/698162f0cf528b62b7a6b1787a79596a.js"></script>