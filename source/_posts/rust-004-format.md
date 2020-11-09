---
title: Rust 004 Format
keywords: rust-004-format
date: 2020-11-09 20:50:45
categories: Rust tutorials
tags:
---
# Rust 格式化輸出

格式化輸出可以讓你方便的排版你想要的輸出方式，以下我們介紹幾中常見的格式化輸出。  

利用大括弧來標示變數所在的地方，由左而右依序輸出。
```rust=
println!("Num: {}, {}", 1, 2);
```
<!-- more -->
在大括弧內設下index，以照後面資料的順序索取你需要的資料。
```rust=
println!("{0} is {0} and {1} haha {2}.", "Bob", "Alice", "John");
```

在大括弧內設下變數，在後面以變數給予值。
```rust=
println!("{a} is {b} and {c} haha {a}.", b = "Bob", a = "Alice", c = "John");
```

依照型態命名，輸出則會以我們所設的型態輸出。
```rust=
println!("Binary: {:b}, Hex: {:x}, Octal: {:o}.", 10, 10, 10);
```

輸出結果
![](HgVZM4p.png)