---
title: Rust 013 Enums
keywords: rust 013 enums
date: 2021-01-19 14:04:02
categories: Rust tutorials
tags:
    - rust
---

# Rust Enums
Rust中的枚舉與其他編譯語言（如C）相似，但有一些重要區別，使它們更強大。如果您來自函數式編程背景，Rust稱為枚舉的數通常被稱為代數數據類型。重要的細節是每個枚舉變量都可以具有數據。
<!-- more -->
```rust=
enum Direction {
    Up(Point),
    Down(Point),
    Left(Point),
    Right(Point),
}

struct Point{
    x: i32,
    y: i32,
}

fn main() {
    // input::single_input_string_I32();

    let u = Direction::Up(Point {x: 0, y: 1});

}
```

我們接著可以利用match來判斷，現在選的是哪個enum。而在下面這個程式是利用座標來判斷這個變數是屬於哪個enum的，然後再輸出對應的按鍵。而在destruct這個函式中可以看到`ref`，`ref`用來表示你要引用一個未打包的值。


```rust=
#![allow(dead_code)]
mod input;

#[derive(Debug)]
struct Point{
    x: i32,
    y: i32,
}

#[derive(Debug)]
enum Direction {
    Up(Point),
    Down(Point),
    Left(Point),
    Right(Point),
}

#[derive(Debug)]
enum Keys {
    UpKey(String),
    DownKey(String),
    LeftKey(String),
    RightKey(String),
}

impl Direction {
    fn match_direction(&self) -> Keys {
        match *self{
            Direction::Up(_) => Keys::UpKey(String::from("W")),
            Direction::Down(_) => Keys::DownKey(String::from("s")),
            Direction::Left(_) => Keys::LeftKey(String::from("a")),
            Direction::Right(_) => Keys::RightKey(String::from("d")),
        }
    }
}

impl Keys {
    fn destruct(&self) -> &String {
        match *self{
            Keys::UpKey(ref s) => s,
            Keys::DownKey(ref s) => s,
            Keys::LeftKey(ref s) => s,
            Keys::RightKey(ref s) => s,
        }
    }
}

fn main() {
    // input::single_input_string_I32();

    let u = Direction::Up(Point {x: 0, y: 1});
    let k = u.match_direction();

    println!("{:?}", k);
}
```