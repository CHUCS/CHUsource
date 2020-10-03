---
title: Codeforces 1426D
keywords: Codeforces Non-zero Segments, Codeforces 1426D
date: 2020-10-03 15:10:30
categories: Codeforces
tags:
    - constructive algorithms
    - data structures
    - greedy
    - sortings
    - 1500
---
# Codeforces 1426D - Non-zero Segments
[題目網址](https://codeforces.com/problemset/problem/1426/D)

#### 題意:
Kolya有一陣列a，裡面數字有正有負，因為Kolya不喜歡0所以不包含0，Kolya也不喜歡子陣列中的總合為0(子陣列為一個連續的範圍)。
你要幫Kolya調整陣列使得任意子陣列總和不為0，你可以在陣列中的任一位置插入任意數字，就算數字超過可顯示範圍也行，請找出「最少」需要插入的數字的次數。
<!-- more -->
#### 思路:
需要從a<sub>i</sub>加到a<sub>j</sub>, (i < j)來確認總和，因此是個前綴和的問題，從開頭開始加，用map紀錄出現過的總和，對每次的總和作判斷，如果前面出現過相同的總和代表在這區間中有子陣列總和為0，例: a=[8 5 -5]，子陣列總和=[8 13 8]，8重複出現可以發現因為有子陣列[5 -5]總和為0的關係，因此這區間需要插入一個數，因為插入一個數的關係，所以左邊的區間總和不會出現0，因此出現過的總和(map)需要重置，重新計算總和。
#### 程式碼:
<script src="https://gist.github.com/zxzxcc112/cb5049de13da8958e88679cb0375f3ac.js"></script>