# Bộ giao diện HTML – Quản lý giao việc & điều hành

## Các màn hình
- `index.html`: Bảng điều hành tổng hợp + luồng xử lý 5 bước.
- `tiep-nhan-ai.html`: Tiếp nhận văn bản/nhiệm vụ và AI hỗ trợ đọc, phân loại.
- `phan-cong.html`: Giao lãnh đạo phụ trách, phòng/bộ phận, chuyên viên, hạn và mốc cảnh báo.
- `nhiem-vu.html`: Danh sách/tra cứu nhiệm vụ.
- `kpi-ca-nhan.html`: KPI cá nhân theo cán bộ: khối lượng, tiến độ, đúng hạn, chất lượng và công việc đang xử lý.
- `chi-tiet-nhiem-vu.html`: Chi tiết nhiệm vụ, tiến độ, lịch sử cập nhật, đánh giá.
- `bao-cao.html`: Báo cáo theo thời gian và dashboard biểu đồ.

## Công nghệ dùng trong prototype
- Tailwind CSS qua CDN.
- Lucide Icons qua CDN.
- Chart.js qua CDN.
- HTML thuần, responsive, không yêu cầu build.

## Gợi ý tích hợp backend
Mỗi trang hiện đang dùng dữ liệu mẫu. Khi tích hợp .NET/AngularJS hoặc framework khác, nên tách:
1. Layout/sidebar/topbar thành component dùng chung.
2. Dữ liệu bảng nhiệm vụ thành API phân trang.
3. Trạng thái/tiến độ từ API dashboard.
4. Luồng AI: upload/nhận văn bản -> API OCR/NLP/LLM -> dữ liệu đề xuất -> người dùng xác nhận.
5. Notification service cho web/mobile/email.
6. API báo cáo nhận tham số từ ngày, đến ngày, đơn vị, trạng thái, kế hoạch.


## Bộ nhận diện cập nhật
- Logo tròn: `assets/logo-quan-ly-cong-viec.svg`
- Màu chủ đạo: `#1d75b0`
- Màu active: `#1560c0`
- Nền sidebar: `#0e3060`
- Tiêu đề hệ thống: **HỆ THỐNG QUẢN LÝ CÔNG VIỆC**


## Responsive menu
- Trên màn hình >= 1024px: sidebar hiển thị cố định.
- Trên tablet/mobile: sidebar ẩn ngoài khung nhìn và mở bằng nút hamburger trên header.
- Có overlay tối, nút đóng, đóng khi bấm ra ngoài, bấm menu, nhấn ESC hoặc chuyển về desktop.
- JavaScript nằm trực tiếp trong từng file HTML, không cần thêm thư viện.
