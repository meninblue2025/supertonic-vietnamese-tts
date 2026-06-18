# noi.py — Supertonic TTS tiếng Việt

Chạy Supertonic TTS hoàn toàn offline trên máy tính.  
10 giọng tiếng Việt (5 nữ, 5 nam), không cần internet sau khi cài xong.  
File audio tự lưu vào Desktop sau khi chạy.

📖 Xem hướng dẫn đầy đủ + nghe thử giọng mẫu:  
https://kaitago.com/2026/06/15/mk-so-003-tts-tieng-viet-doc-audio/

---

## Yêu cầu

- Python 3.8 trở lên
- Internet lần chạy đầu tiên (tự tải model ~vài trăm MB từ Hugging Face)
- Sau đó: chạy offline hoàn toàn, không cần mạng

---

## Bước 1 — Cài đặt (một lần duy nhất)

Mở Terminal (Mac) hoặc Command Prompt (Windows), chạy:

```bash
pip install supertonic
```

---

## Bước 2 — Tải file và chỉnh nội dung

1. Tải `noi.py` về máy
2. Mở bằng bất kỳ text editor nào (Notepad, TextEdit, VS Code...)
3. Tìm và sửa 3 dòng được đánh dấu rõ trong file:

**`VAN_BAN`** — đoạn văn bản bạn muốn đọc, thay vào giữa dấu `"""`

**`GIONG`** — chọn một trong 10 giọng:

| Giọng | Loại |
|-------|------|
| F1, F2, F3, F4, F5 | Nữ |
| M1, M2, M3, M4, M5 | Nam |

**`TOC_DO`** — tốc độ đọc:

| Giá trị | Tốc độ |
|---------|--------|
| 0.7 | Chậm |
| 1.0 | Bình thường |
| 1.3 | Nhanh |
| 1.6 | Rất nhanh |
| 2.0 | Tối đa |

4. Lưu file lại

---

## Bước 3 — Chạy

Mở Terminal (Mac) hoặc Command Prompt (Windows):

```bash
cd đường/dẫn/đến/thư-mục-chứa-noi.py
python3 noi.py
```

> Windows dùng `python` thay vì `python3`

File `.wav` tự lưu vào Desktop với tên dạng `Test_F3_1.6x_143022.wav`  
và tự mở để nghe ngay sau khi tổng hợp xong.

---

## Câu hỏi thường gặp

**Lần đầu chạy lâu và cần internet — bình thường không?**  
Bình thường. Lần đầu tự tải model Supertonic từ Hugging Face (~vài trăm MB).  
Từ lần 2 trở đi chạy offline, nhanh hơn nhiều.

**Báo lỗi `ModuleNotFoundError: No module named 'supertonic'`?**  
Chưa cài hoặc cài nhầm môi trường. Chạy lại: `pip install supertonic`

**File .wav lưu ở đâu?**  
Tự động lưu vào Desktop của bạn.

**Đổi giọng thì phải làm gì?**  
Mở lại `noi.py`, sửa dòng `GIONG = "F3"` thành giọng khác (F1–F5 hoặc M1–M5), lưu, chạy lại.

**Chạy được trên Windows không?**  
Có. Thay `python3` bằng `python` khi chạy lệnh là xong.

---

## Liên hệ

Hỏi thêm hoặc báo lỗi: để lại comment tại bài viết gốc  
https://kaitago.com/2026/06/15/mk-so-003-tts-tieng-viet-doc-audio/
