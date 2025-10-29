Dưới đây là file **`AUDIO_TOOL.md`** mô tả chức năng đầy đủ cho giao diện **Audio Tool — Modern Glow Player** mà bạn đang phát triển:

---

# 🎧 AUDIO TOOL — Modern Glow Player

## 🧩 1. Giới thiệu

**Audio Tool** là một công cụ phát nhạc hiện đại được xây dựng hoàn toàn bằng **HTML, CSS và JavaScript thuần**.
Giao diện được thiết kế theo phong cách **Glassmorphism & Glow UI**, mang lại cảm giác tương lai, mềm mại và trực quan.

Ứng dụng cho phép:

* Phát nhạc từ **file nội bộ** hoặc **URL trực tuyến**
* **Điều khiển phát lại** (Play/Pause, Stop, Tua nhanh/chậm)
* **Hiển thị thời gian & tiến trình phát nhạc**
* **Tương tác trực tiếp bằng chuột hoặc phím tắt**

---

## ⚙️ 2. Chức năng chi tiết

### 🎵 2.1. Nguồn nhạc

* **Tùy chọn 1:** Dán **URL** của file âm thanh vào ô nhập → Nhấn **Load** để tải.
* **Tùy chọn 2:** Nhấn **Chọn file** → Chọn file `.mp3`, `.wav`, `.ogg`, v.v. từ máy tính.

> Khi file được tải, trình phát tự động bắt đầu phát nhạc.

---

### ⏯ 2.2. Điều khiển phát lại

| Nút    | Biểu tượng | Chức năng                               |
| ------ | ---------- | --------------------------------------- |
| ⏪      | `rew5`     | Tua ngược **5 giây**                    |
| ▶ / ❚❚ | `play`     | **Phát / Tạm dừng**                     |
| ⏩      | `fwd5`     | Tua nhanh **5 giây**                    |
| ⏹      | `stop`     | Dừng phát và đưa về thời gian **00:00** |

---

### 🕒 2.3. Hiển thị thời gian

* Phía dưới các nút điều khiển hiển thị:

  ```
  00:00 / 03:42
  ```

  → biểu thị **thời gian hiện tại / tổng thời gian bài hát**.
* Tự động cập nhật theo tiến trình phát nhạc.

---

### 📈 2.4. Thanh tiến trình

* Thanh phát sáng màu **xanh lam neon** thể hiện tiến trình phát nhạc.
* Có thể **click** vào thanh để tua đến vị trí mong muốn.
* Ngoài ra còn có **slider range** giúp tua chính xác hơn.

---

### ⌨️ 2.5. Phím tắt

| Phím      | Hành động        |
| --------- | ---------------- |
| **Space** | Phát / Tạm dừng  |
| **←**     | Tua lùi 5 giây   |
| **→**     | Tua nhanh 5 giây |
| **S**     | Dừng phát        |

> Các phím tắt bị vô hiệu khi đang nhập văn bản trong ô URL.

---

### 💡 2.6. Trạng thái hiển thị

* Nút **Play** tự động đổi biểu tượng khi phát hoặc tạm dừng.
* Tiến trình và thời gian được cập nhật **real-time**.
* Khi phát xong bài nhạc → nút chuyển lại thành **▶**.

---

## 🎨 3. Giao diện (UI/UX)

* **Hiệu ứng Glassmorphism:**

  * Nền mờ (`backdrop-filter: blur(18px)`)
  * Viền sáng mờ & đổ bóng nhẹ.
* **Hiệu ứng Glow:**

  * Nút bấm và thanh tiến trình có ánh sáng xanh (`#38bdf8`) khi hover.
* **Tương thích mobile:**

  * Tự động ẩn phần hiển thị thời gian khi màn hình nhỏ (<520px).
  * Giao diện co giãn linh hoạt (`width: min(700px, 94%)`).

---

## 🧠 4. Kịch bản hoạt động

1. Người dùng chọn nguồn (URL hoặc file).
2. Âm thanh được tải và phát.
3. Giao diện cập nhật tiến trình và thời gian.
4. Người dùng có thể:

   * Dừng / tua / phát / pause
   * Click hoặc kéo thanh tua
   * Sử dụng phím tắt để điều khiển
5. Khi nhạc kết thúc → tiến trình về 0%.

---

## 📁 5. Cấu trúc file

```
audio-tool/
│
├── audio-tool.html      # File chính chứa toàn bộ mã HTML + CSS + JS
├── description.md        # File mô tả chức năng (hiện tại)
└── assets/              # (Tùy chọn) Lưu nhạc mẫu hoặc icon
```

---

## 🔮 6. Hướng phát triển trong tương lai

* Thêm **Equalizer hiển thị sóng âm (visualizer)**.
* Hỗ trợ **Playlist** (nhiều bài nhạc).
* Tùy chỉnh **tốc độ phát (Playback rate)**.
* Lưu lại bài hát đã phát gần đây (LocalStorage).

---

Bạn có muốn tôi **tạo sẵn file `AUDIO_TOOL.md` để tải về** (dạng `.md`) không?
Nếu đồng ý, tôi sẽ xuất file Markdown hoàn chỉnh cho bạn.
