# BÁO CÁO BÀI TẬP: PHÂN TÍCH VÀ XÂY DỰNG CẤU TRÚC WEBSITE TEMPLATE

---

## I. THÔNG TIN CHUNG
* **Tên bài tập:** Phân tích và Xây dựng Cấu Trúc Website Template
* **Môn học:** Thiết kế & Phát triển Trang Web
* **Trang web phân tích mẫu:** [Dev.to](https://dev.to) (Trang chia sẻ kiến thức Lập trình)

---

## II. NHIỆM VỤ 1: PHÂN TÍCH CẤU TRÚC TRANG WEB THỰC TẾ

### 1. Phân tích các thành phần cốt lõi (Semantic HTML Structure)

* **Header (`<header>`):** 
  * Nằm ở vị trí trên cùng của trang web, cố định (fixed/sticky) khi cuộn chuột.
  * Chứa logo trang web (Tiêu đề chính) và thanh tìm kiếm (Search bar), cùng với các nút hành động nhanh như "Create Post" và "Log in/Sign up".
* **Navigation Menu (`<nav>`):** 
  * Được thiết kế kết hợp giữa thanh điều hướng ngang chính và thanh danh mục chuyên mục phía dưới/bên trái.
  * Chứa các mục chính: **Home**, **Reading List**, **Podcasts**, **Videos**, **Tags**, **About**.
* **Content Section (`<main>` / `<section>`):** 
  * Chia làm cấu trúc nhiều cột (Grid System):
    * **Cột chính (Main Content):** Hiển thị danh sách các bài viết nổi bật, đoạn văn ngắn mô tả nội dung và hình ảnh thumbnail minh họa.
    * **Cột phụ (Sidebar):** Hiển thị danh sách tin tức hot, các hashtag phổ biến hoặc thảo luận nổi bật.
* **Footer (`<footer>`):** 
  * Nằm ở cuối trang web.
  * Chứa các thông tin về bản quyền (`© 2026 Dev Community`), chính sách bảo mật, điều khoản sử dụng và các liên kết mạng xã hội.

### 2. Bố trí giao diện (Layout Description)
Giao diện được tổ chức theo bố cục dạng khối (Block layout) hiện đại với flexbox và grid:
* **Chiều dọc:** Đi từ trên xuống dưới theo thứ tự Header -> Nav -> Content -> Footer.
* **Chiều ngang (Content):** Được canh giữa màn hình (Centered layout) với chiều rộng tối đa (Max-width) khoảng `1200px` để tối ưu trải nghiệm đọc trên các thiết bị màn hình lớn.

---

## III. TỔ CHỨC FILE VÀ THƯ MỤC DỰ ÁN

```text
my-website-project/
│
├── index.html          # File chứa mã nguồn HTML chính
├── style.css           # File chứa mã mã nguồn CSS quy định giao diện
└── images/             # Thư mục chứa hình ảnh minh họa (nếu có)
    └── placeholder.jpg
```

---

## IV. NHIỆM VỤ 2: XÂY DỰNG LẠI BỐ CỤC BẰNG HTML & CSS

### 1. Mã nguồn HTML (`index.html`)

```html
<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Website Template - Bài Tập Phân Tích</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- 1. HEADER SECTION -->
    <header class="site-header">
        <div class="container">
            <h1 class="logo">DevCommunity</h1>
            <span class="tagline">Trang chia sẻ kiến thức Lập trình</span>
        </div>
    </header>

    <!-- 2. NAVIGATION MENU SECTION -->
    <nav class="site-nav">
        <div class="container">
            <ul class="nav-list">
                <li><a href="#" class="active">Trang chủ</a></li>
                <li><a href="#">Bài viết</a></li>
                <li><a href="#">Khóa học</a></li>
                <li><a href="#">Giới thiệu</a></li>
                <li><a href="#">Liên hệ</a></li>
            </ul>
        </div>
    </nav>

    <!-- 3. MAIN CONTENT SECTION -->
    <main class="site-content">
        <div class="container content-layout">
            
            <!-- Bài viết chính -->
            <article class="main-article">
                <h2>Cấu Trúc Website Template Chuẩn Trong HTML5</h2>
                <p class="post-meta">Đăng ngày: 06/10/2026 | Tác giả: Admin</p>
                
                <div class="image-wrapper">
                    <img src="https://via.placeholder.com/800x400" alt="Hình ảnh minh họa bố cục website">
                </div>

                <p>Một website chuẩn thường được chia thành 4 phần cơ bản bao gồm Header, Navigation, Content và Footer. Việc phân chia rõ ràng giúp trình duyệt và công cụ tìm kiếm dễ dàng hiểu được ngữ nghĩa (Semantic) của từng phần trên trang web.</p>
                <p>Nội dung chính thường chứa các thông tin cốt lõi mà người dùng quan tâm, được trình bày kết hợp giữa văn bản, hình ảnh và danh sách để tối ưu trải nghiệm đọc.</p>
            </article>

            <!-- Sidebar phụ -->
            <aside class="sidebar">
                <h3>Chủ đề nổi bật</h3>
                <ul>
                    <li><a href="#">Lập trình Web cơ bản</a></li>
                    <li><a href="#">Hướng dẫn HTML5 & CSS3</a></li>
                    <li><a href="#">Xây dựng Layout với Flexbox</a></li>
                    <li><a href="#">Tối ưu hóa Website</a></li>
                </ul>
            </aside>

        </div>
    </main>

    <!-- 4. FOOTER SECTION -->
    <footer class="site-footer">
        <div class="container">
            <p>&copy; 2026 DevCommunity. Tất cả quyền được bảo lưu.</p>
            <p>Thiết kế bởi Học viên | Bài tập Phân tích và Xây dựng Cấu trúc Website</p>
        </div>
    </footer>

</body>
</html>
```

---

### 2. Mã nguồn CSS (`style.css`)

```css
/* --- RESET VÀ CÀI ĐẶT CHUNG --- */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    line-height: 1.6;
    color: #333;
    background-color: #f4f6f9;
}

.container {
    width: 90%;
    max-width: 1100px;
    margin: 0 auto;
}

/* --- 1. HEADER --- */
.site-header {
    background-color: #1e293b;
    color: #ffffff;
    padding: 20px 0;
    text-align: center;
}

.site-header .logo {
    font-size: 28px;
    margin-bottom: 5px;
}

.site-header .tagline {
    font-size: 14px;
    color: #94a3b8;
}

/* --- 2. NAVIGATION MENU --- */
.site-nav {
    background-color: #2563eb;
}

.site-nav .nav-list {
    list-style: none;
    display: flex;
    justify-content: center;
}

.site-nav .nav-list li a {
    display: block;
    color: #ffffff;
    text-decoration: none;
    padding: 14px 20px;
    font-weight: 600;
    transition: background-color 0.3s;
}

.site-nav .nav-list li a:hover,
.site-nav .nav-list li a.active {
    background-color: #1d4ed8;
}

/* --- 3. CONTENT SECTION --- */
.site-content {
    padding: 30px 0;
}

.content-layout {
    display: flex;
    gap: 20px;
}

.main-article {
    flex: 3;
    background-color: #ffffff;
    padding: 25px;
    border-radius: 8px;
    box-shadow: 0 2px 5px rgba(0,0,0,0.05);
}

.main-article h2 {
    color: #0f172a;
    margin-bottom: 10px;
}

.post-meta {
    font-size: 13px;
    color: #64748b;
    margin-bottom: 20px;
}

.image-wrapper img {
    width: 100%;
    height: auto;
    border-radius: 6px;
    margin-bottom: 20px;
}

.main-article p {
    margin-bottom: 15px;
}

/* Sidebar */
.sidebar {
    flex: 1;
    background-color: #ffffff;
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0 2px 5px rgba(0,0,0,0.05);
    height: fit-content;
}

.sidebar h3 {
    margin-bottom: 15px;
    font-size: 18px;
    border-bottom: 2px solid #2563eb;
    padding-bottom: 5px;
}

.sidebar ul {
    list-style: none;
}

.sidebar ul li {
    margin-bottom: 10px;
}

.sidebar ul li a {
    color: #2563eb;
    text-decoration: none;
}

.sidebar ul li a:hover {
    text-decoration: underline;
}

/* --- 4. FOOTER --- */
.site-footer {
    background-color: #0f172a;
    color: #94a3b8;
    text-align: center;
    padding: 20px 0;
    margin-top: 20px;
    font-size: 14px;
}
```

---

## V. ĐÍNH KÈM HÌNH ẢNH TRANG WEB MẪU
*(Người dùng dán ảnh chụp màn hình trang web thực tế đã phân tích vào phần này trước khi xuất ra Word)*

---