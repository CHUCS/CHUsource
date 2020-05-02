---
title: CodeForces 368A Sereja and Coat Rack
date: 2020-04-07 13:47:48
tags:
    - implementation
    - 普通
---
[CodeForces 368A](https://codeforces.com/problemset/problem/368/A)
<!-- more -->

#### 題意:
餐廳有一個有n個鉤子的衣架，每一個鉤子只能掛一件衣服，且第i個鉤子需要付a_i元。現在每個客人來的時候都會想要掛衣服在最便宜的鉤子上，如果沒有鉤子能掛的話老闆需要賠d元給客人。現在輸入鉤子的數量、一次要賠的錢、所有鉤子要掛衣服時要付的價錢以及客人的數量，問你最後老闆今天靠鉤子會收到多少錢(有可能是負的)？

#### 思路:
排序後按照客人數量由最便宜的鉤子開始掛，沒得掛就扣錢，輸出。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/088f66204dfceb4ca145801133690fbe.js"></script>