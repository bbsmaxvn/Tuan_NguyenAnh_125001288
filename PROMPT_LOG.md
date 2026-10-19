# NHẬT KÝ PROMPT ENGINEERING (VIBE CODING LOG)

- **Họ và tên:** Nguyễn Anh Tuấn
- **MSSV:** 125001288
- **Lớp học phần:** 25CT113
- **Tên đề tài Website:** Landing Page giới thiệu game VALORANT
- **Công cụ AI đã sử dụng:** ChatGPT
- **Công nghệ:** HTML5, CSS3, Animate.css, CSS Scroll-driven Animations

## 1. Yêu cầu ban đầu (System/Initial Prompt)

> Xây dựng landing page giới thiệu game bắn súng chiến thuật theo cảm hứng giao diện VALORANT. Tách thành `index.html` và `style.css`, không sử dụng JavaScript. Thiết kế dark theme xanh navy kết hợp đỏ #ff4655, tiêu đề chữ condensed đậm, hero lớn, các section giới thiệu gameplay, đặc vụ, bản đồ, esports và nút chơi ngay. Website cần responsive trên desktop/tablet/mobile, có điều hướng rõ ràng, ảnh minh họa và hiệu ứng vừa phải.

## 2. Quá trình tinh chỉnh & Giải quyết sự cố (Iteration Iterations)

### Lần 1: Dựng khung Semantic HTML & CSS Variables
- **Prompt đã dùng:** Tổ chức trang bằng các thẻ semantic HTML5 đúng ngữ nghĩa như `header`, `nav`, `main`, `section`, `article` và `footer`. Không lạm dụng `div` cho mọi khối. Khai báo CSS Variables trong `:root` để quản lý màu sắc, font, spacing và transition.
- **Kết quả AI tạo ra:** Khung trang có header/navigation, hero, các section nội dung và footer; hệ thống màu sắc sử dụng CSS Variables.
- **Nhận xét & Tinh chỉnh của SV:** Kiểm tra thứ tự heading, liên kết điều hướng, nhãn truy cập và bảo đảm mỗi section có mục đích nội dung rõ ràng.

### Lần 2: Hiệu ứng và tương tác không dùng JavaScript
- **Prompt đã dùng:** Loại bỏ toàn bộ JavaScript. Giữ Animate.css cho hiệu ứng hero, thay hiệu ứng cuộn AOS bằng CSS Scroll-driven Animations và tạo menu mobile bằng checkbox/label cùng CSS.
- **Kết quả AI tạo ra:** Tiêu đề hero có hiệu ứng CSS; menu mobile có thể mở/đóng bằng CSS; một số section có hiệu ứng cuộn trên trình duyệt hỗ trợ.
- **Nhận xét & Tinh chỉnh của SV:** AOS cần JavaScript để khởi tạo nên không dùng AOS thực sự. Phương án CSS thay thế đáp ứng yêu cầu không dùng JS nhưng có thể không được tính là tích hợp AOS nếu giảng viên chấm đúng thư viện.

### Lần 3: Hoàn thiện UI/UX và responsive
- **Prompt đã dùng:** Cải thiện tương phản, khoảng cách, trạng thái hover/focus, responsive mobile, góc cắt phong cách game cho nút và hiển thị hình ảnh nhân vật/bản đồ.
- **Kết quả AI tạo ra:** Giao diện dark theme đỏ/navy, các nút có góc cắt, thẻ nội dung có hover, hình ảnh tải từ URL bên ngoài và bố cục thích ứng với màn hình nhỏ.
- **Nhận xét & Tinh chỉnh của SV:** Kiểm tra trên trình duyệt ở nhiều kích thước, kiểm tra URL ảnh và bảo đảm không có file hoặc đoạn mã JavaScript.

### Lần 4: Kiểm tra và gỡ lỗi
- **Thách thức gặp phải:** Menu mobile và hiệu ứng cuộn ban đầu dựa vào JavaScript/AOS, không phù hợp yêu cầu không dùng JS.
- **Cách sửa prompt (Debug prompt):** Xóa `script.js`, xóa các thẻ `<script>` và liên kết AOS JavaScript; thay menu bằng checkbox/label CSS; thay hiệu ứng cuộn bằng CSS Scroll-driven Animations. Xóa các thuộc tính `data-aos` không còn được sử dụng.
- **Kết quả sau sửa:** Source chỉ còn HTML và CSS. Menu mobile hoạt động bằng CSS; hiệu ứng cuộn chỉ chạy ở trình duyệt hỗ trợ CSS Scroll-driven Animations.

## 3. Đánh giá cá nhân về quá trình Vibe Coding

- **AI đã giúp tiết kiệm thời gian ở phần nào nhất?** AI hỗ trợ dựng cấu trúc HTML, tạo hệ thống CSS Variables, bố trí layout responsive và tinh chỉnh hình ảnh/giao diện.
- **Bài học rút ra khi đặt câu hỏi (Prompt) cho AI trong thiết kế web?** Prompt cần nêu rõ mục tiêu, cấu trúc file, phong cách giao diện, yêu cầu kỹ thuật, thiết bị cần hỗ trợ và tiêu chí kiểm tra. Sau khi AI tạo code, cần đọc, kiểm thử và tinh chỉnh thay vì chấp nhận kết quả ngay.
- **Phần cần tự kiểm tra trước khi nộp:** Xác nhận repository có tên đúng cú pháp `Ten_Ho_MSSV`, tải đủ file lên GitHub, bật GitHub Pages và bổ sung đường link live vào phần mô tả repository.

## Bổ sung tinh chỉnh giao diện VALORANT (19/10/2026)

- **Prompt đã dùng:** Dùng logo VALORANT và các ảnh nhân vật/banner do sinh viên cung cấp; chỉnh hero để hình nhân vật nằm bên phải, dùng tông navy/đỏ và tinh chỉnh responsive.
- **Kết quả AI tạo ra:** Logo và artwork hiển thị trong hero, khu vực đặc vụ và bản đồ sử dụng ảnh tham khảo.
- **Thách thức gặp phải:** URL ảnh bên ngoài có thể thay đổi hoặc bị chặn tải.
- **Cách sửa prompt (Debug prompt):** Dùng URL ảnh trực tiếp trong thuộc tính `src`, đặt `object-fit` phù hợp và thêm `alt` cùng `loading="lazy"` cho ảnh ở dưới màn hình đầu.
