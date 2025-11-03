Chuẩn bài luôn 😎 — bạn đang làm rất “chuẩn repo chuyên nghiệp”!
Vậy ta sẽ **thêm mục “🧾 Lịch sử phiên bản (Changelog)”** ngay đầu file `AUDIO_TOOL.md`, liệt kê các thay đổi qua từng phiên bản (bảng timeline nhỏ gọn như changelog GitHub).

Dưới đây là bản cập nhật **hoàn chỉnh**, có sẵn bảng version history 👇

---

# 🎧 AUDIO TOOL — Modern Glow Player

> **Ngôn ngữ:** HTML / CSS / JavaScript thuần
> **Tác giả:** Web Utils Project
> **Trạng thái:** Đang phát triển

---

## 🧾 Lịch sử phiên bản (Changelog)

| Phiên bản | Ngày cập nhật | Mô tả thay đổi                                                                                                                                               |
| --------- | ------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **1.1**   | 04/11/2025    | ✨ Thêm tùy chỉnh **tốc độ phát (Playback Speed)** bằng thanh trượt và dropdown đồng bộ. <br> 🎨 Cải thiện CSS, tách style sang file riêng `audio-style.css`. |
| **1.0**   | 28/10/2025    | 🚀 Ra mắt phiên bản đầu tiên: phát nhạc từ **URL hoặc file**, có **Play / Pause / Stop / Tua** và **phím tắt điều khiển**.                                   |

---

## 🧩 1. Giới thiệu

**Audio Tool** là công cụ phát nhạc hiện đại được xây dựng bằng **HTML, CSS, JavaScript thuần**.
Giao diện theo phong cách **Glassmorphism + Glow UI**, tạo cảm giác mềm mại và tương lai.

Ứng dụng cho phép:

* Phát nhạc từ **file nội bộ** hoặc **URL trực tuyến**
* **Điều khiển phát lại** (Play / Pause / Stop / Tua)
* Hiển thị **thời gian và tiến trình phát nhạc**
* **Tùy chỉnh tốc độ phát (Playback rate)**
* **Tương tác bằng chuột hoặc phím tắt**

---

## ⚙️ 2. Chức năng chi tiết

### 🎵 2.1. Nguồn nhạc

* **Tùy chọn 1:** Dán **URL** âm thanh → nhấn **Load** để phát.
* **Tùy chọn 2:** Nhấn **Chọn file** → tải file `.mp3`, `.wav`, `.ogg`...

> Khi tải thành công, nhạc tự động phát.

---

### ⏯ 2.2. Điều khiển phát lại

| Nút    | Biểu tượng | Chức năng                   |
| ------ | ---------- | --------------------------- |
| ⏪      | rew5       | Tua ngược **5 giây**        |
| ▶ / ❚❚ | play       | **Phát / Tạm dừng**         |
| ⏩      | fwd5       | Tua nhanh **5 giây**        |
| ⏹      | stop       | Dừng phát, đưa về **00:00** |

---

### 🕒 2.3. Hiển thị thời gian

* Hiển thị **thời gian hiện tại / tổng thời lượng** (vd: `00:42 / 03:27`)
* Cập nhật **real-time** khi phát
* Khi phát xong → trở lại **00:00**

---

### 📈 2.4. Thanh tiến trình

* Thanh phát sáng **xanh lam neon** hiển thị tiến độ
* Có thể **click hoặc kéo** để tua
* Tự động đồng bộ với âm thanh

---

### ⏩ 2.5. Tốc độ phát (NEW in v1.1)

* Cho phép thay đổi tốc độ từ **0.25× đến 2×** bằng:

  * **Thanh trượt (range)** để điều chỉnh mượt
  * **Danh sách chọn (dropdown)** để chọn nhanh
* Hai thành phần đồng bộ với nhau — thay đổi một cái, cái kia cập nhật ngay.

> 🎯 Hữu ích cho việc **nghe học ngoại ngữ** hoặc **tua nhanh nội dung**.

---

### ⌨️ 2.6. Phím tắt

| Phím      | Hành động        |
| --------- | ---------------- |
| **Space** | Phát / Tạm dừng  |
| **←**     | Tua lùi 5 giây   |
| **→**     | Tua nhanh 5 giây |
| **S**     | Dừng phát        |

> Bị vô hiệu khi đang nhập trong ô URL.

---

### 💡 2.7. Trạng thái hiển thị

* Nút **Play/Pause** tự động đổi icon
* Tiến trình, thời gian và tốc độ cập nhật **real-time**
* Khi bài nhạc kết thúc → reset về ban đầu

---

## 🎨 3. Giao diện (UI/UX)

* **Glassmorphism:** nền mờ, viền sáng nhẹ
* **Glow Effect:** ánh sáng neon xanh `#38bdf8`
* **Responsive:** tự co giãn trên màn hình nhỏ, ẩn bớt thông tin khi <520px
* **Layout:** gọn gàng, cân đối, trực quan

---

## 📁 4. Cấu trúc file

```
audio-tool/
│
├── audio-tool.html       # File chính (HTML + JS)
├── audio-style.css        # File CSS (Glassmorphism + Glow)
└── AUDIO_TOOL.md          # File mô tả & changelog
```

---

## 🔮 5. Hướng phát triển

* [ ] Equalizer hiển thị sóng âm (Visualizer)
* [ ] Hỗ trợ Playlist (nhiều bài nhạc liên tiếp)
* [x] Điều chỉnh tốc độ phát (hoàn thành v1.1)
* [ ] Lưu lịch sử bài hát (LocalStorage)
* [ ] Thêm chế độ Dark / Light

---

