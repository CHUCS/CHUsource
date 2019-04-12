---
title: Let's Watch Football
date: 2019-04-12 23:13:54
tags:
    - CHU Training
    - CodeForces
    - binary search 
    - 普通
---
Valeric and Valerko missed the last Euro football game, so they decided to watch the game's key moments on the Net. They want to start watching as soon as possible but the connection speed is too low. If they turn on the video right now, it will "hang up" as the size of data to watch per second will be more than the size of downloaded data per second.

The guys want to watch the whole video without any pauses, so they have to wait some integer number of seconds for a part of the video to download. After this number of seconds passes, they can start watching. Waiting for the whole video to download isn't necessary as the video can download after the guys started to watch.

Let's suppose that video's length is c seconds and Valeric and Valerko wait t seconds before the watching. Then for any moment of time t<sub>0</sub>, t ≤ t<sub>0</sub> ≤ c + t, the following condition must fulfill: the size of data received in t<sub>0</sub> seconds is not less than the size of data needed to watch t<sub>0</sub> - t seconds of the video.

Of course, the guys want to wait as little as possible, so your task is to find the minimum integer number of seconds to wait before turning the video on. The guys must watch the video without pauses.
<!-- more -->
#### Input:
The first line contains three space-separated integers a, b and c (1 ≤ a, b, c ≤ 1000, a > b). The first number (a) denotes the size of data needed to watch one second of the video. The second number (b) denotes the size of data Valeric and Valerko can download from the Net per second. The third number (c) denotes the video's length in seconds.

#### Output:
Print a single number — the minimum integer number of seconds that Valeric and Valerko must wait to watch football without pauses.

#### 範例:
input:
```
4 1 1
```
output:
```
3
```
input:
```
10 3 2
```
output:
```
5
```
input:
```
13 12 1
```
output:
```
1
```
#### Note:
In the first sample video's length is 1 second and it is necessary 4 units of data for watching 1 second of video, so guys should download 4 · 1 = 4 units of data to watch the whole video. The most optimal way is to wait 3 seconds till 3 units of data will be downloaded and then start watching. While guys will be watching video 1 second, one unit of data will be downloaded and Valerik and Valerko will have 4 units of data by the end of watching. Also every moment till the end of video guys will have more data then necessary for watching.

In the second sample guys need 2 · 10 = 20 units of data, so they have to wait 5 seconds and after that they will have 20 units before the second second ends. However, if guys wait 4 seconds, they will be able to watch first second of video without pauses, but they will download 18 units of data by the end of second second and it is less then necessary.

#### 題意:
現在想看網路影片，但是撥放需要的流量(每秒A)比下載需要的流量(每秒B)還大，但是他們可以先等t秒，然後再開始看總長C秒的影片，問你t最少是多少？

#### 思路:
要找的是當(A*C <= B* (C + t))的最小t，因此用二分搜尋找0~(A * C / B + 1)就好。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/0d3a4bd6acd4ec4bf08cf6f7bb206f7c.js"></script>

[題目網址](https://codeforces.com/problemset/problem/195/A)