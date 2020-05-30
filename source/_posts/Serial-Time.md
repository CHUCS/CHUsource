---
title: Codeforces 60B
keywords: Codeforces Serial Time!, Codeforces 60B
date: 2020-05-30 20:47:58
categories: Codeforces
tags:
    - dfs and similar
    - dsu
    - 1400
---
# Codeforces 60B - Serial Time!
[題目網址](https://codeforces.com/problemset/problem/60/B)


#### 題意:
Serial Guy有個立體空間，有k層，每層是nxm的矩形，'.'代表空的，'#'代表障礙物，Serial Guy想要裝水到這個空間裡，有個水龍頭在第一層的(x,y)位置，水能通過空的空間但不能通過障礙物，每個空間裝滿要一分鐘，請問在水龍頭的水能通過的空間裡，要裝滿水需要幾分鐘?
<!-- more -->
#### 思路:
像找路一樣，在一個點上有兩種方法尋找路線:
DFS: 遇到能走的方向就直接走，但要記住之前走過的地方，遇到死路就原路返回，遇到新路就直接走，重複到所有地方都被走過。
BFS: 在一個位置上把所有能走的路記起來，從被記起來的新路挑一個走，到下一個地方一樣把所有能走的路記起來，重複直到所有地方被走過。
(程式碼採BFS方法)
#### 程式碼:
<script src="https://gist.github.com/zxzxcc112/60a36daf6059cc6fb76d130a63166a02.js"></script>