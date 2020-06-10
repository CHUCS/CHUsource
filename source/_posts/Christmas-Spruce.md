---
title: Codeforces 913B
keywords: Codeforces Christmas Spruce, Codeforces 913B
date: 2020-06-11 00:56:18
categories: Codeforces
tags:
    - implementation
    - trees
    - 1200
---
# Codeforces 913B - Christmas Spruce
[題目網址](https://codeforces.com/problemset/problem/913/B)


#### 題意:
有個有根樹，若點u有個連接到點v，那我們稱點u為小孩，點v為父母，另外若一個點有父母但沒有小孩，我們稱之為「葉子」。
我們稱一種有根樹叫spruce，這種樹的所有非葉子的點都具有至少三個葉子，給你一個有根樹，從第二個點開始輸入它連接的父母，請問這是spruce嗎?
<!-- more -->
(點1一定是樹根)
#### 思路:
先計算每個點被多少點(孩子)連接，再看每個點是不是葉子，將不是葉子的點的父母連接數-1，被連接數 = 0的就是葉子，但如果因為-1的關係變成0必須判斷為否，可以提早判斷變成判斷是否小於3，最後確認每個非葉子的點是不是至少有三個葉子。
#### 程式碼:
<script src="https://gist.github.com/zxzxcc112/bb663ba790cb88e745dc1c8c1a0647ff.js"></script>