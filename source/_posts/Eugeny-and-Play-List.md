---
title: Codeforces 302B
date: 2019-04-12 23:18:15
link: Eugeny-and-Play-Lis
keywords: Codeforces 302B, Codeforces Eugeny and Play Lis
tags:
    - CHU Training
    - CodeForces
    - binary search 
    - 普通
---
# Codeforces 302B - Eugeny and Play List
[Eugeny and Play List](https://codeforces.com/problemset/problem/302/B)

Eugeny loves listening to music. He has n songs in his play list. We know that song number i has the duration of t<sub>i</sub> minutes. Eugeny listens to each song, perhaps more than once. He listens to song number i c<sub>i</sub> times. Eugeny's play list is organized as follows: first song number 1 plays c<sub>1</sub> times, then song number 2 plays c<sub>2</sub> times, ..., in the end the song number n plays cn times.
<!-- more -->
Eugeny took a piece of paper and wrote out m moments of time when he liked a song. Now for each such moment he wants to know the number of the song that played at that moment. The moment x means that Eugeny wants to know which song was playing during the x-th minute of his listening to the play list.

Help Eugeny and calculate the required numbers of songs.

#### Input:
The first line contains two integers n, m (1 ≤ n, m ≤ 10<sup>5</sup>). The next n lines contain pairs of integers. The i-th line contains integers c<sub>i</sub>, t<sub>i</sub> (1 ≤ c<sub>i</sub>, t<sub>i</sub> ≤ 10<sup>9</sup>) — the description of the play list. It is guaranteed that the play list's total duration doesn't exceed 10<sup>9</sup>.

The next line contains m positive integers v<sub>1</sub>, v<sub>2</sub>, ..., v<sub>m</sub>, that describe the moments Eugeny has written out. It is guaranteed that there isn't such moment of time v<sub>i</sub>, when the music doesn't play any longer. It is guaranteed that v<sub>i</sub> < v<sub>i</sub> + 1 (i < m).

The moment of time v<sub>i</sub> means that Eugeny wants to know which song was playing during the v<sub>i</sub>-th munite from the start of listening to the playlist.

#### Output:
Print m integers — the i-th number must equal the number of the song that was playing during the v<sub>i</sub>-th minute after Eugeny started listening to the play list.

#### 範例:
input:
```
1 2
2 8
1 16
```
output:
```
1
1
```
input:
```
4 9
1 2
2 1
1 1
2 2
1 2 3 4 5 6 7 8 9
```
output:
```
1
1
2
2
3
4
4
4
4
```

#### 題意:
現在有n首歌，每首歌會撥放ci次，每次ti分鐘長，當聽到喜歡的歌時會做下筆記。現在有m次做下筆記的時間，問你這m次分別是第幾首歌？

#### 思路:
先做出每首歌的累加長度陣列，再對每次的筆記在陣列中做二分搜尋即可。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/a131929a6eff93a0bb4e3e48f44ce349.js"></script>

