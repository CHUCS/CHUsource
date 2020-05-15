---
title: CodeForces 1324B
date: 2020-03-20 13:26:00
tags:
    - brute force
    - strings
    - 普通
---
# CodeForces 1324B - Yet Another Palindrome Problem
[Yet Another Palindrome Problem](https://codeforces.com/problemset/problem/1324/B)


#### 題意:
給你一串數列，問你能不能在其中挑出長度至少為3並且是迴文的子序列？
<!-- more -->
#### 思路:
首先，迴文長度若是偶數，表示中心兩個字是一樣的，那就可以不取其中一個，將迴文長度轉為奇數；其次，若迴文長度是奇數，則最旁邊兩個一定是一樣的，可以一起去掉，讓長度減2且還是奇數。綜合前面兩點，可以得知若有迴文，則一定可以推導成長度3的迴文，因此，目標可以推導成要找出有沒有長度正好是3的迴文。接下來觀察長度正好是3迴文，發現只有兩種模式，aaa和aba，第一種由3個一樣的字組成，第二個由兩個不連續的一樣字夾著一個不一樣的字組成。邊輸入邊記錄所有數字的出現次數和出現位置，若有數字出現3次以上，那就可以形成第一種迴文，輸出YES；若有數字出現兩次了，計算這兩次出現位置是不是不再隔壁，是的話中間就可以隨便挑一個夾著形成第二種迴文，輸出YES；都無法滿足就輸出NO。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/0ad7961413bd4ebb31fcc13a4ab418e5.js"></script>