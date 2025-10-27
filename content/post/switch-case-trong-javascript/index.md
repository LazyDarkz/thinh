---
title: "Lệnh switch case trong Javascript"
description: "Tìm hiểu cú pháp và cách sử dụng lệnh switch case trong Javascript qua các ví dụ thực tế."
date: 2025-10-27
tags: ["javascript", "switch case", "lập trình"]
categories: ["Programming"]
---

# Lệnh switch case trong Javascript

Lệnh `switch case` là một cách khác để xử lý rẽ nhánh trong chương trình, tương tự như `if else`. Tuy nhiên, nó hoạt động dựa trên so sánh bằng và thường được dùng khi có nhiều trường hợp cụ thể cần xử lý.

## Ví dụ lệnh switch case trong Javascript

Dưới đây là ví dụ kiểm tra số chẵn/lẻ bằng `switch`:

```javascript
var number = parseInt(prompt("Nhập số cần kiểm tra"));
var mod = number % 2;

switch (mod) {
  case 0:
    document.write(number + " là số chẵn");
    break;
  case 1:
    document.write(number + " là số lẻ");
    break;
  default:
    document.write("Giá trị nhập không hợp lệ");
}
```

Trường hợp không có default

Trường hợp này nếu bạn nhập một màu khác với màu đỏ (red) và vàng (yellow) thì sẽ không có thông báo gì.
```javascript
//Nếu không có default, khi không có case nào khớp thì chương trình sẽ không thực hiện gì cả.
    switch (color) {
  case 'red':
    document.write("Màu đỏ");
    break;
  case 'yellow':
    document.write("Màu vàng");
    break;
}
```

Trường hợp không có break

Trường hợp này nếu bạn nhập vào màu đỏ (red) thì chương trình sẽ in ra cả lệnh ở case màu vàng (yellow) phía dưới, lý do là trong case màu đỏ ta không sử dụng lệnh break để thoát khỏi lệnh switch nên nó sẽ chạy thẳng xuống case phía dưới luôn mà không cần kiểm tra điều kiện.

```javascript
//Nếu thiếu break, chương trình sẽ tiếp tục thực hiện các case phía sau:
switch (color) {
  case 'red':
    document.write("Màu đỏ");
  case 'yellow':
    document.write("Màu vàng");
    break;
}
```

Trường hợp gom nhóm case

Nếu bạn để ý kỹ hơn thì thì thấy rằng nếu người dùng nhập vào màu đỏ (red), vàng (yellow) và xanh (blue) thì đều có thông báo nhập đúng. Vậy tai sao mình không gom ba trường hợp đó thành một thôi.

```javascript
//Bạn có thể gom nhiều case lại để xử lý chung:
switch (color) {
  case 'red':
  case 'yellow':
  case 'blue':
    document.write("Bạn nhập màu " + color + ", đúng rồi đó");
    break;
  default:
    document.write("Màu không có trong hệ thống");
}
```