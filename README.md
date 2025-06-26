# Lab3_XLAS: Biến đổi hình học

**Sinh viên thực hiện: Lê Hoài Phương MSSV: 207CT10264
**Môn học: Nhập môn Xử lý ảnh số
**Giảng viên: Đỗ Hữu Quân

# 1. Chọn đối tượng trong ảnh
   Mục đích:
   * **Cắt ảnh nhỏ trong ảnh gốc ban đầu
   Cấu trúc code:
   ```bash
   example = data[800:1200, 570:980]
   ```
   * `800:1200`: Chỉ định phạm vi cột dọc (từ 800 đến 1199).
   * `570:980`: Chỉ định phạm vi cột ngang (từ 570 đến 979).
   
# 2. Tịnh tiến đơn
   Mục đích:
   * Để dịch chuyển ảnh 
   Cấu trúc code:
   ```bash
   example = nd.shift(data, (100, 25))
   ```
   * `nd.shift()`: Là hàm từ scipy.ndimage để dịch chuyển dữ liệu
   * `(100, 25)`: Đây là tham số dịch chuyển (dịch chuyển 100 pixel xuống dưới và 25 pixel sang phải)
   
# 3. Thay đổi kích thước ảnh
   Mục đích:
   * Phóng to ảnh
   Cấu trúc code:
   ```bash
   example = nd.zoom(data, (5, 5, 1))
   ```
   * `nd.zoom()`: Đây là một hàm từ thư viện scipy.ndimage, được dùng để phóng to ảnh
   * `(5, 5, 1)`: (tỷ lệ phóng to cho chiều thứ nhất, tỷ lệ phóng to cho chiều thứ 2, tỷ lệ phóng to cho chiều thứ 3)

# 4. Xoay ảnh
   Mục đích:
   * Xoay ảnh theo góc mong muốn
   Cấu trúc code:
   ```bash
   example = nd.rotate(data, 30)
   ```
   * `nd.rotate()`: Đây là một hàm từ thư viện scipy.ndimage, dùng để xoay ảnh
   * `30`: là số góc muốn xoay

# Lab3_XLAS: Các Biến Đổi Hình Học Cơ Bản Trên Ảnh

**Sinh viên thực hiện:** Lê Hoài Phương
**Mã số sinh viên:** 207CT10264
**Môn học:** Nhập môn Xử lý ảnh số
**Giảng viên:** Đỗ Hữu Quân

---

## Giới thiệu

Lab này tập trung vào việc khám phá và thực hành các phép biến đổi hình học cơ bản trên ảnh số. Chúng ta sẽ sử dụng các thư viện mạnh mẽ của Python như `NumPy`, `SciPy.ndimage`, `ImageIO`, và `Matplotlib` để thực hiện các thao tác như chọn vùng đối tượng, tịnh tiến, thay đổi kích thước và xoay ảnh.

## Các Thư Viện Sử Dụng

Để chạy các đoạn mã trong Lab này, bạn cần cài đặt các thư viện Python sau:

* **`numpy`**: Thư viện cơ bản cho tính toán số học với mảng đa chiều, nền tảng cho việc biểu diễn và thao tác dữ liệu ảnh.
* **`scipy`** (cụ thể là `scipy.ndimage`): Cung cấp các hàm xử lý ảnh đa chiều tiên tiến, bao gồm các phép biến đổi hình học.
* **`imageio`**: Dùng để đọc và ghi các định dạng tệp ảnh khác nhau một cách dễ dàng.
* **`matplotlib`** (cụ thể là `matplotlib.pyplot`): Dùng để hiển thị hình ảnh và trực quan hóa kết quả.

Bạn có thể cài đặt tất cả chúng bằng pip thông qua lệnh sau:

```bash
pip install numpy scipy imageio matplotlib
