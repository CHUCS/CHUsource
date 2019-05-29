---
title: Bakery
date: 2019-05-05 22:01:07
tags:
    - 簡單
    - graphs
---
Masha wants to open her own bakery and bake muffins in one of the n cities numbered from 1 to n. There are m bidirectional roads, each of whose connects some pair of cities.

To bake muffins in her bakery, Masha needs to establish flour supply from some storage. There are only k storages, located in different cities numbered a<sub>1</sub>, a<sub>2</sub>, ..., a<sub>k</sub>.

Unforunately the law of the country Masha lives in prohibits opening bakery in any of the cities which has storage located in it. She can open it only in one of another n - k cities, and, of course, flour delivery should be paid — for every kilometer of path between storage and bakery Masha should pay 1 ruble.

Formally, Masha will pay x roubles, if she will open the bakery in some city b (a<sub>i</sub> ≠ b for every 1 ≤ i ≤ k) and choose a storage in some city s (s = aj for some 1 ≤ j ≤ k) and b and s are connected by some path of roads of summary length x (if there are more than one path, Masha is able to choose which of them should be used).

Masha is very thrifty and rational. She is interested in a city, where she can open her bakery (and choose one of k storages and one of the paths between city with bakery and city with storage) and pay minimum possible amount of rubles for flour delivery. Please help Masha find this amount.
<!-- more -->
#### Input:
The first line of the input contains three integers n, m and k (1 ≤ n, m ≤ 10<sup>5</sup>, 0 ≤ k ≤ n) — the number of cities in country Masha lives in, the number of roads between them and the number of flour storages respectively.

Then m lines follow. Each of them contains three integers u, v and l (1 ≤ u, v ≤ n, 1 ≤ l ≤ 10<sup>9</sup>, u ≠ v) meaning that there is a road between cities u and v of length of l kilometers .

If k > 0, then the last line of the input contains k distinct integers a<sub>1</sub>, a<sub>2</sub>, ..., a<sub>k</sub> (1 ≤ a<sub>i</sub> ≤ n) — the number of cities having flour storage located in. If k = 0 then this line is not presented in the input.

#### Output:
Print the minimum possible amount of rubles Masha should pay for flour delivery in the only line.

If the bakery can not be opened (while satisfying conditions) in any of the n cities, print  - 1 in the only line.

#### 範例:
input:
```
5 4 2
1 2 5
1 2 3
2 3 4
1 4 10
1 5
```
output:
```
3
```
input:
```
3 1 1
1 2 3
3
```
output:
```
-1
```
input:
```
2 5
5 4 3 2 1
```
output:
```
1
```
input:
```
3 9
42 42 42 42 42 42 42 42 42
```
output:
```
3
```
#### Note:
![A](A.PNG)

#### 題意:
輸入N個人跟M包食物，再輸入這M包食物的種類。現在規定每個人指定一種食物，每天只能吃一樣種類的食物，沒有每個人都要指定一樣或不一樣的種類，問你這些食物最多能吃幾天？

#### 思路:
用二分搜尋法搜尋天數d，判斷食物夠不夠吃d天。先統計食物的出現次數，出現次數除以天數就等於能給幾個人吃d天，加總所有食物能供給的人數，若是大於等於N就表示這些食物可以吃d天。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/fcc80ed825820de5d02df437d0351496.js"></script>
[題目網址](https://codeforces.com/problemset/problem/707/B)