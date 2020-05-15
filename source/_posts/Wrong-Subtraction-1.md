---
title: CodeForces 977A v2
date: 2019-12-13 16:52:00
tags:
    - implementation
    - 新手
---
# CodeForces 977A v2 - Wrong Subtraction
[Wrong Subtraction](http://codeforces.com/problemset/problem/977/A)


#### 題意:
他給你一個N然後可以有K次操作。
操作條件:
● if the last digit of the number is non-zero, she decreases the number by one.(如果他不為0則減一)

● if the last digit of the number is zero, she divides the number by 10 (i.e. removes the last digit).(如果他為0就除以10)
<!-- more -->
#### 思路:
每次將N模10看看於數是不是0如果不是就減1，其餘除10。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/be92977c98e9f69528282fcd181111e3.js"></script>