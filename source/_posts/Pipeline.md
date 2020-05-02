---
title: Codeforces 287B Pipeline
date: 2019-10-20 22:51:40
tags:
    - binary search
    - math
---
[Codeforces 287B](https://codeforces.com/problemset/problem/287/B)
<!-- more -->
Vova, the Ultimate Thule new shaman, wants to build a pipeline. As there are exactly n houses in Ultimate Thule, Vova wants the city to have exactly n pipes, each such pipe should be connected to the water supply. 

A pipe can be connected to the water supply if there's water flowing out of it. Initially Vova has only one pipe with flowing water. Besides, Vova has several splitters.

A splitter is a construction that consists of one input (it can be connected to a water pipe) and x output pipes. When a splitter is connected to a water pipe, water flows from each output pipe. You can assume that the output pipes are ordinary pipes. For example, you can connect water supply to such pipe if there's water flowing out from it. At most one splitter can be connected to any water pipe.

![A](A.PNG)

Vova has one splitter of each kind: with 2, 3, 4, ..., k outputs. Help Vova use the minimum number of splitters to build the required pipeline or otherwise state that it's impossible.

Vova needs the pipeline to have exactly n pipes with flowing out water. Note that some of those pipes can be the output pipes of the splitters.

#### Input:
The first line contains two space-separated integers n and k (1 ≤ n ≤ 10<sup>18</sup>, 2 ≤ k ≤ 10<sup>9</sup>).

Please, do not use the %lld specifier to read or write 64-bit integers in С++. It is preferred to use the cin, cout streams or the %I64d specifier.
#### Output:
Print a single integer — the minimum number of splitters needed to build the pipeline. If it is impossible to build a pipeline with the given splitters, print -1.
#### 範例:
input:
```
4 3
```
output:
```
2
```
input:
```
5 5
```
output:
```
1
```
input:
```
8 4
```
output:
```
-1
```

#### 題意:
Vova希望在一個叫the Ultimate Thule new shaman的城市建立一條管道，城市中有n座房子，因此Vova希望剛好有n條管道，因此每條這樣的管道都應連接到供水系統。如果有水流出，則可以將管道連接到供水系統。最初，Vova只有一根流水的管道。此外，Vova有幾個分離器。

Vova有每種分配器：具有2、3、4，...，k個輸出。幫助Vova使用最少數量的拆分器來構建所需的管道，或者以其他方式聲明這是不可能的。

Vova需要管道中有正好n根流出水的管道。其中一些管道可以是分配器的輸出管道。

#### 思路:
因為分離器是2,3,4,...,k個輸出，則在正常情況下只要不超過所有分離器組合起來的輸出總數就一定能滿足條件，尋找n到k的分離器組合的輸出總數，如超過目標值或等於目標值，則答案為(k-n+1)個。

#### 程式碼:
<script src="https://gist.github.com/89snnfk561/e95472b21f34e1b7ca5440a4a11da55a.js"></script>

