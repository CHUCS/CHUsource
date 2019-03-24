---
title: They Are Everywhere
date: 2019-03-09 20:00:18
tags:
    - CHU Training
    - CodeForces
    - binary search
    - two pointers
    - 普通
---
Sergei B., the young coach of Pokemons, has found the big house which consists of n flats ordered in a row from left to right. It is possible to enter each flat from the street. It is possible to go out from each flat. Also, each flat is connected with the flat to the left and the flat to the right. Flat number 1 is only connected with the flat number 2 and the flat number n is only connected with the flat number n - 1.

There is exactly one Pokemon of some type in each of these flats. Sergei B. asked residents of the house to let him enter their flats in order to catch Pokemons. After consulting the residents of the house decided to let Sergei B. enter one flat from the street, visit several flats and then go out from some flat. But they won't let him visit the same flat more than once.

Sergei B. was very pleased, and now he wants to visit as few flats as possible in order to collect Pokemons of all types that appear in this house. Your task is to help him and determine this minimum number of flats he has to visit.

<!-- more -->
#### Input:
The first line contains the integer n (1 ≤ n ≤ 100 000) — the number of flats in the house.

The second line contains the row s with the length n, it consists of uppercase and lowercase letters of English alphabet, the i-th letter equals the type of Pokemon, which is in the flat number i.

#### Output:
Print the minimum number of flats which Sergei B. should visit in order to catch Pokemons of all types which there are in the house.

#### 範例:
input:
```
3
AaA
```
output:
```
2
```
input:
```
7
bcAAcbc
```
output:
```
3
```
input:
```
6
aaBCCe
```
output:
```
5
```
#### Note:
In the first test Sergei B. can begin, for example, from the flat number 1 and end in the flat number 2.

In the second test Sergei B. can begin, for example, from the flat number 4 and end in the flat number 6.

In the third test Sergei B. must begin from the flat number 2 and end in the flat number 6.

#### 題意:
本題題意是給你ㄧ串字母(只包含a-zA-Z)，你要選一段子字串"包含所有出現過的字母"，問你最短的子字串是多長，也就是最短且出現過母字串所有的字母。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/d78d6145cc18240f8586230ea46b906c.js"></script>

[題目網址](https://codeforces.com/problemset/problem/701/C)