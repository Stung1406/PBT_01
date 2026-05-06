Phần A — Kiểm tra đọc hiểu

Câu A1 (5đ) — 3 cách nhúng CSS
    1. Inline CSS (CSS nội dòng)
    Là cách viết trực tiếp CSS vào thuộc tính style của thẻ HTML
    Ví dụ:
    <h1 style="color: blue; font-size: 20px;">Chào mừng bạn!</h1>
    Ưu điểm:
    Nhanh, tiện khi test hoặc chỉnh sửa 1 phần tử
    Nhược điểm:
    Code rối, khó bảo trì
    Không tái sử dụng được
    Khi dùng:
    Sửa nhanh một element
    Email (ưu tiên inline CSS)
    2. Internal CSS (CSS nội bộ)
    Viết CSS trong thẻ <style> (thường trong <head>)
    Ví dụ:
    <head>
    <style>
        p {
        color: red;
        line-height: 1.5;
        }
    </style>
    </head>
    Ưu điểm:
    Quản lý style của một trang tại một nơi
    Nhược điểm:
    Chỉ áp dụng cho một trang
    Khó tái sử dụng
    Khi dùng:
    Trang đơn (landing page)
    Style riêng cho một trang
    3. External CSS (CSS bên ngoài)
    Viết CSS trong file .css riêng và liên kết với HTML
    Ví dụ:
    File style.css:
    body {
    background-color: #f0f0f0;
    }
    .content {
    margin: 20px;
    }
    File index.html:
    <head>
    <link rel="stylesheet" href="style.css">
    </head>
    Ưu điểm:
    Code sạch, dễ bảo trì
    Tái sử dụng cho nhiều trang
    Nhược điểm:
    Phải tải thêm file CSS
    Khi dùng:
    Website nhiều trang
    Dùng chung style
    4. Thứ tự ưu tiên (Specificity)
    Inline > Internal ≈ External
    Giải thích:
    Inline cao nhất vì áp dụng trực tiếp lên phần tử
    Internal và External có cùng mức ưu tiên
    Nếu xung đột → rule khai báo sau sẽ được áp dụng

Câu A2 (8đ) — CSS Selectors
    h1 → ShopTLU
    .price → 25.990.000đ, 45.990.000đ
    #app header → toàn bộ nội dung trong <header>
    nav a:first-child → Home
    .product.featured h2 → MacBook Pro
    article > p → giá và mô tả của từng sản phẩm
    a[href="/"] → Home
    .top-bar.dark h1 → ShopTLU

Câu A3 (7đ) — Box Model
    Trường hợp 1: content-box (mặc định)
    .box-1 {
    width: 400px;
    padding: 20px;
    border: 5px solid black;
    margin: 10px;
    }
    Chiều rộng hiển thị = 400 + (20×2) + (5×2) = 450px
    Không gian chiếm = 450 + (10×2) = 470px
    Trường hợp 2: border-box
    .box-2 {
    box-sizing: border-box;
    width: 400px;
    padding: 20px;
    border: 5px solid black;
    margin: 10px;
    }
    Chiều rộng hiển thị = 400px
    Content thực = 400 - (20×2) - (5×2) = 350px
    Không gian chiếm = 400 + (10×2) = 420px
    Trường hợp 3: Margin collapse
    .box-a { margin-bottom: 25px; }
    .box-b { margin-top: 40px; }
    Khoảng cách thực = 40px
    Giải thích:
    Margin dương → lấy giá trị lớn hơn
    Không cộng dồn
    Nâng cao (có margin âm):
    40 + (-10) = 30px
    Câu A4 (5đ) — Specificity
    1. Độ ưu tiên
    p → 0-0-1
    .price → 0-1-0
    #main-price → 1-0-0
    p.price → 0-1-1
    2. Màu áp dụng
    → Đỏ (ID có độ ưu tiên cao nhất)
    3. Có inline style
    <p class="price" id="main-price" style="color: orange;">
    → Cam
    4. Có !important
    → Đỏ
    Giải thích:
    !important ghi đè tất cả các rule khác
    Kể cả ID