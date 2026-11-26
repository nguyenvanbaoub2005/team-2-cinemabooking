# Task list

## 1. Khung ứng dụng và sơ đồ ghế hiển thị được

- What to do: Tạo `index.html`, `style.css`, `script.js` chạy trực tiếp bằng cách mở file trong trình duyệt. Vẽ thanh "MÀN HÌNH", sơ đồ 5 hàng (A–E) × 8 ghế có mã ghế và nhãn hàng, chú thích ba trạng thái, cùng khung "Ghế đã chọn", tổng tiền 0đ và nút "Xác nhận đặt ghế" (chưa có chức năng).
- Done when: Mở `index.html` thấy đủ 40 ghế mã A1–E8 màu xanh lá kèm 💺, thanh "MÀN HÌNH", phần chú thích 3 trạng thái, tổng tiền 0đ, và nút "Xác nhận đặt ghế" đang bị vô hiệu hóa. Không có lỗi trong console.
- Files touched: `index.html`, `style.css`, `script.js`

## 2. Chọn ghế, chọn loại vé và tính tổng tiền

- What to do: Bấm ghế trống để chọn hoặc bỏ chọn (đổi sang vàng ✅). Ghế đang chọn hiện trong bảng "Ghế đã chọn" với ô chọn loại vé (Người lớn 80.000đ / Sinh viên 60.000đ / Trẻ em 50.000đ, mặc định Người lớn). Tổng tiền và số ghế (x/6) cập nhật ngay. Giới hạn tối đa 6 ghế.
- Done when: Bấm A1 và A2 thì cả hai chuyển vàng, xuất hiện trong bảng và tổng tiền là 160.000đ. Đổi A2 sang Trẻ em thì tổng thành 130.000đ. Bấm lại A1 thì A1 trở về xanh và tổng còn 50.000đ. Chọn đủ 6 ghế rồi bấm ghế thứ 7 thì không có gì thay đổi và hiện thông báo "Tối đa 6 ghế mỗi lượt".
- Files touched: `script.js`, `style.css`, `index.html`
- Order: làm sau task 1.

## 3. Xác nhận đặt ghế và lưu bằng localStorage

- What to do: Nút "Xác nhận đặt ghế" chỉ bật khi có ít nhất 1 ghế đang chọn. Khi bấm, các ghế đang chọn chuyển sang "đã đặt" (xám ❌, không chọn được), bảng "Ghế đã chọn" được làm trống, tổng tiền về 0đ và hiện thông báo thành công kèm số tiền. Lưu ghế đã đặt vào localStorage. Lần mở đầu tiên có sẵn 8 ghế đã đặt.
- Done when: Lần mở đầu tiên có 8 ghế xám ❌ sẵn. Chọn hai ghế trống, xác nhận, thấy thông báo thành công và hai ghế chuyển xám. Bấm lại hai ghế đó thì không có phản ứng. Tải lại trang (F5) thì các ghế đã đặt vẫn còn xám, còn ghế đang chọn dở thì không được giữ.
- Files touched: `script.js`, `style.css`, `index.html`
- Order: làm sau task 2.

## 4. Chặn để lại ghế trống lẻ trong hàng

- What to do: Khi bấm "Xác nhận đặt ghế", kiểm tra từng hàng: nếu lựa chọn khiến đúng 1 ghế trống bị kẹp giữa hai ghế đã đặt/đang chọn, hoặc nằm giữa ghế đã đặt/đang chọn và mép hàng, thì không đặt và hiện thông báo nêu rõ hàng và ghế bị trống lẻ.
- Done when: Chọn A1 và A3 (A2 trống bị kẹp) rồi xác nhận thì không đặt được và thông báo nêu ghế A2 ở hàng A. Chọn A2 thì A1 trống lẻ ở mép nên cũng bị chặn. Chọn A1, A2, A3 thì đặt được bình thường. Sau khi chặn, các ghế đang chọn vẫn giữ nguyên để người dùng sửa.
- Files touched: `script.js`
- Order: làm sau task 3.

## 5. Hoàn thiện giao diện và thông báo

- What to do: Chỉnh bố cục cho gọn và dễ đọc (sơ đồ ghế, bảng "Ghế đã chọn", tổng tiền, nút xác nhận), thống nhất màu sắc và emoji, định dạng tiền theo kiểu `80.000đ`, vùng thông báo hiển thị rõ cảnh báo và thành công. Chỉ chỉnh giao diện, không đổi quy tắc.
- Done when: Chạy đủ kịch bản trình bày (chọn hai ghế trống và loại vé, xem tổng tiền, xác nhận, bấm lại hai ghế vừa đặt không chọn được) và mọi thứ nhìn rõ ràng. Ba trạng thái ghế dễ phân biệt, thông báo lỗi và thành công có màu khác nhau, mọi số tiền có định dạng `.000đ`. Không dùng hình ảnh hay thư viện ngoài.
- Files touched: `style.css`, `index.html`
- Order: làm sau task 3 (có thể làm song song với task 4 nếu chỉ sửa `style.css`).

---

Bước tiếp theo:

- Đưa `docs/tasks.md` vào một PR để cả nhóm đọc.
- Sau khi PR được merge, dùng `/create-issues` để biến mỗi task thành một GitHub Issue.
- Mỗi người bắt đầu một task bằng `/start-task`, lệnh này sẽ gán Issue cho bạn.
