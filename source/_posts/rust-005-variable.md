---
title: Rust 005 Variable
keywords: rust-005-variable
date: 2020-11-09 20:52:30
categories: Rust tutorials
tags:
---
# Rust 變量

在變量中我們可以給予一些固定的值在變數中，而這些值不允許被任意更改。
```rust=
let name = "Bob";
println!("My name is {}.", name);
```
<!-- more -->
```rust=
const ID: i32 = 001;
println!("My ID is {}.", ID);
```

分配多個變量的值。
```rust=
let ( a, b ) = ("Alice", 23);
println!("{} is {}.", a, b);
```

輸出結果
![](gZqndHG.png)