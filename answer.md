# PHẦN A — KIỂM TRA ĐỌC HIỂU

## Câu A1 — 5 Loại Positioning

| Position   | Vẫn chiếm chỗ trong flow? | Tham chiếu vị trí         | Cuộn theo trang? | Use case                  |
|------------|---------------------------|---------------------------|------------------|---------------------------|
| static     | Có                        | Vị trí mặc định           | Có               | Mặc định, không định vị   |
| relative   | Có                        | Chính nó                  | Có               | Dịch chuyển nhẹ           |
| absolute   | Không                     | Nearest positioned ancestor| Không            | Tooltip, badge, overlay   |
| fixed      | Không                     | Viewport                  | Không            | Header, nút nổi           |
| sticky     | Có                        | Tổ tiên cuộn gần nhất     | Có               | Sidebar, header dính      |

**Thêm:**
- `absolute` tham chiếu `body` khi không có tổ tiên nào có position khác static.
- Tham chiếu parent khi parent có position khác static.
- "Nearest positioned ancestor" là tổ tiên gần nhất có position khác static.

## Câu A2 — Flexbox vs Grid

1. Trường hợp 1: 4 items nằm ngang, chia đều 4 cột.
2. Trường hợp 2: 6 items, mỗi hàng 2 item, 3 hàng.
3. Trường hợp 3: 3 items nằm ngang, cách đều 2 bên, căn giữa dọc.
4. Trường hợp 4: 3 items, cột trái 200px, giữa co giãn, phải 200px, có gap.
5. Trường hợp 5: 7 items, 3 cột, 3 hàng (hàng cuối có 1 item).