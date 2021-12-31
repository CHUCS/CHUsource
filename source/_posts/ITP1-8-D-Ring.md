---
title: AOJ ITP1_8_D Ring
keywords: ITP1_8_D Ring
date: 2020-06-14 12:45:58
categories: AOJ
tags:
    - implementation
---
# AOJ ITP1_8_D - Ring
[題目網址](https://onlinejudge.u-aizu.ac.jp/courses/lesson/2/ITP1/all/ITP1_8_D)

#### 題意:
輸入一個字串他是環狀的，也就是頭尾相接的一個字串，問你p字串有沒有在環裡面出現，有的話印"Yes"，否則"No"。

<!-- more -->
#### 思路:
下面有兩個方法，方法一是把頭尾相接然後用c++的函式find去尋找有沒有這個字串，第二個方式是逐一比對如直到比對長度一樣。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/711a21ff7c7a3dc889ec1214d2678117.js"></script>