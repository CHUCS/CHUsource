---
title: Rust 011 EOF input
keywords: rust-011-eof-input
date: 2020-12-31 14:48:20
categories: Rust tutorials
tags:
    - rust
---
# Rust EOF 輸入
如果你的輸入是要EOF的也就是用`ctrl+Z`結束輸入的話，我們可以使用rust的stdin來判斷它是不是0，那我們在這使用Option來回傳使否成功，如果輸入有值得話Some就會回傳輸入的值否則就是空的，那麼上面的while迴圈就會結束。

<!-- more -->
```rust=
fn main() {
    let mut vec1 = Vec::new();
    
    println!("Input");
    while let Some(input) = single_input() { 
        vec1.push(input);
    }
}

fn single_input() -> Option<i32> {
    let mut s = String::new();
    let input = std::io::stdin().read_line(&mut s).expect("err read");
    if input == 0 {
        return None;
    } else {
        return Some(s.trim().parse::<i32>().unwrap());
    }
}
```