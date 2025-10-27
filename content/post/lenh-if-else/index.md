---
title: "Lệnh if else trong Javascript"
description: "Tìm hiểu cách sử dụng lệnh if, if else, kết hợp nhiều điều kiện và lồng nhau trong Javascript."
date: "2025-10-28"
tags: ["javascript", "if else", "lập trình"]
categories: ["Programming"]
---

# Lệnh if else trong Javascript

**Lệnh `if else` là một trong những cấu trúc điều kiện cơ bản nhất trong Javascript, giúp chương trình rẽ nhánh theo các điều kiện khác nhau.**

# 1. Lệnh if trong Javascript

```javascript
if (condition) {
  // Thực thi nếu điều kiện đúng
}

**Ví dụ: Kiểm tra a và b**
var a = 12;
var b = 12;

if (a == b) {
  alert('a và b bằng nhau');
}
//Nếu chỉ có một lệnh bên trong if, bạn có thể viết gọn:
if (a == b) alert('a và b bằng nhau');
```

## 2. Lệnh if else trong Javascript

```javascript
if (condition) {
  // Nếu đúng
} else {
  // Nếu sai
}
**Vi dụ:**
var a = 12;
var b = 10;

if (a == b) {
  alert('a và b bằng nhau');
} else {
  alert('a và b khác nhau');
}
```

### 3. Kết hợp nhiều lệnh if else trong Javascript

```javascript
if (condition1) {
  // Nếu condition1 đúng
} else if (condition2) {
  // Nếu condition2 đúng
} else {
  // Nếu không điều kiện nào đúng
}
**Ví dụ:**
var a = 12;

if (a > 12) {
  alert('a > 12');
} else if (a < 12) {
  alert('a < 12');
} else {
  alert('a = 12');
}
**Hoặc dùng hai khối if riêng biệt:**
var a = 12;

if (a > 12) {
  alert('a > 12');
}

if (a < 12) {
  alert('a < 12');
} else {
  alert('a = 12');
}
```

#### 4. Lệnh if else lồng nhau trong Javascript
Có thể lồng các khối if bên trong nhau:
```javascript
var a = 13;

if (a > 12) {
  var b = 20;

  if (a == b) {
    alert('a = b');
  } else {
    alert('a != b');
  }
}
```