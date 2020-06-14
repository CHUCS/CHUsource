---
title: AOJ ITP1_9_B
keywords: ITP1_9_B Shuffle
date: 2020-06-14 22:16:30
categories: AOJ
tags:
    - implementation
---
# AOJ ITP1_9_B - Shuffle
[題目網址](https://onlinejudge.u-aizu.ac.jp/courses/lesson/2/ITP1/all/ITP1_9_B)

#### 題意:
給你一條字串將h長度的字放到後面去，例如字串abcdeefab，長度h為4會變成eefababcd，原本在前面的abcd被搬到後面去。
<!-- more -->
#### 思路:
把後面的字串搬到前面，前面的搬到後面換完後再放回原字串。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/f9f2de49e808132338c6b518a650aa8e.js"></script>