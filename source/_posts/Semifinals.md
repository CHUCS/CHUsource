---
title: Semifinals
date: 2019-04-27 18:41:46
tags:
    - 普通
    - sortings
    - implementation
---
Two semifinals have just been in the running tournament. Each semifinal had n participants. There are n participants advancing to the finals, they are chosen as follows: from each semifinal, we choose k people (0 ≤ 2k ≤ n) who showed the best result in their semifinals and all other places in the finals go to the people who haven't ranked in the top k in their semifinal but got to the n - 2k of the best among the others.

The tournament organizers hasn't yet determined the k value, so the participants want to know who else has any chance to get to the finals and who can go home.
<!-- more -->
#### Input:
The first line contains a single integer n (1 ≤ n ≤ 10<sup>5</sup>) — the number of participants in each semifinal.

Each of the next n lines contains two integers a<sub>i</sub> and b<sub>i</sub> (1 ≤ a<sub>i</sub>, b<sub>i</sub> ≤ 10<sup>9</sup>) — the results of the i-th participant (the number of milliseconds he needs to cover the semifinals distance) of the first and second semifinals, correspondingly. All results are distinct. Sequences a<sub>1</sub>, a<sub>2</sub>, ..., a<sub>n</sub> and b<sub>1</sub>, b<sub>2</sub>, ..., b<sub>n</sub> are sorted in ascending order, i.e. in the order the participants finished in the corresponding semifinal.

#### Output:
Print two strings consisting of n characters, each equals either "0" or "1". The first line should correspond to the participants of the first semifinal, the second line should correspond to the participants of the second semifinal. The i-th character in the j-th line should equal "1" if the i-th participant of the j-th semifinal has any chances to advance to the finals, otherwise it should equal a "0".

#### 範例:
input:
```
4
9840 9920
9860 9980
9930 10020
10040 10090
```
output:
```
1110
1100
```
input:
```
4
9900 9850
9940 9930
10000 10020
10060 10110
```
output:
```
1100
1100
```

#### Note:
Consider the first sample. Each semifinal has 4 participants. The results of the first semifinal are 9840, 9860, 9930, 10040. The results of the second semifinal are 9920, 9980, 10020, 10090.

>>● If k = 0, the finalists are determined by the time only, so players 9840, 9860, 9920 and 9930 advance to the finals.
>>● If k = 1, the winners from both semifinals move to the finals (with results 9840 and 9920), and the other places are determined by the time (these places go to the sportsmen who run the distance in 9860 and 9930 milliseconds).
>>●If k = 2, then first and second places advance from each seminfial, these are participants with results 9840, 9860, 9920 and 9980 milliseconds. 

#### 題意:
給你兩次比賽的成績，兩邊可以各錄取K名進入決賽(0≤2K≤N)，剩下的名次用成績決定(不會有一樣的成績)，現在K未定，問你那些人是有機會進入決賽的？

#### 思路:
兩邊的前N/2名都有可能，剩下的名次則是到總成績的第N名有可能，將兩種綜合即可。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/aa4d5499ee399a951c3844b6cd5db293.js"></script>
[題目網址](https://codeforces.com/problemset/problem/378/B)