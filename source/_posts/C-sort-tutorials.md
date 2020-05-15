---
title: C++ sort tutorials
date: 2020-04-07 13:39:59
tags:
    - tutorials
    - cpp
---
# C++ sort tutorials
● C++
● #include &lt;algorithm>
● using namespace std;
● sort(sort_start, sort_end, compare_function);
● sort_start：排序範圍開頭記憶體位址，通常直接用陣列名稱
● Sort_end：排序範圍結尾記憶體位址，此位址不參與排序
<!-- more -->
### compare_function
如何排大小的規則函式。若是排序內容是預設基本型態，此參數不輸入會由小排到大，其他需求都要指定此參數。

compare_function規定：bool [functino_name]([type] [left_name], [type] [right_name])

例如要排整數的話可以使用bool fn(int a, int b)
回傳值為false時會交換兩個數值再陣列中的位置

### int sort
將int型態的陣列[0]~[N-1]，從小排到大的範例
<script src="https://gist.github.com/Daviswww/4c8d1bde4175809c360af6d3d94ce31f.js"></script>

### double sort
將double型態的陣列[0]~[N-1]，從大排到小的範例
<script src="https://gist.github.com/Daviswww/f5d5d5ad8889dd901c0592c44cc85dd7.js"></script>

### struct sort
將P型態的陣列[0]~[49]，照xyz的順序從小排到大的範例
<script src="https://gist.github.com/Daviswww/7b7e077c9a039f41b133bcb5a3ae0d0e.js"></script>


將P型態的陣列[10]~[59]，照yzx的順序排序，y從大到小、z從小到大、x從大到小的範例
<script src="https://gist.github.com/Daviswww/be568787c971a111256929843cb0b5ff.js"></script>