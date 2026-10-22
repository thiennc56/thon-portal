# Cổng thông tin điện tử xã Tam Đảo, tỉnh Phú Thọ

Bộ giao diện HTML, CSS, JavaScript thuần, gồm 17 trang. Không cần npm, framework, CDN, API key hoặc bước build. CSS và JavaScript dùng chung. Font hệ thống Segoe UI; nếu máy đã có Inter thì ưu tiên Inter.

## Mở giao diện

1. Giải nén toàn bộ thư mục dự án.
2. Mở `index.html` bằng Chrome, Edge hoặc Firefox.
3. Chọn mục `Các thôn` để xem danh mục 15 thôn trên địa bàn xã.

Có thể chạy bằng VS Code Live Server hoặc lệnh `python -m http.server 8080` ngay trong thư mục này rồi mở `http://localhost:8080`. Đưa nguyên thư mục lên hosting tĩnh hoặc GitHub Pages cũng dùng được. Giữ nguyên đường dẫn tương đối. Liên kết ngoài như Dịch vụ công và Google Maps cần Internet; ảnh, icon, tìm kiếm và biểu mẫu demo đều chạy offline.

## Các trang

| Cấp xã | Đường dẫn |
| --- | --- |
| Trang chủ | index.html |
| Giới thiệu | gioi-thieu.html |
| Tin tức – Sự kiện | tin-tuc.html |
| Chính quyền – Dân sinh | chinh-quyen-dan-sinh.html |
| OCOP – Đặc sản | ocop-dac-san.html |
| Hỏi đáp | hoi-dap.html |
| Danh mục các thôn | cac-thon.html |

| Chuyên mục cộng đồng | Đường dẫn |
| --- | --- |
| Trang chủ thôn | thon-tam-dao/index.html |
| Giới thiệu | thon-tam-dao/gioi-thieu.html |
| Tin tức | thon-tam-dao/tin-tuc.html |
| Toàn dân bảo vệ an ninh | thon-tam-dao/toan-dan-bao-ve-an-ninh.html |
| Đặt lịch | thon-tam-dao/dat-lich.html |
| Phản ánh | thon-tam-dao/phan-anh.html |
| Thư viện sách | thon-tam-dao/thu-vien-sach.html |
| Dữ liệu thôn | thon-tam-dao/du-lieu-thon.html |
| Văn hóa – Xã hội | thon-tam-dao/van-hoa-xa-hoi.html |
| Liên hệ | thon-tam-dao/lien-he.html |

`style.css`: thiết kế chung, biến màu, bố cục và breakpoint responsive.
`script.js`: điều hướng mobile, hiệu ứng cuộn, lên đầu trang, popup, tìm kiếm, slideshow, lọc tin/phân trang, chatbot, tài khoản demo, kiểm tra biểu mẫu và hiển thị chi tiết từng thôn.
`content.js`: chỉ mục tìm kiếm và dữ liệu bài viết, danh mục sách dùng cho popup.
`assets/images/`: 4 ảnh WebP AI minh họa làng quê và Quốc huy SVG.
`assets/docs/`: các tệp PDF, DOCX, CSV mẫu tải xuống được.

## Tính năng trình diễn

- Menu di động có nút mở/đóng và ô tìm kiếm; menu cấp xã có nhóm Dân sinh xổ xuống.
- Header đổi đổ bóng khi cuộn, nút lên đầu trang, slider chuyển ảnh bằng nút hoặc chấm.
- Tìm kiếm có dấu/không dấu trên danh mục và nội dung tin mẫu.
- Tin tức thôn: lọc chuyên mục, phân trang 6 bài/trang; mở bài trong popup.
- Lịch hẹn: trường bắt buộc, điện thoại theo định dạng, ngày không trước hôm nay.
- Phản ánh: tối đa 3 tệp JPG, PNG, WebP hoặc PDF, tối đa 5 MB/tệp; chỉ xem trước, không tải lên.
- Các biểu mẫu tạo mã DEMO và hiển thị xác nhận. Không có API, máy chủ, email thông báo hoặc lưu trữ lâu dài. Tải lại trang sẽ xóa trạng thái demo.
- Thư viện: lọc theo chuyên mục và mở trực tiếp các tài liệu PDF công khai; không có quy trình mượn sách giả lập.
- Dữ liệu thôn: thống kê tổng hợp mẫu, tài liệu tải về thật. Không có danh sách cá nhân/hộ nghèo công khai.
- Hộp thoại có xử lý Escape, giữ focus và trả lại focus; hỗ trợ bàn phím và tùy chọn giảm chuyển động.
- Đồng hồ theo giờ Việt Nam; thời tiết là giá trị mẫu, không gọi API.
- Bản đồ là sơ đồ đồ họa; camera là ảnh tĩnh mô phỏng; danh bạ là dữ liệu mẫu/chưa xác minh.

## Chỉnh sửa và thêm thôn

- Sửa màu trong `:root` ở đầu `style.css`.
- Nội dung chính nằm ngay trong từng file HTML; không cần JavaScript để dựng phần nội dung tĩnh.
- Khi sửa tin hoặc sách, cập nhật đồng thời HTML tương ứng và `content.js` để popup/tìm kiếm khớp nội dung.
- Thay ảnh bằng WebP/JPG của địa phương rồi cập nhật đường dẫn trong HTML và mảng slideshow của `script.js`.
- Nhân bản thư mục `thon-tam-dao` để thêm thôn; sửa tên thôn, nội dung và liên kết từ trang xã. Mỗi thôn dùng lại CSS/JS ở cấp gốc bằng `../`.
- Header/footer được lưu trong từng HTML để mở trực tiếp bằng `file://`, không phụ thuộc fetch. Khi đổi menu hoặc thông tin dùng chung, cập nhật các HTML tương ứng.

## Trước khi vận hành chính thức

Nội dung, danh hiệu, lịch sinh hoạt, số liệu thống kê và nhân sự mẫu cần được địa phương xác minh, phê duyệt và thay thế. Cần bổ sung backend, cơ chế tiếp nhận hồ sơ, phân quyền, bảo vệ dữ liệu, chống spam, nhật ký xử lý và quản trị nội dung nếu dùng thực tế. Các trường hiện không gửi dữ liệu ra ngoài.

## Nguồn tham khảo và hình ảnh

Cấu trúc tham khảo từ https://xadonganh.com/ do người dùng cung cấp. Giao diện và nội dung mẫu được xây dựng mới, không sao chép toàn văn bài gốc. Hai ảnh tham chiếu đính kèm không mở được từ đường dẫn phiên làm việc; vì vậy không khẳng định đã tái hiện chính xác phong cách hai ảnh này.

Quốc huy: https://commons.wikimedia.org/wiki/File:Emblem_of_Vietnam.svg — nguồn ghi tác giả Bùi Trang Chước, phiên bản SVG qua Wikimedia Commons. Không dùng ảnh AI để thay Quốc huy.

Bốn ảnh phong cảnh do công cụ tạo ảnh tích hợp tạo mới; chỉ là minh họa làng quê Việt Nam, không xác nhận là ảnh chính thức của Tam Đảo. Prompt lưu tại `IMAGE-PROMPTS.md`. Bìa sách được dựng bằng HTML/CSS để làm danh mục mẫu; PDF và DOCX là tài liệu mẫu tự biên soạn.
