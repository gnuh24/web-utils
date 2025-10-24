# 🧪 API Tester Pro - Phiên bản 1.0

**API Tester Pro** là một công cụ HTML tĩnh gọn nhẹ giúp bạn **kiểm thử nhanh các API** mà không cần Postman hay cài đặt thêm phần mềm nào khác.  
Chỉ cần mở file `.html` bằng trình duyệt là có thể gửi request, thêm JWT token, test CORS, và lưu lịch sử các lần gọi API.

---

## 🚀 Tính năng chính

### 1️⃣ Gửi yêu cầu API nhanh chóng
- Hỗ trợ đầy đủ các **HTTP methods**: `GET`, `POST`, `PUT`, `DELETE`, `PATCH`.
- Cho phép nhập **URL API** trực tiếp và gửi yêu cầu chỉ bằng một cú nhấp chuột.
- Hiển thị **trạng thái phản hồi**, **headers**, và **body** dưới dạng có thể đọc được.

---

### 2️⃣ Hỗ trợ JWT Token
- Nhập token thủ công trong trường `JWT Token`.
- Tự động thêm header `Authorization: Bearer <token>` khi gửi request.
- Giúp bạn dễ dàng test các endpoint yêu cầu xác thực.

---

### 3️⃣ Gửi Body JSON linh hoạt
- Cho phép nhập body JSON trực tiếp.
- Tự động thêm header `Content-Type: application/json`.
- Có kiểm tra và thông báo lỗi nếu body JSON sai cú pháp.

---

### 4️⃣ Quản lý lịch sử API
- Tự động lưu lại **10 lần request gần nhất** bao gồm:
  - URL
  - Method
  - JWT Token (nếu có)
  - Body
  - Thời gian thực hiện
- Có thể **tải xuống toàn bộ lịch sử** dưới dạng file `api-test-history.json`.
- Nhấn nút 🔁 để **nạp lại một request cũ** vào form và gửi lại.

---

### 5️⃣ Giao diện thân thiện
- Thiết kế nhẹ, dễ đọc, sử dụng font hiện đại.
- Có đánh dấu màu cho trạng thái phản hồi:
  - 🟢 **Màu xanh lá:** Request thành công (`2xx`)
  - 🔴 **Màu đỏ:** Request lỗi hoặc thất bại (`4xx`, `5xx`)
- Toàn bộ dữ liệu lưu trong **localStorage** của trình duyệt.

---

### 6️⃣ Tải file log & khôi phục
- Cho phép tải file log (`api-test-history.json`) để lưu trữ thủ công.
- Lưu trữ này **không bị mất khi reset project**, chỉ mất khi xóa cache trình duyệt.
- (Phiên bản 1.1 sắp tới sẽ hỗ trợ **Import lại file log** để khôi phục lịch sử.)

---

### 7️⃣ Xử lý lỗi chi tiết
Công cụ có thể hiển thị rõ loại lỗi gặp phải:
- `TypeError`: Lỗi mạng hoặc **CORS bị chặn**
- `SyntaxError`: **Body JSON sai cú pháp**
- `Failed to fetch`: Server không phản hồi hoặc HTTPS/CORS lỗi
- Các lỗi khác sẽ hiển thị **stack trace** đầy đủ để debug.

---

## 📂 Lưu ý

| Thành phần | Nơi lưu trữ | Mất khi reset project? | Mất khi xóa cache trình duyệt? |
|-------------|--------------|------------------------|--------------------------------|
| **Lịch sử API** | `localStorage` (trình duyệt) | ❌ Không | ✅ Có |
| **File log tải về** | Máy tính người dùng (`Downloads/`) | ❌ Không | ❌ Không |

---

## 🧰 Cách sử dụng

1. Tải file `quick-call-api.html`.
2. Mở bằng trình duyệt (Chrome, Edge, Firefox đều được).
3. Nhập URL API → chọn phương thức → (tùy chọn) nhập Token hoặc Body.
4. Nhấn **🚀 Gửi yêu cầu** để xem kết quả.
5. Dùng **💾 Tải log** để lưu lại các lần test quan trọng.

---

## 🧩 Phiên bản

| Phiên bản | Mô tả | Ngày phát hành |
|------------|--------|----------------|
| **1.0.0** | Phiên bản đầu tiên — Gửi API, lưu lịch sử, hỗ trợ JWT & CORS test | 24/10/2025 |

---

## 🔮 Dự kiến ở bản 1.1
- Thêm nút **📂 Import Log** để nạp lại file `api-test-history.json`.
- Cho phép **xuất riêng từng request**.
- Tùy chọn **theme tối / sáng**.
- Tự động phát hiện `Content-Type` và format body đẹp hơn.

---

> © 2025 — Developed by **THug24**  
> Lightweight tool for quick API testing and CORS debugging.
