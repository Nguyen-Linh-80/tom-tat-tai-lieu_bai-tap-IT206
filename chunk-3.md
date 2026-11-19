# **TÓM TẮT CHUNK 3 – NHẬP MÔN KIẾN TRÚC MÁY TÍNH**

Nguồn: Giáo trình PDF Chunk 3, trang 74–120 · 

**Lưu ý:** Chunk 3 có nhiều nội dung lặp lại từ Chunk 1 và Chunk 2. Vì vậy, bản tổng hợp dưới đây tập trung vào kiến thức được bổ sung, những phần được giải thích sâu hơn và các nội dung cần ghi nhớ để ôn thi.

# **1. Khái niệm chính**

## **1.1. Bộ nhớ truy cập ngẫu nhiên (RAM)**

Mở rộng kiến thức cũ

- RAM là bộ nhớ tạm, có tính khả biến.
- Tốc độ truy cập được tính bằng nano-giây.
- Dữ liệu trong RAM bị mất khi tắt nguồn.
- Hệ điều hành chịu trách nhiệm cấp phát và thu hồi từng vùng RAM cho các tiến trình.

**Ví dụ:** Trình duyệt giữ các tab đang mở trong RAM. Khi tắt máy, dữ liệu chưa lưu sẽ bị mất.

Nguồn: Chương 10, trang 83–91.

## **1.2. Luồng (Thread)**

Mở rộng kiến thức cũ

- Thread là đơn vị thực thi nhỏ nhất trong một tiến trình.
- Các luồng trong cùng tiến trình có thể dùng chung bộ nhớ.
- Nhiều luồng có thể thực hiện các công việc khác nhau.
- Khi hai luồng cùng ghi vào một biến, có thể xảy ra tranh chấp dữ liệu.
- Cần sử dụng Lock để bảo vệ vùng dữ liệu dùng chung.

**Ví dụ:**

- Một luồng thực hiện tải tệp.
- Một luồng thực hiện vẽ giao diện.

Nguồn: Chương 11, mục 11.1, trang 92–94.

## **1.3. Độ phức tạp thuật toán (Algorithm Complexity)**

Mở rộng kiến thức cũ

Độ phức tạp thuật toán là thước đo thời gian hoặc bộ nhớ cần thiết theo kích thước dữ liệu đầu vào.

| Độ phức tạp | Ví dụ                                |
| ----------- | ------------------------------------ |
| O(N)        | Tìm kiếm tuần tự                     |
| O(log N)    | Tìm kiếm nhị phân                    |
| O(N²)       | Thuật toán có hai vòng lặp lồng nhau |

**Kiến thức bổ sung:** Khi phân tích độ phức tạp, cần chú ý số vòng lặp lồng nhau để ước lượng mức độ tăng thời gian thực hiện.

**Lưu ý:** O(N²) có thể chạy rất chậm khi dữ liệu đầu vào lớn.

Nguồn: Chương 11, mục 11.2, trang 94–96.

## **1.4. Bộ nhớ đệm (Cache)**

Kiến thức được mở rộng sâu

Cache là vùng nhớ nhỏ, tốc độ cao, nằm gần CPU, dùng để lưu bản sao của dữ liệu thường xuyên được sử dụng.

**Vai trò:**

- Giúp CPU truy cập dữ liệu thường dùng nhanh hơn.
- Giảm nhu cầu truy cập trực tiếp RAM.
- Cải thiện hiệu suất xử lý.

**Lưu ý:** Dữ liệu trong Cache có thể lỗi thời nếu không được đồng bộ với bộ nhớ chính.

Nguồn: Chương 11, mục 11.3, trang 97–101.

## **1.5. Hệ thống tệp (File System)**

Mở rộng kiến thức cũ

Hệ thống tệp là cách tổ chức và đặt tên dữ liệu trên thiết bị lưu trữ.

Kiến thức mới được bổ sung:

- Mất điện giữa chừng có thể làm hỏng cấu trúc thư mục.
- Cần sử dụng ghi nhật ký (Journaling) để hỗ trợ khôi phục sau sự cố.

**Ví dụ:** Thư mục chứa các tệp bài tập của sinh viên.

Nguồn: Chương 12, mục 12.1 và Chương 13, mục 13.4, trang 102–120.

## **1.6. Quản lý phiên bản (Version Control)**

Mở rộng kiến thức cũ

Quản lý phiên bản là việc ghi lại lịch sử thay đổi mã nguồn.

Kiến thức được bổ sung:

- Tạo nhánh (Branch) để phát triển riêng.
- Thực hiện chỉnh sửa trên nhánh.
- Gộp nhánh (Merge).
- Giải quyết xung đột khi nhiều người cùng sửa một dòng mã.

**Ví dụ:** Git lưu lại từng lần Commit của các thành viên trong nhóm.

Nguồn: Chương 13, mục 13.1, trang 111–113.

## **1.7. Ổ thể rắn (SSD)**

Mở rộng kiến thức cũ

SSD là thiết bị lưu trữ sử dụng bộ nhớ flash không khả biến, có tốc độ truy cập tính bằng micro-giây.

Kiến thức bổ sung:

- Mỗi ô nhớ flash có giới hạn số lần ghi.
- Bộ điều khiển SSD cần phân bổ đều thao tác ghi lên các ô nhớ.

**Ví dụ:** Lưu tệp báo cáo lên SSD để mở lại vào ngày hôm sau.

Nguồn: Chương 13, mục 13.2, trang 114–115.

## **1.8. Ngắt (Interrupt)**

Mở rộng kiến thức cũ

Ngắt là tín hiệu yêu cầu CPU tạm dừng công việc hiện tại để xử lý một sự kiện.

Kiến thức được bổ sung về quy trình:

- CPU lưu trạng thái hiện tại.
- Chuyển đến trình xử lý ngắt.
- Xử lý sự kiện.
- Quay lại tiếp tục công việc trước đó.

**Ví dụ:** Bàn phím gửi tín hiệu ngắt khi người dùng nhấn phím.

Nguồn: Chương 13, mục 13.3, trang 116–117.

# **2. Thuật ngữ quan trọng**

Các thuật ngữ dưới đây được chọn lọc theo nội dung cần ghi nhớ, không lặp lại toàn bộ bảng thuật ngữ của hai Chunk trước.

| Thuật ngữ            | Giải thích                                                             |
| -------------------- | ---------------------------------------------------------------------- |
| Thread               | Luồng thực thi bên trong tiến trình                                    |
| Lock                 | Khóa bảo vệ vùng dữ liệu dùng chung                                    |
| Data Race            | Tranh chấp dữ liệu khi nhiều luồng cùng truy cập hoặc thay đổi dữ liệu |
| Algorithm Complexity | Độ phức tạp thuật toán                                                 |
| Nested Loops         | Các vòng lặp lồng nhau                                                 |
| Cache                | Bộ nhớ đệm tốc độ cao gần CPU                                          |
| Cache Hit            | Tìm thấy dữ liệu trong Cache                                           |
| Cache Miss           | Không tìm thấy dữ liệu trong Cache                                     |
| Main Memory          | Bộ nhớ chính, trong ngữ cảnh này là RAM                                |
| Journaling           | Ghi nhật ký để hỗ trợ khôi phục hệ thống tệp                           |
| File System          | Hệ thống tổ chức dữ liệu trên thiết bị lưu trữ                         |
| Version Control      | Quản lý lịch sử thay đổi mã nguồn                                      |
| Merge                | Gộp các nhánh mã nguồn                                                 |
| Conflict             | Xung đột khi hợp nhất thay đổi                                         |
| Flash Memory         | Bộ nhớ flash sử dụng trong SSD                                         |
| Controller           | Bộ điều khiển phân bổ thao tác ghi trên SSD                            |
| Interrupt Handler    | Trình xử lý ngắt                                                       |
| Allocation           | Cấp phát tài nguyên bộ nhớ                                             |
| Deallocation         | Thu hồi vùng bộ nhớ đã cấp phát                                        |

# **3. Kiến thức và quy trình cần nhớ**

Đây là phần quan trọng để ôn tập vì tài liệu bổ sung nhiều cơ chế hoạt động cụ thể.

## **3.1. Quy trình hoạt động của Cache**

Cần ghi nhớ

CPU thực hiện kiểm tra Cache trước khi truy cập RAM.

```
CPU cần dữ liệu
      |
      v
Kiểm tra Cache
      |
      v
Có dữ liệu?
   /       \
 Có         Không
 |            |
 v            v
Đọc Cache   Đọc RAM
 |            |
 |            v
 |        Nạp bản sao
 |        vào Cache
 |            |
  \          /
   \        /
      v
  Tiếp tục xử lý
```

- Cache Hit: Dữ liệu đã có trong Cache.
- Cache Miss: Phải đọc dữ liệu từ RAM rồi nạp bản sao vào Cache.
- Cần chú ý đồng bộ dữ liệu giữa Cache và bộ nhớ chính.

**Số liệu trong tài liệu:** Khi tỷ lệ trúng Cache đạt 95%, thời gian truy cập trung bình giảm 40%.

Nguồn: trang 96–97.

## **3.2. Quy trình bảo vệ dữ liệu dùng chung bằng Lock**

```
Nhiều Thread cùng hoạt động
          |
          v
Cùng truy cập một biến?
          |
          v
Có nguy cơ tranh chấp
          |
          v
Sử dụng Lock
          |
          v
Bảo vệ vùng dữ liệu
dùng chung
```

Cần nhớ:

- Các Thread trong cùng Process có thể dùng chung bộ nhớ.
- Hai Thread cùng ghi một biến có thể gây tranh chấp.
- Lock giúp bảo vệ vùng dữ liệu dùng chung.

Nguồn: trang 92–94.

## **3.3. Phân tích độ phức tạp thuật toán**

Các bước cần nhớ:

1. Xác định kích thước dữ liệu đầu vào N.
2. Quan sát số vòng lặp trong thuật toán.
3. Xác định có vòng lặp lồng nhau hay không.
4. Ước lượng độ phức tạp.

Ví dụ:

| Cách thực hiện               | Độ phức tạp |
| ---------------------------- | ----------- |
| Một vòng lặp duyệt N phần tử | O(N)        |
| Tìm kiếm nhị phân            | O(log N)    |
| Hai vòng lặp lồng nhau       | O(N²)       |

**Lưu ý:** Tài liệu nhấn mạnh cần phân tích số vòng lặp lồng nhau để ước lượng độ phức tạp.

Nguồn: trang 94–96.

## **3.4. Quy trình quản lý phiên bản**

```
Tạo Branch
    |
    v
Chỉnh sửa mã nguồn
    |
    v
Gộp nhánh (Merge)
    |
    v
Có xung đột?
   /       \
 Không      Có
  |          |
  v          v
Hoàn tất   Giải quyết
           xung đột
              |
              v
           Hoàn tất
```

Cần nhớ ba thao tác quan trọng:

- Branch: Tạo nhánh riêng.
- Merge: Gộp nhánh.
- Conflict Resolution: Giải quyết xung đột.

Nguồn: trang 111–113.

## **3.5. Quy trình xử lý ngắt**

```
CPU đang thực hiện công việc
             |
             v
       Nhận tín hiệu ngắt
             |
             v
       Lưu trạng thái CPU
             |
             v
      Chuyển đến trình
        xử lý ngắt
             |
             v
       Xử lý sự kiện
             |
             v
      Khôi phục trạng thái
             |
             v
       Tiếp tục công việc
```

**Lưu ý:** Quá nhiều ngắt liên tiếp có thể khiến hệ thống chậm.

Nguồn: trang 116–117.

## **3.6. Cơ chế ghi nhật ký của hệ thống tệp**

- Hệ thống tệp tổ chức và đặt tên dữ liệu.
- Khi mất điện giữa chừng, cấu trúc thư mục có thể bị hỏng.
- Journaling ghi nhật ký nhằm hỗ trợ khôi phục sau sự cố.

Cần phân biệt:

| Cơ chế     | Mục đích                                 |
| ---------- | ---------------------------------------- |
| Journaling | Hỗ trợ khôi phục hệ thống tệp sau sự cố  |
| Backup     | Tạo bản sao dữ liệu để khôi phục khi mất |

Nguồn: trang 118–120.

# **4. Ví dụ và lưu ý quan trọng**

| Nội dung        | Ví dụ trong tài liệu                      | Điểm cần chú ý                              |
| --------------- | ----------------------------------------- | ------------------------------------------- |
| RAM             | Trình duyệt giữ các tab đang mở           | Mất dữ liệu khi tắt nguồn                   |
| Thread          | Một luồng tải tệp, một luồng vẽ giao diện | Hai luồng cùng ghi một biến gây tranh chấp  |
| Complexity      | O(N), O(log N), O(N²)                     | O(N²) chậm khi dữ liệu lớn                  |
| Cache           | CPU đọc cùng một mảng số nhiều lần        | Dữ liệu Cache có thể lỗi thời               |
| File System     | Thư mục chứa tệp bài tập                  | Mất điện có thể làm hỏng cấu trúc thư mục   |
| Version Control | Git lưu từng lần Commit                   | Hai người sửa cùng dòng có thể gây xung đột |
| SSD             | Lưu tệp báo cáo để mở lại hôm sau         | Mỗi ô nhớ flash có giới hạn số lần ghi      |
| Interrupt       | Bàn phím gửi ngắt khi nhấn phím           | Quá nhiều ngắt làm hệ thống chậm            |

## **Những điểm dễ nhầm khi ôn thi**

1. **RAM và SSD:** RAM là bộ nhớ tạm khả biến, SSD là thiết bị lưu trữ flash không khả biến.
2. **Process và Thread:** Process có không gian địa chỉ riêng; các Thread trong cùng Process có thể dùng chung bộ nhớ.
3. **Cache Hit và Cache Miss:** Hit là tìm thấy dữ liệu trong Cache, Miss là phải truy cập RAM.
4. **Lock:** Dùng để bảo vệ dữ liệu dùng chung giữa các luồng, không phải công cụ quản lý phiên bản.
5. **Journaling và Backup:** Journaling hỗ trợ khôi phục hệ thống tệp; Backup tạo bản sao dữ liệu.
6. **Interrupt:** CPU phải lưu trạng thái trước khi chuyển sang xử lý ngắt.

# **5. Kiến thức mới của Chunk 3**

Đây là phần đối chiếu trực tiếp với hai bản tóm tắt Chunk 1 và Chunk 2 mà bạn đã cung cấp.

## **5.1. Kiến thức mới được bổ sung**

| Kiến thức              | Nội dung mới trong Chunk 3                                        | Trang   |
| ---------------------- | ----------------------------------------------------------------- | ------- |
| Cache Hit / Cache Miss | Phân biệt tìm thấy và không tìm thấy dữ liệu trong Cache          | 97      |
| Quy trình Cache        | Kiểm tra Cache, nếu trượt thì đọc RAM và nạp bản sao              | 97      |
| Cache Performance      | Tỷ lệ trúng Cache 95% giúp thời gian truy cập trung bình giảm 40% | 96      |
| Journaling             | Ghi nhật ký để hỗ trợ khôi phục hệ thống tệp sau sự cố            | 118–120 |
| Nested Loops           | Phân tích số vòng lặp lồng nhau để ước lượng độ phức tạp          | 95–96   |
| Interrupt Handler      | CPU lưu trạng thái, chuyển đến trình xử lý ngắt rồi quay lại      | 116–117 |
| RAM Allocation         | Hệ điều hành cấp phát và thu hồi vùng RAM cho tiến trình          | 83–91   |
| Process Management     | Hệ điều hành tạo, lập lịch và kết thúc tiến trình                 | 79–80   |
| Conflict Resolution    | Quy trình giải quyết xung đột khi gộp nhánh Git                   | 111–113 |

## **5.2. Kiến thức cũ được mở rộng**

| Chủ đề      | Đã biết ở Chunk 1–2                           | Mở rộng ở Chunk 3                                 |
| ----------- | --------------------------------------------- | ------------------------------------------------- |
| Thread      | Thread, bộ nhớ dùng chung, Lock               | Làm rõ tranh chấp khi hai luồng cùng ghi một biến |
| Cache       | Bộ nhớ đệm gần CPU                            | Quy trình Cache Hit/Miss và hiệu quả truy cập     |
| File System | Hệ thống tệp                                  | Journaling để khôi phục sau sự cố                 |
| Complexity  | O(N), O(log N), O(N²)                         | Phân tích vòng lặp lồng nhau                      |
| Interrupt   | CPU tạm dừng để xử lý sự kiện                 | Quy trình lưu trạng thái và xử lý ngắt            |
| Process     | Chương trình đang chạy                        | Quản lý tạo, lập lịch và kết thúc tiến trình      |
| RAM         | Bộ nhớ tạm khả biến                           | Cấp phát và thu hồi bộ nhớ                        |
| Git         | Branch, Commit, Merge                         | Quy trình xử lý xung đột khi Merge                |
| SSD         | Giới hạn số lần ghi và phân phối thao tác ghi | Làm rõ vai trò bộ điều khiển SSD                  |

## **5.3. Nội dung không cần học lại**

Các nội dung sau đã được trình bày ở Chunk 1 và Chunk 2. Chunk 3 chủ yếu nhắc lại, không bổ sung đáng kể:

- Transaction và Rollback.
- Giao thức mạng và HTTP.
- Round-robin và Starvation.
- Backup và thử khôi phục dữ liệu.
- Cloud Computing và kiểm soát chi phí.
- Unit Testing và Edge Case.
- Virtual Memory và Thrashing.

Vì vậy, chỉ cần ôn lại kiến thức nền tảng, không cần ghi chép lại toàn bộ.

# **6. Tổng kết kiến thức cần nhớ để ôn thi**

**8 nội dung nên ưu tiên ghi nhớ**

1. **Thread và Lock**

   Thread dùng chung bộ nhớ; Lock bảo vệ dữ liệu dùng chung.
2. **Algorithm Complexity**

   Phân biệt O(N), O(log N), O(N²); chú ý vòng lặp lồng nhau.
3. **Cache**

   Phân biệt Cache Hit và Cache Miss; hiểu quy trình đọc Cache và RAM.
4. **Journaling**

   Ghi nhật ký để hỗ trợ khôi phục hệ thống tệp sau sự cố.
5. **Version Control**

   Branch → chỉnh sửa → Merge → giải quyết Conflict.
6. **SSD**

   Bộ nhớ flash có giới hạn ghi; bộ điều khiển phân bổ đều thao tác ghi.
7. **Interrupt**

   Lưu trạng thái → xử lý ngắt → khôi phục trạng thái → tiếp tục.
8. **RAM và Process**

   Hệ điều hành cấp phát, thu hồi RAM và quản lý vòng đời tiến trình.

## **7. Ghi chú về cấu trúc tài liệu**

PDF có một số nội dung được lặp lại giữa các chương và mục. Cấu trúc chính có thể nhận diện:

| Chương    | Nội dung                                                     |
| --------- | ------------------------------------------------------------ |
| Chương 9  | Transaction, giao thức mạng                                  |
| Chương 10 | RAM, giao thức mạng, sao lưu                                 |
| Chương 11 | Thread, độ phức tạp thuật toán, Cache                        |
| Chương 12 | Hệ thống tệp, Cache                                          |
| Chương 13 | Quản lý phiên bản, SSD, Interrupt, hệ thống tệp              |
| Chương 14 | Chỉ xuất hiện tiêu đề, chưa có nội dung triển khai trong PDF |

Không nên tự bổ sung nội dung Chương 14 vì tài liệu kết thúc ở trang 120 ngay sau tiêu đề chương.

**Kết luận Chunk 3:** Kiến thức đáng chú ý nhất là cơ chế Cache Hit/Miss, Journaling, quy trình xử lý Interrupt, quản lý RAM và Process, cùng cách phân tích vòng lặp lồng nhau. Đây là những phần giúp giải thích sâu hơn cách hệ điều hành, bộ nhớ và CPU phối hợp hoạt động.

Bạn có thể sử dụng bản tổng hợp này làm ngữ cảnh nền để tiếp tục xử lý Chunk 4 theo phương pháp MapReduce.
