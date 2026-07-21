# Landing page – Máy trị liệu sóng ánh sáng Terahertz

Trang giới thiệu và bán sỉ máy trị liệu sóng ánh sáng Terahertz cho **spa dưỡng sinh Đông Y**.

**Liên hệ:** Mr Sáng – 0981 933 233 · https://zalo.me/0981933233

---

## Cấu trúc

| File | Vai trò |
|---|---|
| `index.html` | Toàn bộ landing page (HTML + CSS trong một file, không phụ thuộc thư viện ngoài) |
| `render.yaml` | Cấu hình deploy static site lên Render |
| `.gitignore` | Chặn tài liệu nội bộ lọt lên repo công khai |

Font lấy từ Google Fonts (Playfair Display + Be Vietnam Pro), đồng bộ với dự án `thamdatrilieu` (JM365).

### Bảng màu

| Biến | Mã | Dùng cho |
|---|---|---|
| `--cream` | `#faf5ea` | Nền trang |
| `--cream-soft` | `#f2e9d8` | Nền section xen kẽ |
| `--burgundy` | `#6e1423` | Tiêu đề, nút, hero |
| `--gold` | `#b8892b` | Chữ eyebrow, viền nhấn |
| `--ink` | `#2c1e14` | Chữ nội dung, footer |

---

## Sửa nội dung

Mọi thứ nằm trong `index.html`. Các mốc cần thay khi có dữ liệu thật:

- `[ẢNH SẢN PHẨM – máy Terahertz thân đỏ/trắng]` — thay bằng `<img>` ảnh thật
- `[Tên chủ spa]`, `[Tên]`, `[Tỉnh/TP]` trong phần cảm nhận khách hàng
- Form đăng ký hiện chỉ hiện thông báo cảm ơn, **chưa lưu lead**. Xem mục dưới.

---

## Deploy lên Render

1. Push code lên nhánh `main` của repo này.
2. Trên [Render](https://dashboard.render.com) → **New** → **Static Site** → chọn repo `terahertz`.
3. Render tự đọc `render.yaml`. Nếu phải điền tay: **Publish directory** = `.`, **Build command** để trống.
4. Mỗi lần push lên `main`, Render tự build lại (khoảng 1–2 phút).

---

## Lưu ý về lead khách hàng

Hiện form chỉ hiển thị thông báo cảm ơn ở trình duyệt, **dữ liệu không được gửi đi đâu cả**. Khách vẫn liên hệ được qua nút Zalo và nút Gọi.

Nếu cần lưu lead như dự án `thamdatrilieu`, phải chuyển từ static site sang web service Node/Express (backend lưu lead + trang `/admin` + gửi email báo qua Resend).

---

## Khuyến cáo nội dung

Toàn bộ câu chữ trên trang đã được viết theo hướng **không quảng cáo chữa bệnh**. Sản phẩm là thiết bị chăm sóc sức khoẻ, hỗ trợ thư giãn và làm ấm — không phải thuốc, không thay thế chẩn đoán và điều trị y khoa.

Khi sửa nội dung, **giữ nguyên nguyên tắc này**. Quảng cáo sản phẩm không phải thuốc mà gây hiểu nhầm có tác dụng chữa bệnh bị xử phạt theo Nghị định 38/2021 (30–40 triệu đồng).
