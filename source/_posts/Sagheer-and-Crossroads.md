---
title: Codeforces 812A
date: 2019-03-26 13:24:28
keywords: Codeforces 812A, Codeforces Sagheer and Crossroads
tags:
    - CHU Training
    - CodeForces
    - implementation
    - 簡單
---
# Codeforces 812A - Sagheer and Crossroads
[Sagheer and Crossroads](https://codeforces.com/problemset/problem/812/A)

Sagheer is walking in the street when he comes to an intersection of two roads. Each road can be represented as two parts where each part has 3 lanes getting into the intersection (one for each direction) and 3 lanes getting out of the intersection, so we have 4 parts in total. Each part has 4 lights, one for each lane getting into the intersection (l — left, s — straight, r — right) and a light p for a pedestrian crossing. 
<!-- more -->
![A](A.PNG)
An accident is possible if a car can hit a pedestrian. This can happen if the light of a pedestrian crossing of some part and the light of a lane that can get to or from that same part are green at the same time.

Now, Sagheer is monitoring the configuration of the traffic lights. Your task is to help him detect whether an accident is possible.

#### Input:
The input consists of four lines with each line describing a road part given in a counter-clockwise order.

Each line contains four integers l, s, r, p — for the left, straight, right and pedestrian lights, respectively. The possible values are 0 for red light and 1 for green light.

#### Output:
On a single line, print "YES" if an accident is possible, and "NO" otherwise.

#### 範例:
input:
```
1 0 0 1
0 1 0 0
0 0 1 0
0 0 0 1
```
output:
```
YES
```
input:
```
0 1 1 0
1 0 1 0
1 1 0 0
0 0 0 1
```
output:
```
NO
```
input:
```
1 0 0 0
0 0 0 1
0 0 0 0
1 0 1 0
```
output:
```
NO
```

#### Note:
In the first example, some accidents are possible because cars of part 1 can hit pedestrians of parts 1 and 4. Also, cars of parts 2 and 3 can hit pedestrians of part 4.

In the second example, no car can pass the pedestrian crossing of part 4 which is the only green pedestrian light. So, no accident can occur.

#### 題意:
有個十字路口，每個路口都用l、r、s、p的4個狀態表示3個車道加1個行人穿越道的燈號狀態，1表示綠燈；0表示紅燈。從南開始逆時針依序輸入四個路口的燈號狀態，問你有沒有路口有可能發生人跟車的事故？

#### 思路:
依序比較每個方向的每個車道跟目的地的行人穿越道的燈號就可以了。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/7144cb5d6c8af5c7db3a1405a970a185.js"></script>
