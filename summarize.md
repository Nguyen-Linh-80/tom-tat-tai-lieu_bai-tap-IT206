# TỔNG HỢP KIẾN THỨC CHUNK 1–5
**Môn học:** Nhập môn Kiến trúc máy tính  
**Phương pháp:** MapReduce – Reduce  
**Phạm vi:** Chunk 1–5

## 1. Các khái niệm cốt lõi

### 1.1. CPU và hệ thống bộ nhớ

- **CPU:** Bộ phận xử lý các công việc của máy tính.
- **RAM:** Bộ nhớ tạm, có tính khả biến; dữ liệu bị mất khi tắt nguồn. Hệ điều hành cấp phát và thu hồi RAM cho các tiến trình.
- **SSD:** Thiết bị lưu trữ sử dụng bộ nhớ Flash không khả biến, có giới hạn số lần ghi trên mỗi ô nhớ.
- **Cache:** Bộ nhớ đệm nhỏ, tốc độ cao, nằm gần CPU, lưu bản sao dữ liệu thường xuyên sử dụng nhằm giảm truy cập RAM.
- **Bộ nhớ ảo (Virtual Memory):** Kỹ thuật giúp tiến trình nhìn thấy không gian địa chỉ liên tục lớn hơn RAM thực tế.

### 1.2. Hệ điều hành và quản lý tiến trình

- **Process (Tiến trình):** Chương trình đang chạy với không gian địa chỉ riêng.
- **Thread (Luồng):** Đơn vị thực thi nhỏ nhất trong một tiến trình. Các luồng cùng tiến trình có thể dùng chung bộ nhớ.
- **Scheduler (Bộ lập lịch):** Thành phần lựa chọn tiến trình được chạy tiếp.
- **Interrupt (Ngắt):** Tín hiệu yêu cầu CPU tạm dừng công việc hiện tại để xử lý một sự kiện.
- **Lock:** Khóa bảo vệ vùng dữ liệu dùng chung giữa các luồng.

### 1.3. Xử lý dữ liệu và lưu trữ

- **Transaction (Giao dịch):** Nhóm thao tác phải cùng thành công hoặc cùng thất bại.
- **Rollback:** Khôi phục trạng thái trước đó khi giao dịch gặp lỗi.
- **Backup (Sao lưu):** Tạo bản sao dữ liệu ở nơi khác để khôi phục khi mất dữ liệu.
- **File System (Hệ thống tệp):** Cách tổ chức và đặt tên dữ liệu trên thiết bị lưu trữ.
- **Journaling:** Ghi nhật ký thao tác nhằm hỗ trợ khôi phục hệ thống tệp sau sự cố.

### 1.4. Mạng máy tính và bảo mật

- **IP Address:** Nhãn số dùng để định danh thiết bị trong mạng.
- **DHCP:** Máy chủ cấp phát địa chỉ IP tự động.
- **Network Protocol:** Tập hợp quy tắc giúp các máy tính trao đổi dữ liệu.
- **HTTP:** Giao thức quy định cách trình duyệt yêu cầu trang web.
- **Client-Server:** Mô hình trong đó Client gửi yêu cầu và Server tiếp nhận, phản hồi.
- **Encryption (Mã hóa):** Biến đổi dữ liệu để chỉ người có khóa phù hợp mới đọc được.

### 1.5. Các khái niệm khác

- **Algorithm Complexity:** Thước đo thời gian hoặc bộ nhớ cần thiết theo kích thước đầu vào.
- **Version Control:** Quản lý lịch sử thay đổi mã nguồn.
- **Relational Database:** Cơ sở dữ liệu tổ chức dữ liệu thành các bảng và liên kết bằng khóa.
- **Unit Testing:** Kiểm tra tự động từng hàm nhỏ trong chương trình.
- **Cloud Computing:** Thuê tài nguyên tính toán qua mạng theo nhu cầu.

## 2. Thuật ngữ quan trọng

| Thuật ngữ | Giải thích |
|---|---|
| Ready Queue | Hàng đợi chứa các tiến trình sẵn sàng chạy. |
| Round-robin | Chia mỗi tiến trình một lát thời gian bằng nhau. |
| Starvation | Tiến trình bị thiếu tài nguyên do lập lịch không hợp lý. |
| Data Race | Tranh chấp khi nhiều luồng cùng truy cập hoặc thay đổi dữ liệu. |
| Cache Hit | Tìm thấy dữ liệu trong Cache. |
| Cache Miss | Không tìm thấy dữ liệu trong Cache. |
| Main Memory | Bộ nhớ chính, trong ngữ cảnh này là RAM. |
| Page Table | Bảng ánh xạ địa chỉ ảo sang địa chỉ vật lý. |
| Thrashing | Hiện tượng máy chậm do tráo trang quá nhiều. |
| Journal | Nhật ký ghi lại thông tin giao dịch hoặc thao tác. |
| Edge Case | Trường hợp biên cần kiểm tra để tránh bỏ sót lỗi. |
| O(N) | Độ phức tạp tuyến tính. |
| O(log N) | Độ phức tạp logarithm. |
| O(N²) | Độ phức tạp bậc hai. |
| Branch | Nhánh riêng trong quản lý phiên bản. |
| Commit | Lần ghi nhận thay đổi trong Git. |
| Merge | Gộp các nhánh mã nguồn. |
| Conflict | Xung đột khi hợp nhất thay đổi. |
| Load Balancing | Cân bằng tải giữa các máy chủ. |
| Server-side Cache | Bộ nhớ đệm phía máy chủ. |
| IP Conflict | Xung đột địa chỉ IP. |
| Flash Memory | Bộ nhớ Flash được sử dụng trong SSD. |
| SSD Controller | Bộ điều khiển SSD, phân bổ thao tác ghi lên các ô nhớ. |
| Virtual Machine | Máy ảo sử dụng trong môi trường điện toán đám mây. |
| SQL | Ngôn ngữ sử dụng truy vấn để chọn, nối và tổng hợp dữ liệu giữa các bảng. |

## 3. Quy trình và cơ chế cần nhớ

### 3.1. Quy trình xử lý Interrupt

1. CPU đang thực hiện công việc.
2. Nhận tín hiệu ngắt.
3. Lưu trạng thái CPU hiện tại.
4. Chuyển đến Interrupt Handler.
5. Xử lý sự kiện.
6. Khôi phục trạng thái.
7. Tiếp tục công việc trước đó.

**Lưu ý:** Quá nhiều ngắt liên tiếp có thể khiến hệ thống chậm.

### 3.2. Quy trình quản lý tiến trình

1. Hệ điều hành tạo tiến trình.
2. Các tiến trình sẵn sàng được đưa vào Ready Queue.
3. Scheduler lựa chọn tiến trình theo chính sách lập lịch.
4. Round-robin chia thời gian chạy cho các tiến trình.
5. Tiến trình kết thúc và hệ điều hành thu hồi tài nguyên.

**Lưu ý:** Lập lịch không hợp lý có thể khiến tiến trình ưu tiên thấp bị Starvation.

### 3.3. Cơ chế hoạt động của Cache

1. CPU cần dữ liệu.
2. Kiểm tra dữ liệu trong Cache.
3. Nếu tìm thấy: Cache Hit, đọc dữ liệu từ Cache.
4. Nếu không tìm thấy: Cache Miss, đọc dữ liệu từ RAM và nạp bản sao vào Cache.
5. Tiếp tục xử lý.

**Lưu ý:**
- Cache giúp giảm nhu cầu truy cập trực tiếp RAM.
- Dữ liệu Cache có thể lỗi thời nếu không đồng bộ với bộ nhớ chính.
- Theo số liệu trong tài liệu, tỷ lệ trúng Cache 95% giúp thời gian truy cập trung bình giảm 40%.

### 3.4. Cơ chế bảo vệ dữ liệu bằng Lock

1. Nhiều Thread cùng hoạt động.
2. Kiểm tra xem có cùng truy cập hoặc ghi một biến không.
3. Nếu có, xuất hiện nguy cơ Data Race.
4. Sử dụng Lock để bảo vệ vùng dữ liệu dùng chung.

**Nguyên tắc:** Các Thread trong cùng Process có thể dùng chung bộ nhớ nên cần bảo vệ dữ liệu khi nhiều luồng cùng thao tác.

### 3.5. Quy trình xử lý Transaction

1. Thực hiện các thao tác trong giao dịch.
2. Ghi nhật ký giao dịch (Journal).
3. Nếu thành công, giao dịch hoàn tất.
4. Nếu xảy ra lỗi, sử dụng Rollback để khôi phục trạng thái trước đó.

**Mục đích:** Tránh dữ liệu chỉ được cập nhật một phần.

### 3.6. Quy trình Backup

1. Thực hiện sao lưu định kỳ.
2. Đánh dấu phiên bản bản sao lưu.
3. Thử khôi phục dữ liệu.
4. Kiểm tra khả năng sử dụng bản sao lưu.

**Lưu ý:** Bản sao lưu chưa từng được thử khôi phục có thể không sử dụng được.

### 3.7. Quy trình quản lý phiên bản bằng Git

1. Tạo Branch.
2. Chỉnh sửa mã nguồn trên nhánh.
3. Thực hiện Merge để gộp nhánh.
4. Kiểm tra có Conflict hay không.
5. Nếu có, thực hiện Conflict Resolution.
6. Hoàn tất quá trình hợp nhất.

### 3.8. Quy trình phân tích độ phức tạp thuật toán

1. Xác định kích thước dữ liệu đầu vào N.
2. Quan sát số lần thực hiện thao tác hoặc vòng lặp.
3. Kiểm tra có vòng lặp lồng nhau hay không.
4. Ước lượng độ phức tạp thời gian hoặc bộ nhớ.

| Cách thực hiện | Độ phức tạp |
|---|---|
| Một vòng lặp duyệt N phần tử | O(N) |
| Tìm kiếm nhị phân | O(log N) |
| Hai vòng lặp lồng nhau | O(N²) |

### 3.9. Quy trình trao đổi dữ liệu qua mạng

1. Hai máy tính tuân theo giao thức mạng.
2. Bên gửi đánh số các gói tin.
3. Bên nhận tiếp nhận và xác nhận.
4. Nếu thiếu gói tin, bên nhận yêu cầu gửi lại.

**Lưu ý:** Gói tin có thể bị mất hoặc đến sai thứ tự.

### 3.10. Quy trình mã hóa dữ liệu

1. Bên gửi mã hóa dữ liệu bằng khóa.
2. Dữ liệu được gửi qua mạng.
3. Bên nhận giải mã bằng khóa tương ứng.

**Lưu ý:** Nếu khóa bị lộ, dữ liệu có thể bị xâm phạm.

### 3.11. Quy trình Client-Server

1. Client gửi yêu cầu.
2. Server tiếp nhận yêu cầu.
3. Server xử lý và phản hồi Client.

**Khi Server quá tải:**
- Sử dụng Load Balancing để phân phối yêu cầu, giảm áp lực lên máy chủ.
- Sử dụng Server-side Cache để lưu dữ liệu thường dùng, hỗ trợ xử lý yêu cầu.

### 3.12. Quản lý hệ thống tệp bằng Journaling

1. Hệ thống tệp tổ chức và đặt tên dữ liệu.
2. Ghi nhật ký các thao tác.
3. Khi xảy ra sự cố, sử dụng nhật ký để hỗ trợ khôi phục.

**Phân biệt:**
- Journaling: Hỗ trợ khôi phục hệ thống tệp sau sự cố.
- Backup: Tạo bản sao dữ liệu để khôi phục khi mất.

### 3.13. Quản lý bộ nhớ ảo

- Sử dụng Virtual Memory để cung cấp không gian địa chỉ lớn hơn RAM thực tế.
- Tráo trang ra đĩa khi cần.
- Page Table ánh xạ địa chỉ ảo sang địa chỉ vật lý.
- Tráo trang quá nhiều có thể gây Thrashing và làm máy tính chậm.

### 3.14. Quản lý tài nguyên Cloud

1. Thuê tài nguyên tính toán qua mạng theo nhu cầu.
2. Theo dõi mức sử dụng tài nguyên.
3. Đặt hạn mức chi phí.
4. Bật cảnh báo sử dụng.

**Lưu ý:** Quên tắt máy ảo hoặc tài nguyên thuê theo giờ có thể làm tăng chi phí.

### 3.15. Quy trình Unit Testing

1. Viết test cho từng hàm nhỏ.
2. Chú ý các trường hợp biên (Edge Case).
3. Chạy kiểm thử tự động.
4. Thực hiện lại kiểm thử mỗi khi thay đổi mã nguồn.

**Lưu ý:** Thiếu trường hợp biên có thể khiến chương trình bỏ sót lỗi.

## 4. Ví dụ và tình huống thực tế

| Chủ đề | Ví dụ | Điều cần ghi nhớ |
|---|---|---|
| RAM | Trình duyệt giữ các tab đang mở trong RAM. | Dữ liệu chưa lưu có thể mất khi tắt máy. |
| Interrupt | Bàn phím gửi tín hiệu ngắt khi người dùng nhấn phím. | CPU phải lưu trạng thái trước khi xử lý. |
| Transaction | Chuyển tiền gồm trừ tài khoản A và cộng tài khoản B. | Hai thao tác phải cùng thành công hoặc thất bại. |
| Process | Mỗi cửa sổ trình soạn thảo là một tiến trình. | Tiến trình có không gian địa chỉ riêng. |
| Thread | Một luồng tải tệp, một luồng vẽ giao diện. | Hai luồng cùng ghi một biến có thể gây tranh chấp. |
| Cache | CPU đọc cùng một mảng số nhiều lần. | Cache giúp giảm truy cập RAM. |
| SSD | Lưu tệp báo cáo để mở lại hôm sau. | Ô nhớ Flash có giới hạn số lần ghi. |
| Git | Các thành viên nhóm cùng chỉnh sửa mã nguồn. | Có thể phát sinh Conflict khi sửa cùng dòng. |
| Backup | Sao lưu cơ sở dữ liệu điểm mỗi đêm. | Cần thử khôi phục dữ liệu. |
| Unit Testing | Kiểm tra hàm tính điểm trung bình với danh sách rỗng. | Cần kiểm tra trường hợp biên. |
| Virtual Memory | Máy có 8 GB RAM vẫn chạy chương trình cần nhiều bộ nhớ hơn nhờ tráo trang ra đĩa. | Cần hiểu vai trò Page Table và nguy cơ Thrashing. |
| HTTP | Trình duyệt yêu cầu trang web. | HTTP quy định cách gửi yêu cầu. |
| Client-Server | Ứng dụng xem điểm gửi yêu cầu đến máy chủ trường. | Nhiều người truy cập có thể khiến Server quá tải. |
| IP Address | Máy tính phòng thực hành có IP 192.168.1.20. | Không để hai thiết bị trùng IP. |
| Relational Database | Bảng sinh viên liên kết bảng điểm qua mã số sinh viên. | Các bảng được liên kết bằng khóa. |
| Encryption | Bên gửi mã hóa dữ liệu trước khi truyền. | Cần bảo vệ khóa mã hóa. |
| Cloud | Thuê máy ảo theo giờ để chạy chương trình chấm tự động. | Cần kiểm soát chi phí và tắt tài nguyên khi không sử dụng. |

## 5. Những điểm dễ nhầm lẫn và lưu ý

### 5.1. Phân biệt các khái niệm

| Hai khái niệm | Điểm khác nhau |
|---|---|
| RAM và SSD | RAM là bộ nhớ tạm, khả biến; SSD là thiết bị lưu trữ Flash không khả biến. |
| Process và Thread | Process có không gian địa chỉ riêng; các Thread trong cùng Process có thể dùng chung bộ nhớ. |
| Cache Hit và Cache Miss | Hit là tìm thấy dữ liệu trong Cache; Miss là phải truy cập RAM. |
| Journaling và Backup | Journaling hỗ trợ khôi phục hệ thống tệp; Backup tạo bản sao dữ liệu. |
| Transaction và Rollback | Transaction là nhóm thao tác; Rollback là cơ chế khôi phục khi giao dịch gặp lỗi. |
| Client và Server | Client gửi yêu cầu; Server tiếp nhận và phản hồi. |
| Branch và Merge | Branch tạo nhánh riêng; Merge gộp các nhánh. |
| O(N) và O(log N) | O(N) là tuyến tính; O(log N) là logarithm. |
| O(N) và O(N²) | O(N²) có thể chậm hơn đáng kể khi dữ liệu lớn. |
| Virtual Memory và RAM | Virtual Memory cung cấp không gian địa chỉ lớn hơn RAM thực tế mà tiến trình nhìn thấy. |

### 5.2. Các rủi ro cần tránh

1. **Mạng:** Hai thiết bị trùng địa chỉ IP gây xung đột.
2. **Interrupt:** Quá nhiều ngắt liên tiếp làm hệ thống chậm.
3. **Transaction:** Lỗi giữa chừng có thể khiến dữ liệu không hoàn chỉnh.
4. **Process:** Tiến trình lỗi có thể chiếm hết bộ nhớ.
5. **Thread:** Nhiều luồng cùng ghi một biến có thể gây Data Race.
6. **Cache:** Dữ liệu có thể lỗi thời nếu không đồng bộ với bộ nhớ chính.
7. **RAM:** Dữ liệu bị mất khi tắt nguồn.
8. **SSD:** Mỗi ô nhớ Flash có giới hạn số lần ghi.
9. **Git:** Hai người sửa cùng một dòng có thể gây xung đột.
10. **Virtual Memory:** Tráo trang quá nhiều gây Thrashing.
11. **Network Protocol:** Gói tin có thể mất hoặc đến sai thứ tự.
12. **File System:** Mất điện giữa chừng có thể làm hỏng cấu trúc thư mục.
13. **Database:** Thiết kế chuẩn hóa kém có thể gây trùng lặp dữ liệu.
14. **Encryption:** Để lộ khóa có thể khiến dữ liệu bị xâm phạm.
15. **Client-Server:** Server quá tải có thể khiến hệ thống phản hồi chậm.
16. **Cloud:** Quên tắt tài nguyên thuê có thể làm tăng chi phí.

## 6. Kiến thức trọng tâm cần ôn tập

### Nhóm 1. CPU, bộ nhớ và lưu trữ
- Phân biệt CPU, RAM, SSD và Cache.
- Hiểu Cache Hit và Cache Miss.
- Nắm cơ chế truy cập Cache và RAM.
- Hiểu Virtual Memory và Page Table.
- Ghi nhớ Thrashing và giới hạn ghi của SSD.

### Nhóm 2. Hệ điều hành và xử lý
- Phân biệt Process và Thread.
- Hiểu Scheduler, Ready Queue, Round-robin và Starvation.
- Nắm quy trình xử lý Interrupt.
- Hiểu Data Race và cách sử dụng Lock.
- Ghi nhớ cơ chế cấp phát và thu hồi RAM.

### Nhóm 3. Quản lý dữ liệu
- Hiểu Transaction, Journal và Rollback.
- Phân biệt Journaling và Backup.
- Nắm quy trình sao lưu và thử khôi phục.
- Hiểu File System và vai trò của Journaling.
- Nắm Relational Database và cách các bảng liên kết bằng khóa.

### Nhóm 4. Mạng máy tính và bảo mật
- Hiểu IP Address, DHCP và IP Conflict.
- Phân biệt Client và Server.
- Nắm HTTP và Network Protocol.
- Hiểu cơ chế đánh số, xác nhận và gửi lại gói tin.
- Ghi nhớ Encryption và Decryption.
- Hiểu Load Balancing và Server-side Cache.

### Nhóm 5. Thuật toán và phát triển phần mềm
- Phân biệt O(N), O(log N) và O(N²).
- Biết phân tích vòng lặp và vòng lặp lồng nhau.
- Nắm quy trình Branch, Commit, Merge và Conflict Resolution.
- Hiểu Unit Testing và Edge Case.

### Nhóm 6. Điện toán đám mây
- Hiểu Cloud Computing và Virtual Machine.
- Biết theo dõi mức sử dụng tài nguyên.
- Đặt hạn mức chi phí và cảnh báo.
- Tránh để tài nguyên thuê hoạt động khi không cần thiết.

---

**KẾT LUẬN**

Qua 5 Chunk, kiến thức tập trung vào cách CPU, bộ nhớ và hệ điều hành phối hợp xử lý công việc; cách lưu trữ, bảo vệ và khôi phục dữ liệu; cách các thiết bị trao đổi thông tin qua mạng; cùng những kiến thức về thuật toán, kiểm thử phần mềm và điện toán đám mây.

Các kiến thức được lặp lại đã được hợp nhất thành một nội dung duy nhất. Những phần mở rộng như Cache Hit/Miss, Page Table, Load Balancing, Server-side Cache, Journaling, SSD Controller và Unit Testing vẫn được giữ lại để phục vụ ôn tập.
