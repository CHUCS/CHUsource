---
title: Codeforces 785A Anton and Polyhedrons
date: 2019-04-20 18:05:09
tags:
    - implementation
    - string
    - 新手
---
[Codeforces 785A](https://codeforces.com/problemset/problem/785/A)
<!-- more -->
Anton's favourite geometric figures are regular polyhedrons. Note that there are five kinds of regular polyhedrons:
>>● Tetrahedron. Tetrahedron has 4 triangular faces.
>>● Cube. Cube has 6 square faces.
>>● Octahedron. Octahedron has 8 triangular faces.
>>● Dodecahedron. Dodecahedron has 12 pentagonal faces.
>>● Icosahedron. Icosahedron has 20 triangular faces.
All five kinds of polyhedrons are shown on the picture below:
![A](A.PNG)
Anton has a collection of n polyhedrons. One day he decided to know, how many faces his polyhedrons have in total. Help Anton and find this number!

#### Input:
The first line of the input contains a single integer n (1 ≤ n ≤ 200 000) — the number of polyhedrons in Anton's collection.
Each of the following n lines of the input contains a string s<sub>i</sub> — the name of the i-th polyhedron in Anton's collection. 
The string can look like this:
>>● "Tetrahedron" (without quotes), if the i-th polyhedron in Anton's collection is a tetrahedron.
>>● "Cube" (without quotes), if the i-th polyhedron in Anton's collection is a cube.
>>● "Octahedron" (without quotes), if the i-th polyhedron in Anton's collection is an octahedron.
>>● "Dodecahedron" (without quotes), if the i-th polyhedron in Anton's collection is a dodecahedron.
>>● "Icosahedron" (without quotes), if the i-th polyhedron in Anton's collection is an icosahedron.

#### Output:
Output one number — the total number of faces in all the polyhedrons in Anton's collection.

#### 範例:
input:
```
4
Icosahedron
Cube
Tetrahedron
Dodecahedron
```
output:
```
42
```
input:
```
3
Dodecahedron
Octahedron
Octahedron
```
output:
```
28
```

#### Note:
In the first sample Anton has one icosahedron, one cube, one tetrahedron and one dodecahedron. Icosahedron has 20 faces, cube has 6faces, tetrahedron has 4 faces and dodecahedron has 12 faces. In total, they have 20 + 6 + 4 + 12 = 42 faces.

#### 題意:
計算輸入的多面體總共面數是多少？

#### 思路:
根據輸入的字串累加對應的面即可。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/549840b54864ea08c6b80c319837adee.js"></script>
