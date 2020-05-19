---
title: Codeforces 217A
date: 2019-10-18 17:22:26
link: Ice-Skating
keywords: Codeforces 217A, Codeforces Ice Skating
tags:
    - brute force
    - dfs and similar
    - dus
    - graphs
---
# Codeforces 217A - Ice Skating
[Ice Skating](https://codeforces.com/contest/217/problem/A)

Bajtek is learning to skate on ice. He's a beginner, so his only mode of transportation is pushing off from a snow drift to the north, east, south or west and sliding until he lands in another snow drift. He has noticed that in this way it's impossible to get from some snow drifts to some other by any sequence of moves. He now wants to heap up some additional snow drifts, so that he can get from any snow drift to any other one. He asked you to find the minimal number of snow drifts that need to be created.
<!-- more -->
We assume that Bajtek can only heap up snow drifts at integer coordinates.


#### Input:
The first line of input contains a single integer n (1 ≤ n ≤ 100) — the number of snow drifts. Each of the following n lines contains two integers x<sub>i</sub> and y<sub>i</sub> (1 ≤ x<sub>i</sub>, y<sub>i</sub> ≤ 1000) — the coordinates of the i-th snow drift.

Note that the north direction coinсides with the direction of Oy axis, so the east direction coinсides with the direction of the Ox axis. All snow drift's locations are distinct.

#### Output:
Output the minimal number of snow drifts that need to be created in order for Bajtek to be able to reach any snow drift from any other one.

#### 範例:
input:
```
2
2 1
1 2
```
output:
```
1
```
input:
```
2
2 1
4 1
```
output:
```
0
```


#### 題意:
Bajtek是一個滑雪的初心者，而它只能滑行四個方向(東南西北)，在滑行的途中它無法停下，除非撞到雪堆它才能停下改變行滑行的方向(或不改變)，而他需要堆積額外的雪堆來確保每個雪堆他都能前往。他問最少需要多少額外的雪堆。

#### 思路:
在輸入時會給你雪堆數和它在平面的座標，而現有的雪堆能組成多個區塊(單一或複數個雪堆，無法前往其他雪堆或能相互前往)，我們需要找出共有幾個區塊並計數，假設共為n個區塊，則最少需要(n-1)個雪堆來組成統一的大區塊，而(n-1)就是我們要的答案。

#### 程式碼:
<script src="https://gist.github.com/89snnfk561/ec5c3671547a0f0dff77dbacaafbe7ec.js"></script>

