# NHẬT KÝ PROMPT ENGINEERING (VIBE CODING LOG)

- **Họ và tên:** Dương Quang Vinh
- **MSSV:** 125001483
- **Tên đề tài Website:** Trang bán pizza — Crust & Co.
- **Công cụ AI đã sử dụng:** ChatGPT

> Lưu ý: Nhật ký dưới đây là bản ghi mẫu được tổng hợp để mô tả quy trình xây dựng website. Hãy điều chỉnh phần “nhận xét” và “thách thức” theo đúng những gì bạn thực sự đã kiểm tra, chỉnh sửa trong quá trình làm bài.

## 1. Yêu cầu ban đầu (System/Initial Prompt)

> Hãy tạo một website giới thiệu và bán pizza có giao diện hiện đại, đẹp mắt, mang phong cách thương hiệu pizza thủ công. Chỉ sử dụng HTML5 và CSS thuần, không dùng JavaScript, Bootstrap hay framework. Website cần responsive trên máy tính, tablet và điện thoại; sử dụng Semantic HTML5 gồm header, nav, main, section/article và footer; dùng CSS Variables trong :root để quản lý màu sắc, font và khoảng cách; sử dụng Flexbox/Grid; có hiệu ứng hover, focus và chuyển động CSS nhẹ. Nội dung bằng tiếng Việt, có hero, thực đơn pizza, câu chuyện thương hiệu, đánh giá khách hàng, lời kêu gọi đặt hàng và footer. Tạo hai file index.html và style.css.

## 2. Quá trình tinh chỉnh & Giải quyết sự cố (Iteration Iterations)

### Lần 1: Dựng khung Semantic HTML & CSS Variable

- **Prompt đã dùng:** “Hãy tổ chức trang bằng HTML5 semantic. Dùng header cho logo/navigation, main cho nội dung chính, section cho từng khu vực, article cho từng thẻ pizza và footer cho thông tin cuối trang. Không dùng div thay thế các thẻ semantic khi không phù hợp. Khai báo bảng màu và font trong :root.”
- **Kết quả AI tạo ra:** Khung trang gồm phần thông báo, header/navigation, hero, thực đơn, câu chuyện thương hiệu, đánh giá, CTA và footer. CSS Variables được dùng xuyên suốt để quản lý bảng màu đỏ, kem, vàng và xanh lá.
- **Nhận xét & Tinh chỉnh của SV:** Kiểm tra các vùng nội dung có thẻ semantic phù hợp; giữ `div` cho các nhóm chỉ phục vụ bố cục, hình ảnh trang trí và các cụm thành phần không có ngữ nghĩa riêng. Đặt tên class theo từng khối để CSS dễ đọc và bảo trì.

### Lần 2: Hoàn thiện giao diện, responsive và hiệu ứng CSS

- **Prompt đã dùng:** “Tinh chỉnh giao diện theo phong cách editorial/premium: typography có tương phản, khoảng trắng rộng, ảnh pizza lớn, thẻ menu bo góc, màu đỏ làm điểm nhấn. Viết media queries cho màn hình dưới 1000px, 760px và 480px. Thêm hover/focus rõ ràng và chuyển động CSS tinh tế; tôn trọng prefers-reduced-motion.”
- **Kết quả AI tạo ra:** Bố cục hai cột cho hero, lưới ba thẻ pizza trên desktop, phần giới thiệu chia đôi và các breakpoint để điều chỉnh trên tablet/mobile.
- **Thách thức gặp phải:** Khi màn hình hẹp, thanh điều hướng, các thẻ menu và ghi chú nổi có nguy cơ chật hoặc tràn.
- **Cách sửa prompt (Debug prompt):** “Ở màn hình 760px, chuyển hero và phần câu chuyện thành một cột, cho navigation xuống hàng riêng, lưới pizza còn hai cột; ở 480px chuyển menu thành một cột và giảm cỡ chữ/khoảng cách. Kiểm tra không có nội dung quan trọng bị cắt.”
- **Nhận xét & Tinh chỉnh của SV:** Mở trang ở nhiều kích thước màn hình, kiểm tra thanh điều hướng, nút CTA, nội dung thẻ và chân trang. Điều chỉnh thêm nếu phát hiện tràn ngang hoặc chữ quá nhỏ.

### Lần 3: Kiểm tra đường dẫn và khả năng sử dụng

- **Prompt đã dùng:** “Rà soát toàn bộ liên kết neo trong navigation, CTA và footer; bảo đảm chúng trỏ đến đúng id. Dùng alt tiếng Việt mô tả ảnh, focus-visible cho liên kết và mailto làm phương án liên hệ/đặt hàng minh họa vì dự án không dùng JavaScript hay backend.”
- **Kết quả AI tạo ra:** Các liên kết điều hướng đến section tương ứng; ảnh có alt; nút đặt pizza mở email soạn sẵn thay vì giả lập giỏ hàng không hoạt động.
- **Thách thức gặp phải:** Website tĩnh HTML/CSS không thể xử lý giỏ hàng, thanh toán hoặc lưu đơn hàng thật mà không có backend hay JavaScript.
- **Cách sửa prompt (Debug prompt):** “Không trình bày nút cộng như thể đã thêm món vào giỏ hàng. Hãy để liên kết mở email đặt hàng với tên pizza có sẵn trong tiêu đề email, và ghi rõ đây là website demo tĩnh.”
- **Nhận xét & Tinh chỉnh của SV:** Thử các liên kết đặt hàng và liên hệ; thay email minh họa bằng email thật nếu được yêu cầu. Kiểm tra ảnh cần kết nối Internet để tải từ nguồn bên ngoài.

## 3. Đánh giá cá nhân về quá trình Vibe Coding

- **AI đã giúp tiết kiệm thời gian ở phần nào nhất?** AI hỗ trợ phác thảo nhanh cấu trúc HTML, hệ thống class CSS, bảng màu, bố cục lưới và các breakpoint responsive. Nhờ đó có thể dành thời gian xem lại ngữ nghĩa, tính nhất quán và trải nghiệm người dùng.
- **Bài học rút ra khi đặt câu hỏi (Prompt) cho AI trong thiết kế web?** Prompt càng cụ thể về công nghệ được phép dùng, cấu trúc HTML, phong cách hình ảnh, kích thước màn hình và tiêu chí kiểm tra thì kết quả càng sát yêu cầu. Nên chia công việc thành từng vòng: dựng cấu trúc, tạo phong cách, responsive, rồi kiểm tra liên kết và các giới hạn kỹ thuật.
- **Điểm cần lưu ý theo đề thi:** Đề gốc có yêu cầu tích hợp Animate.css và AOS. Bản này tuân thủ giới hạn chỉ HTML5/CSS thuần nên dùng animation CSS tự viết và không tải hai thư viện đó. Nếu giảng viên chấm theo đúng yêu cầu thư viện, cần hỏi lại xem có cho phép dùng CDN hay không; không nên khai rằng đã tích hợp Animate.css/AOS khi chưa thực hiện.
