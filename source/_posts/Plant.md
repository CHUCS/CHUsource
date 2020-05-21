---
title: Codeforces 185A
date: 2019-09-30 20:11:01
keywords: Codeforces 185A, Codeforces Plant
tags:
    - 普通
    - math
---
# Codeforces 185A - Plant
[Plant](https://codeforces.com/problemset/problem/185/A)

Dwarfs have planted a very interesting plant, which is a triangle directed "upwards". This plant has an amusing feature. After one year a triangle plant directed "upwards" divides into four triangle plants: three of them will point "upwards" and one will point "downwards". After another year, each triangle plant divides into four triangle plants: three of them will be directed in the same direction as the parent plant, and one of them will be directed in the opposite direction. Then each year the process repeats. The figure below illustrates this process.
<!-- more -->
![A](A.PNG)
Help the dwarfs find out how many triangle plants that point "upwards" will be in n years.
#### Input:
The first line contains a single integer n (0 ≤ n ≤ 10<sup>18</sup>) — the number of full years when the plant grew.

Please do not use the %lld specifier to read or write 64-bit integers in С++. It is preferred to use cin, cout streams or the %I64d specifier.
#### Output:
Print a single integer — the remainder of dividing the number of plants that will point "upwards" in n years by 1000000007 (10<sup>9</sup> + 7).
#### 範例:
input:
```
1
```
output:
```
3
```
input:
```
2
```
output:
```
10
```
#### Note:
The first test sample corresponds to the second triangle on the figure in the statement. The second test sample corresponds to the third one.

#### 題意:
觀察後可以得到N=1時向上的三角形有1+2=3個，N=2時有1+2+3+4=1+2+…+2<sup>2</sup>=10個，因此推導出輸入N時有1+…+2N=((2<sup>N</sup>+1) 2<sup>N</sup>)/2個三角形，因此題目可以等價為求((2<sup>N</sup>+1) 2<sup>N</sup>)/2%1000000007 
另外一個要知道的數學知識是:
(a*b*c*d)%e≡((a%e)∙(b%e)∙(c%e)∙(d%e))%e

#### 思路:
我們現在需要求出2<sup>𝑁</sup>%1000000007是多少，將2<sup>N</sup>分解開並分別求出餘數後用前面的方式求出乘起來後的餘數，然後再算出最後的餘數就是答案，例如2<sup>11</sup>=2<sup>8</sup>∙2<sup>2</sup>∙2<sup>1</sup>  

#### 程式碼:
<script src="https://gist.github.com/Daviswww/74951133f40de6bd5ff946f1de27f2f9.js"></script>


