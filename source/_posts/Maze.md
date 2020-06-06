---
title: Codeforces 377A
keywords: Codeforces Maze, Codeforces 377A
date: 2020-06-07 02:48:57
categories: Codeforces
tags:
    - dfs and similar
    - 1600
---
# Codeforces 377A - Maze
[題目網址](https://codeforces.com/problemset/problem/377/A)


#### 題意:
Pavel喜歡格子迷宮，迷宮由nxm的矩形組成，每個點可以是空曠的也可以是圍牆，空曠地點可以移動到另一個空曠的點，Pavel畫了一張格子迷宮，但Pavel希望多k個牆，想將空曠的點變成牆後還能使所有空曠的點相通，請幫Pavel決定哪些空地要變成牆並把結果印出。
<!-- more -->
'#':牆 , '.':空地 , 'X':由空地變成牆
#### 思路:
利用DFS尋找路，當遇到死路就把空地變牆，因為是死路所以不會讓空地出現不相通的情況。
#### 程式碼:
<script src="https://gist.github.com/zxzxcc112/56030cba02a4f75b6f6210825042fb99.js"></script>