Tuyệt vời 😎 Dưới đây là bản **`QR Tool - Version 1.0.md`** được viết theo cùng phong cách với `API Tester Pro`, giúp bạn có file mô tả chính thức cho phiên bản đầu tiên của công cụ QR Code nhé:

---

# 📷 QR Tool — Phiên bản 1.0

**QR Tool** là một công cụ HTML tĩnh giúp bạn **quét, giải mã, và tạo mã QR nhanh chóng** ngay trên trình duyệt.
Không cần cài đặt phần mềm — chỉ cần mở file `.html` là có thể sử dụng trực tiếp.

---

## 🚀 Tính năng chính

### 1️⃣ Quét QR trực tiếp từ webcam

* Sử dụng **camera thiết bị (facingMode: environment)** để quét mã QR thời gian thực.
* Tự động hiển thị **nội dung giải mã** ngay khi phát hiện QR trong khung hình.
* Hỗ trợ **dừng / bật lại** quá trình quét bằng nút điều khiển.
* Không cần internet — toàn bộ xử lý được thực hiện **cục bộ trên trình duyệt**.

---

### 2️⃣ Giải mã ảnh chứa mã QR

* Cho phép **upload hình ảnh bất kỳ** (JPEG, PNG, v.v.) có chứa mã QR.
* Tự động nhận diện và giải mã nội dung.
* Nếu ảnh không có QR hợp lệ → hiển thị thông báo `❌ Không tìm thấy QR code.`
* Thích hợp cho việc **kiểm tra mã QR in sẵn hoặc ảnh chụp**.

---

### 3️⃣ Tạo mã QR Code từ nội dung tùy chọn

* Nhập nội dung bất kỳ (văn bản, URL, JSON, số điện thoại, v.v.).
* Nhấn nút **“Tạo QR”** để sinh ra hình ảnh mã QR tương ứng.
* Có thể **sao chép hoặc tải ảnh QR** để sử dụng cho in ấn, liên kết nhanh, v.v.
* Dùng thư viện `qrcodejs` để bảo đảm khả năng tương thích cao trên mọi trình duyệt.

---

### 4️⃣ Giao diện thân thiện, gọn nhẹ

* Xây dựng với **TailwindCSS** giúp bố cục trực quan và hiện đại.
* Giao diện gồm ba khối chức năng rõ ràng:

  1. Quét trực tiếp bằng webcam
  2. Upload ảnh để giải mã
  3. Tạo QR Code từ văn bản
* Giao diện phản hồi tốt (responsive) và hoạt động tốt trên **máy tính lẫn điện thoại**.

---

## 🧩 Công nghệ sử dụng

| Thành phần      | Mô tả                           | Phiên bản / Nguồn                       |
| --------------- | ------------------------------- | --------------------------------------- |
| **TailwindCSS** | Thiết kế giao diện nhanh, gọn   | CDN (latest)                            |
| **jsQR**        | Giải mã QR từ hình ảnh / webcam | v1.4.0                                  |
| **qrcodejs**    | Tạo mã QR                       | v1.0.0                                  |
| **WebRTC API**  | Truy cập webcam để quét mã      | `navigator.mediaDevices.getUserMedia()` |

---

## 🧰 Cách sử dụng

1. Tải file `qr-tool.html`.
2. Mở file bằng trình duyệt (Chrome, Edge, hoặc Firefox).
3. Sử dụng một trong ba tính năng:

   * **Quét QR từ webcam** → Bấm **“Bắt đầu”**.
   * **Giải mã ảnh** → Chọn ảnh QR từ máy.
   * **Tạo QR mới** → Nhập nội dung → Bấm **“Tạo QR”**.
4. Xem nội dung giải mã trong khung hiển thị (`<pre>`).

---

## ⚙️ Cấu trúc giao diện chính

| Thành phần  | Mô tả                                            |
| ----------- | ------------------------------------------------ |
| `video`     | Hiển thị luồng video từ webcam                   |
| `canvas`    | Dùng để phân tích hình ảnh QR từ video hoặc file |
| `result`    | Hiển thị kết quả giải mã                         |
| `fileInput` | Chọn ảnh QR từ thiết bị                          |
| `qrcode`    | Vùng hiển thị QR được tạo ra                     |

---

## 🔒 Bảo mật & Quyền riêng tư

* Mọi xử lý (giải mã / quét / tạo QR) đều diễn ra **hoàn toàn cục bộ**.
* **Không gửi bất kỳ dữ liệu nào ra ngoài** hoặc lưu trữ trên server.
* Người dùng có thể **tắt camera bất cứ lúc nào** bằng nút **“Dừng”**.

---

## 🧩 Phiên bản

| Phiên bản | Mô tả                                                                   | Ngày cập nhật |
| --------- | ----------------------------------------------------------------------- | ------------- |
| **1.0.0** | Phiên bản đầu tiên — Hỗ trợ quét QR webcam, giải mã ảnh, và tạo QR Code | 03/11/2025    |

---

## 🔮 Dự kiến ở bản 1.1

* Hỗ trợ **phân tích và quét Barcode (EAN, Code128, v.v.)**
* Cho phép **tải ảnh QR đã tạo** về máy.
* Tự động nhận diện **loại dữ liệu trong QR** (URL, Wi-Fi, vCard, JSON…).
* Thêm **chế độ theme tối / sáng** và lưu lựa chọn người dùng.
* Tối ưu hóa tốc độ quét cho thiết bị di động.

---

> © 2025 — Developed by **THug24**
> Lightweight QR utility for scanning, decoding, and generating codes directly in your browser.

---
