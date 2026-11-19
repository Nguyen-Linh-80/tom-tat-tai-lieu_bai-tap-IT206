# **TÓM TẮT CHUNK 2 – NHẬP MÔN KIẾN TRÚC MÁY TÍNH**

Nguồn: Giáo trình PDF, trang 38–73 

## **1. Khái niệm chính**

Chunk 2 tiếp tục mở rộng kiến thức về hệ điều hành, lưu trữ, mạng máy tính và kiểm thử phần mềm. Các nội dung đáng chú ý:

### **1.1. Bộ lập lịch (Scheduler)**

- Là thành phần lựa chọn tiến trình nào được chạy tiếp.
- Sử dụng hàng đợi sẵn sàng để lựa chọn tiến trình theo chính sách.
- Round-robin chia mỗi tiến trình một lát thời gian bằng nhau.
- Lập lịch không hợp lý có thể khiến tiến trình ưu tiên thấp bị thiếu tài nguyên.

Trang 40–41, 47–48, 64–65

### **1.2. Giao dịch (Transaction) – Mở rộng**

- Một giao dịch gồm nhiều thao tác phải cùng thành công hoặc cùng thất bại.
- Khi xảy ra lỗi giữa chừng, hệ thống sử dụng ghi nhật ký và rollback để khôi phục trạng thái trước đó.
- Giúp tránh dữ liệu chỉ được cập nhật một phần.

Trang 42–43

### **1.3. Sao lưu (Backup) – Mở rộng**

- Sao lưu tạo bản sao dữ liệu ở nơi khác để khôi phục khi mất dữ liệu.
- Cần thực hiện sao lưu định kỳ, đánh dấu phiên bản và thử khôi phục.
- Bản sao lưu chưa từng được thử khôi phục có thể không sử dụng được.

Trang 44–46, 60–63

### **1.4. Ổ thể rắn (SSD)**

- SSD là thiết bị lưu trữ flash không khả biến.
- Tốc độ truy cập được tính bằng micro-giây.
- Mỗi ô nhớ flash có số lần ghi hữu hạn.
- Bộ điều khiển cần phân bổ đều thao tác ghi lên các ô nhớ.

Trang 49–50

### **1.5. Giao thức mạng – Mở rộng**

- Giao thức mạng là tập hợp quy tắc để hai máy tính trao đổi dữ liệu.
- HTTP quy định cách trình duyệt yêu cầu trang web.
- Khi gói tin bị mất hoặc đến sai thứ tự, bên gửi cần đánh số gói, bên nhận xác nhận và yêu cầu gửi lại khi thiếu.

Trang 51–53

### **1.6. Điện toán đám mây – Mở rộng**

- Cho phép thuê tài nguyên tính toán qua mạng theo nhu cầu.
- Có thể thuê máy ảo theo giờ để chạy chương trình.
- Cần đặt hạn mức chi phí và cảnh báo sử dụng để tránh phát sinh chi phí ngoài dự kiến.

Trang 54–56, 72–73

### **1.7. Kiểm thử đơn vị (Unit Testing)**

- Là phương pháp kiểm tra tự động từng hàm nhỏ.
- Giúp phát hiện lỗi trong từng phần của chương trình.
- Cần viết kiểm thử và chạy tự động mỗi khi thay đổi mã nguồn.
- Phải chú ý các trường hợp biên để tránh bỏ sót lỗi.

Trang 56–57

### **1.8. Độ phức tạp thuật toán – Mở rộng**

- Đánh giá thời gian hoặc bộ nhớ cần thiết theo kích thước đầu vào.
- Tìm kiếm tuần tự có độ phức tạp O(N).
- Tìm kiếm nhị phân có độ phức tạp O(log N).
- Thuật toán O(N²) có thể chạy rất chậm khi dữ liệu lớn.

Trang 59–60

### **1.9. Tiến trình và luồng – Mở rộng**

- Tiến trình (Process): Chương trình đang chạy cùng không gian địa chỉ riêng.
- Luồng (Thread): Đơn vị thực thi nhỏ nhất trong một tiến trình, dùng chung bộ nhớ.
- Nhiều luồng cùng ghi một biến có thể gây tranh chấp dữ liệu.
- Cần sử dụng lock để bảo vệ vùng dữ liệu dùng chung.

Trang 66–70

## **2. Thuật ngữ quan trọng và định nghĩa ngắn gọn**

| Thuật ngữ       | Định nghĩa                                                          |
| --------------- | ------------------------------------------------------------------- |
| Scheduler       | Thành phần lựa chọn tiến trình được chạy tiếp.                      |
| Round-robin     | Phương pháp chia lát thời gian bằng nhau cho mỗi tiến trình.        |
| Ready Queue     | Hàng đợi chứa các tiến trình sẵn sàng chạy.                         |
| Starvation      | Tình trạng tiến trình bị thiếu tài nguyên do lập lịch không hợp lý. |
| Journal         | Nhật ký ghi lại thông tin giao dịch.                                |
| Rollback        | Khôi phục lùi khi giao dịch gặp lỗi.                                |
| Backup          | Tạo bản sao dữ liệu để khôi phục khi mất.                           |
| SSD             | Thiết bị lưu trữ flash không khả biến.                              |
| HTTP            | Giao thức quy định cách trình duyệt yêu cầu trang web.              |
| Virtual Machine | Máy ảo được sử dụng trong môi trường điện toán đám mây.             |
| Unit Testing    | Kiểm tra tự động từng hàm nhỏ.                                      |
| Edge Case       | Trường hợp biên cần kiểm tra để tránh bỏ sót lỗi.                   |
| O(N)            | Độ phức tạp tuyến tính.                                             |
| O(log N)        | Độ phức tạp logarithm.                                              |
| O(N²)           | Độ phức tạp bậc hai.                                                |

## **3. Kiến thức và quy trình cần nhớ**

### **3.1. Quy trình lập lịch tiến trình**

1. Các tiến trình được đưa vào hàng đợi sẵn sàng.
2. Scheduler duyệt hàng đợi.
3. Lựa chọn tiến trình theo chính sách lập lịch.
4. Round-robin chia thời gian chạy cho các tiến trình.

**Lưu ý:** Lập lịch không hợp lý có thể khiến tiến trình ưu tiên thấp bị đói tài nguyên.

### **3.2. Quy trình xử lý giao dịch**

1. Thực hiện các thao tác trong giao dịch.
2. Ghi nhật ký giao dịch.
3. Nếu thành công, giao dịch hoàn tất.
4. Nếu xảy ra lỗi, sử dụng rollback để khôi phục.

### **3.3. Quy trình sao lưu dữ liệu**

1. Thực hiện sao lưu định kỳ.
2. Đánh dấu phiên bản bản sao lưu.
3. Thử khôi phục dữ liệu.
4. Kiểm tra khả năng sử dụng bản sao lưu.

### **3.4. Quy trình kiểm thử đơn vị**

1. Viết test cho từng hàm nhỏ.
2. Chú ý các trường hợp biên.
3. Chạy kiểm thử tự động.
4. Thực hiện lại kiểm thử mỗi khi thay đổi mã nguồn.

### **3.5. Phân tích độ phức tạp thuật toán**

- Xác định kích thước đầu vào N.
- Phân tích số lần thực hiện thao tác hoặc vòng lặp.
- Xác định mức độ tăng của thời gian hoặc bộ nhớ.
- Ước lượng độ phức tạp thuật toán.

## **4. Ví dụ và lưu ý quan trọng**

| Nội dung       | Ví dụ trong giáo trình                                | Lưu ý                                        |
| -------------- | ----------------------------------------------------- | -------------------------------------------- |
| Scheduler      | Round-robin chia thời gian cho các tiến trình.        | Lập lịch kém gây thiếu tài nguyên.           |
| Transaction    | Chuyển tiền gồm trừ tài khoản A và cộng tài khoản B.  | Lỗi giữa chừng gây dữ liệu không hoàn chỉnh. |
| Backup         | Sao lưu cơ sở dữ liệu điểm mỗi đêm.                   | Phải thử khôi phục.                          |
| SSD            | Lưu tệp báo cáo để mở lại hôm sau.                    | Mỗi ô nhớ flash có số lần ghi hữu hạn.       |
| Giao thức mạng | Trình duyệt sử dụng HTTP để yêu cầu trang web.        | Gói tin có thể mất hoặc sai thứ tự.          |
| Cloud          | Thuê máy ảo theo giờ để chạy bài chấm tự động.        | Quên tắt tài nguyên làm tăng chi phí.        |
| Unit Testing   | Kiểm tra hàm tính điểm trung bình với danh sách rỗng. | Thiếu trường hợp biên có thể bỏ sót lỗi.     |
| Độ phức tạp    | Tìm kiếm tuần tự O(N), tìm kiếm nhị phân O(log N).    | O(N²) chậm khi dữ liệu lớn.                  |
| Process        | Mỗi cửa sổ trình soạn thảo là một tiến trình.         | Tiến trình lỗi có thể chiếm hết bộ nhớ.      |
| Thread         | Một luồng tải tệp, một luồng vẽ giao diện.            | Hai luồng cùng ghi một biến gây tranh chấp.  |

## **5. Kiến thức mới của Chunk 2**

Đây là phần quan trọng nhất để sử dụng khi tổng hợp Chunk 1 và Chunk 2.

Các kiến thức dưới đây chỉ ghi nhận phần bổ sung, không viết lại toàn bộ khái niệm đã học ở Chunk 1.

| Kiến thức đã có ở Chunk 1 | Phần kiến thức mới được bổ sung                                           |
| ------------------------- | ------------------------------------------------------------------------- |
| Scheduler                 | Round-robin, hàng đợi sẵn sàng và nguy cơ starvation.                     |
| Transaction               | Ghi nhật ký giao dịch trước khi sử dụng rollback.                         |
| Backup                    | Sao lưu định kỳ, đánh dấu phiên bản và thử khôi phục.                     |
| SSD                       | Bộ điều khiển phân bổ đều thao tác ghi vì số lần ghi flash hữu hạn.       |
| Giao thức mạng            | Đánh số gói tin, xác nhận và yêu cầu gửi lại khi thiếu.                   |
| Điện toán đám mây         | Đặt hạn mức chi phí và cảnh báo sử dụng.                                  |
| Độ phức tạp thuật toán    | So sánh O(N), O(log N), O(N²) và phân tích vòng lặp lồng nhau.            |
| Process                   | Hệ điều hành tạo, lập lịch và kết thúc tiến trình.                        |
| Thread                    | Hai luồng có thể tranh chấp khi cùng ghi dữ liệu; sử dụng lock để bảo vệ. |

**Kiến thức hoàn toàn mới so với bản tóm tắt Chunk 1:**

1. **SSD:** Đặc điểm lưu trữ flash và giới hạn số lần ghi.
2. **Unit Testing:** Kiểm thử từng hàm nhỏ, kiểm tra trường hợp biên và tự động chạy lại khi sửa code.
3. **Round-robin:** Phương pháp chia lát thời gian cho tiến trình.
4. **Starvation:** Nguy cơ tiến trình ưu tiên thấp bị thiếu tài nguyên.
5. **Edge Case:** Các trường hợp biên cần đưa vào kiểm thử.

## **6. Kết luận Chunk 2**

Chunk 2 mở rộng kiến thức về cách hệ điều hành quản lý tiến trình, cách lưu trữ và bảo vệ dữ liệu, cách truyền dữ liệu qua mạng và cách kiểm thử chương trình.

**Các nội dung cần ưu tiên ghi nhớ:**

- Scheduler và Round-robin.
- Transaction, Journal và Rollback.
- Backup và quy trình khôi phục.
- SSD và giới hạn ghi flash.
- Unit Testing và Edge Case.
- Độ phức tạp O(N), O(log N), O(N²).
- Process, Thread và Lock.

Ghi chú nguồn: Các số trang là số trang in trên giáo trình PDF, không phải số thứ tự trang của trình đọc PDF.
