---
title: Rust-006 Types
keywords: rust-006-types
date: 2020-11-09 20:53:39
categories: Rust tutorials
tags:
---
# Rust 型態
#### Integer Types
整數是沒有小數部分的數字。以下是在RUST中整數型態的表示方法。
<!-- more -->
| Length  | Signed | Unsigned |
| ------- | ------ | -------- |
| 8-bit   | i8     | u8       |
| 16-bit  | i16    | u16      |
| 32-bit  | i32    | u32      |
| 64-bit  | i64    | u64      |
| 128-bit | i128   | u128     |


```rust=
let a: i8 = 1;

let b: i16 = 2;

let c: i32 = 3;
```

#### Floating-Point Types
Rust對於浮點數也有兩種原始類型`f32`和`f64`。

```rust=
let x = 5.0; // f64

let y: f32 = 3.0; // f32
```

#### The Boolean Type
在布林函數中只有對和錯。
```rust=
let x = true;

let y: bool = false;
```

#### The Character Type
字元型態中可儲存一個字，如果一個以上就會變成字串。
```rust=
let a = 'A';

let b = 'B';
```

#### The Array Type
利用陣列儲存多筆資料，取用時只需要輸入對應的`index`就可以了。
```rust=
let a = [1, 2, 3, 4, 5];

let first = a[0];
let second = a[1];
```