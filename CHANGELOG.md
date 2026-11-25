# Changelog

## 3.0.0 - 2026-11-25

### Breaking — Từ Semi (@semi/ui v1.0.0 schema)
- `semi` range `>=0.35.0 <1.0.0` -> `>=1.0.0 <2.0.0`; dựng lại toàn bộ `dist/brand.css`, `dist/brand.json`, `BRAND.md`, `AGENTS.brand.md` theo lược đồ brand kit Semi 1.0 (chỉ sinh màu chính / phụ, chữ trên nút, hover, chữ nhãn "Mới" và font).
- Xoá các khoá cũ 0.x khỏi `brand.json`: `neutral` (`"tinted"`), `styles` (`flat` / `soft` / `sharp`), `color.accent` (`"restrained"`). Từ Semi 1.0 mọi thương hiệu dùng chung một style và bảng xám trung tính của `@semi/ui` (không còn xám phủ màu thương hiệu, không còn `accent-subtle` / `accent-line` hay thang màu primary).
- Quy tắc màu thương hiệu 1.0 (`BRAND.md`, `AGENTS.brand.md`): màu chính (`#dd592a`, chữ `#0c0d0e`, hover `#f26c3f` dùng chung cả hai theme) chỉ dùng cho nút chính của trang / hộp thoại / thanh điều hướng, badge đếm cần chú ý, nhãn "Mới" và gạch chân tab lớn đang chọn.
- Bảng đọc rõ: 4/4 cặp đạt AA (chữ trên nút chính 5.13:1, hover 6.48:1, nút tách nền tối 4.59:1, nền sáng 3.18:1).

### Thương hiệu
- Giữ nguyên màu chính `#DD592A`, không màu phụ, font Inter + Plus Jakarta Sans, giọng văn, brief và hình ảnh.

## 2.5.0 - 2026-11-23

### Từ Semi (@semi/ui v0.36.0; brand.json không đổi lựa chọn nào)
- Rebuilt on Semi 0.36.0 (C-030/C-033 surfaces): dev dependency @semi/ui v0.35.0 -> v0.36.0; `dist/` và BRAND.md build lại.
- Các bậc nền (canvas, app, panel, field, raised) theo bước nhỏ, đều của Semi 0.36.0; thêm `card` và `tint`. Màu chính, font, logo không đổi; tùy chọn mới (`neutral: "pure"`, `primaryStyle: "inverted"`) giữ mặc định.
- Bảng đọc rõ: 42/42 cặp đạt AA (thêm các cặp chữ mờ trên thẻ, thẻ tách khỏi nền).

## 2.4.0 - 2026-11-22

### Từ Semi (@semi/ui v0.35.0; brand.json không đổi lựa chọn nào)
- `semi` range `>=0.30.0 <1.0.0` -> `>=0.35.0 <1.0.0`; dev dependency @semi/ui v0.30.0 -> v0.35.0. Build lại `dist/` và BRAND.md.
- **Màu chính theo từng theme** (quyết định C-024, ds#84): theme sáng dùng bậc 600 (`#bd4516`, chữ trên nút `#ffffff`, hover `#9d3100`), theme tối dùng bậc 400-500 (`#dd592a`, chữ trên nút `#0c0d0e`). Trước đây cả hai theme dùng `#dd592a`.
- **Nền app của Flat sáng** `#ffffff` -> `#fcf9f8` (panel giữ `#ffffff`) (ds#88).
- Thay đổi nhìn thấy: nút chính và accent ở theme sáng đậm hơn, chữ nút chuyển sang trắng; nền trang Flat sáng hơi ấm thay vì trắng thuần. Theme tối không đổi. Bảng đọc rõ: 30/30 cặp đạt AA.

### Thương hiệu
- Không đổi lựa chọn nào trong brand.json.


## 2.3.0 - 2026-11-20

### Từ Semi (@semi/ui v0.30.0; brand.json không đổi lựa chọn nào)
- `semi` range `>=0.29.0 <1.0.0` -> `>=0.30.0 <1.0.0`; dev dependency @semi/ui v0.29.2 -> v0.30.0.
- **Màu lỗi xoay 8°** (`#f43f5e` → `#f23e72`, đỏ hơi ngả hồng) để không lẫn với màu cam chính `#DD592A` (trước chỉ cách 22° sắc độ). `brand.css` ghi đè `--semi-danger-fg | bg | border | solid` ở cả hai theme; độ sáng giữ nguyên nên chữ lỗi vẫn đạt AA (30/30 cặp đạt).
- Token đổi tên theo vai trò ở Semi (`text-kpi` → `text-figure`, `z-keypad` → `z-sheet`) không đụng tới kit; luật cho agent (`AGENTS.brand.md`) không đổi.

### Thương hiệu
- Không đổi.

## 2.2.0 - 2026-11-20

### Từ Semi (@semi/ui v0.29.0; brand.json không đổi lựa chọn nào)
- `semi` range `>=0.26.0 <1.0.0` -> `>=0.29.0 <1.0.0`; dev dependency @semi/ui v0.27.0 -> v0.29.0. Màu, font và giọng văn không đổi (`dist/brand.css` chỉ đổi dòng ghi phiên bản).
- Bảng đọc rõ (BRAND.md, `dist/brand.json` → `report`) có thêm viền ô nhập (`control-line`, ≥ 3:1) cho Flat, Soft, Sharp và chữ trạng thái của Semi (lỗi, thành công, cảnh báo, thông tin) trên nền của thương hiệu: 30/30 cặp đạt.
- Lưu ý mới: kit chưa có logo; cảnh báo màu chính gần màu lỗi ghi rõ độ lệch (24°, ΔE 0.14 so với `#be123c`).
- `package.json` bỏ export `./dist/logo/*` (kit chưa có logo; thêm lại tự động khi có `logo` trong brand.json).
- Workflow `brand-pages.yml` kiểm tra cả pull request (chỉ đăng GitHub Pages từ main). Workflow mới `semi-update.yml` build lại kit với @semi/ui mới nhất mỗi thứ Hai và mở pull request khi kit sinh ra khác đi.
- Tuỳ chọn mới `color.buttonText` (`auto` mặc định, `white`, `dark`); kit này giữ `auto` (chữ tối trên nút cam ở theme sáng).

### Thương hiệu
- Không đổi.

## 2.1.0 - 2026-11-18

### Changed
- `semi` range `^0.24.0` -> `">=0.26.0 <1.0.0"`: the kit covers @semi/ui v0.26 and every later 0.x minor, so `/semi-sync` can install v0.26.1, v0.27.0 and later in apps of this brand (hoanghuynh296/semi-brand#1). Plugins older than v0.27.0 do not parse this form and read it as uncapped; that is safe because no 1.x tag exists.
- Dev dependency on @semi/ui is now v0.27.0 (its validator accepts the wide range); generated files rebuilt (only the @semi/ui version stamp and `semi` change).
- `next` (site preview dev dependency) 16.4.3 -> 16.4.6, fixing the Next.js security advisories that failed the site build.
- No colour, font, logo or voice change. @semi/ui 0.25.0 to 0.26.1 changes (BootLoader, shell lint rules, FileDrop, fixes) need nothing in a brand kit.

## 2.0.0 - 2026-11-16

### Từ Semi (@semi/ui v0.24.0)
- `semi` range `^0.19.0` -> `^0.24.0`.
- Theme tối: bề mặt panel / field / raised sáng hơn, chữ mờ và viền rõ hơn (Semi 0.20.0). Theme sáng và màu thương hiệu không đổi. Major vì giao diện tối đổi thấy rõ.
- Luật cho agent: rule `primary-fill` (không tô nền bằng `bg-primary-500`; dùng `bg-accent`).

## 1.0.0 - 2026-11-02

### Thương hiệu
- Bản đầu: màu chính `#DD592A`, màu trung tính phủ theo màu chính, style Flat (mặc định) / Soft / Sharp, font Inter + Plus Jakarta Sans, giọng văn trung tính gọi "bạn", brief và dữ liệu mẫu.
