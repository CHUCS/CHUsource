---
title: Mashmokh and ACM
date: 2019-11-30 08:53:08
tags:
    - 普通
    - combinatorics
    - number theory
    - dp
---
[CodeForces 414B](http://codeforces.com/problemset/problem/414/B)
<!-- more -->

#### 題意:
輸入N、K，指定數列長度K，其中所有元素都在1~N之間，且每一個元素都可以整除下一個元素，問有幾種數列滿足條件？

#### 思路:
當數列長度為x，結尾為y時，要增長數列的方法就是在數列尾端增加一個是y的倍數的元素，因此這個數列可以衍伸出y、2y、3y…ty，ty <= N，共t個數列。以這個想法下去建置一個陣列，紀錄當前長度結尾為x(x=1~N)的數列有幾個，逐次增加長度，跑完後就是答案。
![A](A.PNG)
![B](B.PNG)
![C](C.PNG)
![D](D.PNG)
![E](E.PNG)
![F](F.PNG)
![G](G.PNG)

#### 程式碼:
<script src="https://gist.github.com/Daviswww/4c631d92b0f0aec4e4e887ca67ded26a.js"></script>