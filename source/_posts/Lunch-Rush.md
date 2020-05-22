---
title: Codeforces 276A
date: 2019-04-27 18:41:02
keywords: Codeforces 276A, Codeforces Lunch Rush
categories: Codeforces
tags:
    - 新手
    - implementation
---
# Codeforces 276A - Lunch Rush
[Lunch Rush](https://codeforces.com/problemset/problem/276/A)

Having written another programming contest, three Rabbits decided to grab some lunch. The coach gave the team exactly k time units for the lunch break.
<!-- more -->
The Rabbits have a list of n restaurants to lunch in: the i-th restaurant is characterized by two integers f<sub>i</sub> and t<sub>i</sub>. Value t<sub>i</sub> shows the time the Rabbits need to lunch in the i-th restaurant. If time t<sub>i</sub> exceeds the time k that the coach has given for the lunch break, then the Rabbits' joy from lunching in this restaurant will equal f<sub>i</sub> - (t<sub>i</sub> - k). Otherwise, the Rabbits get exactly f<sub>i</sub> units of joy.

Your task is to find the value of the maximum joy the Rabbits can get from the lunch, depending on the restaurant. The Rabbits must choose exactly one restaurant to lunch in. Note that the joy value isn't necessarily a positive value. 

#### Input:
The first line contains two space-separated integers — n (1 ≤ n ≤ 10<sup>4</sup>) and k (1 ≤ k ≤ 10<sup>9</sup>) — the number of restaurants in the Rabbits' list and the time the coach has given them to lunch, correspondingly. Each of the next n lines contains two space-separated integers — f<sub>i</sub> (1 ≤ f<sub>i</sub> ≤ 10<sup>9</sup>) and ti (1 ≤ t<sub>i</sub> ≤ 10<sup>9</sup>) — the characteristics of the i-th restaurant.

#### Output:
In a single line print a single integer — the maximum joy value that the Rabbits will get from the lunch. 

#### 範例:
input:
```
2 5
3 3
4 5
```
output:
```
4
```
input:
```
4 6
5 8
3 6
2 3
2 2
```
output:
```
3
```
input:
```
1 5
1 7
```
output:
```
-1
```

#### 題意:
有休息時間K可以去吃午餐，只能選一間餐廳，每間餐廳需花費t<sub>i</sub>時間吃飯，得到f<sub>i</sub>的快樂值，若是時間不夠的話則是得到f<sub>i</sub>-(t<sub>i</sub>-K)的快樂值，問你快樂值最大是多少？

#### 思路:
根據公式紀錄最大值，要注意的是會超過int的值域以及有可能會有負數。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/912deec3e5ca92ecb803eaa07b4b6fef.js"></script>
