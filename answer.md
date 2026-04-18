Câu A1: 
    5 bước xảy ra khi gõ https://shopee.vn
    Bước 1: yêu cầu sẽ xuất phát từ lap top -> đi qua router Wifi của bạn
    Bước 2: Qua nhà mạng VNPT qua cáp mạng kết nối chạy xuyên cáp dưới đáy THái Bình Dương đến data center của Shoppe tại Sea Group tại Singapore 
    Bước 3: Sever xử lý :"Bạn muốn xem Product Feed"
    Bước 4: Response chạy ngược lại : cáp quang->VNPT->router->laptop
    Bước 5: Chorme nhận HTML,CSS,JS->render giao diện -> Bạn thấy Product Feed

Câu A2:
- Do Google sẽ khó hiểu nội dung div giống như một chiếc hộp và nếu ta gõ <div = header> thì google sẽ phải đoán xem đây có phải là header không

<div class="header"> //Lỗi 1 : không dùng header
    <div class="logo">ShopTLU</div> 
    <div class="menu"> //Lỗi 2 : Sử dụng menu thay vì <nav>
        <div><a href="/">Trang chủ</a></div>  //nên bỏ div vì sẽ làm ch code rồi thêm
        <div><a href="/products">Sản phẩm</a></div>
    </div>
</div>
<div class="main"> Lỗi 3 Không sử dụng <main>
    <div class="product"> //Có thể sử dụng<article chứa nội dung độc lập >
        <div class="title">iPhone 16 Pro</div> // nên sử dụng h2 để làm tiêu đề phụ cho main 
        <div class="price">25.990.000đ</div> // sử dụng <p> để chứa trên 1 đoạn văn
        <div class="image"><img src="iphone.jpg"></div>
        // nên dùng <imagie> để chứa ảnh 
    </div>
</div>
<div class="footer">© 2026 ShopTLU</div> Lỗi 4 : Sử dụng footer 

-Sửa:
<header>
    <div class="logo">ShopTLU</div>

    <nav>
        <a href="/">Trang chủ</a>
        <a href="/products">Sản phẩm</a>
    </nav>
</header>

<main>
    <article class="product">
        <h2>iPhone 16 Pro</h2>
        <p class="price">25.990.000đ</p>
        <img src="iphone.jpg" alt="iPhone 16 Pro">
    </article>
</main>

<footer>
    <p>&copy; 2026 ShopTLU</p>
</footer>


Câu A3
Text art
    Hộp 1
    Text A Text B
    Hộp 2
    Text C Text D
    Hộp 3
    Do thẻ <div> sẽ chiếm cả dòng do div sẽ chứa cả nội dung còn <span> theo em hiểu đơn giản chỉ là nội dung của một dòng đó thôi nghĩa là ta chỉ viết vào một phần nội dung và sau đó ta có thể viết tiếp vào hoặc xuống dòng viết nội dung mới 

Câu A4:
<thead> là phần đầu của bảng theo em hiểu đơn giản là hàng đầu tiên của bảng có thể chứa các tiêu đề hay thậm chí là tên của các cột trong bảng
<tbody> là phần thân của bảng tức là các hàng dưới <thead> sẽ là phần chứa các hàng khác gồm các nội dung tương ứng
<tfoot> là phần chân của bảng hay chính là hàng cuối cùng của bảng ta có thể để ghi chú về cột hoặc tính tổng tiền của cột,....



