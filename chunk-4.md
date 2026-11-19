# **TÓM TẮT CHUNK 4 – NHẬP MÔN KIẾN TRÚC MÁY TÍNH**

**Môn học:** Nhập môn Kiến trúc máy tính\
**Nguồn:** Giáo trình PDF Chunk 4 (trang 74–120)\
**Phương pháp:** MapReduce\
**Mục đích:** Trích xuất kiến thức mới và phần mở rộng so với Chunk 1, 2 và 3.

## **1. Khái niệm và kiến thức mới**

### **1.1. Giao dịch (Transaction)**

Mở rộng kiến thức cũ

- Transaction là nhóm thao tác phải cùng thành công hoặc cùng thất bại.
- Ví dụ: Chuyển tiền gồm hai thao tác: trừ tiền tài khoản A và cộng tiền tài khoản B.
- Nếu xảy ra lỗi giữa chừng, dữ liệu có thể ở trạng thái chưa hoàn chỉnh.
- Cần sử dụng ghi nhật ký và khôi phục lùi (Rollback) để xử lý lỗi.

**Điểm cần nhớ:** Không để giao dịch chỉ thực hiện thành công một phần.

*Trang 74–76.*

### **1.2. Giao thức mạng (Network Protocol)**

Mở rộng kiến thức cũ

- Giao thức mạng là tập hợp quy tắc giúp hai máy trao đổi dữ liệu.
- HTTP quy định cách trình duyệt yêu cầu trang web.
- Dữ liệu truyền qua mạng có thể bị mất hoặc đến sai thứ tự.

**Cơ chế xử lý:**

1. Bên gửi đánh số các gói tin.
2. Bên nhận xác nhận gói tin đã nhận.
3. Nếu thiếu gói tin, bên nhận yêu cầu gửi lại.

**Ví dụ:** Trình duyệt gửi yêu cầu HTTP để lấy nội dung trang web.

*Trang 76–78.*

### **1.3. Tiến trình (Process)**

Mở rộng kiến thức cũ

- Process là một chương trình đang chạy cùng không gian địa chỉ riêng.
- Mỗi tiến trình có vùng bộ nhớ riêng.
- Ví dụ: Mỗi cửa sổ trình soạn thảo có thể được xem là một tiến trình.
- Rủi ro: Tiến trình gặp lỗi hoặc sử dụng quá nhiều bộ nhớ có thể ảnh hưởng đến hệ thống.

*Trang 79–80.*

### **1.4. Kiểm thử đơn vị (Unit Testing)**

Kiến thức được củng cố

- Unit Testing là kiểm tra từng hàm nhỏ một cách tự động.
- Mục đích: Phát hiện lỗi trong từng thành phần của chương trình.
- Ví dụ: Kiểm tra hàm tính điểm trung bình với danh sách rỗng.
- Lưu ý: Nếu thiếu các trường hợp biên (Edge Case), kiểm thử có thể bỏ sót lỗi.

*Trang 81–83.*

### **1.5. Sao lưu (Backup)**

Mở rộng kiến thức cũ

- Backup là tạo bản sao dữ liệu ở nơi khác để khôi phục khi dữ liệu gốc bị mất.
- Ví dụ: Sao lưu cơ sở dữ liệu điểm vào mỗi đêm.

**Quy trình cần nhớ:**

1. Sao lưu dữ liệu định kỳ.
2. Đánh dấu và quản lý phiên bản bản sao lưu.
3. Thử khôi phục dữ liệu để kiểm tra khả năng sử dụng.

**Lưu ý:** Bản sao lưu chưa từng được thử khôi phục có thể vô dụng.

*Trang 88–89.*

### **1.6. Độ phức tạp thuật toán (Algorithm Complexity)**

Mở rộng kiến thức cũ

- Là thước đo thời gian hoặc bộ nhớ mà thuật toán sử dụng theo kích thước đầu vào.
- O(N): Tìm kiếm tuần tự.
- O(log N): Tìm kiếm nhị phân.
- O(N²): Thường xuất hiện khi có vòng lặp lồng nhau và chạy chậm khi dữ liệu lớn.

**Điểm cần nhớ:** Phân tích số vòng lặp, đặc biệt là vòng lặp lồng nhau, để ước lượng độ phức tạp.

*Trang 94–96.*

### **1.7. Bộ nhớ đệm (Cache)**

Mở rộng kiến thức cũ

- Cache là vùng nhớ nhỏ, tốc độ cao, nằm gần CPU.
- Dùng để giữ bản sao của dữ liệu thường xuyên được sử dụng.
- Ví dụ: CPU đọc cùng một mảng số nhiều lần, các phần tử có thể được giữ trong Cache.

**Kiến thức bổ sung:**

- Dữ liệu trong Cache có thể bị lỗi thời nếu không được đồng bộ với bộ nhớ chính.
- CPU cần kiểm tra và bảo đảm dữ liệu Cache phù hợp với bộ nhớ chính.

*Trang 97–99.*

### **1.8. Hệ thống tệp (File System)**

Mở rộng kiến thức cũ

- File System tổ chức và đặt tên dữ liệu trên thiết bị lưu trữ.
- Ví dụ: Thư mục chứa các tệp bài tập của sinh viên.
- Rủi ro: Mất điện giữa chừng có thể làm hỏng cấu trúc thư mục.
- Cần sử dụng ghi nhật ký (Journaling) để hỗ trợ khôi phục sau sự cố.

*Trang 102–103.*

### **1.9. Quản lý phiên bản (Version Control)**

Mở rộng kiến thức cũ

- Git lưu lại lịch sử thay đổi mã nguồn thông qua các lần Commit.
- Khi hai người sửa cùng một dòng, có thể xảy ra xung đột (Conflict).

**Quy trình xử lý:**

1. Tạo nhánh (Branch).
2. Thực hiện chỉnh sửa.
3. Gộp nhánh (Merge).
4. Giải quyết xung đột nếu có (Conflict Resolution).

*Trang 111–112.*

### **1.10. Ổ thể rắn (SSD)**

Mở rộng kiến thức cũ

- SSD sử dụng bộ nhớ flash không khả biến (Non-Volatile).
- Tốc độ truy cập tính bằng micro-giây.
- Mỗi ô nhớ flash có số lần ghi hữu hạn.
- Bộ điều khiển cần phân bổ đều thao tác ghi lên các ô nhớ.

**Điểm cần nhớ:** Phân phối thao tác ghi giúp tránh tập trung ghi quá nhiều vào một ô nhớ.

*Trang 113–115.*

### **1.11. Ngắt (Interrupt)**

Mở rộng kiến thức cũ

- Interrupt là tín hiệu yêu cầu CPU tạm dừng công việc hiện tại để xử lý sự kiện.
- Ví dụ: Bàn phím gửi ngắt khi người dùng nhấn phím.
- Quá nhiều ngắt liên tiếp có thể khiến hệ thống chậm.

**Quy trình xử lý:**

1. CPU lưu trạng thái hiện tại.
2. CPU chuyển đến trình xử lý ngắt.
3. Xử lý sự kiện.
4. Quay lại công việc đang thực hiện.

*Trang 115–117.*

### **1.12. Hệ thống tệp (File System)**

Mở rộng kiến thức cũ

- File System tổ chức và đặt tên dữ liệu trên thiết bị lưu trữ.
- Ví dụ: Thư mục chứa các tệp bài tập.
- Mất điện giữa chừng có thể làm hỏng cấu trúc thư mục.
- Cần ghi nhật ký (Journaling) để hỗ trợ khôi phục sau sự cố.

*Trang 117–120.*

## **2. Thuật ngữ quan trọng của Chunk 4**

| Thuật ngữ             | Giải thích ngắn                                     |
| --------------------- | --------------------------------------------------- |
| Process               | Chương trình đang chạy, có không gian địa chỉ riêng |
| Unit Testing          | Kiểm thử từng hàm nhỏ                               |
| Backup                | Sao lưu dữ liệu                                     |
| Edge Case             | Trường hợp biên cần kiểm tra                        |
| Network Protocol      | Quy tắc trao đổi dữ liệu                            |
| Conflict Resolution   | Giải quyết xung đột mã nguồn                        |
| Commit                | Lưu lại một lần thay đổi trong Git                  |
| Journaling            | Ghi nhật ký để hỗ trợ khôi phục                     |
| Non-Volatile          | Không mất dữ liệu khi tắt nguồn                     |
| Write Distribution    | Phân bổ thao tác ghi lên các ô nhớ                  |
| Cache Synchronization | Đồng bộ dữ liệu Cache với bộ nhớ chính              |
| Interrupt Handler     | Trình xử lý ngắt                                    |

## **3. Đối chiếu Chunk 1–3 và Chunk 4**

| Chủ đề       | Kiến thức được bổ sung trong Chunk 4                 |
| ------------ | ---------------------------------------------------- |
| Transaction  | Nhấn mạnh xử lý lỗi giữa giao dịch                   |
| Network      | Đánh số, xác nhận và yêu cầu gửi lại gói tin         |
| Process      | Không gian địa chỉ riêng                             |
| Unit Testing | Kiểm tra hàm với danh sách rỗng                      |
| Backup       | Quản lý phiên bản và thử khôi phục                   |
| Complexity   | Phân tích số vòng lặp lồng nhau                      |
| Cache        | Nguy cơ dữ liệu lỗi thời và đồng bộ                  |
| File System  | Journaling hỗ trợ khôi phục                          |
| Git          | Quy trình Branch → sửa → Merge → giải quyết Conflict |
| SSD          | Bộ điều khiển phân bổ đều thao tác ghi               |
| Interrupt    | Lưu trạng thái CPU và quay lại công việc             |
| RAM          | Hệ điều hành cấp phát và thu hồi vùng nhớ            |
| Thread       | Tiếp tục nhấn mạnh tranh chấp dữ liệu và Lock        |

## **4. Kiến thức trọng tâm cần ôn thi**

Ưu tiên ghi nhớ các nội dung sau:

1. **Transaction:** Cơ chế Rollback khi giao dịch gặp lỗi.
2. **Network Protocol:** Đánh số gói tin, xác nhận và gửi lại khi thiếu.
3. **Process:** Chương trình đang chạy và không gian địa chỉ riêng.
4. **Unit Testing:** Kiểm tra từng hàm và trường hợp biên.
5. **Backup:** Sao lưu định kỳ, quản lý phiên bản, thử khôi phục.
6. **Complexity:** Phân biệt O(N), O(log N), O(N²).
7. **Cache:** Nguy cơ dữ liệu lỗi thời và đồng bộ.
8. **Journaling:** Ghi nhật ký để khôi phục sau sự cố.
9. **SSD:** Số lần ghi hữu hạn, cần phân bổ đều thao tác ghi.
10. **Interrupt:** Lưu trạng thái → xử lý ngắt → quay lại.
11. **Git:** Branch, Commit, Merge và Conflict Resolution.

## **5. Lưu ý khi học Chunk 4**

- Không học lại định nghĩa cũ nếu không có nội dung bổ sung.
- Chú ý phân biệt Process và Thread.
- Không nhầm Backup với Journaling: Backup tạo bản sao dữ liệu, Journaling ghi nhật ký hỗ trợ khôi phục.
- Không nhầm RAM với SSD: RAM khả biến, SSD không khả biến.
- Chú ý các câu hỏi tình huống: mất điện, mất gói tin, dữ liệu lỗi thời, tranh chấp dữ liệu và xung đột mã nguồn.

**Kết luận:** Chunk 4 chủ yếu củng cố và mở rộng kiến thức từ Chunk 1–3. Những phần đáng chú ý nhất là cơ chế xác nhận gói tin, kiểm thử đơn vị, quy trình kiểm tra Backup, đồng bộ Cache, phân bổ thao tác ghi SSD và xử lý Interrupt.

giao-trinh-nhap-mon-kien-truc-may-tinh-74-120.pdf
