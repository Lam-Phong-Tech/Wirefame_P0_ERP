# Design System — Module 1: Quản lý Tổ chức (Wireframe P0)

> Tài liệu hệ thống thiết kế dùng chung cho toàn bộ wireframe Module 1 (Org Unit · Department · Employee · Chức vụ · Sơ đồ tổ chức · Giao việc & phê duyệt).
> Mức độ: **Low-fi / MVP**. Mục đích: thống nhất màu, chữ, khoảng cách, component và quy ước trạng thái trước khi dựng hi-fi.

---

## 1. Nguyên tắc chung

- **Một hệ token, áp dụng nhất quán** trên mọi màn — list, form, detail, modal, sơ đồ.
- **Tối giản, ưu tiên cấu trúc** hơn trang trí. Mỗi phần tử phải có lý do tồn tại.
- **Tiếng Việt là ngôn ngữ chính** → font bắt buộc hỗ trợ đầy đủ dấu.
- **Icon đơn sắc, một tông** để không gây "nhiễu thị giác".
- Mỗi màn gắn **mã chức năng BRD** (F1.x–F9.x) để truy vết yêu cầu.

---

## 2. Màu sắc (Color tokens)

### 2.1. Nền & mực (Neutrals)

| Token | Hex | Dùng cho |
|---|---|---|
| `canvas` | `#e7e5df` | Nền tổng (ngoài khung) |
| `paper` | `#ffffff` | Nền thẻ/khung nội dung |
| `paper-alt` | `#fcfbf8` / `#fbfaf7` | Nền canvas sơ đồ, node phòng ban |
| `ink` | `#2b2b2b` | Chữ chính, viền khung, nút phụ |
| `ink-2` | `#4a463e` | Chữ cấp 2 (dữ liệu bảng) |
| `muted` | `#7a766c` | Chú thích, mã, phụ đề |
| `muted-2` | `#8c887e` | Nhãn trường, header bảng |
| `placeholder` | `#9a968c` | Chữ gợi ý trong ô input |
| `table-head` | `#f3f1ea` | Nền dòng tiêu đề bảng |

### 2.2. Đường kẻ (Borders / dividers)

| Token | Hex | Dùng cho |
|---|---|---|
| `border-input` | `#b9b6ad` | Viền ô nhập, nút phụ nhạt |
| `divider` | `#d8d5cc` | Kẻ ngăn toolbar / header bảng |
| `divider-soft` | `#e3e0d8` | Kẻ trong thẻ, khối thống kê |
| `row-line` | `#ece9e1` | Kẻ giữa các dòng bảng |
| `connector` | `#b9b6ad` | Đường nối node sơ đồ tổ chức |

### 2.3. Màu nhấn (Accent — xanh dương)

| Token | Hex | Dùng cho |
|---|---|---|
| `accent` | `#356fa3` | Nút chính, trạng thái chọn, link |
| `accent-bg` | `#eaf1f8` | Nền node/ô được chọn, radio active |
| `accent-border` | `#bcd2e6` | Viền vùng nhấn nhạt |
| `accent-ink` | `#5b6b7e` | Chữ phụ trên nền accent |

### 2.4. Màu ngữ nghĩa (Semantic)

| Ý nghĩa | Nền | Chữ | Viền |
|---|---|---|---|
| Thành công / Đang hoạt động | `#dceadf` | `#3c6e4f` | `#9cc3a8` |
| Cảnh báo / Tạm ngưng | `#f6eed6` | `#8a6d1f` | `#d9c489` |
| Nguy hiểm / Vô hiệu | `#fbe7e6` | `#b94a48` / `#a5413f` | `#d8a9a6` |
| Trung tính / Nghỉ – Hủy | `#eceae6` | `#6b675e` | `#c9c5bb` |
| Quá hạn | `#fbe3d6` | `#b15a2a` | `#e0b598` |

### 2.5. Ghi chú thiết kế (Sticky note)

| Token | Hex |
|---|---|
| Nền | `#fff4cf` |
| Viền (dashed) | `#c9a227` |
| Chữ | `#6b5a12` |

---

## 3. Typography

- **Font chữ:** `Be Vietnam Pro` (Google Fonts) — hỗ trợ đầy đủ dấu tiếng Việt.
- **Fallback:** `system-ui, sans-serif`.
- **Trọng lượng dùng:** 400 (thường) · 500 · 600 (nhấn nhẹ) · 700 (đậm/tiêu đề).

| Vai trò | Cỡ | Trọng lượng | Màu |
|---|---|---|---|
| Tiêu đề trang | 23px | 700 | `ink` |
| Nhãn khung (frame label) | 17px | 700 | `ink` |
| Tiêu đề form / card | 18–20px | 700 | `ink` |
| Tiêu đề mục trong form | 15px | 700 | `accent` |
| Nhãn trường (field label) | 13px | 400 | `muted-2` |
| Nội dung input / dữ liệu | 14–15px | 400 | `ink` / `ink-2` |
| Header bảng | 13px | 400 | `muted-2` |
| Ô bảng | 14px | 400/700 | `ink` |
| Badge / pill | 11–12.5px | 400/600 | theo ngữ nghĩa |
| Chú thích nhỏ | 11–12px | 400 | `muted` |

**Quy tắc cỡ chữ tối thiểu:** không nhỏ hơn 11px trong wireframe; ở hi-fi nâng nhãn trường lên ≥13px.

---

## 4. Spacing, bo góc & đổ bóng

### 4.1. Khoảng cách
- Padding ngoài màn: `40px 48px`.
- Khoảng cách giữa các khung (frame gap): `44px`.
- Padding thẻ form: `20–22px`.
- Padding ô/dòng bảng: `12–14px 16px`.
- Gap giữa các trường trong form: `14px`; trong nhóm ngang: `12px`.

### 4.2. Bo góc (Radius)
| Phần tử | Radius |
|---|---|
| Thẻ / khung lớn | `4px` |
| Ô input, nút, filter | `3px` |
| Node sơ đồ tổ chức | `5–6px` |
| Pill / badge trạng thái | `10px` |
| Avatar | `50%` (tròn) |

### 4.3. Đổ bóng (Shadow)
- Thẻ khung: `4px 5px 0 rgba(43,43,43,.12)` (bóng cứng, lệch — phong cách low-fi).
- Node sơ đồ: `2px 2px 0 rgba(43,43,43,.08)`; node chọn: `2px 2px 0 rgba(53,111,163,.18)`.

---

## 5. Iconography

- **Bộ icon:** [Icons8](https://icons8.com) — style **`fluency-systems-regular`** (line, đơn sắc).
- **Nguồn:** `https://img.icons8.com/fluency-systems-regular/96/<COLOR>/<NAME>.png`
- **Cỡ hiển thị:** 13–16px (icon trong nút/label), 18–20px (icon cảnh báo).
- **Màu:** một tông trung tính `#5b574e` cho icon thực thể; màu chức năng riêng cho vài icon (xem bảng).
- **Căn chỉnh inline:** `vertical-align:-2px; display:inline-block; flex:none`.

| Ngữ cảnh | Icon (Icons8 name) | Màu |
|---|---|---|
| Công ty mẹ | `company` | `5b574e` |
| Công ty con | `organization` | `5b574e` |
| Chi nhánh | `marker` | `5b574e` |
| Tìm kiếm | `search` | `8c887e` |
| Xuất dữ liệu | `export` | `5b574e` |
| Tải lên (logo) | `upload` | `9a968c` |
| Ngày tháng | `calendar` | `9a968c` |
| Cảnh báo | `error` | `b94a48` |
| Tích chọn | `checkmark` | `6b675e` |
| Ghim ghi chú | `pin` | `8a7320` |

> ⚠️ Icon nạp từ CDN Icons8 → cần internet. Khi cần chạy offline, tải PNG về nhúng trong dự án (giữ nguyên tên & màu).
>
> Các ký tự đơn sắc dạng typographic (`▾ ▸ ◉ ○ ◐ ⋯ ✎ ⊘ ＋ －`) được giữ nguyên vì đã hợp tông line, không cần thay.

---

## 6. Component

### 6.1. Khung màn (Frame card)
Nền `paper`, viền `2px solid ink`, radius `4px`, shadow thẻ. Mỗi khung có **nhãn** phía trên (17px/700) kèm mã BRD màu `muted`.

### 6.2. Thanh công cụ (Toolbar)
Hàng ngang: ô tìm kiếm (icon `search` + placeholder) → các filter dropdown (viền `border-input`) → spacer → nút phụ (Export) → **nút chính** (`+ Thêm…`).

### 6.3. Bảng danh sách (Table)
- Header: nền `table-head`, chữ `muted-2` 13px, kẻ dưới `divider`.
- Dòng: kẻ `row-line`, chữ 14px, cột tên in đậm.
- Mỗi dòng kết thúc bằng cụm hành động `✎ ⋯` màu `accent`.
- Phân trang ở chân: ‹ 1 2 3 › (ô active dùng `accent-bg` + viền `accent`).

### 6.4. Trường nhập (Form field)
- Nhãn 13px `muted-2`, cách ô `4px`.
- Ô: cao `34–36px`, viền `1.5px border-input`, radius `3px`.
- Trường bắt buộc đánh dấu `*`.
- Select hiển thị `▾`; ô có icon (ngày/người) đặt icon ở đầu.
- Textarea: cao `64–72px`.

### 6.5. Nút (Button)
| Loại | Style |
|---|---|
| Chính (primary) | nền `accent`, chữ trắng 700, radius 3px |
| Phụ (secondary) | viền `1.5px ink`, chữ `ink` |
| Nguy hiểm (danger) | viền/chữ `#b94a48` |
| Duyệt (approve) | nền `#3c6e4f`, chữ trắng 700 |

### 6.6. Radio / Segmented
Nhóm ô ngang, ô chọn = viền `accent` + nền `accent-bg`; ô thường = viền `border-input`, chữ `muted`. Ký hiệu `◉` (chọn) / `○` (chưa).

### 6.7. Pill trạng thái (Status pill)
Bo `10px`, padding `2px 9px`, 12.5px, có chấm dẫn (`●/◐/○/✕…`) theo bảng màu ngữ nghĩa (§2.4, §7).

### 6.8. Chip ưu tiên (Priority)
Bo `3px`, 12px/600: **Cao** (đỏ) · **TB** (vàng) · **Thấp** (xám).

### 6.9. Cây phân cấp (Tree — tab Org Unit)
Thụt lề theo cấp (`22px`/cấp), mũi tên `▾/▸`, icon thực thể, badge loại (`Mẹ/Con`) bên phải. Node chọn: nền `accent-bg` + viền `accent`.

### 6.10. Sơ đồ tổ chức (Org chart node)
- Node pháp nhân/chi nhánh: viền `1.5px ink`, radius 6px, có caption loại + tên đậm + dòng "GĐ/ĐD · số NV".
- Node phòng ban: nhỏ hơn, viền `1.5px #6b675e`, nền `paper-alt`.
- Node đang chọn: viền `2px accent` + nền `accent-bg`.
- Node thu gọn: badge `▸ N chi nhánh/phòng ban`.
- Đường nối: `2px` màu `connector`, nền canvas có lưới chấm `#e7e4dc`.

### 6.11. Ghi chú thiết kế (Annotation note)
Nền `#fff4cf`, viền `1px dashed #c9a227`, xoay nhẹ `-0.5°`, mở đầu bằng icon `pin`. Dùng để ghi rule/giả định BRD (BR-xx, Axx).

### 6.12. Tab điều hướng
Hàng nút (wrap), nút active = nền `accent` + chữ trắng + bóng cứng; nút thường = nền `paper` + viền `ink`. Đánh số `①–⑥`.

### 6.13. Timeline trạng thái (tab Giao việc)
Cột dấu chấm + đường nối dọc; mốc hiện tại to hơn, có viền nhạt, chữ 600.

---

## 7. Quy ước trạng thái (State conventions)

### 7.1. Trạng thái đơn vị / phòng ban / nhân sự
| Trạng thái | Pill |
|---|---|
| Đang hoạt động / Đang làm | ● xanh lá |
| Tạm ngưng | ◐ vàng |
| Vô hiệu hóa | ○ đỏ nhạt |
| Nghỉ việc | ✕ xám |

### 7.2. Vòng trạng thái công việc (F9.2)
`○ Mới tạo` → `◔ Đã giao` → `◑ Đang xử lý` → `◕ Chờ duyệt` → `● Hoàn thành`
nhánh phụ: `✕ Từ chối / Yêu cầu làm lại` · `⊘ Hủy` · `⏱ Quá hạn` (theo hạn hoàn thành).

### 7.3. Phê duyệt 1 cấp (F9.4)
Người nhận **gửi duyệt** → trưởng phòng người nhận (hoặc người được chỉ định) **Duyệt / Từ chối**. **Người nhận không được tự duyệt.** Workflow nhiều cấp = Future.

---

## 8. Mẫu bố cục (Layout patterns)

- **Trình bày nhiều khung cạnh nhau:** nền `canvas` phủ kín (`width:max-content`), hàng khung căn trái (`align-items:flex-start`), mỗi khung `flex:none` + rộng cố định. Cuộn ngang để xem hết.
- **List view:** Toolbar → Bảng → Phân trang/Legend.
- **Form view:** Tiêu đề → các nhóm trường (chia mục có tiêu đề `accent`) → hàng nút (Hủy/Lưu) căn phải.
- **Detail / Confirm / Modal:** Header tóm tắt → thân (thống kê, danh sách, lựa chọn) → hành động → ghi chú rule.

---

## 9. Phạm vi & mã chức năng (tham chiếu BRD)

| Tab | Epic | Mã MVP chính |
|---|---|---|
| ① Org Unit | A | F1.1–F1.4 |
| ② Department | B | F2.1, F2.2, F2.4 |
| ③ Employee | C | F3.1–F3.4, F3.6 |
| ④ Chức vụ | D | F4.1 (F4.2a = MVP+) |
| ⑤ Sơ đồ tổ chức | F | F6.1, F6.3 (F6.2/F6.4 = MVP+) |
| ⑥ Giao việc & phê duyệt | I | F9.1–F9.4 |

> Nhãn `MVP+` / `Future` hiển thị ngay trên các control chưa thuộc P0 (vd: lọc sơ đồ, xuất PDF) để tránh hiểu nhầm phạm vi.
