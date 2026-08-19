# Cách dùng

1. Giải nén, mở toàn bộ thư mục `pccc24-landing/` này làm project trong Antigravity.
2. (Tuỳ chọn) Cài skill thiết kế landing page — xem mục "Cài skill" bên dưới.
3. Paste **Lệnh 1** vào Antigravity trước — nó sẽ điền nội dung vào các thẻ `<!-- TODO -->` có sẵn trong `index.html`.
4. Sau khi hài lòng với nội dung, paste **Lệnh 2** — nó sẽ viết CSS thật vào `assets/style.css`.

Không cần tạo file mới — file `index.html` và `assets/style.css` đã có sẵn trong project, Antigravity sẽ **chỉnh sửa trực tiếp** các file này.

---

## Lệnh 1 — Dựng nội dung lên khung HTML có sẵn

```
Dự án đã có sẵn index.html với các section rỗng đánh dấu bằng comment <!-- TODO -->, và assets/style.css, assets/script.js trống.

Hãy điền nội dung thật vào index.html hiện có (không tạo file mới, không đổi cấu trúc section/id đã đặt), cho landing page bán hàng trực tiếp của pccc24.com (Công ty TNHH MTV Hoàng Quân Phát - thiết bị PCCC).

Bối cảnh: Mục tiêu bán hàng trực tiếp online, không chỉ thu lead. Đối tượng: cả B2B (nhà xưởng, nhà thầu, đại lý mua sỉ, cần hỗ trợ hồ sơ nghiệm thu) VÀ B2C (hộ gia đình mua bình chữa cháy, tủ báo cháy mini, thiết bị lẻ).

Với từng section trong index.html:
- #hero: headline nhấn mạnh uy tín + an toàn, CTA rõ ràng "Mua ngay" / "Xem sản phẩm", hotline nổi bật
- #products: danh mục sản phẩm (bình chữa cháy, hệ thống báo cháy, vòi/họng nước chữa cháy, tủ chữa cháy, đồ bảo hộ PCCC) — mỗi sản phẩm có ảnh placeholder, tên, giá, nút "Thêm vào giỏ"/"Mua ngay"
- #for-household: nội dung dành cho hộ gia đình (mua lẻ, giao nhanh)
- #for-business: nội dung dành cho doanh nghiệp/dự án (báo giá sỉ, hỗ trợ hồ sơ nghiệm thu PCCC)
- #why-us: lý do chọn (chứng nhận, bảo hành, giao hàng, đội ngũ kỹ thuật)
- #best-sellers: sản phẩm bán chạy / khuyến mãi
- #testimonials: 2-3 đánh giá mẫu (ghi rõ đây là placeholder cần thay bằng dữ liệu thật)
- #faq: câu hỏi thường gặp (bảo hành, vận chuyển, quy trình nghiệm thu)
- #site-footer: thông tin công ty, giấy phép kinh doanh, liên hệ

Copy bằng tiếng Việt, giọng chuyên nghiệp - đáng tin cậy, không dùng ngôn từ tuyệt đối/cường điệu (tránh vi phạm chính sách quảng cáo sàn TMĐT). Không thêm nav/sidebar phức tạp.

CHỈ sửa index.html (nội dung/markup), KHÔNG động vào assets/style.css ở bước này.
```

---

## Lệnh 2 — Áp thiết kế lên assets/style.css

```
Dự án đã có index.html với nội dung đầy đủ và assets/style.css hiện chỉ có reset CSS cơ bản.

Hãy viết CSS thật vào assets/style.css (chỉnh sửa file có sẵn, không tạo file CSS mới) để thiết kế landing page pccc24.com.

Phong cách: Chuyên nghiệp, đáng tin cậy — tông màu đỏ/cam an toàn (safety red/orange) làm màu chủ đạo, kết hợp trắng/xám đậm để cân bằng, tránh chói mắt. Đây là ngành PCCC nên đỏ cam vừa đúng brand vừa gợi liên tưởng an toàn - khẩn cấp, không dùng bảng màu mì ăn liền/generic AI (tránh tông cam đất be #D97757, tránh nền đen kèm 1 màu neon).

Typography: Font rõ ràng, dễ đọc trên mobile, tiêu đề đậm chắc chắn tạo cảm giác uy tín (không phải kiểu playful/startup).

Yêu cầu:
- Mobile-first, responsive đầy đủ (test ở 375px trước)
- Nút CTA nổi bật, tương phản cao, dễ bấm trên mobile
- #products và #best-sellers: card sản phẩm có khung/border rõ ràng như catalog thương mại
- #for-business dùng tông nghiêm túc hơn (navy/xám đậm) để phân biệt với #for-household (đỏ/cam tươi hơn)
- Micro-interaction nhẹ (hover, transition) cho nút và card, không lạm dụng animation
- Contrast ratio đạt chuẩn accessibility cho text trên nền đỏ/cam

CHỈ sửa assets/style.css, KHÔNG động vào nội dung/markup trong index.html.
```

---

## Cài skill (không bắt buộc, nhưng giúp Antigravity dựng đẹp hơn)

Chạy trong terminal tại thư mục gốc project này:

```bash
mkdir -p .agents/skills
git clone https://github.com/jiji262/claude-design-skill.git /tmp/design-skill-tmp
cp -r /tmp/design-skill-tmp .agents/skills/claude-design-skill
rm -rf /tmp/design-skill-tmp
```

Antigravity sẽ tự nhận diện skill này khi chạy Lệnh 2 ở trên (task "thiết kế landing page" khớp với description của skill).
