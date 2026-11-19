# **CHUNK 4 – TRÍCH XUẤT KIẾN THỨC NHẬP MÔN KIẾN TRÚC MÁY TÍNH**

**Nguồn:** Giáo trình PDF, trang 121–158 (PDF Chunk 4).\
**Phương pháp:** MapReduce – đối chiếu với Chunk 1, 2 và 3.\
**Mục tiêu:** Chỉ ghi nhận kiến thức mới và phần kiến thức được mở rộng.

## **1. Khái niệm và kiến thức mới**

### **1.1. Cơ sở dữ liệu quan hệ (Relational Database)**

Kiến thức mới

- **Khái niệm:** Tập dữ liệu được tổ chức thành các bảng và liên kết với nhau bằng khóa.
- **Ví dụ:** Bảng sinh viên liên kết với bảng điểm thông qua mã số sinh viên.
- **SQL:** Sử dụng truy vấn để chọn, nối và tổng hợp dữ liệu giữa các bảng.
- **Lưu ý:** Thiết kế chuẩn hóa kém có thể gây trùng lặp dữ liệu.

Trang 128–129

### **1.2. Địa chỉ IP (IP Address)**

Kiến thức mới

- **Khái niệm:** Nhãn số dùng để định danh một thiết bị trong mạng.
- **Ví dụ:** Máy tính trong phòng thực hành có địa chỉ `192.168.1.20`.
- **DHCP:** Máy chủ DHCP cấp phát địa chỉ IP tự động cho thiết bị.
- **Lưu ý:** Hai thiết bị trùng địa chỉ IP có thể gây xung đột mạng.

Trang 137–140

### **1.3. Kiến trúc Client-Server**

Kiến thức mới

- **Khái niệm:** Mô hình trong đó máy khách (Client) gửi yêu cầu và máy chủ (Server) trả lời.
- **Ví dụ:** Ứng dụng xem điểm gửi yêu cầu đến máy chủ của trường.
- **Lưu ý:** Máy chủ có thể quá tải khi có nhiều người truy cập cùng lúc.

Trang 138–141

### **1.4. Mã hóa (Encryption)**

Kiến thức mới

- **Khái niệm:** Biến đổi dữ liệu để chỉ người có khóa phù hợp mới có thể đọc được.
- **Quy trình:**
  1. Bên gửi mã hóa dữ liệu bằng khóa.
  2. Dữ liệu được gửi qua mạng.
  3. Bên nhận giải mã bằng khóa tương ứng.
- **Lưu ý:** Nếu khóa bị lộ, dữ liệu có thể bị lộ.

Trang 146–148

## **2. Kiến thức được mở rộng từ Chunk 1–3**

| Chủ đề           | Nội dung bổ sung trong Chunk 4                                               |
| ---------------- | ---------------------------------------------------------------------------- |
| Network Protocol | Bên gửi đánh số gói tin; bên nhận xác nhận và yêu cầu gửi lại khi thiếu.     |
| Unit Testing     | Viết test trước và chạy tự động mỗi khi thay đổi mã nguồn.                   |
| Transaction      | Sử dụng ghi nhật ký và Rollback để khôi phục khi xảy ra lỗi.                 |
| Backup           | Định kỳ sao lưu, đánh dấu phiên bản và thử khôi phục dữ liệu.                |
| Virtual Memory   | Sử dụng Page Table để ánh xạ địa chỉ ảo sang địa chỉ vật lý.                 |
| Cache            | Nhấn mạnh nguy cơ dữ liệu Cache lỗi thời nếu không đồng bộ với bộ nhớ chính. |

### **2.1. Giao thức mạng (Network Protocol)**

- Gói tin có thể bị mất hoặc đến sai thứ tự.
- Bên gửi đánh số các gói tin.
- Bên nhận xác nhận và yêu cầu gửi lại khi thiếu.

Trang 130–132

### **2.2. Kiểm thử đơn vị (Unit Testing)**

- Kiểm tra từng hàm nhỏ một cách tự động.
- Ví dụ: Kiểm tra hàm tính điểm trung bình với danh sách rỗng.
- Cần viết test trước và chạy tự động mỗi khi thay đổi mã.
- Thiếu trường hợp biên (Edge Case) có thể khiến chương trình bỏ sót lỗi.

Trang 135–136

### **2.3. Giao dịch (Transaction)**

- Các thao tác trong một giao dịch phải cùng thành công hoặc cùng thất bại.
- Khi xảy ra lỗi giữa chừng, hệ thống sử dụng ghi nhật ký (Journal) và khôi phục lùi (Rollback).
- Mục đích: Tránh để dữ liệu ở trạng thái nửa vời.

Trang 149–150

### **2.4. Sao lưu (Backup)**

- Tạo bản sao dữ liệu ở nơi khác để khôi phục khi xảy ra mất mát.
- Ví dụ: Sao lưu cơ sở dữ liệu điểm mỗi đêm.
- Quy trình cần nhớ:
  1. Sao lưu định kỳ.
  2. Đánh dấu phiên bản.
  3. Thử khôi phục dữ liệu.
- Lưu ý: Bản sao lưu chưa từng được thử khôi phục có thể vô dụng.

Trang 151–152

### **2.5. Bộ nhớ ảo (Virtual Memory)**

- Cho phép tiến trình nhìn thấy không gian địa chỉ liên tục lớn hơn RAM thực tế.
- Ví dụ: Máy có 8 GB RAM vẫn có thể chạy chương trình cần nhiều bộ nhớ hơn nhờ tráo trang ra đĩa.
- **Page Table:** Bảng trang ánh xạ địa chỉ ảo sang địa chỉ vật lý.
- **Thrashing:** Tráo trang quá nhiều khiến máy tính hoạt động chậm.

Trang 153–155

## **3. Kiến thức cũ được nhắc lại – không cần học lại**

Các nội dung sau xuất hiện trong PDF nhưng đã được đề cập ở Chunk 1–3, không có bổ sung đáng kể:

- Scheduler: Round-robin, Ready Queue, Starvation.
- Thread: Bộ nhớ dùng chung, tranh chấp dữ liệu và Lock.
- Cache: Cache Hit, Cache Miss và truy cập RAM.
- SSD: Bộ nhớ flash và giới hạn số lần ghi.
- Interrupt: CPU tạm dừng để xử lý sự kiện.
- Git: Commit, lịch sử thay đổi và Conflict.
- Algorithm Complexity: O(N), O(log N), O(N²).

## **4. Tổng hợp kiến thức Chunk 4 sau đối chiếu**

| Nhóm           | Nội dung cần ghi nhớ                                             |
| -------------- | ---------------------------------------------------------------- |
| Kiến thức mới  | Relational Database, IP Address, DHCP, Client-Server, Encryption |
| Network        | Đánh số gói tin, xác nhận và gửi lại                             |
| Testing        | Viết test trước, tự động chạy lại khi thay đổi mã                |
| Transaction    | Journal và Rollback                                              |
| Backup         | Sao lưu, đánh dấu phiên bản, thử khôi phục                       |
| Virtual Memory | Page Table ánh xạ địa chỉ ảo và địa chỉ vật lý                   |
| Cache          | Nguy cơ dữ liệu lỗi thời khi không đồng bộ                       |

## **5. Lưu ý ôn tập**

Các kiến thức nên ưu tiên ghi nhớ:

1. Phân biệt cơ sở dữ liệu quan hệ và cách các bảng liên kết bằng khóa.
2. Hiểu IP Address và vai trò cấp phát IP tự động của DHCP.
3. Phân biệt Client và Server.
4. Nắm quy trình mã hóa và giải mã.
5. Nhớ cách xử lý gói tin bị mất trong giao thức mạng.
6. Hiểu vai trò của Page Table trong Virtual Memory.
7. Nắm quy trình sao lưu và thử khôi phục dữ liệu.
8. Hiểu tại sao Unit Testing cần kiểm tra trường hợp biên.


**Kết luận:** Chunk 4 bổ sung đáng kể kiến thức về cơ sở dữ liệu, định danh thiết bị mạng, Client-Server, mã hóa và mở rộng cách quản lý bộ nhớ, kiểm thử, sao lưu và giao dịch. Đây là những nội dung nên đưa vào bộ kiến thức tích lũy của môn học.
