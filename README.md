# DHMT - Mô Phỏng Hệ Mặt Trời và Hệ Thống Đất-Mặt Trăng

Dự án này là một ứng dụng trực quan hóa 3D mô phỏng hệ mặt trời và chuyển động của Trái Đất, Mặt Trăng, và Mặt Trời bằng OpenGL.

## Mô Tả

Dự án bao gồm hai ứng dụng chính:

- **SolarSystem.py**: Mô phỏng toàn bộ hệ mặt trời với 9 hành tinh (Thủy, Kim, Trái Đất, Sao Hỏa, Mộc, Thổ, Thiên Vương, Hải Vương, Sao Diêm Vương) kèm theo các chuyển động quanh quỹ đạo và tự quay.

- **EarthMoonSun.py**: Mô phỏng đơn giản hệ thống Đất-Mặt Trăng-Mặt Trời với chuyển động chi tiết của Trái Đất quay quanh Mặt Trời và Mặt Trăng quay quanh Trái Đất.

## Tính Năng

✨ **Các tính năng chính:**

- Hình ảnh 3D được kết xuất bằng OpenGL
- Hỗ trợ texture cho các hành tinh
- Điều khiển camera tương tác (xoay, phóng to/thu nhỏ)
- Giao diện imgui cho tương tác người dùng
- Hiệu ứng ánh sáng động (ambient và diffuse lighting)
- Skybox để tạo không gian lập thể

## Yêu Cầu Hệ Thống

- Python 3.8+
- Windows/Linux/macOS

## Cài Đặt

1. **Clone hoặc tải về dự án:**
   ```bash
   git clone <repository-url>
   cd DHMT-main
   ```

2. **Cài đặt các thư viện cần thiết:**
   ```bash
   pip install -r requirements.txt
   ```

   Các thư viện được sử dụng:
   - `pygame`: Xử lý cửa sổ và input
   - `PyOpenGL`: Render 3D graphics
   - `PyOpenGL_accelerate`: Tăng tốc độ PyOpenGL
   - `pillow`: Xử lý hình ảnh (texture)
   - `imgui`: Giao diện người dùng

3. **Đảm bảo thư mục `TexImg/` chứa các texture cần thiết cho các hành tinh**

## Cách Sử Dụng

### Chạy mô phỏng hệ mặt trời:
```bash
python SolarSystem.py
```

### Chạy mô phỏng hệ Đất-Mặt Trăng-Mặt Trời:
```bash
python EarthMoonSun.py
```

## Điều Khiển

### Điều khiển camera:
- **Chuột**: Kéo để xoay view
- **Cuộn chuột**: Phóng to/thu nhỏ
- **W/A/S/D hoặc mũi tên**: Di chuyển camera
- **+/-**: Tăng/giảm tốc độ

### Tương tác trong ứng dụng:
- Giao diện imgui cho phép bật/tắt hiển thị các hành tinh
- Điều chỉnh tốc độ mô phỏng
- Theo dõi các hành tinh cụ thể

## Cấu Trúc Dự Án

```
DHMT-main/
├── SolarSystem.py           # Ứng dụng mô phỏng hệ mặt trời
├── EarthMoonSun.py          # Ứng dụng mô phỏng hệ Đất-Mặt Trăng-Mặt Trời
├── requirements.txt         # Danh sách thư viện cần thiết
├── TexImg/                  # Thư mục chứa texture hình ảnh
├── imgui.ini                # Cấu hình imgui
└── README.md                # File này
```

## Ghi Chú

- Khoảng cách và kích thước của các hành tinh được điều chỉnh cho mục đích trực quan hóa, không đại diện chính xác tỷ lệ thực tế.
- Dự án sử dụng các lực sáng ambient và diffuse để tạo hiệu ứng ánh sáng thực tế.
- Skybox được sử dụng để tạo nền không gian.

## Lỗi Thường Gặp

**ModuleNotFoundError**: Đảm bảo tất cả các package trong `requirements.txt` đã được cài đặt:
```bash
pip install -r requirements.txt
```

**Missing textures**: Kiểm tra xem thư mục `TexImg/` có chứa các file texture cần thiết hay không.
