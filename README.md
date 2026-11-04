# CV cá nhân - Chu Việt Anh

## Giới thiệu

Trang CV/portfolio cá nhân giới thiệu Chu Việt Anh, sinh viên Đại học Đại Nam. Trang trình bày thông tin giới thiệu, kỹ năng, một số dự án tiêu biểu và cách liên hệ.

Đây là website tĩnh, phù hợp để xem trên máy tính và thiết bị di động. Dự án không có backend, cơ sở dữ liệu hay bước biên dịch.

## Chức năng

- Điều hướng nhanh đến các phần Giới thiệu, Kỹ năng, Dự án và Liên hệ.
- Hiển thị thông tin cá nhân và ảnh đại diện.
- Giới thiệu các kỹ năng HTML5, Ruby, JavaScript, C#, C++ và GDScript.
- Trình bày các dự án liên quan đến RPG Maker, Unity, Unreal Engine và Godot.
- Cung cấp email và các kênh mạng xã hội để liên hệ.
- Bố cục responsive, hỗ trợ màn hình nhỏ, máy tính bảng và máy tính để bàn.

## Công nghệ

- HTML5: cấu trúc và nội dung trang.
- CSS3: giao diện, Flexbox, CSS Grid và bố cục responsive.
- Nginx (tùy chọn): phục vụ website khi chạy bằng Docker.

## Yêu cầu môi trường

Để xem trang trực tiếp, cần một trình duyệt hiện đại như Chrome, Firefox, Edge hoặc Safari. Không cần cài Node.js, npm hay cơ sở dữ liệu.

Để chạy bằng máy chủ cục bộ, cần Python 3. Để chạy bằng Docker, cần cài Docker Desktop (Windows/macOS) hoặc Docker Engine (Linux).

## Cài đặt

Tải hoặc sao chép dự án về máy, sau đó mở thư mục `My-CV`. Cấu trúc cần có:

```text
My-CV/
├── index.html
├── README.md
└── assets/
	├── css/
	│   └── styles.css
	└── img/
		└── Steve_(Minecraft).png
```

Không cần cài thêm thư viện hay chạy lệnh build.

## Cấu hình và tùy chỉnh

- Nội dung, tiêu đề trang, thông tin kỹ năng, dự án và liên hệ nằm trong `index.html`.
- Giao diện, màu sắc và bố cục nằm trong `assets/css/styles.css`.
- Ảnh đại diện hiện được tham chiếu tại `assets/img/Steve_(Minecraft).png`. Khi thay ảnh, cập nhật đường dẫn `src` trong `index.html`.
- Một số ảnh minh họa dự án được tải từ các website bên ngoài; cần kết nối Internet để hiển thị các ảnh này.
- Dự án hiện không sử dụng tệp cấu hình môi trường hoặc thông tin bí mật.

## Chạy thử

### Windows

Mở PowerShell tại thư mục dự án và chạy máy chủ tĩnh bằng Python:

```powershell
py -m http.server 8000
```

Mở <http://localhost:8000> trong trình duyệt. Nếu lệnh `py` không có trên máy, cài Python 3 hoặc mở trực tiếp `index.html` bằng trình duyệt.

### macOS

Mở Terminal, chuyển đến thư mục dự án rồi chạy:

```bash
cd /duong-dan/toi/My-CV
python3 -m http.server 8000
```

Mở <http://localhost:8000> trong trình duyệt. Có thể mở trực tiếp `index.html` nếu không muốn chạy máy chủ cục bộ.

### Linux

Mở Terminal, chuyển đến thư mục dự án rồi chạy:

```bash
cd /duong-dan/toi/My-CV
python3 -m http.server 8000
```

Mở <http://localhost:8000> trong trình duyệt. Có thể mở trực tiếp `index.html` nếu không muốn chạy máy chủ cục bộ.

> **Lưu ý:** Thay `/duong-dan/toi/My-CV` bằng đường dẫn thực tế đến thư mục dự án. Nhấn `Ctrl+C` trong cửa sổ terminal để dừng máy chủ Python.

## Chạy bằng Docker

Cần Docker đang hoạt động. Các lệnh bên dưới dùng Nginx để phục vụ thư mục dự án, không cần tạo image riêng.

### Windows (PowerShell)

Chạy tại thư mục dự án:

```powershell
docker run --rm -d --name my-cv -p 8080:80 -v "${PWD}:/usr/share/nginx/html:ro" nginx:alpine
```

### macOS và Linux

Chạy tại thư mục dự án:

```bash
docker run --rm -d --name my-cv -p 8080:80 -v "$PWD:/usr/share/nginx/html:ro" nginx:alpine
```

Sau khi container khởi động, mở <http://localhost:8080>. Dừng website bằng lệnh:

```bash
docker stop my-cv
```

Nếu cổng `8080` đang được sử dụng, đổi phần `8080:80` thành một cổng trống khác, ví dụ `8081:80`, rồi mở cổng tương ứng trên trình duyệt.

## Thông tin liên hệ

- **Tác giả:** Chu Việt Anh
- **Email:** [anhc6138@gmail.com](mailto:anhc6138@gmail.com)
- **GitHub:** [github.com/AnhChuCVA](https://github.com/AnhChuCVA)
- **TikTok:** [@anhchu3045](https://www.tiktok.com/@anhchu3045)
