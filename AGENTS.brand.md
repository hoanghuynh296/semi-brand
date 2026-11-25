<!-- semi-brand:start -->
## Brand: Semi (`@semi/brand`)

This product belongs to the **Semi** brand. Colours, fonts, logo and voice come only from `@semi/brand` (full guideline: `node_modules/@semi/brand/BRAND.md`; with the Semi MCP server, `semi_brand` answers from it).

**Colour**
- The brand colour is only for the main button of a page, a dialog or the nav (`Button variant="primary"`, `bg-primary` + `text-on-primary`; at most one filled brand button per page or dialog), attention count badges, "New" tags and the active big-tab underline.
- This brand has no secondary colour: do not add one.
- Ordinary buttons, selected items, links and focus are Semi's neutrals (`bg-subtle-button`, `bg-item-selected`, `text-strong`, `ring-focus`); status (success, error, warning) keeps Semi's status tokens, never the brand colour.
- Never define brand colours or override Semi tokens in this app (`--semi-*`, `@theme` colours, hex values): `semi-lint` blocks it (`brand-override`).

**Type**
- Fonts: Inter + Plus Jakarta Sans, loaded with `next/font` in the root layout (`--font-inter`, `--font-plus-jakarta-sans`). `font-display` only for the hero, a reading-page title, big tabs and editorial section heads; everything else `font-sans`. Headings are not bold (400 / 500).

**Voice (UI text)** — Trung tính. Address the user as “bạn”; the brand says “chúng tôi”. Emoji: none. Write UI text in the product's language (Vietnamese unless the product says otherwise).
- Ngắn, rõ, đúng sự việc
- Không cảm thán, không đùa
- Thuật ngữ nhất quán: một khái niệm, một từ
- Nút: động từ + đối tượng, tối đa 3 từ, viết hoa chữ đầu (Lưu, Tạo đơn hàng), không "OK" / "Xác nhận" chung chung
- Lỗi: chuyện gì xảy ra + cách sửa, không đổ lỗi cho người dùng, không mã lỗi trần
- Trạng thái trống: vì sao trống + một hành động để bắt đầu
- Không viết "Đang tải…": dùng skeleton hoặc thanh tiến trình
- Không phụ đề dưới tiêu đề trang; nhãn ngắn, icon đi trước chữ
- Do: Nói thẳng điều người dùng cần làm, câu ngắn, động từ đứng đầu
- Do: Khi có lỗi, nói rõ chuyện gì xảy ra và cách sửa
- Don't: Dùng thuật ngữ kỹ thuật hoặc tiếng Anh khi đã có từ tiếng Việt quen thuộc
- Don't: Hứa hẹn quá đà hay dùng dấu chấm than liên tục
- Example (button): “Lưu thay đổi” · “Tạo dự án” · “Thử lại”
- Example (error): “Không lưu được thay đổi vì mất kết nối. Kiểm tra mạng rồi bấm Thử lại.”
- Example (empty): “Chưa có dự án nào. Tạo dự án đầu tiên để bắt đầu.”

**Who it is for** — Mọi người dùng: dân văn phòng trên máy tính và người dùng phổ thông trên điện thoại; personality: nhanh, rõ ràng, đáng tin. Choose words and imagery for them.

**Sample content** — placeholders, seed data and empty states use this product's own things: main list “Dự án”; items “Đặt lịch khám”, “App giao hàng”, “Đối soát hoá đơn”; main figure “Dự án đang chạy” (12). Never "Lorem", "John Doe" or another domain.

**Imagery** — Ảnh chụp màn hình sản phẩm thật và minh hoạ phẳng đơn giản; tránh ảnh stock người cười trước laptop.

**Density and type scale** are this product's own choice (`data-density`, `data-type-scale` on `<html>`, mirrored in `semi-lint.json`), not the brand's. Big numbers: `<KpiCard featured>`.

**Avoid the generic AI look**
- Not every screen is sidebar + title + four equal KPI cards + a table: give each screen one main block (the thing the user came for) and make it bigger than the rest.
- KPI icons stay neutral or are left out; colour on a KPI means something (`tone="good"|"danger"`), never one decorative colour per card.
- No row of three feature cards with an icon, a one-word title and a vague promise (“Fast”, “Secure”, “Dedicated”). Show proof instead: a product shot, a real number, a customer quote.
- No icon in front of every label: icons where they help scanning (navigation, actions, status), not as decoration.
- Sample and empty-state text comes from this brand's product and voice, never generic (“Lorem”, “John Doe”, “Acme”, orders for a product the brand does not sell).
- Vary the rhythm: not every block a card with the same padding; use plain sections, dividers and white space too.

A change to the brand happens in the brand repo (`/semi-brand`), then `/semi-sync` here.
<!-- semi-brand:end -->
