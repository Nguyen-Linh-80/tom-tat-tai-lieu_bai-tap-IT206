# **TÓM TẮT CHUNK 5 – NHẬP MÔN KIẾN TRÚC MÁY TÍNH**

**Nguồn:** Giáo trình PDF, trang 159–194.\
**Phương pháp:** MapReduce – đối chiếu Chunk 1, 2, 3 và 4.\
**Mục đích:** Trích xuất kiến thức mới, kiến thức mở rộng và loại bỏ nội dung trùng lặp.

## **1. Kiến thức mới hoặc được mở rộng**

### **1.1. Kiến trúc Client-Server mở rộng**

- **Khái niệm:** Mô hình trong đó Client gửi yêu cầu và Server tiếp nhận, phản hồi.
- **Kiến thức mở rộng:** Khi nhiều người truy cập cùng lúc, Server có thể bị quá tải.
- **Giải pháp được đề cập:**
  - Load Balancing (Cân bằng tải): Phân phối yêu cầu để giảm áp lực lên máy chủ.
  - Server-side Cache (Bộ nhớ đệm phía máy chủ): Lưu dữ liệu thường dùng để hỗ trợ xử lý yêu cầu.
- **Ví dụ:** Ứng dụng xem điểm của trường có nhiều sinh viên truy cập cùng lúc.
- **Lưu ý:** Máy chủ quá tải có thể khiến hệ thống phản hồi chậm.

PDF trang 176–177, mục 20.1.

### **1.2. Địa chỉ IP mở rộng**

- **Khái niệm:** Địa chỉ IP là nhãn số dùng để định danh thiết bị trong mạng.
- **Kiến thức mở rộng:** Hai thiết bị trùng địa chỉ IP có thể gây xung đột.
- **DHCP:** Máy chủ có nhiệm vụ cấp phát địa chỉ IP tự động.
- **Ví dụ:** Máy tính trong phòng thực hành có địa chỉ `192.168.1.20`.
- **Lưu ý:** Cần tránh tình trạng hai thiết bị sử dụng cùng địa chỉ IP.

PDF trang 178–179, mục 20.2.

### **1.3. Hệ thống tệp mở rộng**

- **Khái niệm:** Hệ thống tệp quản lý cách tổ chức và đặt tên dữ liệu trên thiết bị lưu trữ.
- **Kiến thức mở rộng:** Mất điện giữa chừng có thể làm hỏng cấu trúc thư mục.
- **Journaling:** Ghi nhật ký các thao tác để hỗ trợ khôi phục hệ thống tệp sau sự cố.
- **Ví dụ:** Thư mục chứa các tệp bài tập của sinh viên.
- **Lưu ý:** Cần có cơ chế ghi nhật ký để hỗ trợ khôi phục khi xảy ra sự cố.

PDF trang 180–182, mục 20.3 và trang 187–189, mục 21.2.

### **1.4. Ổ thể rắn SSD mở rộng**

- **Khái niệm:** SSD là thiết bị lưu trữ sử dụng bộ nhớ Flash, không khả biến.
- **Đặc điểm:** Tốc độ truy cập được tài liệu nêu tính bằng micro-giây.
- **Kiến thức mở rộng:** Mỗi ô nhớ Flash có số lần ghi hữu hạn.
- **Giải pháp:** Bộ điều khiển SSD phân bổ đều thao tác ghi lên các ô nhớ.
- **Ví dụ:** Lưu tệp báo cáo trên SSD để mở lại vào ngày hôm sau.
- **Lưu ý:** Phân bổ thao tác ghi giúp hạn chế việc một số ô nhớ bị ghi quá nhiều.

PDF trang 191–194, mục 21.4.

## **2. Thuật ngữ quan trọng cần nhớ**

| Thuật ngữ         | Ý nghĩa                                  |
| ----------------- | ---------------------------------------- |
| Load Balancing    | Cân bằng tải giữa các máy chủ            |
| Server-side Cache | Bộ nhớ đệm phía máy chủ                  |
| DHCP              | Cấp phát địa chỉ IP tự động              |
| IP Conflict       | Xung đột địa chỉ IP                      |
| Journaling        | Ghi nhật ký thao tác để hỗ trợ khôi phục |
| SSD Controller    | Bộ điều khiển SSD                        |
| Flash Memory      | Bộ nhớ Flash                             |

## **3. Kiến thức cũ được nhắc lại**

Các nội dung sau đã xuất hiện trong Chunk 1–4, không cần học lại như khái niệm mới:

- Thread, Lock và tranh chấp dữ liệu.
- Scheduler, Ready Queue, Round-robin và Starvation.
- Cloud Computing và Virtual Machine.
- Encryption và Decryption.
- Transaction, Journal và Rollback.
- SSD và giới hạn số lần ghi.
- File System và Journaling.
- Client-Server và IP Address.
- Backup và khôi phục dữ liệu.

**Một số nội dung có mở rộng đáng chú ý:**

- Cloud Computing: Đặt hạn mức chi phí và cảnh báo sử dụng.
- Scheduler: Duyệt hàng đợi sẵn sàng và chọn tiến trình theo chính sách.
- Thread: Sử dụng Lock để bảo vệ dữ liệu dùng chung.

## **4. Quy trình và nguyên tắc cần nhớ**

1. **Client-Server:** Client gửi yêu cầu → Server tiếp nhận → Server phản hồi. Khi quá tải cần cân bằng tải và bộ nhớ đệm phía máy chủ.
2. **DHCP:** Máy chủ DHCP cấp phát địa chỉ IP tự động cho thiết bị.
3. **Journaling:** Ghi nhật ký thao tác → xảy ra sự cố → sử dụng nhật ký để hỗ trợ khôi phục.
4. **SSD:** Bộ điều khiển phân bổ đều thao tác ghi để hạn chế hao mòn các ô nhớ Flash.
5. **Cloud:** Theo dõi tài nguyên → đặt hạn mức chi phí → bật cảnh báo sử dụng.

## **5. Ví dụ và lưu ý quan trọng**

- Nhiều sinh viên cùng xem điểm có thể khiến Server quá tải.
- Hai máy tính sử dụng cùng địa chỉ IP có thể gây xung đột.
- Mất điện giữa lúc thao tác có thể làm hỏng cấu trúc hệ thống tệp.
- Quên tắt máy ảo thuê theo giờ có thể làm tăng chi phí.
- Để lộ khóa mã hóa có thể khiến dữ liệu bị xâm phạm.
- Không quản lý tốt thao tác ghi có thể làm một số ô nhớ SSD hao mòn nhanh hơn.

## **6. Kết luận đối chiếu Chunk 1–5**

**Kiến thức mới đáng chú ý nhất của Chunk 5:**

1. Load Balancing và Server-side Cache.
2. DHCP và IP Conflict.
3. Journaling trong khôi phục hệ thống tệp.
4. SSD Controller và phân bổ thao tác ghi.

Các nội dung còn lại chủ yếu củng cố hoặc mở rộng kiến thức đã học.

**Lưu ý về tài liệu:** PDF có nhiều đoạn văn lặp lại, một số mục bị trùng tên (19.4 Mã hóa và 20.4 Mã hóa). Vì vậy, phần tổng hợp trên đã loại bỏ các đoạn lặp, chỉ giữ kiến thức có giá trị. Không tự bổ sung các thuật toán hay cơ chế kỹ thuật mà tài liệu không trình bày.

giao-trinh-nhap-mon-kien-truc-may-tinh-159-194.pdf
