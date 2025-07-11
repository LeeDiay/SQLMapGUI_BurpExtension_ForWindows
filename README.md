# 🛠 SQLMap GUI - Tiện ích mở rộng cho Burp Suite (Windows)

**SQLMap GUI** là một tiện ích mở rộng tích hợp SQLMap vào Burp Suite, cho phép bạn thực hiện kiểm tra SQL Injection trực tiếp từ các request trong Burp thông qua giao diện đồ họa dễ sử dụng.

---

## 🚀 Tính năng chính

- 🖱 Chuột phải vào request → **Send to SQLMap**
- ⚙️ Cấu hình tham số SQLMap qua giao diện GUI (vd: `--risk`, `--level`, `--dbs`, `--dump`, `--tamper`, ...)
- 🔍 Xem kết quả đầu ra thời gian thực với phân loại màu sắc (Thông tin / Cảnh báo / Lỗi)
- 💾 Tự động lưu các request thành file `.req` trong thư mục tạm
- ⛔ Cho phép dừng tiến trình SQLMap bất cứ lúc nào

---

## 🧰 Yêu cầu hệ thống

- **Burp Suite** (Community hoặc Pro)
- **Jython 2.7.x** (dùng để chạy extension Python trong Burp)
- **SQLMap** (tải từ: [https://github.com/sqlmapproject/sqlmap](https://github.com/sqlmapproject/sqlmap))
- Hệ điều hành: **Windows**

---

## ⚙️ Hướng dẫn cài đặt

### 1. Cài SQLMap

Tải và giải nén SQLMap từ GitHub:  
👉 [https://github.com/sqlmapproject/sqlmap](https://github.com/sqlmapproject/sqlmap)

### 2. Cài Jython

Tải Jython `standalone`:  
👉 [https://www.jython.org/download](https://www.jython.org/download)

> ⚠️ Khuyên dùng `jython-standalone-2.7.x.jar`

### 3. Cấu hình trong Burp

1. Vào **Extender → Options**
2. Trong phần **Python Environment**, chọn đường dẫn tới file `jython-standalone-2.7.x.jar`

### 4. Thêm extension

1. Vào **Extender → Extensions → Add**
2. Chọn:
   - **Extension type**: `Python`
   - **Extension file**: trỏ đến file `SQLGui.py`

---

## 🧪 Cách sử dụng

1. Chặn một request có thể bị SQL Injection trong Burp.
2. Chuột phải vào request → chọn **Send to SQLMap**.
3. Chuyển sang tab **SQLMap GUI**.
4. Chọn request đã lưu, tick các tham số cần sử dụng.
5. Nhấn **Run SQLMap** để bắt đầu quét.
6. Theo dõi kết quả ở bảng log bên phải.

---

## 📝 Ghi chú

- Mặc định đường dẫn SQLMap trong mã là:
`D:\Tool\sqlmap-master\sqlmap-master\sqlmap.py`
> ✏️ Bạn có thể sửa trong file `SQLGui.py` nếu SQLMap của bạn ở nơi khác.
---

## 👨‍💻 Tác giả

- **Lê Đức Anh**
- Mục đích: Tạo công cụ hỗ trợ pentest nhanh gọn và trực quan ngay trong Burp Suite

---

## 📬 Liên hệ & Góp ý

Nếu gặp lỗi hoặc muốn cải tiến công cụ, hãy tạo issue hoặc liên hệ trực tiếp. Chúc bạn pentest vui vẻ! 😎
