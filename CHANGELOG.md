# Changelog

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
