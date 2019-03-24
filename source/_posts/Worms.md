---
title: Worms
date: 2019-03-14 10:03:23
tags:
    - CHU Training
    - CodeForces
    - binary search
    - 普通
---
It is lunch time for Mole. His friend, Marmot, prepared him a nice game for lunch.

Marmot brought Mole n ordered piles of worms such that i-th pile contains ai worms. He labeled all these worms with consecutive integers: worms in first pile are labeled with numbers 1 to a<sub>1</sub>, worms in second pile are labeled with numbers a<sub>1</sub> + 1 to a<sub>1</sub> + a<sub>2</sub> and so on. See the example for a better understanding.

Mole can't eat all the worms (Marmot brought a lot) and, as we all know, Mole is blind, so Marmot tells him the labels of the best juicy worms. Marmot will only give Mole a worm if Mole says correctly in which pile this worm is contained.

Poor Mole asks for your help. For all juicy worms said by Marmot, tell Mole the correct answers.
<!-- more -->
#### Input:
The first line contains a single integer n (1 ≤ n ≤ 10<sup>5</sup>), the number of piles.

The second line contains n integers a<sub>1</sub>, a<sub>2</sub>, ..., a<sub>n</sub> (1 ≤ a<sub>i</sub> ≤ 10<sup>3</sup>, a<sub>1</sub> + a<sub>2</sub> + ... + a<sub>n</sub> ≤ 10<sup>6</sup>), where ai is the number of worms in the i-th pile.

The third line contains single integer m (1 ≤ m ≤ 10<sup>5</sup>), the number of juicy worms said by Marmot.

The fourth line contains m integers q<sub>1</sub>, q<sub>2</sub>, ..., qm (1 ≤ q<sub>i</sub> ≤ a<sub>1</sub> + a<sub>2</sub> + ... + a<sub>n</sub>), the labels of the juicy worms.

#### Output:
Print m lines to the standard output. The i-th line should contain an integer, representing the number of the pile where the worm labeled with the number q<sub>i</sub> is.

#### 範例:

input:
```
5
2 7 3 4 9
3
1 25 11
```
output:
```
1
5
3
```
#### Note:
For the sample input:

● The worms with labels from [1, 2] are in the first pile.
● The worms with labels from [3, 9] are in the second pile.
● The worms with labels from [10, 12] are in the third pile.
● The worms with labels from [13, 16] are in the fourth pile.
● The worms with labels from [17, 25] are in the fifth pile.

#### 題意:
有隻鼴鼠正準備吃午餐，有另一隻鼴鼠幫他將N隻蟲，照編號頭尾相連的排成了一列，座標從第一隻蟲的最左邊為1開始延續，然後跟他講M次他該吃座標多少的蟲。現在問你他每一次吃的蟲是編號幾號的蟲？

#### 思路:
建一個陣列，將蟲的長度累加，陣列中的第i格存的是編號i的蟲的尾巴座標是多少。接著將每次輸入的座標用二分搜尋法查找蟲的編號。
![A](A.PNG)
#### 程式碼:
<script src="https://gist.github.com/Daviswww/b3c379b0cf5a291cb9f2a117b6a6c1a2.js"></script>

[題目網址](https://codeforces.com/problemset/problem/474/B)