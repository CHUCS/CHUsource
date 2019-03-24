---
title: Drinks
date: 2019-03-21 09:37:08
tags:
    - CHU Training
    - CodeForces
    - implementation
    - 新手 
---
Little Vasya loves orange juice very much. That's why any food and drink in his kitchen necessarily contains orange juice. There are n drinks in his fridge, the volume fraction of orange juice in the i-th drink equals p<sub>i</sub> percent.

One day Vasya decided to make himself an orange cocktail. He took equal proportions of each of the n drinks and mixed them. Then he wondered, how much orange juice the cocktail has.

Find the volume fraction of orange juice in the final drink.
<!-- more -->
#### Input:
The first input line contains a single integer n (1 ≤ n ≤ 100) — the number of orange-containing drinks in Vasya's fridge. The second line contains n integers pi (0 ≤ p<sub>i</sub> ≤ 100) — the volume fraction of orange juice in the i-th drink, in percent. The numbers are separated by a space.
#### Output:
Print the volume fraction in percent of orange juice in Vasya's cocktail. The answer will be considered correct if the absolute or relative error does not exceed 10<sup>-4</sup>.
#### 範例:
input:
```
3
50 50 100
```
output:
```
66.666666666667
```
input:
```
4
0 25 50 75
```
output:
```
37.500000000000
```

#### Note:
![A](A.PNG)

#### 題意:
有n種飲料，第i種飲料的柳橙汁含量比例是百分之p<sub>i</sub>。現在將n種飲料等比例的混合做成綜合柳橙汁，最後的柳橙汁含量百分比是多少？

#### 思路:
加總平均。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/b9a845e27cfb68cdf7fc52926580f9bc.js"></script>

[題目網址](https://codeforces.com/problemset/problem/200/B)