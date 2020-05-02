---
title: Codeforces 118B Present from Lena
date: 2019-03-07 19:44:21
tags:
    - CHU Training
    - CodeForces
    - implementation
    - 簡單
---
[Codeforces 118B](https://codeforces.com/problemset/problem/118/B)
<!-- more -->
Vasya's birthday is approaching and Lena decided to sew a patterned handkerchief to him as a present. Lena chose digits from 0 to n as the pattern. The digits will form a rhombus. The largest digit n should be located in the centre. The digits should decrease as they approach the edges. For example, for n = 5 the handkerchief pattern should look like that:


          0
        0 1 0
      0 1 2 1 0
    0 1 2 3 2 1 0
  0 1 2 3 4 3 2 1 0
0 1 2 3 4 5 4 3 2 1 0
  0 1 2 3 4 3 2 1 0
    0 1 2 3 2 1 0
      0 1 2 1 0
        0 1 0
          0
Your task is to determine the way the handkerchief will look like by the given n.

#### Input:
The first line contains the single integer n (2 ≤ n ≤ 9).

#### Output:
Print a picture for the given n. You should strictly observe the number of spaces before the first digit on each line. Every two adjacent digits in the same line should be separated by exactly one space. There should be no spaces after the last digit at the end of each line.

#### 範例:
input:
```
2
```
output:
```
    0
  0 1 0
0 1 2 1 0
  0 1 0
    0
```
input:
```
3
```
output:
```
      0
    0 1 0
  0 1 2 1 0
0 1 2 3 2 1 0
  0 1 2 1 0
    0 1 0
      0
```

#### 題意:
印出一個按照他的規則的菱形。
每個數字後面必須要有空白，但最後一個字後面不能有空白!

#### 思路:
```
    0 1 2 3 4 5 6 7 8 9 10  
A             0
B           0 1 0
C         0 1 2 1 0
D       0 1 2 3 2 1 0
E     0 1 2 3 4 3 2 1 0
F   0 1 2 3 4 5 4 3 2 1 0
G     0 1 2 3 4 3 2 1 0
H       0 1 2 3 2 1 0
I         0 1 2 1 0
J           0 1 0
K             0
```

要印菱形要先決定起始的位置，這一題菱形的第一列的起始位置是第六行(編號5)。
第二列(編號B)的起始位置則是上一列減1，依此類推直到第五列。
第六列(編號F)開始起始位置正好相反，是上一列加1。
菱形的第一列印的結束位置也是是第六行(編號5)，也就是印完就換下一行。
每一行的結束位置的流程則和開始位置相反，先加後減。
	 
*這樣會印出緊湊的菱形，這一題菱形的數字之間"要加空白，但每一列最後一行不可以有空白"。

中間沒空白的菱形:
```
     *
    ***
   *****
  *******
 *********
***********
 *********
  *******
   *****
    ***
     *
```
中間有空白的菱形:
```
          *
        * * *
      * * * * *
    * * * * * * *
  * * * * * * * * *
* * * * * * * * * * *
  * * * * * * * * *
    * * * * * * *
      * * * * *
        * * *
          *
```
這樣菱形就完成了，剩下就是印出數字!

#### 程式碼:
<script src="https://gist.github.com/Daviswww/9465b85756422ea5cf249d925c518520.js"></script>

