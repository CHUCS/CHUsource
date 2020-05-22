---
title: Codeforces 990B
date: 2019-03-09 19:42:15
keywords: Codeforces 990B, Codeforces Micro-World
categories: Codeforces
tags:
    - CodeForces
    - sortings
    - 簡單
---
# Codeforces 990B - Micro-World
[Micro-World](https://codeforces.com/problemset/problem/990/B)

You have a Petri dish with bacteria and you are preparing to dive into the harsh micro-world. But, unfortunately, you don't have any microscope nearby, so you can't watch them.
<!-- more -->
You know that you have n bacteria in the Petri dish and size of the i-th bacteria is a<sub>i</sub>. Also you know intergalactic positive integer constant K.

The i-th bacteria can swallow the j-th bacteria if and only if a<sub>i</sub>>a<sub>j</sub> and a<sub>i</sub>≤a<sub>j</sub>+K. The j-th bacteria disappear, but the i-th bacteria doesn't change its size. The bacteria can perform multiple swallows. On each swallow operation any bacteria i can swallow any bacteria j if a<sub>i</sub>a<sub>j</sub> and a<sub>i</sub>≤a<sub>j</sub>+K. The swallow operations go one after another.

For example, the sequence of bacteria sizes a=[101,53,42,102,101,55,54] and K=1. The one of possible sequences of swallows is: [101,53,42,102,(101),55,54] → [101,(53),42,102,55,54] → [(101),42,102,55,54] → [42,102,55,(54)] → [42,102,55]. In total there are 3 bacteria remained in the Petri dish.

Since you don't have a microscope, you can only guess, what the minimal possible number of bacteria can remain in your Petri dish when you finally will find any microscope.


#### Input:
The first line contains two space separated positive integers n and K (1≤n≤2⋅10<sup>5</sup>, 1≤K≤10<sup>6</sup>) — number of bacteria and intergalactic constant K.

The second line contains n space separated integers a<sub>1</sub>,a<sub>2</sub>,…,a<sub>n</sub> (1≤a<sub>i</sub>≤10<sup>6</sup>) — sizes of bacteria you have.

#### Output:
Print the only integer — minimal possible number of bacteria can remain.

#### 範例:
input:
```
7 1
101 53 42 102 101 55 54
```
output:
```
3
```
input:
```
6 5
20 15 10 15 20 25
```
output:
```
1
```
input:
```
7 1000000
1 1 1 1 1 1 1
```
output:
```
7
```
#### Note:
The first example is clarified in the problem statement.

In the second example an optimal possible sequence of swallows is: [20,15,10,15,(20),25] → [20,15,10,(15),25] → [20,15,(10),25] → [20,(15),25] → [(20),25] → [25].

In the third example no bacteria can swallow any other bacteria.

#### 題意:
這題再說有N個細菌，每個細菌大小為ai，細菌ai可以吃其他細菌aj不過只有兩個規則，一個規則是ai > aj 而且 ai <= aj + k 才可以吃掉。

#### 思路:
我們就先存好同樣尺寸的細菌，然後把全部細菌排序，之後符合規則的細菌我就一次吃掉。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/ea7da7267654c3a79516b4bb44aac686.js"></script>

