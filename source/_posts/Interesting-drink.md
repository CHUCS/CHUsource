---
title: Codeforces 706B Interesting drink
date: 2019-03-26 13:25:37
tags:
    - CHU Training
    - CodeForces
    - binary search
    - sortings
    - 普通
---
[Codeforces 706B](https://codeforces.com/problemset/problem/706/B)
<!-- more -->
Vasiliy likes to rest after a hard work, so you may often meet him in some bar nearby. As all programmers do, he loves the famous drink "Beecola", which can be bought in n different shops in the city. It's known that the price of one bottle in the shop i is equal to x<sub>i</sub> coins.

Vasiliy plans to buy his favorite drink for q consecutive days. He knows, that on the i-th day he will be able to spent m<sub>i</sub> coins. Now, for each of the days he want to know in how many different shops he can buy a bottle of "Beecola".

#### Input:
The first line of the input contains a single integer n (1 ≤ n ≤ 100 000) — the number of shops in the city that sell Vasiliy's favourite drink.

The second line contains n integers xi (1 ≤ x<sub>i</sub> ≤ 100 000) — prices of the bottles of the drink in the i-th shop.

The third line contains a single integer q (1 ≤ q ≤ 100 000) — the number of days Vasiliy plans to buy the drink.

Then follow q lines each containing one integer mi (1 ≤ m<sub>i</sub> ≤ 10<sup>9</sup>) — the number of coins Vasiliy can spent on the i-th day.
#### Output:
Print q integers. The i-th of them should be equal to the number of shops where Vasiliy will be able to buy a bottle of the drink on the i-th day.
#### 範例:
input:
```
5
3 10 8 6 11
4
1
10
3
11
```
output:
```
0
4
1
5
```

#### Note:
On the first day, Vasiliy won't be able to buy a drink in any of the shops.

On the second day, Vasiliy can buy a drink in the shops 1, 2, 3 and 4.

On the third day, Vasiliy can buy a drink only in the shop number 1.

Finally, on the last day Vasiliy can buy a drink in any shop.

#### 題意:
現在有n間商店，各自賣蜜蜂可樂xi元，你知道你接下來q天會各自有mi元，沒花完不會累積，問每一天有幾間商店是買得起的？

#### 思路:
先將n間商店依售價從小排到大，接下來輸入每個mi時做二分搜尋法即可。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/a67e4431ea72f8dae5ebc9b935fa6b50.js"></script>
