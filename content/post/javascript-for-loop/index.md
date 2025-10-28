---
title: "Vòng Lặp For Trong JavaScript"
description: "Tìm hiểu chi tiết về vòng lặp for và cách sử dụng trong JavaScript"
date: "2023-10-27"
tags: ["javascript", "programming", "loop", "for"]
categories: ["Programming"]
series: ["JavaScript Cơ Bản"]
---

## 1. Vòng lặp for trong JavaScript là gì?

Vòng lặp for là một cấu trúc điều khiển trong JavaScript cho phép thực hiện một đoạn code nhiều lần với một số lần lặp xác định. Nó là một trong những vòng lặp phổ biến nhất trong lập trình.

Cấu trúc cơ bản của vòng lặp for:

```javascript
for (khởi tạo; điều kiện; cập nhật) {
    // Khối lệnh được thực hiện
}
```

Trong đó:
- **Khởi tạo**: Thực hiện một lần khi bắt đầu vòng lặp
- **Điều kiện**: Kiểm tra trước mỗi lần lặp
- **Cập nhật**: Thực hiện sau mỗi lần lặp

## 2. Cách sử dụng vòng lặp for trong JavaScript

### Vòng lặp cơ bản

```javascript
// In ra các số từ 1 đến 5
for (let i = 1; i <= 5; i++) {
    console.log(i);
}
// Kết quả: 1, 2, 3, 4, 5
```

### Lặp qua mảng

```javascript
const fruits = ['Apple', 'Banana', 'Orange'];
for (let i = 0; i < fruits.length; i++) {
    console.log(fruits[i]);
}
// Kết quả: Apple, Banana, Orange
```

### Lặp với bước nhảy khác 1

```javascript
// In ra các số chẵn từ 0 đến 10
for (let i = 0; i <= 10; i += 2) {
    console.log(i);
}
// Kết quả: 0, 2, 4, 6, 8, 10
```

### Lặp ngược

```javascript
// Đếm ngược từ 5 về 1
for (let i = 5; i >= 1; i--) {
    console.log(i);
}
// Kết quả: 5, 4, 3, 2, 1
```

## 3. Vòng lặp for vô hạn trong JavaScript

Vòng lặp vô hạn xảy ra khi điều kiện dừng không bao giờ được thỏa mãn. Đây thường là một lỗi cần tránh trong lập trình.

```javascript
// KHÔNG NÊN: Vòng lặp vô hạn
for (let i = 1; i > 0; i++) {
    console.log(i); // Sẽ chạy mãi
}

// KHÔNG NÊN: Thiếu điều kiện dừng
for (let i = 1; ; i++) {
    console.log(i); // Sẽ chạy mãi
}
```

### Cách tránh vòng lặp vô hạn

```javascript
// Luôn đảm bảo có điều kiện dừng
for (let i = 1; i <= 1000000; i++) {
    console.log(i);
    if (someCondition) {
        break; // Thoát vòng lặp khi cần
    }
}
```

## 4. Vòng lặp for lồng nhau trong JavaScript

Vòng lặp for có thể được lồng vào nhau để xử lý các tác vụ phức tạp hơn.

### Ví dụ về ma trận

```javascript
// In ra ma trận 3x3
for (let i = 0; i < 3; i++) {
    for (let j = 0; j < 3; j++) {
        console.log(`Phần tử [${i}][${j}]`);
    }
}
```

### Tạo tam giác sao

```javascript
// In ra tam giác sao
for (let i = 1; i <= 5; i++) {
    let stars = '';
    for (let j = 1; j <= i; j++) {
        stars += '* ';
    }
    console.log(stars);
}
/*
Kết quả:
* 
* * 
* * * 
* * * * 
* * * * * 
*/
```

### Kiểm tra số nguyên tố

```javascript
// Tìm số nguyên tố từ 2 đến 20
for (let i = 2; i <= 20; i++) {
    let isPrime = true;
    for (let j = 2; j < i; j++) {
        if (i % j === 0) {
            isPrime = false;
            break;
        }
    }
    if (isPrime) {
        console.log(`${i} là số nguyên tố`);
    }
}
```

## Các mẹo khi sử dụng vòng lặp for

1. **Tối ưu hiệu năng**
```javascript
// Lưu length vào biến để tránh tính toán lại
const arr = [1, 2, 3, 4, 5];
const len = arr.length;
for (let i = 0; i < len; i++) {
    console.log(arr[i]);
}
```

2. **Sử dụng break và continue**
```javascript
// break: thoát khỏi vòng lặp
for (let i = 1; i <= 5; i++) {
    if (i === 3) break;
    console.log(i);
} // Kết quả: 1, 2

// continue: bỏ qua lần lặp hiện tại
for (let i = 1; i <= 5; i++) {
    if (i === 3) continue;
    console.log(i);
} // Kết quả: 1, 2, 4, 5
```

3. **Đặt tên cho vòng lặp**
```javascript
outerLoop: for (let i = 0; i < 3; i++) {
    for (let j = 0; j < 3; j++) {
        if (i === 1 && j === 1) {
            break outerLoop; // Thoát cả vòng lặp ngoài
        }
        console.log(`[${i}][${j}]`);
    }
}
```

## Tổng kết

Vòng lặp for là một công cụ mạnh mẽ trong JavaScript để:
- Thực hiện các tác vụ lặp lại
- Xử lý mảng và collections
- Tạo các mẫu và cấu trúc phức tạp
- Tối ưu hóa code với các điều kiện lặp xác định

Khi sử dụng vòng lặp for, cần:
1. Đảm bảo điều kiện dừng hợp lý
2. Tránh vòng lặp vô hạn
3. Tối ưu hiệu năng khi cần thiết
4. Sử dụng break và continue một cách hợp lý