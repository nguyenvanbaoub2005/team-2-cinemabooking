# Ứng dụng đặt ghế rạp chiếu phim

- Nhóm: (số nhóm và các thành viên)
- Chủ đề: Đặt ghế rạp chiếu phim cho một suất chiếu.
- Khách hàng: Rạp chiếu phim.
- Mục tiêu: Giúp khách chọn ghế còn trống, chọn loại vé cho từng ghế, xem tổng tiền và xác nhận đặt ghế.

## Cách chạy

Nhấp chuột phải vào `index.html` → Open In Browser

## Thao tác trình bày Buổi 5

1. Mở `index.html` trên trình duyệt từ nhánh `main`.
2. Chọn hai ghế còn trống sao cho không để lại một ghế trống lẻ trong hàng.
3. Chọn vé Người lớn cho một ghế và vé Sinh viên cho ghế còn lại. Kiểm tra tổng tiền hiển thị là **140.000đ**.
4. Bấm **Xác nhận đặt ghế**. Kiểm tra cả hai ghế chuyển sang trạng thái **Đã đặt** và không thể chọn lại.
5. Tải lại trang. Kiểm tra cả hai ghế vẫn ở trạng thái **Đã đặt**.

## Cách làm việc

1. Yêu cầu nằm ở `docs/requirements.md`, task nằm ở `docs/tasks.md`
2. Dùng `/create-issues` để chuyển các task thành Issue trên GitHub
3. **Khi bắt đầu một task, dùng `/start-task`** (bạn sẽ trở thành người phụ trách Issue đó và một nhánh mới sẽ được tạo)
4. Ghi `Closes #số` trong phần mô tả của PR. Khi PR được merge vào main, Issue sẽ tự đóng
