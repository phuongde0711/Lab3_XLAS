# Lab3_XLAS

Sinh viên thực hiện: Example MSSV: Example
Môn học: Nhập môn Xử lý ảnh số
Giảng viên: Đỗ Hữu Quân

Biến đổi hình học

1. Chọn đối tượng trong ảnh
   Mục đích:
   Cắt ảnh nhỏ trong ảnh gốc ban đầu
   Cấu trúc code:
   example = data[800:1200, 570:980]
   800:1200: Chỉ định phạm vi cột dọc (từ 800 đến 1199).
   570:980: Chỉ định phạm vi cột ngang (từ 570 đến 979).
   
2. Tịnh tiến đơn
   Mục đích:
   Để dịch chuyển ảnh 
   Cấu trúc code:
   example = nd.shift(data, (100, 25))
   nd.shift(): Là hàm từ scipy.ndimage để dịch chuyển dữ liệu
   (100, 25): Đây là tham số dịch chuyển (dịch chuyển 100 pixel xuống dưới và 25 pixel sang phải)
   
3. Thay đổi kích thước ảnh
   Mục đích:
   Phóng to ảnh
   Cấu trúc code:
   example = nd.zoom(data, (5, 5, 1))
   nd.zoom(): Đây là một hàm từ thư viện scipy.ndimage, được dùng để phóng to ảnh
   (5, 5, 1): (tỷ lệ phóng to cho chiều thứ nhất, tỷ lệ phóng to cho chiều thứ 2, tỷ lệ phóng to cho chiều thứ 3)

4. Xoay ảnh
   Mục đích:
   Xoay ảnh theo góc mong muốn
   Cấu trúc code:
   example = nd.rotate(data, 30)
   nd.rotate(): Đây là một hàm từ thư viện scipy.ndimage, dùng để xoay ảnh
   30: là số góc muốn xoay

