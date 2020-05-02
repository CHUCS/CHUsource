---
title: Codeforces 230A Dragons
date: 2019-04-20 18:50:40
tags:
    - sortings
    - greedy
    - 簡單
---
[Codeforces 230A](https://codeforces.com/problemset/problem/230/A)
<!-- more -->
Kirito is stuck on a level of the MMORPG he is playing now. To move on in the game, he's got to defeat all n dragons that live on this level. Kirito and the dragons have strength, which is represented by an integer. In the duel between two opponents the duel's outcome is determined by their strength. Initially, Kirito's strength equals s.

If Kirito starts duelling with the i-th (1 ≤ i ≤ n) dragon and Kirito's strength is not greater than the dragon's strength x<sub>i</sub>, then Kirito loses the duel and dies. But if Kirito's strength is greater than the dragon's strength, then he defeats the dragon and gets a bonus strength increase by y<sub>i</sub>.

Kirito can fight the dragons in any order. Determine whether he can move on to the next level of the game, that is, defeat all dragons without a single loss.

#### Input:
The first line contains two space-separated integers s and n (1 ≤ s ≤ 10<sup>4</sup>, 1 ≤ n ≤ 10<sup>3</sup>). Then n lines follow: the i-th line contains space-separated integers xi and yi (1 ≤ x<sub>i</sub> ≤ 10<sup>4</sup>, 0 ≤ y<sub>i</sub> ≤ 10<sup>4</sup>) — the i-th dragon's strength and the bonus for defeating it.

#### Output:
On a single line print "YES" (without the quotes), if Kirito can move on to the next level and print "NO" (without the quotes), if he can't.

#### 範例:
input:
```
2 2
1 99
100 0
```
output:
```
YES
```
input:
```
10 1
100 100
```
output:
```
NO
```
#### Note:
In the first sample Kirito's strength initially equals 2. As the first dragon's strength is less than 2, Kirito can fight it and defeat it. After that he gets the bonus and his strength increases to 2 + 99 = 101. Now he can defeat the second dragon and move on to the next level.

In the second sample Kirito's strength is too small to defeat the only dragon and win.

#### 題意:
給你一開始的力量跟每頭龍的力量和打倒後增加的力量，當你的力量大於龍的力量時可以打倒他並增加力量，問你能不能打倒所有龍？

#### 思路:
從力量小的龍開始打，能打到最後就可以，否則不行。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/01d749d51e34af8688dac86000dff39e.js"></script>
