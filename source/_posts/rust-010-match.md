---
title: Rust 010 Match
keywords: rust 010 match
date: 2020-11-12 20:26:47
categories: Rust tutorials
tags:
    - rust
---
# Rust 匹配

這語法就像一個選擇器一樣，根據值選擇內容，而你也可以設定很多個值甚至是一個範圍都可以。
<!-- more -->
```rust=
fn matchs(n: u32) {
    match n {
        1 => println!("1"),
        | 2 | 3 | 4 => println!("234"),
        5..=6 => println!("5~6"),
        _ => println!("GG"),
    }
}

fn main() {
    matchs(3);
}
```

match還可以用tuple來判斷裡面的值。

```rust=
fn match_tuple() {
    let tuple = (1, 1);

    match tuple {
        (0, x) => println!("(0, {})", x),
        (x, y) if x == y => println!("({}, {})", x, y),
        _ => println!("GG"),
    }
}

fn main() {
    match_tuple();
}
```

match可以允許我們綁定其他的變數，假設我設定n但是我想用k是可以的，只需要加一個@。

```rust=
fn match_v(n: u32) {
    match n {
        k @ 1 ..= 3 => println!("Value {}", k),
        k @ 4 ..= 6 => println!("Value {}", k),
        _ => println!("GG"),
    }
}

fn main() {
    match_v(4);
}
```