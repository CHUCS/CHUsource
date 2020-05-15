---
title: Codeforces 888C
date: 2019-04-27 18:42:21
tags:
    - 普通
    - binary search
    - implementation
    - two pointers
---
# Codeforces 888C - K-Dominant Character
[K-Dominant Character](https://codeforces.com/problemset/problem/888/C)

You are given a string s consisting of lowercase Latin letters. Character c is called k-dominant iff each substring of s with length at least k contains this character c.
<!-- more -->
You have to find minimum k such that there exists at least one k-dominant character.

#### Input:
The first line contains string s consisting of lowercase Latin letters (1 ≤ |s| ≤ 100000).

#### Output:
Print one number — the minimum value of k such that there exists at least one k-dominant character.

#### 範例:
input:
```
abacaba
```
output:
```
2
```
input:
```
zzzzz
```
output:
```
1
```
input:
```
abcde
```
output:
```
3
```

#### 題意:
給你一個字串，當所有長度為K的子字串都有至少一個共同字元c時，則c在此字串中稱為K-Dominant 。現在c未定，但至少要有一個c存在K-Dominant ，問你K最小可以是多少？

#### 思路:
用二分搜尋法依照規則搜尋子字串長度。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/a14ccf51ce05c20cd0948abbd3425b79.js"></script>
