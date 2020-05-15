---
title: CodeForces 1321A
date: 2020-03-04 08:21:22
tags:
    - greedy
    - 簡單
---
# CodeForces 1321A - Contest for Robots
[Contest for Robots](http://codeforces.com/problemset/problem/1321/A)


#### 題意:
有兩台機器人要比賽解題，現在你可以對每一題分配一個大於等於1的分數，答對時可以獲得該分數，答錯沒有分數。現在輸入問題數量及每個問題兩邊的機器人是否會答對，問你如果要讓第一台機器人贏的話，所有配分中分數最高的題目，最少分數要是多少？
<!-- more -->
#### 思路:
計算1對2錯的題數(a)及1錯2對的題數(b)，a>b時，不用調整配分，輸出1；a<=b且a!=0時，因為分數要比第二隊多，不能一樣，將b+1分盡量平均分配到a題上，輸出答案；a==0時，怎麼調整都無法達成，輸出-1。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/fb445b42e4ab3b7419d04804ab503890.js"></script>