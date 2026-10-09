# [Bài tập] Tạo Layout Với Các Thẻ HTML5 và CSS

## 📌 Giới Thiệu & Mục Tiêu

Bài tập hướng dẫn kỹ thuật thiết kế bố cục trang web hiện đại (**Web Layout Design**) sử dụng các thẻ ngữ nghĩa chuẩn **HTML5 (Semantic Elements)** kết hợp với **CSS Flexbox / CSS Grid**, thay thế hoàn toàn thói quen lạm dụng thẻ `<div>` vô nghĩa trước đây.

### 🎯 Mục tiêu bài học:
- **Làm chủ các thẻ HTML5 Semantic**: Sử dụng chuẩn xác 6 thẻ cấu trúc cốt lõi: `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>` và `<footer>`.
- **Hiểu rõ sự khác biệt giữa `<section>` và `<article>`**: Phân biệt phân vùng nhóm nội dung (`section`) và bài viết độc lập hoàn chỉnh (`article`).
- **Thiết kế bố cục trang web chuẩn đáp ứng (Responsive Layout)**: Chia cột nội dung chính và thanh bên (Sidebar), tự động co giãn thích ứng trên màn hình máy tính và thiết bị di động.
- **Tối ưu hóa SEO & Khả năng tiếp cận (Accessibility - a11y)**: Giúp công cụ tìm kiếm và trình đọc màn hình (*Screen Reader*) dễ dàng phân tích cấu trúc trang web.

---

## 🏗️ Sơ Đồ Cấu Trúc Bố Cục HTML5 Semantic

```text
┌──────────────────────────────────────────────────────────────────┐
│                          <header>                                │
│          Tiêu đề trang web, Logo thương hiệu & Tagline           │
├──────────────────────────────────────────────────────────────────┤
│                           <nav>                                  │
│             Thanh menu liên kết điều hướng chính                 │
├──────────────────────────────────┬───────────────────────────────┤
│             <section>            │            <aside>            │
│       Khu vực nội dung chính     │      Thanh bên (Sidebar)      │
│  ┌────────────────────────────┐  │  ┌─────────────────────────┐  │
│  │         <article>          │  │  │   Chủ đề thịnh hành     │  │
│  │   Bài viết độc lập số 1    │  │  └─────────────────────────┘  │
│  └────────────────────────────┘  │  ┌─────────────────────────┐  │
│  ┌────────────────────────────┐  │  │   Góc lời khuyên / Info │  │
│  │         <article>          │  │  └─────────────────────────┘  │
│  │   Bài viết độc lập số 2    │  │                               │
│  └────────────────────────────┘  │                               │
├──────────────────────────────────┴───────────────────────────────┤
│                          <footer>                                │
│            Thông tin bản quyền, liên hệ & điều khoản             │
└──────────────────────────────────────────────────────────────────┘
```

---

## 📂 Cấu Trúc Dự Án

```text
tao_layout_html5_css/
├── index.html           # Bản chuẩn theo yêu cầu bài học CodeGym
├── styles.css           # Định kiểu CSS Flexbox 2 cột đáp ứng (Responsive)
├── modern_layout.html   # Bản nâng cấp giao diện tạp chí công nghệ cao cấp
├── modern_layout.css    # CSS Grid 2 chiều, Dark/Indigo Palette, Glassmorphism
└── README.md            # Báo cáo kỹ thuật phân tích chi tiết
```

---

## 📊 Bảng Phân Tích Ý Nghĩa & Vai Trò Các Thẻ HTML5

| Thẻ HTML5 | Ý nghĩa ngữ nghĩa (Semantics) | Vai trò trong bố cục |
| :--- | :--- | :--- |
| **`<header>`** | Phần đầu trang / biểu ngữ | Chứa tiêu đề trang, logo, slogan hoặc phần đầu của từng bài viết |
| **`<nav>`** | Thanh điều hướng | Đóng gói danh sách liên kết dẫn đến các phân mục chính của website |
| **`<main>`** | Vùng nội dung trọng tâm | Bao bọc nội dung trung tâm duy nhất của trang, không lặp lại giữa các trang |
| **`<section>`** | Phân vùng nội dung có chủ đề | Nhóm các nội dung có liên quan logic với nhau (thường có một tiêu đề `<h2>`) |
| **`<article>`** | Khối nội dung độc lập | Đại diện cho một bài báo, bài viết blog có thể tái sử dụng độc lập ở nơi khác |
| **`<aside>`** | Nội dung phụ trợ / bên lề | Chứa sidebar, danh sách xem nhiều, quảng cáo hoặc ghi chú liên quan |
| **`<footer>`** | Phần chân trang | Chứa thông tin bản quyền, liên hệ, chính sách bảo mật hoặc sơ đồ trang |

---

## ⚡ Tại Sao Phải Sử Dụng HTML5 Semantic Thay Vì Thẻ `<div>`?

1. **Tối ưu hóa công cụ tìm kiếm (Semantic SEO)**:
   - Googlebot và các công cụ tìm kiếm có thể nhận diện ngay đâu là bài viết chính (`<article>`), đâu là thanh điều hướng (`<nav>`), và đâu là nội dung phụ (`<aside>`), từ đó lập chỉ mục chính xác hơn.
2. **Khả năng tiếp cận cho người khiếm thị (Accessibility / a11y)**:
   - Các phần mềm đọc màn hình (*Screen Reader*) có thể điều hướng người dùng nhảy thẳng tới nội dung chính (`<main>`) mà không bị kẹt ở các thanh menu phức tạp.
3. **Mã nguồn sạch & Dễ bảo trì**:
   - Tránh hiện tượng *"Div Soup"* (lồng hàng chục thẻ `<div>` vô nghĩa khiến cấu trúc mã bị rối loạn).

---

## ✨ Điểm Nổi Bật Ở Bản Hiện Đại (`modern_layout.html`)

Ngoài bản chuẩn CodeGym, dự án trang bị thêm phiên bản hiện đại:
- **CSS Grid hai chiều**: Tách biệt rõ ràng các khu vực nội dung với độ phân giải linh hoạt.
- **Phong cách Glassmorphism & Editorial**: Viền kính mờ tinh tế, đổ bóng đa tầng, typography hiện đại (*Plus Jakarta Sans*).
- **Hệ thống thẻ bài viết hoàn chỉnh**: Bổ sung thời gian đọc (Reading Time), huy hiệu danh mục (Category Badges) và thông tin tác giả với avatar tròn.
- **Hoàn toàn thích ứng (Fully Responsive)**: Tự động chuyển đổi từ bố cục 2 cột sang 1 cột liền mạch trên điện thoại di động.

---

## 🚀 Hướng Dẫn Mở & Kiểm Thử Trên Trình Duyệt

1. **Bản chuẩn CodeGym**: Mở tệp [**`index.html`**](file:///C:/Users/dathao/Downloads/tao_layout_html5_css/index.html).
2. **Bản nâng cấp UI/UX cao cấp**: Mở tệp [**`modern_layout.html`**](file:///C:/Users/dathao/Downloads/tao_layout_html5_css/modern_layout.html).
