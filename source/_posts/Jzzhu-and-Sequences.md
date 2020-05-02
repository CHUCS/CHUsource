---
title: Jzzhu and Sequences
date: 2019-05-05 22:00:30
tags:
    - 普通
    - implementation
    - math
---
[Codeforces 450B](https://codeforces.com/problemset/problem/450/B)
<!-- more -->
Jzzhu has invented a kind of sequences, they meet the following property:
![A](A.PNG)
You are given x and y, please calculate f<sub>n</sub> modulo 1000000007 (10<sup>9</sup> + 7).

#### Input:
The first line contains two integers x and y (|x|, |y| ≤ 10<sup>9</sup>). The second line contains a single integer n (1 ≤ n ≤ 2·10<sup>9</sup>).

#### Output:
Output a single integer representing f<sub>n</sub> modulo 1000000007 (10<sup>9</sup> + 7).

#### 範例:
input:
```
2 3
3
```
output:
```
1
```
input:
```
0 -1
2
```
output:
```
1000000006
```
#### Note:
In the first sample, f<sub>2</sub> = f<sub>1</sub> + f<sub>3</sub>, 3 = 2 + f<sub>3</sub>, f<sub>3</sub> = 1.

In the second sample, f<sub>2</sub> =  - 1;  - 1 modulo (10<sup>9</sup> + 7) equals (10<sup>9</sup> + 6).
#### 題意:
輸入X跟Y作為一個數列的前兩項，並給你數列的規則，問你第N項對100000007取餘數後的值是多少？

#### 思路:
將規則用X跟Y繼續列舉，發現每6項數值會有一個循環，因此先將前6項計算好，再計算第N項是6項中的第幾項後就可以取餘數了，要注意的是餘數是負數的時候要加回正數。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/050a756b7c15a39d45e2148f120cc259.js"></script>
