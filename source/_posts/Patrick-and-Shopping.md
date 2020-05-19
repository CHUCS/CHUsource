---
title: Codeforces 599A
date: 2019-05-05 21:59:55
link: Patrick-and-Shopping
keywords: Codeforces 599A, Codeforces Patrick and Shopping
tags:
    - 新手
    - implementation
---
# Codeforces 599A - Patrick and Shopping
[Patrick and Shopping](https://codeforces.com/problemset/problem/599/A)

Today Patrick waits for a visit from his friend Spongebob. To prepare for the visit, Patrick needs to buy some goodies in two stores located near his house. There is a d1 meter long road between his house and the first shop and a d2 meter long road between his house and the second shop. Also, there is a road of length d3 directly connecting these two shops to each other. Help Patrick calculate the minimum distance that he needs to walk in order to go to both shops and return to his house.
<!-- more -->
![A](A.PNG)
Patrick always starts at his house. He should visit both shops moving only along the three existing roads and return back to his house. He doesn't mind visiting the same shop or passing the same road multiple times. The only goal is to minimize the total distance traveled.

#### Input:
The first line of the input contains three integers d<sub>1</sub>, d<sub>2</sub>, d<sub>3</sub> (1 ≤ d<sub>1</sub>, d<sub>2</sub>, d<sub>3</sub> ≤ 10<sup>8</sup>) — the lengths of the paths.

>>● d<sub>1</sub> is the length of the path connecting Patrick's house and the first shop.
>>● d<sub>2</sub> is the length of the path connecting Patrick's house and the second shop.
>>● d<sub>3</sub> is the length of the path connecting both shops. 
#### Output:
Print the minimum distance that Patrick will have to walk in order to visit both shops and return to his house.

#### 範例:
input:
```
10 20 30
```
output:
```
60
```
input:
```
1 1 5
```
output:
```
4
```
#### Note:
The first sample is shown on the picture in the problem statement. One of the optimal routes is: house -> first -> shop -> second -> shop house.

In the second sample one of the optimal routes is: house -> first -> shop -> house -> second -> shop -> house.
#### 題意:
輸入家到商店1、家到商店2和商店1到商店2的距離，問你從家開始，去過兩間商店，在回到家中的最短距離是多少？可以重複經過同一條路或同一個點。

#### 思路:
比較繞一圈或不走其中一條路的走法哪個最短即可。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/6b0632575d93f2313d96708316709aa8.js"></script>

