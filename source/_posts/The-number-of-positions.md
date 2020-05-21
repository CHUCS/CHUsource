---
title: Codeforces 124A
date: 2019-03-26 13:24:16
keywords: Codeforces 124A, Codeforces The number of positions
tags:
    - CHU Training
    - CodeForces
    - math
    - 新手
---
# Codeforces 124A - The number of positions
[The number of positions](https://codeforces.com/problemset/problem/124/A)

Petr stands in line of n people, but he doesn't know exactly which position he occupies. He can say that there are no less than a people standing in front of him and no more than b people standing behind him. Find the number of different positions Petr can occupy.
<!-- more -->
#### Input:
The only line contains three integers n, a and b (0 ≤ a, b < n ≤ 100).

#### Output:
Print the single number — the number of the sought positions.

#### 範例:
input:
```
3 1 1
```
output:
```
2
```
input:
```
5 2 3
```
output:
```
3
```

#### Note:
The possible positions in the first sample are: 2 and 3 (if we number the positions starting with 1).

In the second sample they are 3, 4 and 5.

#### 題意:
在n個人的隊列中，他前面有不小於a個的人；後面有不多於b個的人，問你他有幾個可能的位置？

#### 思路:
將隊列以編號[1,n]來看，則前面有不小於a個的人表示他在[a+1,n]的位置；後面有不多於b個的人表示他在[n-b,n]的位置，取兩者的交集即可。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/7d368f649a7201e7031fea98970cb0bf.js"></script>

