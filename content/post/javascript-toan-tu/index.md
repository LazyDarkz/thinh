---
title: "Các Toán Tử Trong JavaScript"
description: "Tìm hiểu chi tiết về các loại toán tử và cách sử dụng trong JavaScript"
date: "2023-10-27"
tags: ["javascript", "programming", "operators"]
categories: ["Programming"]
series: ["JavaScript Cơ Bản"]
image: "/img/featured/featured-image.webp"
---

## 1. Toán tử toán học trong JavaScript

JavaScript hỗ trợ các toán tử toán học cơ bản để thực hiện các phép tính số học.

```javascript
// Phép cộng (+)
let sum = 5 + 3;      // 8

// Phép trừ (-)
let diff = 10 - 4;    // 6

// Phép nhân (*)
let product = 6 * 3;  // 18

// Phép chia (/)
let quotient = 15 / 3;// 5

// Phép chia lấy dư (%)
let remainder = 17 % 5;// 2

// Phép tăng (++)
let x = 5;
x++;                  // x = 6

// Phép giảm (--)
let y = 8;
y--;                  // y = 7

// Phép lũy thừa (**)
let power = 2 ** 3;   // 8
```

## 2. Toán tử gán trong JavaScript

Toán tử gán được sử dụng để gán giá trị cho biến.

```javascript
// Gán đơn giản (=)
let x = 5;

// Cộng và gán (+=)
x += 3;      // x = x + 3

// Trừ và gán (-=)
x -= 2;      // x = x - 2

// Nhân và gán (*=)
x *= 4;      // x = x * 4

// Chia và gán (/=)
x /= 2;      // x = x / 2

// Chia lấy dư và gán (%=)
x %= 3;      // x = x % 3

// Lũy thừa và gán (**=)
x **= 2;     // x = x ** 2
```

## 3. Toán tử quan hệ trong JavaScript

Toán tử quan hệ dùng để so sánh giá trị và trả về kết quả boolean.

```javascript
let a = 5;
let b = 10;

// So sánh bằng (==)
console.log(a == 5);    // true
console.log(a == "5");  // true (chỉ so sánh giá trị)

// So sánh bằng nghiêm ngặt (===)
console.log(a === 5);   // true
console.log(a === "5"); // false (so sánh cả giá trị và kiểu dữ liệu)

// So sánh khác (!=)
console.log(a != b);    // true

// So sánh khác nghiêm ngặt (!==)
console.log(a !== "5"); // true

// Lớn hơn (>)
console.log(b > a);     // true

// Nhỏ hơn (<)
console.log(a < b);     // true

// Lớn hơn hoặc bằng (>=)
console.log(a >= 5);    // true

// Nhỏ hơn hoặc bằng (<=)
console.log(b <= 10);   // true
```

## 4. Toán tử luận lý trong JavaScript

Toán tử luận lý dùng để kết hợp các điều kiện.

```javascript
let x = 5;
let y = 10;

// Toán tử AND (&&)
console.log(x > 0 && y < 20);   // true
// Cả hai điều kiện đều phải đúng

// Toán tử OR (||)
console.log(x < 0 || y > 5);    // true
// Chỉ cần một điều kiện đúng

// Toán tử NOT (!)
console.log(!(x > y));          // true
// Đảo ngược giá trị boolean

// Kết hợp các toán tử
console.log((x > 0 && y < 20) || x === 5); // true
```

## 5. Độ ưu tiên các toán tử trong JavaScript

Độ ưu tiên của các toán tử quyết định thứ tự thực hiện các phép tính.

```javascript
// Thứ tự từ cao đến thấp:
// 1. ()         - Dấu ngoặc
// 2. ++ --      - Tăng giảm
// 3. ** !       - Lũy thừa và phủ định
// 4. * / %      - Nhân, chia, chia lấy dư
// 5. + -        - Cộng trừ
// 6. < <= > >=  - So sánh
// 7. == === != !== - So sánh bằng
// 8. &&         - AND logic
// 9. ||         - OR logic
// 10. =         - Gán

let result = 2 + 3 * 4;    // 14 (không phải 20)
let result2 = (2 + 3) * 4; // 20
```

## 6. Lưu ý với toán tử so sánh bằng JavaScript

Khi sử dụng toán tử so sánh trong JavaScript, cần chú ý một số điểm đặc biệt:

### So sánh == vs ===

```javascript
// == (So sánh lỏng lẻo)
console.log(5 == "5");     // true
console.log(1 == true);    // true
console.log(null == undefined); // true

// === (So sánh nghiêm ngặt)
console.log(5 === "5");    // false
console.log(1 === true);   // false
console.log(null === undefined); // false
```

### So sánh với NaN

```javascript
console.log(NaN == NaN);   // false
console.log(NaN === NaN);  // false
// Sử dụng isNaN() để kiểm tra NaN
console.log(isNaN(NaN));   // true
```

### So sánh chuỗi

```javascript
// So sánh theo bảng mã ASCII
console.log("a" < "b");    // true
console.log("abc" < "abd"); // true
console.log("2" > "12");   // true (so sánh từng ký tự)
```

### Các trường hợp đặc biệt

```javascript
// So sánh với null và undefined
console.log(null == undefined);  // true
console.log(null === undefined); // false

// So sánh với 0
console.log(false == 0);   // true
console.log(false === 0);  // false

// So sánh chuỗi rỗng
console.log("" == false);  // true
console.log("" === false); // false
```

## Thực hành và lưu ý

1. Luôn sử dụng === thay vì == khi có thể để tránh các kết quả không mong muốn
2. Cẩn thận với phép so sánh chuỗi và số
3. Sử dụng dấu ngoặc để làm rõ thứ tự thực hiện các phép tính
4. Kiểm tra kiểu dữ liệu trước khi thực hiện các phép toán

```javascript
// Ví dụ về lỗi thường gặp
let num = "5";
let sum = num + 3;    // "53" thay vì 8
let sum2 = +num + 3;  // 8 (chuyển chuỗi thành số)
```