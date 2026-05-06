# Phần A — Kiểm tra đọc hiểu
## Câu A1 — 3 cách nhúng CSS
### 1. Inline CSS (CSS nội dòng)
- Viết trực tiếp CSS vào thuộc tính `style` của thẻ HTML  
**Ví dụ:**
```html
<h1 style="color: blue; font-size: 20px;">Chào mừng bạn!</h1>
````
**Ưu điểm:**
* Nhanh, tiện khi test hoặc chỉnh sửa 1 phần tử
**Nhược điểm:**
* Code rối, khó bảo trì
* Không tái sử dụng được
**Khi dùng:**
* Sửa nhanh một element
* Email (ưu tiên inline CSS)

---
### 2. Internal CSS (CSS nội bộ)
* Viết trong thẻ `<style>` (trong `<head>`)

```html
<head>
  <style>
    p {
      color: red;
      line-height: 1.5;
    }
  </style>
</head>
```
**Ưu điểm:**
* Quản lý style của một trang tại một nơi
**Nhược điểm:**
* Không tái sử dụng được
**Khi dùng:**
* Trang đơn (landing page)
---
### 3. External CSS (CSS bên ngoài)

* Tách ra file `.css`

```css
body {
  background-color: #f0f0f0;
}
```
```html
<link rel="stylesheet" href="style.css">
```
**Ưu điểm:**
* Code sạch, dễ bảo trì
* Tái sử dụng
**Nhược điểm:**
* Phải tải thêm file
---
### 4. Thứ tự ưu tiên
```
Inline > Internal ≈ External
```
* Inline cao nhất
* Nếu trùng → rule viết sau thắng
---
## Câu A2 — CSS Selectors
1. `h1` → ShopTLU
2. `.price` → 25.990.000đ, 45.990.000đ
3. `#app header` → toàn bộ `<header>`
4. `nav a:first-child` → Home
5. `.product.featured h2` → MacBook Pro
6. `article > p` → giá + mô tả
7. `a[href="/"]` → Home
8. `.top-bar.dark h1` → ShopTLU
---
## Câu A3 — Box Model
### Trường hợp 1: content-box
```css
.box-1 {
  width: 400px;
  padding: 20px;
  border: 5px;
  margin: 10px;
}
```
* Width = 400 + 40 + 10 = **450px**
* Tổng = 450 + 20 = **470px**

---
### Trường hợp 2: border-box
```css
.box-2 {
  box-sizing: border-box;
  width: 400px;
  padding: 20px;
  border: 5px;
  margin: 10px;
}
```
* Width = **400px**
* Content = **350px**
* Tổng = **420px**

---
### Trường hợp 3: Margin collapse
```css
.box-a { margin-bottom: 25px; }
.box-b { margin-top: 40px; }
```
* Khoảng cách = **40px**
## Câu A4 — Specificity
* `p` → 0-0-1
* `.price` → 0-1-0
* `#main-price` → 1-0-0
* `p.price` → 0-1-1
👉 Kết quả: **Đỏ**
* Có inline:
```html
<p style="color: orange;">
```
→ **Cam**
* Có `!important`
  → Rule đó thắng