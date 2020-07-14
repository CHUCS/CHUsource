---
title: AOJ ALDS1_4_B
keywords: ALDS1 Binary Search
date: 2020-07-14 13:24:03
categories: AOJ
tags:
    - implementation
---
# AOJ ALDS1_4_B - Binary Search
[題目網址](https://onlinejudge.u-aizu.ac.jp/courses/lesson/1/ALDS1/all/ALDS1_4_B)

#### 題意:
給N個整數數列S，還有q個整數數列T，請輸出T在S裡面有找到幾個。利用二分搜索來尋找。

<!-- more -->
#### 思路:
宣告三個變數分別紀錄左邊、右邊和中間位置，每次判斷中間那個數字是否等於要找的數字，如果沒有則判斷大於小於以利切割，如果大於的話就把r換成中間的位置，小於則把l換成中間的位置。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/b7e47a957066b3bb5888030be0aac43f.js"></script>