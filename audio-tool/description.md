Tuyệt vời 😎 đây là bản cập nhật mới của file `AUDIO_TOOL.md` — **đã bổ sung mục “Playlist (NEW in v1.2)”** và cập nhật changelog chuẩn bài GitHub style:

---

# 🎧 AUDIO TOOL — Modern Glow Player

> **Ngôn ngữ:** HTML / CSS / JavaScript thuần
> **Tác giả:** Web Utils Project
> **Trạng thái:** Đang phát triển

---

## 🧾 Lịch sử phiên bản (Changelog)

| Phiên bản | Ngày cập nhật | Mô tả thay đổi                                                                                                                                               |
| --------- | ------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **1.2**   | 07/11/2025    | 🧾 **Thêm Playlist** — hỗ trợ phát nhiều bài nhạc liên tiếp, tự động phát bài tiếp theo và cho phép chọn bài trực tiếp từ danh sách.                         |
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
* **Danh sách phát (Playlist)**
* **Phím tắt tiện dụng cho người dùng bàn phím**

---

## ⚙️ 2. Chức năng chi tiết

### 🎵 2.1. Nguồn nhạc

* **Tùy chọn 1:** Dán **URL** âm thanh → nhấn **Tải URL** để thêm vào danh sách.
* **Tùy chọn 2:** Nhấn **Chọn file** → tải 1 hoặc nhiều file `.mp3`, `.wav`, `.ogg`...

> Khi tải thành công, file tự động được thêm vào **Playlist** và phát bài đầu tiên.

---

### ⏯ 2.2. Điều khiển phát lại

| Nút    | Biểu tượng | Chức năng                   |
| ------ | ---------- | --------------------------- |
| Prev ⏮      | prevTrack  | Bài trước trong playlist    |
| -5s      | rew5       | Tua ngược **5 giây**        |
| ▶ / ❚❚ | play       | **Phát / Tạm dừng**         |
| +5s     | fwd5       | Tua nhanh **5 giây**        |
| Next ⏭      | nextTrack  | Bài tiếp theo               |
| ⏹      | stop       | Dừng phát, đưa về **00:00** |

---

### 🕒 2.3. Hiển thị thời gian

* Hiển thị **thời gian hiện tại / tổng thời lượng** (vd: `00:42 / 03:27`)
* Cập nhật **real-time** khi phát
* Khi phát xong → tự động sang bài kế tiếp (nếu có)

---

### 📈 2.4. Thanh tiến trình

* Thanh phát sáng **xanh lam neon** hiển thị tiến độ
* Có thể **click để tua** đến vị trí bất kỳ
* Tự động đồng bộ với âm thanh đang phát

---

### ⏩ 2.5. Tốc độ phát (v1.1)

* Cho phép thay đổi tốc độ từ **0.25× đến 2×** qua:

  * **Thanh trượt (range)** để điều chỉnh mượt
  * **Danh sách chọn (dropdown)** để chọn nhanh

> Hai thành phần này đồng bộ — thay đổi một, cái kia cập nhật ngay.

---

### 📜 2.6. Playlist (NEW in v1.2)

| Tính năng                     | Mô tả                                                                  |
| ----------------------------- | ---------------------------------------------------------------------- |
| ➕ **Thêm bài**                | Khi người dùng chọn file hoặc dán URL, bài hát được thêm vào danh sách |
| ▶ **Phát tự động**            | Sau khi bài hiện tại kết thúc → phát tiếp bài kế tiếp                  |
| 🖱 **Chọn bài thủ công**      | Người dùng có thể click vào bài trong danh sách để phát                |
| 🔁 **Vòng lặp**               | Khi đến cuối danh sách → tự động quay lại bài đầu tiên                 |
| ✨ **Highlight bài đang phát** | Bài đang phát được tô sáng bằng hiệu ứng `active glow`                 |

> 🎯 Playlist được thiết kế nhẹ, không phụ thuộc framework — dễ mở rộng thêm tính năng sau này.

---

### ⌨️ 2.7. Phím tắt

| Phím      | Hành động        |
| --------- | ---------------- |
| **Space** | Phát / Tạm dừng  |
| **←**     | Tua lùi 5 giây   |
| **→**     | Tua nhanh 5 giây |
| **S**     | Dừng phát        |

> Bị vô hiệu khi đang nhập trong ô URL.

---

### 💡 2.8. Trạng thái hiển thị

* Nút **Play/Pause** tự đổi icon
* Tiến trình, thời gian, tốc độ và playlist cập nhật **real-time**
* Khi bài hát kết thúc → chuyển bài tiếp theo hoặc quay lại đầu danh sách

---

## 🎨 3. Giao diện (UI/UX)

* **Glassmorphism:** nền mờ, viền sáng nhẹ
* **Glow Effect:** ánh sáng neon xanh `#38bdf8`
* **Responsive:** tự co giãn trên màn hình nhỏ
* **Bố cục:** cân đối, tập trung vào trải nghiệm người dùng

---

## 📁 4. Cấu trúc file

```
audio-tool/
│
├── audio-tool.html       # File chính (HTML + JS)
├── audio-style.css       # File CSS (Glassmorphism + Glow)
└── AUDIO_TOOL.md         # File mô tả & changelog
```

---

## 🔮 5. Hướng phát triển

* [ ] Equalizer hiển thị sóng âm (Visualizer)
* [x] Playlist (đã hoàn thành v1.2)
* [x] Điều chỉnh tốc độ phát (hoàn thành v1.1)
* [ ] Lưu lịch sử bài hát (LocalStorage)
* [ ] Thêm chế độ Dark / Light
* [ ] Giao diện Drag & Drop thêm bài vào playlist

---