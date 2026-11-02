# Semi: brand kit

Bộ nhận diện của **Semi** trên Semi Design System. File duy nhất người sửa là `brand.json`; mọi file trong
`dist/`, `BRAND.md` và `AGENTS.brand.md` do `semi-brand build` sinh ra.

- Guideline: [BRAND.md](BRAND.md)
- Xem trước: `npm run preview` (http://localhost:4600); bản online: GitHub Pages của repo này (workflow
  `.github/workflows/brand-pages.yml` build lại mỗi lần push lên main)
- Đổi lựa chọn: `/semi-brand` (hoặc sửa `brand.json`, rồi `npm run build`)
- Bản Semi mới: `/semi-brand update`
- Dùng trong sản phẩm mới: `/semi-new-app --brand github:<owner>/<repo>`; sản phẩm có sẵn: `/semi-sync`

Hướng dẫn đầy đủ: `node_modules/@semi/ui/docs/BRANDS.md`.
