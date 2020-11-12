---
title: Rust 009 Loop
keywords: rust 009 loop
date: 2020-11-12 20:26:28
categories: Rust tutorials
tags:
    - rust
---
# Rust 迴圈
迴圈的好處就是可以替我們重複做一些固定得事情，使程式更加簡潔與方便。
<!-- more -->
## #loop
迴圈可以重複做同樣的事情，如下面範例我就重複印出`Hello rust!`，再利用剛剛所學的`if`來判斷`i`有沒有大於等於`n`，而`break`這個指令是用來結束這個回圈用的，也就是說跳出這一層迴圈。
```rust=
fn loops(n: u32) {
    let mut i = 0;
    loop {
        println!("Hello rust!");
        i += 1;
        if i >= n {
            break;
        }
    }
}

fn main() {
    loops(3);
}
```

## #while loop
在while中可以加入判斷，如下面範例就是判斷`i<n`，所以如果當i大於n時就會結束迴圈。

```rust=
fn while_loop(n: u32) {
    let mut i = 0;
    while i < n {
        println!("Hello rust {}", i);
        i += 1;
    }
}

fn main() {
    while_loop(5);
}
```

## #for loop
for迴圈是一個比較特別的迴圈，看下面範例來說的話，i是a給他的值，就像是第一次拿到10，第二次拿到20以此類推遞增。

```rust=
fn for_loop_vec() {
    let a = vec![10, 20, 30];

    for i in a {
        println!("{}", i);
    }
}

fn main() {
    for_loop_vec();
}
```

當然你也可以設定範圍給他，而`..`就是小於的意思，`..=`則是小於等於。
```rust=
fn for_loop_var(n: u32) {
    for i in 1..n {
        println!("A {}", i);
    }

    for i in 1..=n {
        println!("B {}", i);
    }
}

fn main() {
    for_loop_var(5);
}
```