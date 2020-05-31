---
title: Codeforces 902B
keywords: Codeforces Coloring a Tree, Codeforces 902B
date: 2020-05-31 17:17:44
categories: Codeforces
tags:
    - dfs and similar
    - dsu
    - greedy
    - 1200
---
# Codeforces 902B - Coloring a Tree
[題目網址](https://codeforces.com/problemset/problem/902/B)

#### 題意:
你有一個有n個點的有根樹，根的編號為1，要為每個點上色，每個點的顏色為c1,c2,...cn，一開始每個點都沒顏色c = 0，你必須用「最少」的步驟來完成上色，每一步你能選擇任點v與任一顏色x，然後被選擇的點v與v的子樹顏色都會變成x，可以確定最後每個點都有顏色c != 0。
輸入n-1個數字p2,p3,...,pn代表第i個點與pi相連。
<!-- more -->
#### 思路:
一棵樹上方會影響下方，所以就從第一個點看到最後，紀錄每個點當下是什麼顏色，對每一個點看這個點的上一個點是什麼顏色，如果是目標顏色就不用加一次步驟，並把當下顏色改成目標顏色。
#### 程式碼:
<script src="https://gist.github.com/zxzxcc112/bfc82b72c03fee5a5657c8b26dbd1d96.js"></script>