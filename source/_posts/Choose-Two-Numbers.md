---
title: CodeForces 1206A Choose Two Numbers
date: 2020-04-07 13:47:59
tags:
    - math
    - sortings
    - 普通
---
[CodeForces 1206A](https://codeforces.com/problemset/problem/1206/A)
<!-- more -->

#### 題意:
輸入兩個集合的元素數量及集合中的所有元素，請你從兩個集合中各挑出一個元素，讓這兩個元素的和不在這兩個集合中。

#### 思路:
因為元素都是正整數，所以兩個元素的和一定比這兩個元素大，因次只要挑出兩個集合中各自最大的元素相加就一定不在原本的集合中。排序，輸出各自最大的元素。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/d975ad83e445dcad60d027f3b73a057e.js"></script>