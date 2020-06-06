---
title: Codeforces 540C
keywords: Codeforces Ice Cave, Codeforces 540C
date: 2020-06-07 02:49:24
categories: Codeforces
tags:
    - dfs and similar
    - 2000
---
# Codeforces 540C - Ice Cave
[題目網址](https://codeforces.com/problemset/problem/540/C)


#### 題意:
你玩一款電腦遊戲，你的角色在一個冰窟裡為了進下一關必須從指定的位置掉落洞穴。
這一關，冰窟大小為nxm，每個位置的冰塊可以是完整的或裂開的，因為遊戲機制你的角色只能一次移動一格而且不能從原地移動到原地，當移動到裂冰時，角色就會掉下去，當移動到完整冰時，冰會裂開，請問能從指定的起點到指定的終點嗎?
<!-- more -->
起點一定會再裂冰的位置。
'.': 完整的冰 , 'X':裂開的冰
#### 思路:
利用BFS將可走的路記錄起來，紀錄的位置用'*'標記，看能不能到目的地，目的地的冰可能是完整或裂開的，因為要在目的地掉落，因此如果目的地是完整的冰就要走兩次，那判斷就會是「裂開的冰」或「走過一次的冰」。
#### 程式碼:
<script src="https://gist.github.com/zxzxcc112/56f174868a744aa1e3791f83dd573ebf.js"></script>