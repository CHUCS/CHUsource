---
title: UVA 11636
date: 2019-11-17 10:09:51
link: Hello-World
keywords: UVA 11636, UVA Hello World
tags:
- implementation
---
# UVA 11636 - Hello World
[Hello World](https://onlinejudge.org/external/116/11636.pdf)


#### 題意:
有個人他很懶，他懶得打這麼多個Hello World所以他只用複製的，假如他要印7個Hello World!，他要複製3次，因為第一次他複製他打好的一個Hello World，變2個，然後再複製便4個，然後再複製3個變7個。
<!-- more -->
#### 思路:
我們可以先建出一個答案表提供我們查詢以免超時，i是他需要印的數量，而每次複製我都檢查複製出來的最大值有沒有小於等於複製出來的數量，像是上面範例5、6、7、8都只需要複製3次，因為複製到三次的時候最大值複製數是8個，以此類推往下建表把所有答案都列出。

#### 程式碼:
<script src="https://gist.github.com/Daviswww/c9a27cb1bb5ca17fe0914ef6dcc0cfd4.js"></script>