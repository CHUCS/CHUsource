---
title: Codeforces 218C
keywords: Codeforces Ice Skating, Codeforces 218C
date: 2020-05-31 17:17:18
categories: Codeforces
tags: 
    - dfs and similar
    - dsu
    - graphs
    - 1200
---
# Codeforces 218C - Ice Skating
[題目網址](https://codeforces.com/problemset/problem/218/C)


#### 題意:
Bajtek在學習溜冰，溜冰場裡有n個雪堆在不同的位置，Bajtek只會往東西南北四個方向移動，並且停不下來因此必須要依靠雪堆停下來，為了確保Bajtek能停下來，也就是說，每個雪堆的四個方向至少要有另一個雪堆，他想要多堆幾個雪堆，請幫忙找出Bajtek「最少」還需要堆多少雪堆?
<!-- more -->
#### 思路:
用平面來看，一個雪堆往四個方向延伸尋找有沒有其他雪堆，如此可以將數個雪堆連在一起形成符合條件的集合，而平面中可以形成多個集合，代表每個集合中的任一雪堆不會與另一個集合中的任何雪堆有交集，讓任兩個集合有交集就需要多一個雪堆放在能讓兩集合相通的位置，所以答案是(集合數量-1)。
#### 程式碼:
<script src="https://gist.github.com/zxzxcc112/e6dc78157461da5abb256bf66544c028.js"></script>