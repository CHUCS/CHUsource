---
title: Single Push
date: 2019-11-30 09:27:04
tags:
    - 簡單
    - implementation
---
[CodeForces 1253A](http://codeforces.com/problemset/problem/1253/A)
<!-- more -->

#### 題意:
給你兩條字串問你兩條字串是否相等，而你可以將連續的區間加上一個N使的兩個字串相等，例如a=[3,7,1,4,1,2], b=[3,7,3,6,3,2]， 所以你可以把a[2]~a[4]加上2兩條數列就會一樣，可以相等輸出YES否則NO(如果a陣列有數字大於b也是輸出NO)。

#### 思路:
將兩數列相減後的結果存在一個陣列內，接著比對前後相不相等，不相等的話ok++，如果ok大於等於2的話代表有超過2次不一樣，所以一定不可能將一個區間加上一個數就可以相等。如果是負的話直接加10讓他超過2。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/a66ce2a9835ca967ca1fa19211c5fd2b.js"></script>