---
title: Magical Boxes
date: 2019-10-15 13:25:45
tags:
    - 普通 
    - implementation
    - math
    - sortings
---
Emuskald is a well-known illusionist. One of his trademark tricks involves a set of magical boxes. The essence of the trick is in packing the boxes inside other boxes.

From the top view each magical box looks like a square with side length equal to 2<sup>k</sup> (k is an integer, k ≥ 0) units. A magical box v can be put inside a magical box u, if side length of v is strictly less than the side length of u. In particular, Emuskald can put 4 boxes of side length 2<sup>k - 1</sup> into one box of side length 2<sup>k</sup>, or as in the following figure:
<!-- more -->
![A](A.PNG)
Emuskald is about to go on tour performing around the world, and needs to pack his magical boxes for the trip. He has decided that the best way to pack them would be inside another magical box, but magical boxes are quite expensive to make. Help him find the smallest magical box that can fit all his boxes.
#### Input:
The first line of input contains an integer n (1 ≤ n ≤ 10<sup>5</sup>), the number of different sizes of boxes Emuskald has. Each of following n lines contains two integers k<sub>i</sub> and a<sub>i</sub> (0 ≤ k<sub>i</sub> ≤ 10<sup>9</sup>, 1 ≤ a<sub>i</sub> ≤ 10<sup>9</sup>), which means that Emuskald has ai boxes with side length 2<sup>k<sub>i</sub></sup>. It is guaranteed that all of ki are distinct.
#### Output:
Output a single integer p, such that the smallest magical box that can contain all of Emuskald’s boxes has side length 2<sup>p</sup>.
#### 範例:
input:
```
2
0 3
1 5
```
output:
```
3
```
input:
```
1
0 4
```
output:
```
1
```
input:
```
2
1 10
2 2
```
output:
```
3
```
#### Note:
Picture explanation. If we have 3 boxes with side length 2 and 5 boxes with side length 1, then we can put all these boxes inside a box with side length 4, for example, as shown in the picture.

In the second test case, we can put all four small boxes into a box with side length 2.
#### 題意:
輸入N，再輸入N種箱子的尺寸跟數量， 1個箱子可以裝1~4個比自己小一號的箱子，問你需要一個多大的箱子才能裝得下全部的箱子。


#### 思路:
1個箱子可以裝4個比自己小一號的箱子，所以先把輸入的箱子按尺寸大到小排序，記錄現在最大的尺寸，計算可不可以裝得下那些比較小的，要注意的是同一尺寸的箱子最多只會有1000000000個，所以可以裝超過這個數字就不用判斷了，一定裝的下；裝不下的就計算需要幾個目前最大的箱子才裝得下，先記著。

最後跑完全部後再用需要幾個目前最大的箱子來算需要多大的箱子。
#### 程式碼:
<script src="https://gist.github.com/Daviswww/ffe732aec0bdd1ce3ec815518e180d71.js"></script>
[題目網址](https://codeforces.com/problemset/problem/269/A)
