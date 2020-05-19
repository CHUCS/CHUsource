---
title: CodeForces 996A
date: 2019-12-14 11:57:51
link: Hit-the-Lottery
keywords: Codeforces 996A, Codeforces Hit the Lottery
tags:
    - dp
    - greedy
    - 新手
---
# CodeForces 996A - Hit the Lottery
[Hit the Lottery](http://codeforces.com/problemset/problem/996/A)


#### 題意:
給你N元利用他給你的幣值數1, 5, 10, 20, 100換出最少的硬幣數量，例如125元可以換1個100元，1個20元，1個5元，總共換了3個。
<!-- more -->
#### 思路:
先將幣值定義好，接著由大的幣值開始換，換完後再將剩下的錢存起來。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/506667681b6d86205d3ef998c8f1ad80.js"></script>