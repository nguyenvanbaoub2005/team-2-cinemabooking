# Requirements — Ứng dụng đặt ghế rạp chiếu phim

## What it does

- Phục vụ khách của rạp chiếu phim, đặt ghế cho đúng một suất chiếu duy nhất.
- Có 3 loại vé, chọn riêng cho từng ghế: Người lớn 80.000đ, Sinh viên 60.000đ, Trẻ em 50.000đ.
- Mỗi lượt đặt chọn tối thiểu 1 ghế và tối đa 6 ghế.
- Không được để lại đúng 1 ghế trống lẻ trong một hàng (ghế trống bị kẹp giữa hai ghế đã đặt/đang chọn, hoặc giữa ghế đã đặt/đang chọn và mép hàng). Lựa chọn như vậy không được xác nhận.
- Mọi ghế đều là ghế thường, không có ghế dành riêng cho xe lăn.
- Tổng tiền bằng tổng giá vé của từng ghế đang chọn, tự cập nhật mỗi khi đổi ghế hoặc đổi loại vé.
- Ghế đã đặt được lưu trong localStorage, tải lại trang vẫn giữ nguyên. Lần mở đầu tiên có sẵn 8 ghế đã đặt để minh họa.

## Screen

- Một trang duy nhất, chạy trực tiếp trong trình duyệt, chỉ dùng màu sắc và emoji, không dùng hình ảnh.
- Phía trên là thanh "MÀN HÌNH" để chỉ hướng màn chiếu.
- Sơ đồ ghế gồm 5 hàng (A–E) × 8 ghế, mỗi ghế ghi mã như A1, A2… và có nhãn hàng ở đầu mỗi hàng.
- Ba trạng thái ghế phân biệt bằng màu và emoji: còn trống (xanh lá, 💺), đang chọn (vàng, ✅), đã đặt (xám, ❌).
- Có chú thích giải thích ba trạng thái ghế.
- Bên cạnh hoặc bên dưới sơ đồ là bảng "Ghế đã chọn": mỗi ghế đang chọn một dòng gồm mã ghế, ô chọn loại vé (Người lớn / Sinh viên / Trẻ em) và giá.
- Hiển thị tổng tiền, số ghế đang chọn (ví dụ 2/6) và nút "Xác nhận đặt ghế".
- Có vùng thông báo ngắn để hiện cảnh báo hoặc kết quả đặt thành công.

## Interactions

- Bấm ghế trống: ghế chuyển sang "đang chọn", xuất hiện trong bảng "Ghế đã chọn" với loại vé mặc định là Người lớn, tổng tiền cập nhật ngay.
- Bấm lại ghế đang chọn: ghế trở về "còn trống", bị xóa khỏi bảng và tổng tiền cập nhật.
- Đổi loại vé của một ghế trong bảng: giá của ghế đó và tổng tiền cập nhật ngay.
- Bấm ghế thứ 7 khi đã chọn đủ 6 ghế: không có tác dụng và hiện thông báo "Tối đa 6 ghế mỗi lượt".
- Bấm ghế đã đặt: không có tác dụng, không đổi trạng thái.
- Khi chưa chọn ghế nào, nút "Xác nhận đặt ghế" bị vô hiệu hóa và tổng tiền là 0đ.
- Bấm "Xác nhận đặt ghế" khi lựa chọn để lại đúng 1 ghế trống lẻ trong hàng: không đặt, hiện thông báo nêu rõ hàng và ghế bị trống lẻ.
- Bấm "Xác nhận đặt ghế" khi hợp lệ: các ghế đang chọn chuyển sang "đã đặt", được lưu vào localStorage, bảng "Ghế đã chọn" được làm trống, tổng tiền về 0đ và hiện thông báo thành công kèm tổng tiền đã đặt.
- Sau khi tải lại trang, các ghế đã đặt vẫn ở trạng thái "đã đặt"; ghế đang chọn dở (chưa xác nhận) không được lưu.
- Không có đăng nhập, không có bước thanh toán, không có nút hủy hoặc hoàn lại ghế đã đặt.

## Out of scope

- Đăng nhập, đăng ký hoặc quản lý thành viên.
- Thanh toán trực tuyến.
- Chọn phim, rạp hoặc nhiều suất chiếu.
- Lưu dữ liệu trên máy chủ hoặc đồng bộ giữa các thiết bị.
- Ghế dành cho xe lăn hoặc các loại ghế đặc biệt khác (ghế VIP, ghế đôi).
- Hủy hoặc đổi ghế đã đặt (kể cả nút đặt lại dữ liệu).
- Mã giảm giá, phí dịch vụ, thuế.
- Hình ảnh và thư viện bên ngoài.
