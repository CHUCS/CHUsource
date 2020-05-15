---
title: CodeForces 1253C
date: 2019-12-13 16:52:43
tags:
    - 一般
    - greedy
    - dp
    - math
    - sortings
---
# CodeForces 1253C - Sweets Eating
[Sweets Eating](http://codeforces.com/problemset/problem/1253/C)


#### 題意:
輸入N(有多少個甜點)、M(一天可以吃幾個)和N個甜點的含糖數，在第D天吃下含糖A的甜點時會得到加權含糖數A x D，求吃K(K=1~N)個時的最少加權含糖數是多少？
<!-- more -->
#### 思路:
先由題目需求得知，在吃X個的情況下一定是挑含糖數最少的X個出來，並且由高的開始吃，得出的就是K=X時的最少含糖數，因此先排序得到陣列A。計算累加陣列S，S[i]等於A[0]~A[i]的總和。現在要求陣列K，記錄所有答案，觀察後得知，K[i] = K[i – M] + S[i]，如下一頁所示，將陣列輸出就是答案。
![A](A.PNG)
#### 程式碼:
<script src="https://gist.github.com/Daviswww/0a2cb1dad996580b67cf36a5a37bc11c.js"></script>