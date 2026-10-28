# English Speaking Adventure 5

Website luyện nói tiếng Anh cho học sinh tiểu học (chương trình *Tiếng Anh Global Success*, lớp 5).
Dự án chỉ gồm **một file `index.html`** (HTML + CSS + JavaScript thuần): không cần cài đặt thư viện, không cần bước build, không dùng API key hay máy chủ.

## Cấu trúc

```
├── index.html   # Toàn bộ website (HTML + CSS + JavaScript trong một file)
├── .nojekyll    # Cho GitHub Pages phục vụ file nguyên trạng
└── README.md    # Hướng dẫn này
```

Website không dùng file hình ảnh hay âm thanh riêng: biểu tượng là emoji, giọng đọc dùng Web Speech API của trình duyệt.
Chỉ có **một tài nguyên bên ngoài**: phông chữ Google Fonts (Fredoka, Nunito). Nếu không có mạng, trang vẫn chạy và tự dùng phông chữ hệ thống.

## Chạy thử trên máy

**Cách 1 – mở trực tiếp:** nhấp đúp `index.html`. Phần lớn chức năng chạy được.

**Cách 2 – chạy máy chủ cục bộ (khuyến nghị, cần để dùng micro):**

```bash
python3 -m http.server 8080
```

Rồi mở <http://localhost:8080>.

> Micro (ghi âm / nhận dạng giọng nói) chỉ hoạt động khi trang chạy trên `https://` hoặc `localhost`, không hoạt động khi mở bằng `file://`.
> Nhận dạng giọng nói phụ thuộc trình duyệt (Chrome/Edge hỗ trợ tốt nhất); giọng đọc phụ thuộc giọng tiếng Anh có sẵn trên thiết bị.

## Đưa lên GitHub và triển khai bằng GitHub Pages

```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/<tai-khoan>/<ten-repo>.git
git push -u origin main
```

Sau đó vào **Settings → Pages → Build and deployment → Deploy from a branch → Branch: `main` / `(root)` → Save**.
Sau vài phút, website có địa chỉ `https://<tai-khoan>.github.io/<ten-repo>/`.

Có thể triển khai tương tự trên Netlify, Vercel hoặc Cloudflare Pages: chọn thư mục gốc làm thư mục xuất bản, để trống lệnh build.

## Lưu ý về dữ liệu

- Tiến độ, huy hiệu và tên học sinh được lưu bằng `localStorage` của trình duyệt (khóa `esa5`), nên chỉ lưu trên từng máy/trình duyệt, không đồng bộ giữa các thiết bị.
- Nội dung Unit 1–9 được soạn theo tên chủ điểm, **chưa đối chiếu với sách giáo khoa**; Unit 10–20 và các bài Review chưa có nội dung chính thức. Giáo viên nên kiểm tra và bổ sung ở mục **Giáo viên** (Teacher).
- Rubric chấm điểm nói trong khu giáo viên là rubric tự lập, không phải tiêu chí chính thức.

## Giấy phép

Chưa chọn giấy phép. Nếu đưa lên GitHub công khai, hãy cân nhắc nội dung có nguồn từ sách giáo khoa trước khi chọn giấy phép.
