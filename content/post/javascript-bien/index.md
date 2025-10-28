---
title: "Biến và Khai Báo Biến trong JavaScript"
description: "Tìm hiểu chi tiết về cách khai báo và sử dụng biến trong JavaScript"
date: "2023-10-27"
tags: ["javascript", "programming", "variables"]
categories: ["Programming"]
series: ["JavaScript Cơ Bản"]
---

## 1. Các cách khai báo biến trong JavaScript

Trong JavaScript, có ba cách để khai báo biến: `var`, `let`, và `const`. Mỗi cách có những đặc điểm và trường hợp sử dụng riêng.

### Khai báo biến trong JS bằng từ khóa var

```javascript
var name = "John";
var age = 25;
var isStudent = true;

// Có thể khai báo lại
var name = "Jane"; // Hợp lệ

// Có phạm vi function scope
function test() {
    var x = 10;
    console.log(x); // 10
}
console.log(x); // ReferenceError: x is not defined
```

### Khai báo biến trong JS bằng từ khóa let

```javascript
let count = 0;
let message = "Hello";

// Không thể khai báo lại
let count = 1; // SyntaxError

// Có phạm vi block scope
if (true) {
    let y = 20;
    console.log(y); // 20
}
console.log(y); // ReferenceError: y is not defined
```

### Khai báo biến trong JS bằng từ khóa const

```javascript
const PI = 3.14159;
const API_URL = "https://api.example.com";

// Không thể thay đổi giá trị
PI = 3.14; // TypeError: Assignment to constant variable

// Nhưng có thể thay đổi nội dung object/array
const user = { name: "John" };
user.name = "Jane"; // Hợp lệ
```

## 2. Cách đặt tên cho biến trong JavaScript

Quy tắc đặt tên biến trong JavaScript:

1. **Bắt đầu bằng chữ cái, dấu gạch dưới hoặc dấu $**
```javascript
let firstName = "John";
let _privateVar = "secret";
let $price = 99.99;
```

2. **Phân biệt chữ hoa chữ thường**
```javascript
let color = "red";
let Color = "blue";
// color và Color là hai biến khác nhau
```

3. **Không được dùng từ khóa**
```javascript
// Không hợp lệ
let class = "Math"; // SyntaxError
let function = "test"; // SyntaxError
```

## 3. Cách gán giá trị cho biến trong JavaScript

```javascript
// Gán giá trị khi khai báo
let name = "John";

// Gán giá trị sau khi khai báo
let age;
age = 25;

// Gán nhiều biến cùng lúc
let x = 1, y = 2, z = 3;

// Gán cùng giá trị cho nhiều biến
let a = b = c = 0;
```

## 4. Kiểu giá trị của biến trong JavaScript

JavaScript có các kiểu dữ liệu cơ bản:

```javascript
// Number
let age = 25;
let price = 99.99;

// String
let name = "John";
let message = 'Hello';

// Boolean
let isStudent = true;
let isWorking = false;

// Undefined
let undefinedVar;

// Null
let nullVar = null;

// Object
let person = {
    name: "John",
    age: 25
};

// Array
let colors = ["red", "green", "blue"];
```

## 5. In giá trị của biến JS ra trình duyệt

```javascript
// Sử dụng console.log()
let name = "John";
console.log(name); // John

// Sử dụng document.write()
document.write("<h1>" + name + "</h1>");

// Sử dụng alert()
alert(name);

// Sử dụng innerHTML
document.getElementById("demo").innerHTML = name;
```

## 6. Các phép toán thường dùng trên biến trong JavaScript

### Phép toán số học

```javascript
let a = 10;
let b = 5;

// Cộng
let sum = a + b; // 15

// Trừ
let difference = a - b; // 5

// Nhân
let product = a * b; // 50

// Chia
let quotient = a / b; // 2

// Chia lấy dư
let remainder = a % b; // 0

// Tăng/giảm
a++; // a = 11
b--; // b = 4
```

### Phép toán chuỗi

```javascript
let firstName = "John";
let lastName = "Doe";

// Nối chuỗi
let fullName = firstName + " " + lastName; // John Doe

// Template literals (ES6)
let greeting = `Hello, ${firstName}!`; // Hello, John!
```

### Phép toán gán kết hợp

```javascript
let x = 5;

x += 3; // x = 8 (x = x + 3)
x -= 2; // x = 6 (x = x - 2)
x *= 4; // x = 24 (x = x * 4)
x /= 3; // x = 8 (x = x / 3)
x %= 5; // x = 3 (x = x % 5)
```

### Phép toán so sánh

```javascript
let a = 5;
let b = "5";

// So sánh giá trị
console.log(a == b); // true

// So sánh giá trị và kiểu dữ liệu
console.log(a === b); // false

// So sánh lớn hơn/nhỏ hơn
console.log(a > 3); // true
console.log(a <= 5); // true
```

## Tổng kết

Biến trong JavaScript là một khái niệm cơ bản nhưng rất quan trọng. Việc hiểu rõ các cách khai báo biến và các quy tắc sử dụng sẽ giúp bạn:
- Viết code chất lượng hơn
- Tránh được các lỗi phổ biến
- Tối ưu hiệu suất ứng dụng

Khi làm việc với biến, hãy nhớ:
1. Chọn cách khai báo phù hợp (`var`, `let`, `const`)
2. Đặt tên biến có ý nghĩa
3. Hiểu rõ scope và hoisting
4. Sử dụng đúng kiểu dữ liệu