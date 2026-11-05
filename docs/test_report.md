# BÁO CÁO KIỂM THỬ TRƯỚC BÀN GIAO

## 1. Thông tin chung

| Thông tin | Chi tiết |
|---|---|
| Tên dự án | My-CV - Website CV cá nhân Chu Việt Anh |
| Phiên bản | v1.0.0 |
| Ngày kiểm thử | 05/11/2026 |
| Người thực hiện/đánh giá | Chưa ghi nhận |
| Phạm vi | Rà soát mã nguồn HTML/CSS, tài liệu dự án và mức độ sẵn sàng bàn giao |
| Môi trường kiểm thử | Chưa ghi nhận; chưa có kết quả chạy trên trình duyệt hoặc Docker |
| Loại đánh giá | Rà soát tĩnh sơ bộ; chưa thay thế kiểm thử chức năng và tương thích thực tế |

### Quy ước trạng thái

- **Đạt:** Có đủ kiểm tra/minh chứng cho thấy hạng mục đáp ứng yêu cầu.
- **Chưa đạt:** Đã xác nhận có lỗi hoặc hành vi chưa đáp ứng.
- **Cần cải thiện:** Chưa có đủ kết quả kiểm thử/minh chứng, hoặc cần kiểm tra và hoàn thiện thêm.

> Trạng thái **Cần cải thiện** thường có nghĩa là chưa được xác minh trong môi trường chạy, không tự động đồng nghĩa với lỗi đã được xác nhận. Các nhận xét trong báo cáo được lập từ mã nguồn và tài liệu hiện có; cần thực hiện kiểm thử runtime trước khi phê duyệt bàn giao.

## 2. Bảng tổng quan trạng thái

| # | Nhóm tiêu chí | Trạng thái | Tóm tắt |
|---|---|---|---|
| 1 | Tính đúng đắn và mức độ đáp ứng yêu cầu chức năng | Chưa đạt | Cấu trúc các mục và liên kết nội bộ có trong mã nguồn; liên kết GitHub và TikTok tại phần Liên hệ đang dùng `href="#"`. |
| 2 | Giao diện, trải nghiệm người dùng và khả năng tương thích | Cần cải thiện | CSS có breakpoint responsive và hỗ trợ focus/reduced motion; chưa kiểm tra hiển thị thực tế, khả năng tiếp cận hoặc tương thích trình duyệt. |
| 3 | Khả năng vận hành, xử lý lỗi và hiệu năng cơ bản | Cần cải thiện | Có hướng dẫn chạy bằng máy chủ tĩnh/Docker; chưa có kết quả khởi chạy, kiểm tra lỗi tài nguyên hoặc đo hiệu năng. |
| 4 | Bảo mật, quản lý cấu hình và dữ liệu | Cần cải thiện | Website tĩnh, tài liệu không ghi nhận cấu hình bí mật; chưa có biên bản rà soát bảo mật và quyền công khai dữ liệu cá nhân. |
| 5 | Chất lượng mã nguồn, cấu trúc repository và tài liệu bàn giao | Cần cải thiện | Có phân tách HTML/CSS và tài liệu README/release note; cần xác minh tài nguyên, liên kết và hoàn tất rà soát chất lượng. |
| 6 | Khả năng triển khai, kiểm thử và cung cấp minh chứng | Cần cải thiện | README có hướng dẫn triển khai; chưa có kết quả chạy thử, biên bản test hoặc ảnh minh chứng trong thư mục `docs/sreenshots`. |

## 3. Chi tiết kiểm tra

### 3.1. Tính đúng đắn và mức độ đáp ứng yêu cầu chức năng

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Điều hướng đến các phần Giới thiệu, Kỹ năng, Dự án và Liên hệ | Đạt | Trong `index.html`, các liên kết điều hướng trỏ đến `#about`, `#skills`, `#projects`, `#contact`; các phần tương ứng có ID. Chưa xác minh thao tác trên trình duyệt. |
| Nút xem dự án và liên hệ tại phần giới thiệu | Đạt | Liên kết trỏ đến `#projects` và `#contact`, khớp ID trong tài liệu HTML. |
| Hiển thị thông tin cá nhân, kỹ năng và danh sách dự án | Cần cải thiện | Nội dung có trong HTML; cần mở trang và xác minh nội dung, ảnh, bố cục được tải đầy đủ. |
| Liên kết email | Đạt | Có liên kết `mailto:anhc6138@gmail.com`; chưa kiểm tra ứng dụng email được mở khi nhấn. |
| Liên kết GitHub và TikTok | Chưa đạt | Hai liên kết ở phần Liên hệ có `href="#"`, không dẫn đến hồ sơ tương ứng. Cần thay bằng URL thật và kiểm tra lại. |
| Ảnh đại diện và ảnh minh họa dự án | Cần cải thiện | Ảnh đại diện dùng đường dẫn cục bộ; ảnh dự án tải từ website bên ngoài. Chưa xác minh tất cả tài nguyên trả về thành công. |

### 3.2. Giao diện, trải nghiệm người dùng và khả năng tương thích

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Bố cục ở kích thước điện thoại, máy tính bảng và máy tính để bàn | Cần cải thiện | CSS khai báo mobile-first, breakpoint từ 768px và 1280px; chưa chụp hoặc kiểm tra trực tiếp ở các viewport này. |
| Điều hướng, lưới dự án và nội dung không tràn/che khuất | Cần cải thiện | CSS khai báo menu có thể xuống dòng, lưới dự án 1/2/3 cột; cần xác minh trực quan trên trình duyệt và thiết bị thực tế. |
| Tương thích Chrome, Edge, Firefox và Safari | Cần cải thiện | README nêu các trình duyệt mục tiêu nhưng chưa có ma trận hoặc kết quả kiểm thử trình duyệt. |
| Điều hướng bằng bàn phím và hiển thị focus | Cần cải thiện | CSS có `:focus-visible`; cần thử Tab/Shift+Tab và xác minh focus nhìn thấy, đúng thứ tự. |
| Độ tương phản, khả năng đọc và nội dung thay thế ảnh | Cần cải thiện | Một số ảnh có `alt`; chưa đo tương phản màu hoặc rà soát toàn bộ nội dung và khả năng tiếp cận. |
| Tôn trọng thiết lập giảm chuyển động | Đạt | CSS có quy tắc `prefers-reduced-motion: reduce`; cần xác nhận hành vi trong trình duyệt nếu yêu cầu kiểm thử runtime. |

### 3.3. Khả năng vận hành, xử lý lỗi và hiệu năng cơ bản

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Mở trang trực tiếp hoặc qua máy chủ tĩnh Python | Cần cải thiện | README có hướng dẫn `py -m http.server 8000`; chưa ghi nhận kết quả khởi chạy và truy cập. |
| Triển khai qua Docker/Nginx | Cần cải thiện | README có lệnh chạy container Nginx; chưa xác minh image, ánh xạ thư mục, cổng và khả năng truy cập. |
| Xử lý khi ảnh/tài nguyên bên ngoài không khả dụng | Cần cải thiện | Ảnh dự án lấy từ các máy chủ ngoài; chưa thử mất kết nối, URL lỗi hoặc phương án hiển thị thay thế. |
| Tải trang và hiệu năng cơ bản | Cần cải thiện | Chưa có số liệu thời gian tải, kích thước tài nguyên hoặc kết quả kiểm tra hiệu năng. |
| Lỗi console và lỗi tải tài nguyên | Cần cải thiện | Chưa chạy trang và chưa thu thập log console/network. |

### 3.4. Bảo mật, quản lý cấu hình và dữ liệu

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Cấu hình bí mật, khóa API và thông tin xác thực | Cần cải thiện | README cho biết dự án không dùng tệp cấu hình môi trường hoặc thông tin bí mật; cần rà soát toàn bộ repository trước khi phát hành. |
| Dữ liệu cá nhân được công khai | Cần cải thiện | Trang hiển thị thông tin cá nhân và địa chỉ email; cần chủ sở hữu xác nhận nội dung được phép công khai. |
| Tài nguyên và liên kết từ bên thứ ba | Cần cải thiện | Ảnh dự án được tải từ website bên ngoài; cần đánh giá độ tin cậy, tính sẵn sàng và ảnh hưởng quyền riêng tư. |
| Phạm vi xử lý dữ liệu phía máy chủ | Đạt | Theo README, đây là website tĩnh, không có backend hoặc cơ sở dữ liệu. Nhận định này dựa trên tài liệu, chưa phải kiểm toán hạ tầng triển khai. |

### 3.5. Chất lượng mã nguồn, cấu trúc repository và tài liệu bàn giao

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Phân tách nội dung và giao diện | Đạt | `index.html` tham chiếu stylesheet riêng tại `assets/css/styles.css`. |
| Ngôn ngữ trang và cấu trúc nội dung cơ bản | Đạt | HTML khai báo `lang="vi"`; các phần nội dung chính được tổ chức theo section. Chưa chạy HTML validator. |
| Liên kết và đường dẫn tài nguyên nội bộ | Cần cải thiện | Cần xác minh ảnh đại diện và toàn bộ đường dẫn tồn tại trong repository; chưa thực hiện kiểm tra tự động. |
| Tài liệu sử dụng và triển khai | Đạt | Có README mô tả chức năng, yêu cầu môi trường, chạy máy chủ tĩnh và Docker. Cần thực hiện theo hướng dẫn để xác nhận tính chính xác. |
| Tài liệu phiên bản và nhật ký thay đổi | Đạt | Có `docs/RELEASENOTE.md` và `docs/AI_LOG.md`; cần cập nhật nếu có thay đổi mới trước bàn giao. |
| Kiểm tra chất lượng HTML/CSS và lỗi liên kết | Cần cải thiện | Chưa có kết quả lint/validator hoặc kiểm tra liên kết; liên kết GitHub/TikTok đang dùng placeholder `#`. |

### 3.6. Khả năng triển khai, kiểm thử và cung cấp minh chứng

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Triển khai theo hướng dẫn trong README | Cần cải thiện | Có hướng dẫn chạy bằng Python và Docker; chưa ghi nhận kết quả thực thi trên môi trường bàn giao. |
| Kiểm thử khói sau triển khai | Cần cải thiện | Chưa có checklist kết quả xác nhận trang chủ, điều hướng, email, ảnh và liên kết ngoài sau khi triển khai. |
| Minh chứng kiểm thử | Cần cải thiện | Thư mục `docs/sreenshots` hiện chưa có tệp minh chứng; chưa có log hoặc ảnh kết quả kiểm thử được đính kèm. |
| Truy vết lỗi và kiểm thử lại | Cần cải thiện | Chưa có danh sách lỗi, mức độ ưu tiên, người xử lý và kết quả kiểm thử lại. |

## 4. Đánh giá tổng kết và đề xuất

### Nhận định chung

> Sản phẩm có phạm vi phù hợp với một website CV tĩnh và đã có cấu trúc nội dung, CSS responsive cùng hướng dẫn chạy cơ bản. Tuy nhiên, đây mới là đánh giá sơ bộ từ mã nguồn/tài liệu, chưa có bằng chứng kiểm thử runtime. Đã xác nhận ít nhất một lỗi chức năng: liên kết GitHub và TikTok ở phần Liên hệ chưa trỏ đến URL thật.

**Kết luận:** Chưa khuyến nghị phê duyệt bàn giao ở thời điểm lập báo cáo. Cần xử lý liên kết chưa đạt, chạy kiểm thử trên trình duyệt và môi trường triển khai dự kiến, sau đó cập nhật trạng thái cùng minh chứng thực tế.

### Đề xuất trước khi bàn giao

1. Thay `href="#"` của GitHub và TikTok bằng URL chính xác; kiểm tra mở đúng trang đích.
2. Kiểm tra các luồng chính: điều hướng giữa các mục, nút CTA, email, liên kết dự án và tải ảnh.
3. Kiểm tra giao diện ở các viewport di động, máy tính bảng và máy tính để bàn; thử ít nhất các trình duyệt mục tiêu đã nêu trong README.
4. Chạy website bằng máy chủ tĩnh và Docker theo README; lưu kết quả truy cập, lỗi console/network và các vấn đề phát sinh.
5. Rà soát tương phản, thao tác bàn phím, đường dẫn/tài nguyên và nội dung cá nhân được công khai.
6. Lưu ảnh chụp màn hình, log chạy thử và danh sách lỗi đã xử lý vào thư mục minh chứng; cập nhật báo cáo sau khi kiểm thử lại.

## 5. Phê duyệt

| Vai trò | Họ tên | Kết quả | Ngày | Xác nhận |
|---|---|---|---|---|
| Người kiểm thử | Chưa ghi nhận | Chờ kiểm thử runtime |  |  |
| Người phụ trách sản phẩm |  | Chờ xem xét |  |  |
| Người phê duyệt bàn giao |  | Chưa phê duyệt |  |  |
