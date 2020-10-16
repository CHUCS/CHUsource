---
title: CodeForces 1418B
keywords: CodeForces 1418B, CodeForces Negative Prefixes
date: 2020-09-22 22:52:31
categories: Codeforces
tags:
    - greedy
    - sortings
    - 1300
---
# CodeForces 1418B - Negative Prefixes
[題目網址](https://codeforces.com/problemset/problem/1418/B)

#### 題意:
你有一個陣列a，裡面有n個整數，有些整數被鎖住有些沒有，你能對沒有鎖住的整數做交換位置的動作(沒鎖對沒鎖)，另外有個序列p，為a<sub>1</sub>~a<sub>n</sub>的總和:p<sub>1</sub> = a<sub>1</sub>, p<sub>2</sub> = a<sub>1</sub> + a<sub>2</sub>... p<sub>n</sub> = a<sub>1</sub> + a<sub>2</sub> +...+ a<sub>n</sub>
讓k為最大值j，並且p<sub>j</sub> < 0 ，若p中沒有任何p<sub>j</sub> < 0，則 k=0
你要交換未鎖住整數的位置，使得k為最小值，印出調整過後的陣列a
<!-- more -->
#### 思路:
將沒鎖住的整數獨立出來，由大到小排序，再依序從頭一一放回陣列中沒鎖住的位置。
不考慮鎖住的數字，當正整數總和 >= 負整數總和時，將正整數排前面則k=0
當正整數總和 < 負整數總和時，則不管甚麼順序k最大
不選擇小排到大是因為第一個狀況，若負整數先在前面則k值不會最小

#### 程式碼:
<script src="https://gist.github.com/zxzxcc112/14bcb2bffc5c9b8cd2341a8758f78b47.js"></script>