# 3. Yêu cầu cụ thể

## 3.1. Yêu cầu giao diện

|    Mã     | Loại         | Yêu cầu                                                                                                                                                                                                                            |
| :-------: | :----------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **IR-01** | Người dùng   | Giao diện sinh viên theo bố cục prototype trang tra cứu (Hình 3.1) và chi tiết vật phẩm (Hình 3.2); giao diện quản lý trạm quét mã QR hiển thị rõ ảnh và thông tin đối soát; mọi thông báo lỗi nêu lý do cụ thể và cách khắc phục. |
| **IR-02** | Phần cứng    | Camera điện thoại thông minh hoặc máy quét mã vạch 2D (QR Code) cổng USB giả lập bàn phím để đọc mã nhãn kho và phiếu hẹn (NFR-COMP-002).                                                                                          |
| **IR-03** | Phần mềm     | Dịch vụ đăng nhập dùng chung (SSO) của Trường Đại học Cần Thơ; API hoặc tệp danh sách sinh viên từ hệ thống quản lý đào tạo của trường.                                                                                            |
| **IR-04** | Truyền thông | HTTPS (TLS 1.3) cho mọi kết nối web; thông báo gửi qua máy chủ thư điện tử (SMTP) của Trường Đại học Cần Thơ và giao thức WSS.                                                                                                     |

```text
[CHÈN HÌNH ẢNH TẠI ĐÂY KHI LÊN WORD]
File ảnh nguồn: 02_ThuThap/Prototype/HTML/TraCuu/screen.png
Tên hình: Hình 3.1. Prototype trang tra cứu và danh sách đồ thất lạc
```

```text
[CHÈN HÌNH ẢNH TẠI ĐÂY KHI LÊN WORD]
File ảnh nguồn: 02_ThuThap/Prototype/HTML/ChiTietVatPham/screen.png
Tên hình: Hình 3.2. Prototype màn hình chi tiết vật phẩm và câu hỏi xác minh
```

---

## 3.2. Yêu cầu chức năng

### 3.2.1. Quy tắc nghiệp vụ

|    Mã     | Quy tắc nghiệp vụ                                                                                                                                    | Nguồn gốc         |
| :-------: | :--------------------------------------------------------------------------------------------------------------------------------------------------- | :---------------- |
| **BR-01** | Mỗi tài khoản sinh viên chỉ được duy trì tối đa 5 tin đăng đang ở trạng thái xử lý hoặc chờ xác nhận cùng một thời điểm.                             | BB-KH-02; PV-01   |
| **BR-02** | Thời hạn lưu giữ đồ vật tại trạm: Đồ thông thường tối đa 30 ngày; Đồ có giá trị cao (tiền, ví, laptop, điện thoại, giấy tờ cá nhân) tối đa 90 ngày.  | XĐ-01; BB-KH-01   |
| **BR-03** | Tự động che mờ đặc điểm nhận dạng cốt lõi trên ảnh chụp và ẩn thông tin liên hệ đối với đồ vật thuộc danh mục có giá trị cao khi hiển thị công khai. | XĐ-02; BB-KH-01   |
| **BR-04** | Người mất trả lời sai câu hỏi xác minh sở hữu quá 3 lần liên tiếp sẽ bị khóa tạm thời quyền gửi yêu cầu nhận đồ trong vòng 48 giờ.                   | XĐ-02; BB-KH-02   |
| **BR-05** | Sinh viên chỉ được đặt lịch hẹn nhận đồ trong khung giờ trạm mở cửa trực (07:30–11:00 và 13:30–17:00, từ thứ Hai đến thứ Sáu).                       | XĐ-03; BB-KH-02   |
| **BR-06** | Bắt buộc đối chiếu Thẻ sinh viên hoặc Căn cước công dân gốc và quét mã QR lịch hẹn trước khi xác nhận trao trả đồ tại quầy.                          | XĐ-03; PV02-3     |
| **BR-07** | Khi đồ vật phát sinh từ 2 yêu cầu nhận trở lên hoặc có báo cáo tranh chấp, hệ thống tự động phong tỏa giao dịch và chuyển Phòng CTSV giải quyết.     | FR-MOD-001; UC-08 |
| **BR-08** | Đồ vật quá hạn lưu giữ tại trạm phải được xuất khỏi kho kèm biên bản bàn giao điện tử chuyển giao về Phòng CTSV.                                     | XĐ-01; PV02-2     |

Ghi chú từ phân tích CRUDL: Vật phẩm lưu kho, tài khoản người dùng, tin nhắn ẩn danh, yêu cầu nhận đồ, biên bản bàn giao CTSV và thông báo không bị xoá vật lý; dùng các trạng thái Đã trao trả, Quá hạn / Đã bàn giao CTSV, Vô hiệu hoá để giữ lịch sử đối soát.

---

### 3.2.2. Đặc tả use case chính

Năm use case quan trọng nhất được đặc tả đầy đủ theo khung ở mục 3.2.5 giáo trình (bổ sung luồng thay thế theo yêu cầu đồ án). Các use case còn lại được đặc tả qua yêu cầu chức năng ở mục 3.2.3.

#### UC-02. Đăng tin tìm đồ thất lạc

`đặc tả theo mẫu SRS trong đồ án mẫu`

#### UC-04. Tra cứu và lọc danh sách đồ thất lạc

`đặc tả theo mẫu SRS trong đồ án mẫu`

#### UC-07. Xác minh quyền sở hữu đồ thất lạc

`đặc tả theo mẫu SRS trong đồ án mẫu`

#### UC-09. Đặt và quản lý lịch hẹn nhận đồ tại trạm

`đặc tả theo mẫu SRS trong đồ án mẫu`

#### UC-11. Quét mã QR và giao trả đồ trực tiếp tại trạm

`đặc tả theo mẫu SRS trong đồ án mẫu`

---

### 3.2.3. Danh sách yêu cầu chức năng

Hệ thống gồm 28 yêu cầu chức năng (FR) được tổ chức thành 9 nhóm nghiệp vụ. Các yêu cầu dùng từ khóa PHẢI / NÊN / CÓ THỂ theo Bảng 4.5 và tuân thủ template Bảng 4.9 giáo trình.

#### Bảng tổng hợp 28 yêu cầu chức năng

|         Mã         | Tên yêu cầu chức năng                                    | Độ ưu tiên | Use case liên quan |
| :----------------: | :------------------------------------------------------- | :--------: | :----------------: |
|  **FR-AUTH-001**   | Đăng nhập bằng tài khoản trường qua SSO                  | Essential  |       UC-01        |
|  **FR-AUTH-002**   | Phân quyền truy cập theo vai trò                         | Essential  |       UC-01        |
|  **FR-ROLE-001**   | Quản lý và phân quyền nhân sự trạm                       | Essential  |       UC-16        |
|  **FR-POST-001**   | Đăng tin tìm đồ thất lạc                                 | Essential  |       UC-02        |
|  **FR-POST-002**   | Đăng tin nhặt được đồ kèm câu hỏi xác minh               | Essential  |       UC-03        |
|  **FR-POST-003**   | Quản lý và chỉnh sửa tin đăng cá nhân                    | Desirable  |    UC-02, UC-03    |
| **FR-SEARCH-001**  | Tra cứu và lọc danh sách đồ thất lạc đa tiêu chí         | Essential  |       UC-04        |
| **FR-SEARCH-002**  | Xem thông tin chi tiết vật phẩm và làm mờ ảnh đồ giá trị | Essential  |       UC-04        |
|  **FR-MATCH-001**  | Tự động so khớp và gợi ý tin tương đồng                  | Desirable  |       UC-05        |
| **FR-VERIFY-001**  | Thiết lập câu hỏi xác minh ẩn danh                       | Essential  |    UC-03, UC-07    |
| **FR-VERIFY-002**  | Trả lời câu hỏi xác minh sở hữu                          | Essential  |       UC-07        |
| **FR-VERIFY-003**  | Khóa tạm thời 48h khi trả lời sai quá 3 lần              | Essential  |       UC-07        |
| **FR-VERIFY-004**  | Đối chiếu thông tin giấy tờ tùy thân tại quầy            | Essential  |       UC-11        |
|  **FR-CHAT-001**   | Nhắn tin trao đổi ẩn danh in-app                         | Desirable  |       UC-06        |
|  **FR-APPT-001**   | Đặt lịch hẹn nhận đồ trực tuyến theo ca trực             | Essential  |       UC-09        |
|  **FR-APPT-002**   | Điều chỉnh và hủy lịch hẹn nhận đồ                       | Desirable  |       UC-09        |
| **FR-STATION-001** | Tiếp nhận hiện vật vào kho trạm và in/cấp mã QR          | Essential  |       UC-10        |
| **FR-STATION-002** | Quản lý vị trí ngăn tủ và trạng thái vật phẩm lưu kho    | Essential  |    UC-10, UC-12    |
| **FR-RETURN-001**  | Quét mã QR tra cứu hồ sơ và xác nhận trao trả đồ         | Essential  |       UC-11        |
| **FR-RETURN-002**  | Chụp ảnh lưu bằng chứng giao nhận điện tử                | Essential  |       UC-11        |
|  **FR-SHIFT-001**  | Điểm danh nhận ca và bàn giao ca trực trạm               | Essential  |       UC-12        |
|  **FR-SHIFT-002**  | Kiểm kê kho hiện vật đối soát thực tế theo ca            | Desirable  |       UC-12        |
| **FR-OVERDUE-001** | Tự động quét và cảnh báo vật phẩm quá hạn lưu trữ        | Essential  |       UC-13        |
| **FR-OVERDUE-002** | Lập biên bản bàn giao điện tử chuyển Phòng CTSV          | Essential  |       UC-13        |
|   **FR-MOD-001**   | Tiếp nhận báo cáo vi phạm và phong tỏa đồ tranh chấp     | Essential  |    UC-08, UC-14    |
|   **FR-CAT-001**   | Cấu hình tham số quy định trạm và danh mục loại đồ       | Essential  |       UC-15        |
|   **FR-RPT-001**   | Thống kê số liệu và xuất báo cáo định kỳ                 | Essential  |       UC-17        |
|  **FR-NOTI-001**   | Gửi thông báo tự động đa kênh (Web, Email)               | Essential  |       UC-18        |

---

#### Bảng thẻ đặc tả chi tiết các yêu cầu chức năng (Template Bảng 4.9 giáo trình)

```text
[HƯỚNG DẪN DÀNH CHO ANH EM KHI LÊN WORD]
Mỗi yêu cầu chức năng được trình bày thành 1 bảng độc lập theo đúng mẫu chuẩn giáo trình như dưới đây.
Anh em copy câu văn Given/When/Then tương ứng từ sheet RTM của file CT241_Nhom02_RTM_v1.0.xlsx để đồng bộ 100%.
```

##### Nhóm AUTH – Đăng nhập và phân quyền

| Mục                    | Nội dung                                                                                                                                                                                   |
| :--------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Mã yêu cầu (ID)**    | **FR-AUTH-001**                                                                                                                                                                            |
| **Tên yêu cầu**        | Đăng nhập bằng tài khoản trường qua SSO                                                                                                                                                    |
| **Mô tả chi tiết**     | Hệ thống PHẢI xác thực người dùng qua dịch vụ đăng nhập dùng chung (SSO) của Trường Đại học Cần Thơ khi truy cập các chức năng cần định danh, để không phải quản lý mật khẩu riêng (C-01). |
| **Use case liên quan** | UC-01                                                                                                                                                                                      |
| **Tác nhân**           | Sinh viên, Quản lý trạm, Cán bộ CTSV                                                                                                                                                       |
| **Tiền điều kiện**     | Người dùng có tài khoản email trường Đại học Cần Thơ còn hiệu lực.                                                                                                                         |
| **Hậu điều kiện**      | Phiên làm việc được khởi tạo đúng vai trò tương ứng.                                                                                                                                       |
| **Luồng chính**        | 1. Người dùng chọn Đăng nhập.<br>2. Hệ thống chuyển hướng sang cổng SSO của trường.<br>3. SSO xác thực thành công và trả về định danh; hệ thống cấp quyền theo vai trò.                    |
| **Luồng ngoại lệ**     | SSO báo lỗi hoặc tài khoản bị khóa: Hệ thống hiển thị thông báo lỗi và giữ người dùng ở trang công khai.                                                                                   |
| **Quy tắc nghiệp vụ**  | C-01; Phiên làm việc tự động hết hạn sau 30 phút rảnh (NFR-SEC-002).                                                                                                                       |
| **Nguồn gốc**          | Tầm nhìn 2.3; Biên bản PV02-5                                                                                                                                                              |
| **Độ ưu tiên**         | Essential (Bắt buộc)                                                                                                                                                                       |
| **Tiêu chí chấp nhận** | Given sinh viên có tài khoản trường hợp lệ, When đăng nhập qua SSO, Then trang chủ hiển thị họ tên, MSSV và vai trò Sinh viên.                                                             |
| **Trạng thái**         | Approved                                                                                                                                                                                   |
| **Phiên bản**          | v1.0 (29/11/2026)                                                                                                                                                                          |

| Mục                    | Nội dung                                                                                                                                                                         |
| :--------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Mã yêu cầu (ID)**    | **FR-AUTH-002**                                                                                                                                                                  |
| **Tên yêu cầu**        | Phân quyền truy cập theo vai trò                                                                                                                                                 |
| **Mô tả chi tiết**     | Hệ thống PHẢI giới hạn quyền truy cập menu và chức năng theo 4 vai trò (Sinh viên, Quản lý trạm, Cán bộ CTSV, Quản trị hệ thống) để bảo đảm an toàn dữ liệu.                     |
| **Use case liên quan** | UC-01, UC-16                                                                                                                                                                     |
| **Tác nhân**           | Hệ thống                                                                                                                                                                         |
| **Tiền điều kiện**     | Người dùng đã đăng nhập.                                                                                                                                                         |
| **Hậu điều kiện**      | Menu và API chỉ mở các chức năng thuộc thẩm quyền của vai trò.                                                                                                                   |
| **Luồng chính**        | 1. Hệ thống đọc vai trò người dùng sau khi xác thực.<br>2. Hệ thống tải menu giao diện tương ứng.<br>3. Mọi truy cập vào chức năng ngoài phạm vi vai trò đều bị chặn từ máy chủ. |
| **Luồng ngoại lệ**     | Truy cập trái phép qua URL: Hệ thống trả mã lỗi 403, từ chối truy cập và ghi nhật ký kiểm toán.                                                                                  |
| **Quy tắc nghiệp vụ**  | Phân quyền do Quản trị hoặc Cán bộ CTSV cấu hình (UC-16).                                                                                                                        |
| **Nguồn gốc**          | Biên bản PV02-5; NFR-SEC-001                                                                                                                                                     |
| **Độ ưu tiên**         | Essential                                                                                                                                                                        |
| **Tiêu chí chấp nhận** | Given sinh viên đã đăng nhập, When cố ý mở đường dẫn trang quản lý kho trạm, Then hệ thống từ chối và ghi log vi phạm.                                                           |
| **Trạng thái**         | Approved                                                                                                                                                                         |
| **Phiên bản**          | v1.0 (29/11/2026)                                                                                                                                                                |

##### Nhóm POST – Đăng tin thất lạc và nhặt được

| Mục                    | Nội dung                                                                                                                                                                                                                |
| :--------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Mã yêu cầu (ID)**    | **FR-POST-001**                                                                                                                                                                                                         |
| **Tên yêu cầu**        | Đăng tin tìm đồ thất lạc                                                                                                                                                                                                |
| **Mô tả chi tiết**     | Hệ thống PHẢI cho phép sinh viên đăng tin tìm đồ thất lạc gồm danh mục, khu vực rơi, thời gian, mô tả đặc điểm chi tiết và ảnh đính kèm (nếu có).                                                                       |
| **Use case liên quan** | UC-02                                                                                                                                                                                                                   |
| **Tác nhân**           | Sinh viên                                                                                                                                                                                                               |
| **Tiền điều kiện**     | Sinh viên đã đăng nhập qua SSO trường.                                                                                                                                                                                  |
| **Hậu điều kiện**      | Tin đăng được lưu ở trạng thái "Chờ xác nhận".                                                                                                                                                                          |
| **Luồng chính**        | 1. Sinh viên nhập thông tin theo biểu mẫu.<br>2. Hệ thống kiểm tra tính hợp lệ của dữ liệu.<br>3. Hệ thống kiểm tra giới hạn $\le 5$ tin đang mở (BR-01).<br>4. Hệ thống lưu tin đăng và hiển thị thông báo thành công. |
| **Luồng ngoại lệ**     | Thiếu trường bắt buộc hoặc vượt quá 5 tin đang mở: Hệ thống từ chối lưu bài viết và thông báo lý do cụ thể.                                                                                                             |
| **Quy tắc nghiệp vụ**  | BR-01                                                                                                                                                                                                                   |
| **Nguồn gốc**          | Biên bản PV01-1; Khảo sát KS-01 Q6                                                                                                                                                                                      |
| **Độ ưu tiên**         | Essential                                                                                                                                                                                                               |
| **Tiêu chí chấp nhận** | Given sinh viên có dưới 5 tin đang mở, When gửi biểu mẫu đăng tin hợp lệ, Then hệ thống lưu bài viết ở trạng thái Chờ xác nhận.                                                                                         |
| **Trạng thái**         | Approved                                                                                                                                                                                                                |
| **Phiên bản**          | v1.0 (29/11/2026)                                                                                                                                                                                                       |

| Mục                    | Nội dung                                                                                                                                                                                                                                                                                              |
| :--------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Mã yêu cầu (ID)**    | **FR-POST-002**                                                                                                                                                                                                                                                                                       |
| **Tên yêu cầu**        | Đăng tin nhặt được đồ kèm câu hỏi xác minh                                                                                                                                                                                                                                                            |
| **Mô tả chi tiết**     | Hệ thống PHẢI cho phép người nhặt đăng tin nhặt được đồ; PHẢI bắt buộc thiết lập ít nhất 1 câu hỏi xác minh ẩn danh và TỰ ĐỘNG làm mờ ảnh nếu đồ thuộc danh mục giá trị cao (BR-03).                                                                                                                  |
| **Use case liên quan** | UC-03                                                                                                                                                                                                                                                                                                 |
| **Tác nhân**           | Sinh viên, Quản lý trạm                                                                                                                                                                                                                                                                               |
| **Tiền điều kiện**     | Người nhặt đã đăng nhập.                                                                                                                                                                                                                                                                              |
| **Hậu điều kiện**      | Tin nhặt được lưu trữ và hiển thị công khai dạng bảo mật (ẩn SĐT và mờ ảnh đồ giá trị).                                                                                                                                                                                                               |
| **Luồng chính**        | 1. Người nhặt nhập thông tin món đồ nhặt được và tải ảnh lên.<br>2. Người nhặt thiết lập câu hỏi và đáp án xác minh bí mật.<br>3. Hệ thống kiểm tra loại đồ; nếu là đồ giá trị (ví, laptop, tiền, điện thoại), tự động áp dụng bộ lọc làm mờ chi tiết cốt lõi.<br>4. Hệ thống lưu tin đăng công khai. |
| **Luồng ngoại lệ**     | Chưa nhập câu hỏi xác minh bí mật: Hệ thống báo lỗi và yêu cầu nhập câu hỏi trước khi cho phép đăng tin.                                                                                                                                                                                              |
| **Quy tắc nghiệp vụ**  | BR-03                                                                                                                                                                                                                                                                                                 |
| **Nguồn gốc**          | XĐ-02; BB-KH-01 KH01-2; KS-01 Q13, Q14                                                                                                                                                                                                                                                                |
| **Độ ưu tiên**         | Essential                                                                                                                                                                                                                                                                                             |
| **Tiêu chí chấp nhận** | Given người nhặt đăng ảnh một chiếc ví nhặt được, When lưu tin đăng thành công, Then ảnh ví trên trang công khai bị làm mờ chi tiết và hiển thị câu hỏi xác minh ẩn danh.                                                                                                                             |
| **Trạng thái**         | Approved                                                                                                                                                                                                                                                                                              |
| **Phiên bản**          | v1.0 (29/11/2026)                                                                                                                                                                                                                                                                                     |

##### Nhóm SEARCH – Tra cứu và gợi ý so khớp

| Mục                    | Nội dung                                                                                                                                                                          |
| :--------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Mã yêu cầu (ID)**    | **FR-SEARCH-001**                                                                                                                                                                 |
| **Tên yêu cầu**        | Tra cứu và lọc danh sách đồ thất lạc đa tiêu chí                                                                                                                                  |
| **Mô tả chi tiết**     | Hệ thống PHẢI cho phép tìm kiếm từ khóa và lọc danh sách đồ theo loại đồ, khu vực rơi/nhặt, mốc thời gian và trạng thái tồn kho trạm trong thời gian $\le 2$ giây (NFR-PERF-001). |
| **Use case liên quan** | UC-04                                                                                                                                                                             |
| **Tác nhân**           | Sinh viên, Quản lý trạm, Cán bộ CTSV                                                                                                                                              |
| **Tiền điều kiện**     | Không có (chức năng công khai).                                                                                                                                                   |
| **Hậu điều kiện**      | Danh sách kết quả phù hợp được hiển thị.                                                                                                                                          |
| **Luồng chính**        | 1. Người dùng chọn các tiêu chí lọc và nhấn Tìm kiếm.<br>2. Hệ thống truy vấn CSDL và trả về danh sách kết quả phù hợp.<br>3. Kết quả tự động phân trang (mỗi trang 12 mục).      |
| **Luồng ngoại lệ**     | Không có kết quả: Hệ thống hiển thị thông báo không tìm thấy kết quả và gợi ý đăng tin mới.                                                                                       |
| **Quy tắc nghiệp vụ**  | Mặc định ẩn các tin đã trao trả thành công.                                                                                                                                       |
| **Nguồn gốc**          | Biên bản PV01-6; KS-01 Q7, Q8                                                                                                                                                     |
| **Độ ưu tiên**         | Essential                                                                                                                                                                         |
| **Tiêu chí chấp nhận** | Given có 500 tin đăng trong hệ thống, When người dùng lọc theo loại "Thẻ sinh viên" và khu vực "Nhà học C1", Then kết quả trả về trong vòng dưới 2 giây.                          |
| **Trạng thái**         | Approved                                                                                                                                                                          |
| **Phiên bản**          | v1.0 (29/11/2026)                                                                                                                                                                 |

| Mục                    | Nội dung                                                                                                                                                                                                                                              |
| :--------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Mã yêu cầu (ID)**    | **FR-MATCH-001**                                                                                                                                                                                                                                      |
| **Tên yêu cầu**        | Tự động so khớp và gợi ý tin tương đồng                                                                                                                                                                                                               |
| **Mô tả chi tiết**     | Hệ thống NÊN tự động so sánh mức độ tương đồng giữa tin đăng mất và tin đăng nhặt (loại đồ, địa điểm, thời gian, từ khóa mô tả); khi độ tương đồng $\ge 70\%$, hệ thống tự động phát thông báo gợi ý cho sinh viên trong $\le 5$ giây (NFR-PERF-002). |
| **Use case liên quan** | UC-05                                                                                                                                                                                                                                                 |
| **Tác nhân**           | Hệ thống, Sinh viên                                                                                                                                                                                                                                   |
| **Tiền điều kiện**     | Có tin đăng mới được tạo thành công.                                                                                                                                                                                                                  |
| **Hậu điều kiện**      | Thông báo gợi ý được gửi vào hòm thư nội bộ của sinh viên có tin tương đồng.                                                                                                                                                                          |
| **Luồng chính**        | 1. Hệ thống kích hoạt tác vụ nền sau khi có tin đăng mới.<br>2. Giải thuật quét đối soát độ khớp dữ liệu.<br>3. Khi phát hiện các cặp tin khớp nhau $\ge 70\%$, hệ thống gửi thông báo kèm đường dẫn xem chi tiết.                                    |
| **Luồng ngoại lệ**     | Độ tương đồng $< 70\%$: Hệ thống không phát thông báo gợi ý.                                                                                                                                                                                          |
| **Quy tắc nghiệp vụ**  | NFR-PERF-002                                                                                                                                                                                                                                          |
| **Nguồn gốc**          | Khảo sát KS-01 Q12 (87,9% sinh viên cần); AD-03                                                                                                                                                                                                       |
| **Độ ưu tiên**         | Desirable (Nên có)                                                                                                                                                                                                                                    |
| **Tiêu chí chấp nhận** | Given sinh viên A đăng mất thẻ sinh viên tại Khoa CNTT&TT, When người nhặt B đăng nhặt thẻ tại cùng địa điểm, Then hệ thống gửi thông báo gợi ý cho A trong vòng 5 giây.                                                                              |
| **Trạng thái**         | Approved                                                                                                                                                                                                                                              |
| **Phiên bản**          | v1.0 (29/11/2026)                                                                                                                                                                                                                                     |

##### Nhóm VERIFY & CHAT – Xác minh sở hữu và trao đổi

| Mục                    | Nội dung                                                                                                                                        |
| :--------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------- |
| **Mã yêu cầu (ID)**    | **FR-VERIFY-002**                                                                                                                               |
| **Tên yêu cầu**        | Trả lời câu hỏi xác minh sở hữu                                                                                                                 |
| **Mô tả chi tiết**     | Hệ thống PHẢI cho phép sinh viên gửi câu trả lời xác minh đặc điểm đồ vật và tự động đối soát với đáp án của người nhặt.                        |
| **Use case liên quan** | UC-07                                                                                                                                           |
| **Tác nhân**           | Sinh viên                                                                                                                                       |
| **Tiền điều kiện**     | Sinh viên đã đăng nhập; tài khoản không bị khóa 48h.                                                                                            |
| **Hậu điều kiện**      | Nếu đúng: mở khóa đặt lịch hẹn; nếu sai: ghi nhận số lần sai.                                                                                   |
| **Luồng chính**        | 1. Sinh viên nhập câu trả lời xác minh.<br>2. Hệ thống so khớp đáp án.<br>3. Đáp án chính xác: Hệ thống mở quyền đặt lịch hẹn nhận đồ tại trạm. |
| **Luồng ngoại lệ**     | Trả lời sai: Hệ thống báo lỗi câu trả lời không khớp, tăng biến đếm số lần sai và thông báo số lần còn lại.                                     |
| **Quy tắc nghiệp vụ**  | BR-04                                                                                                                                           |
| **Nguồn gốc**          | XĐ-02; BB-KH-02 KH02-2                                                                                                                          |
| **Độ ưu tiên**         | Essential                                                                                                                                       |
| **Tiêu chí chấp nhận** | Given câu hỏi xác minh có đáp án là "màu đỏ", When sinh viên nhập đúng "màu đỏ", Then hệ thống mở quyền chuyển sang màn hình Đặt lịch hẹn.      |
| **Trạng thái**         | Approved                                                                                                                                        |
| **Phiên bản**          | v1.0 (29/11/2026)                                                                                                                               |

| Mục                    | Nội dung                                                                                                                                                                                                                                                          |
| :--------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Mã yêu cầu (ID)**    | **FR-VERIFY-003**                                                                                                                                                                                                                                                 |
| **Tên yêu cầu**        | Khóa tạm thời 48h khi trả lời sai quá 3 lần                                                                                                                                                                                                                       |
| **Mô tả chi tiết**     | Hệ thống PHẢI tự động khóa quyền gửi yêu cầu nhận đồ của tài khoản sinh viên trong vòng 48 giờ nếu người dùng trả lời sai câu hỏi xác minh liên tiếp quá 3 lần, nhằm ngăn chặn hành vi dò đoán để nhận vơ tài sản (BR-04).                                        |
| **Use case liên quan** | UC-07                                                                                                                                                                                                                                                             |
| **Tác nhân**           | Hệ thống                                                                                                                                                                                                                                                          |
| **Tiền điều kiện**     | Sinh viên trả lời sai lần thứ 3 liên tiếp.                                                                                                                                                                                                                        |
| **Hậu điều kiện**      | Tài khoản bị gắn cờ khóa tạm thời 48 giờ; gửi thông báo cảnh báo.                                                                                                                                                                                                 |
| **Luồng chính**        | 1. Hệ thống ghi nhận lần trả lời sai thứ 3.<br>2. Hệ thống cập nhật trạng thái tài khoản sang Khóa xác minh 48h.<br>3. Hệ thống hiển thị thông báo thời gian khóa và đồng hồ đếm ngược.<br>4. Mọi yêu cầu nhận đồ từ tài khoản bị từ chối cho đến khi hết 48 giờ. |
| **Luồng ngoại lệ**     | Hết 48 giờ: Hệ thống tự động mở khóa và reset số lần thử về 0.                                                                                                                                                                                                    |
| **Quy tắc nghiệp vụ**  | BR-04                                                                                                                                                                                                                                                             |
| **Nguồn gốc**          | XĐ-02; BB-KH-02 KH02-2; SD-03                                                                                                                                                                                                                                     |
| **Độ ưu tiên**         | Essential                                                                                                                                                                                                                                                         |
| **Tiêu chí chấp nhận** | Given tài khoản sinh viên đã trả lời sai 2 lần, When nhập sai tiếp lần thứ 3, Then tài khoản bị khóa quyền nhận đồ trong 48 giờ và hiển thị thông báo khóa.                                                                                                       |
| **Trạng thái**         | Approved                                                                                                                                                                                                                                                          |
| **Phiên bản**          | v1.0 (29/11/2026)                                                                                                                                                                                                                                                 |

##### Nhóm APPT – Lịch hẹn nhận đồ tại trạm

| Mục                    | Nội dung                                                                                                                                                                                                              |
| :--------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Mã yêu cầu (ID)**    | **FR-APPT-001**                                                                                                                                                                                                       |
| **Tên yêu cầu**        | Đặt lịch hẹn nhận đồ trực tuyến theo ca trực                                                                                                                                                                          |
| **Mô tả chi tiết**     | Hệ thống PHẢI cho phép sinh viên chọn ngày và khung giờ hẹn đến trạm theo đúng giờ mở cửa trực bàn (07:30–11:00 và 13:30–17:00, thứ Hai đến thứ Sáu); sau khi lưu, hệ thống PHẢI cấp mã QR lịch hẹn duy nhất (BR-05). |
| **Use case liên quan** | UC-09                                                                                                                                                                                                                 |
| **Tác nhân**           | Sinh viên                                                                                                                                                                                                             |
| **Tiền điều kiện**     | Yêu cầu nhận đồ đã được xác minh sở hữu hợp lệ.                                                                                                                                                                       |
| **Hậu điều kiện**      | Phiếu hẹn được tạo trạng thái "Chờ xác nhận"; mã QR lịch hẹn được gửi về tài khoản.                                                                                                                                   |
| **Luồng chính**        | 1. Sinh viên chọn ngày và khung giờ trực còn trống.<br>2. Hệ thống kiểm tra khung giờ hợp lệ.<br>3. Hệ thống lưu phiếu hẹn và cấp mã QR lịch hẹn.                                                                     |
| **Luồng ngoại lệ**     | Chọn ngoài khung giờ trực trạm: Hệ thống từ chối và báo lỗi ngoài giờ phục vụ.                                                                                                                                        |
| **Quy tắc nghiệp vụ**  | BR-05                                                                                                                                                                                                                 |
| **Nguồn gốc**          | XĐ-03; BB-KH-02 KH02-5; KS-01 Q16 (93,5% SV ủng hộ)                                                                                                                                                                   |
| **Độ ưu tiên**         | Essential                                                                                                                                                                                                             |
| **Tiêu chí chấp nhận** | Given sinh viên xác minh đúng món đồ, When chọn khung giờ "08:00 - 08:30 sáng Thứ Tư", Then phiếu hẹn được tạo và hiển thị mã QR lịch hẹn.                                                                            |
| **Trạng thái**         | Approved                                                                                                                                                                                                              |
| **Phiên bản**          | v1.0 (29/11/2026)                                                                                                                                                                                                     |

| Mục                    | Nội dung                                                                                                                                                                                                                                                       |
| :--------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Mã yêu cầu (ID)**    | **FR-APPT-002**                                                                                                                                                                                                                                                |
| **Tên yêu cầu**        | Điều chỉnh và hủy lịch hẹn nhận đồ                                                                                                                                                                                                                             |
| **Mô tả chi tiết**     | Hệ thống NÊN cho phép sinh viên tự đổi khung giờ hoặc hủy lịch hẹn trước giờ hẹn tối thiểu 2 giờ để giải phóng chỗ cho người khác (phát hiện từ phân tích CRUDL).                                                                                              |
| **Use case liên quan** | UC-09                                                                                                                                                                                                                                                          |
| **Tác nhân**           | Sinh viên                                                                                                                                                                                                                                                      |
| **Tiền điều kiện**     | Lịch hẹn đang ở trạng thái Chờ xác nhận hoặc Đã xác nhận; còn trước giờ hẹn $\ge 2$ giờ.                                                                                                                                                                       |
| **Hậu điều kiện**      | Lịch hẹn được cập nhật khung giờ mới hoặc chuyển trạng thái sang "Đã hủy".                                                                                                                                                                                     |
| **Luồng chính**        | 1. Sinh viên chọn Đổi lịch hoặc Hủy hẹn tại danh sách lịch hẹn cá nhân.<br>2. Chọn Hủy hẹn: Hệ thống xác nhận và cập nhật trạng thái phiếu hẹn sang "Đã hủy".<br>3. Chọn Đổi giờ: Sinh viên chọn khung giờ mới; hệ thống cập nhật lịch và phát hành mã QR mới. |
| **Luồng ngoại lệ**     | Thao tác cận giờ hẹn ($< 2$ giờ): Hệ thống thông báo không thể đổi lịch trực tuyến và yêu cầu liên hệ trực tiếp bàn trực trạm.                                                                                                                                 |
| **Quy tắc nghiệp vụ**  | Phát hiện từ phân tích CRUDL                                                                                                                                                                                                                                   |
| **Nguồn gốc**          | Phân tích CRUDL; Phản hồi PT-01 #3                                                                                                                                                                                                                             |
| **Độ ưu tiên**         | Desirable                                                                                                                                                                                                                                                      |
| **Tiêu chí chấp nhận** | Given sinh viên có lịch hẹn lúc 14:00 ngày mai, When chọn Hủy lịch hẹn lúc 09:00 hôm nay, Then trạng thái lịch hẹn chuyển sang Đã hủy và ô lịch được giải phóng.                                                                                               |
| **Trạng thái**         | Approved                                                                                                                                                                                                                                                       |
| **Phiên bản**          | v1.0 (29/11/2026)                                                                                                                                                                                                                                              |

##### Nhóm STATION & RETURN – Tiếp nhận kho và giao trả đồ

| Mục                    | Nội dung                                                                                                                                                                       |
| :--------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Mã yêu cầu (ID)**    | **FR-STATION-001**                                                                                                                                                             |
| **Tên yêu cầu**        | Tiếp nhận hiện vật vào kho trạm và in/cấp mã QR                                                                                                                                |
| **Mô tả chi tiết**     | Hệ thống PHẢI cho phép quản lý trạm nhập thông tin tiếp nhận hiện vật thực tế, gán vị trí ngăn tủ kho và cấp mã QR định danh duy nhất in dán lên nhãn đồ vật.                  |
| **Use case liên quan** | UC-10                                                                                                                                                                          |
| **Tác nhân**           | Quản lý trạm                                                                                                                                                                   |
| **Tiền điều kiện**     | Quản lý trạm đã đăng nhập trên máy bàn trực.                                                                                                                                   |
| **Hậu điều kiện**      | Bản ghi vật phẩm được tạo trạng thái "Đang lưu kho"; mã QR được sinh ra.                                                                                                       |
| **Luồng chính**        | 1. Quản lý trạm nhập đặc điểm món đồ tiếp nhận và chọn ngăn tủ lưu giữ.<br>2. Hệ thống tạo bản ghi VatPhamLuuKho.<br>3. Hệ thống sinh mã QR định danh vật phẩm để in nhãn dán. |
| **Luồng ngoại lệ**     | Ngăn tủ đã đầy: Hệ thống cảnh báo sức chứa và gợi ý chọn ngăn tủ khác.                                                                                                         |
| **Quy tắc nghiệp vụ**  | Phân tích CRUDL (không xóa vật lý bản ghi lưu kho).                                                                                                                            |
| **Nguồn gốc**          | XĐ-03; Biên bản PV03-4                                                                                                                                                         |
| **Độ ưu tiên**         | Essential                                                                                                                                                                      |
| **Tiêu chí chấp nhận** | Given trạm tiếp nhận một chiếc tai nghe, When quản lý trạm lưu kho vào ngăn T1-02, Then hệ thống cấp mã QR nhãn và cập nhật trạng thái Đang lưu kho.                           |
| **Trạng thái**         | Approved                                                                                                                                                                       |
| **Phiên bản**          | v1.0 (29/11/2026)                                                                                                                                                              |

| Mục                    | Nội dung                                                                                                                                                                                                                                                                                                            |
| :--------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Mã yêu cầu (ID)**    | **FR-RETURN-001**                                                                                                                                                                                                                                                                                                   |
| **Tên yêu cầu**        | Quét mã QR tra cứu hồ sơ và xác nhận trao trả đồ                                                                                                                                                                                                                                                                    |
| **Mô tả chi tiết**     | Hệ thống PHẢI cho phép quản lý trạm quét mã QR lịch hẹn để tải hồ sơ đối soát trong $\le 1$ giây (NFR-PERF-003); sau khi đối chiếu Thẻ sinh viên/CCCD gốc khớp, quản lý trạm bấm xác nhận và hệ thống PHẢI cập nhật trạng thái vật phẩm thành "Đã trao trả" (BR-06).                                                |
| **Use case liên quan** | UC-11                                                                                                                                                                                                                                                                                                               |
| **Tác nhân**           | Quản lý trạm                                                                                                                                                                                                                                                                                                        |
| **Tiền điều kiện**     | Quản lý trạm đã đăng nhập; vật phẩm ở trạng thái Đang lưu kho.                                                                                                                                                                                                                                                      |
| **Hậu điều kiện**      | Vật phẩm chuyển sang trạng thái "Đã trao trả"; xuất khỏi danh sách tồn kho trạm.                                                                                                                                                                                                                                    |
| **Luồng chính**        | 1. Quản lý trạm quét mã QR lịch hẹn của sinh viên.<br>2. Hệ thống hiển thị hồ sơ đối soát kèm ảnh và thông tin người hẹn.<br>3. Quản lý trạm đối chiếu Thẻ sinh viên/CCCD gốc.<br>4. Thông tin khớp: Bấm Xác nhận trao trả.<br>5. Hệ thống chuyển trạng thái vật phẩm sang "Đã trao trả" và gửi thông báo hoàn tất. |
| **Luồng ngoại lệ**     | Quét mã QR của đồ đang tranh chấp (UC-08): Hệ thống cảnh báo đỏ và khóa nút xác nhận trao trả (BR-07).                                                                                                                                                                                                              |
| **Quy tắc nghiệp vụ**  | BR-06, BR-07; Mục tiêu MT-04                                                                                                                                                                                                                                                                                        |
| **Nguồn gốc**          | XĐ-03; Biên bản PV02-3; AD-02, SD-02                                                                                                                                                                                                                                                                                |
| **Độ ưu tiên**         | Essential                                                                                                                                                                                                                                                                                                           |
| **Tiêu chí chấp nhận** | Given sinh viên xuất trình mã QR hợp lệ và Thẻ sinh viên trùng khớp, When quản lý trạm bấm Xác nhận trao trả, Then trạng thái vật phẩm cập nhật thành Đã trao trả trong vòng 1 giây.                                                                                                                                |
| **Trạng thái**         | Approved                                                                                                                                                                                                                                                                                                            |
| **Phiên bản**          | v1.0 (29/11/2026)                                                                                                                                                                                                                                                                                                   |

##### Nhóm OVERDUE & SHIFT – Ca trực và xử lý quá hạn

| Mục                    | Nội dung                                                                                                                                                                                                                                     |
| :--------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Mã yêu cầu (ID)**    | **FR-OVERDUE-001**                                                                                                                                                                                                                           |
| **Tên yêu cầu**        | Tự động quét và cảnh báo vật phẩm quá hạn lưu trữ                                                                                                                                                                                            |
| **Mô tả chi tiết**     | Hệ thống PHẢI chạy tác vụ quét định kỳ hằng ngày lúc 00:00 để tự động lọc các hiện vật vượt quá thời hạn lưu kho (30 ngày đối với đồ thường, 90 ngày đối với đồ giá trị), chuyển trạng thái sang "Quá hạn" và cảnh báo nhân sự trạm (BR-02). |
| **Use case liên quan** | UC-13                                                                                                                                                                                                                                        |
| **Tác nhân**           | Hệ thống                                                                                                                                                                                                                                     |
| **Tiền điều kiện**     | Có đồ vật lưu kho vượt quá số ngày quy định.                                                                                                                                                                                                 |
| **Hậu điều kiện**      | Vật phẩm chuyển sang trạng thái "Quá hạn"; thêm vào danh sách chờ bàn giao CTSV.                                                                                                                                                             |
| **Luồng chính**        | 1. Hệ thống quét ngày nhập kho của các vật phẩm Đang lưu kho.<br>2. Tính số ngày lưu = Ngày hiện tại - Ngày nhập kho.<br>3. Nếu số ngày lưu vượt hạn quy định: Chuyển trạng thái sang "Quá hạn" và đưa vào danh sách chờ bàn giao.           |
| **Luồng ngoại lệ**     | Đồ vật đang có lịch hẹn nhận trong ngày: Tạm hoãn chuyển quá hạn thêm 24 giờ.                                                                                                                                                                |
| **Quy tắc nghiệp vụ**  | BR-02; Mục tiêu MT-05                                                                                                                                                                                                                        |
| **Nguồn gốc**          | XĐ-01; BB-KH-01 KH01-1; ST-01                                                                                                                                                                                                                |
| **Độ ưu tiên**         | Essential                                                                                                                                                                                                                                    |
| **Tiêu chí chấp nhận** | Given một cuốn giáo trình đã lưu kho 31 ngày, When hệ thống quét tác vụ nửa đêm, Then trạng thái cuốn sách chuyển sang Quá hạn.                                                                                                              |
| **Trạng thái**         | Approved                                                                                                                                                                                                                                     |
| **Phiên bản**          | v1.0 (29/11/2026)                                                                                                                                                                                                                            |

| Mục                    | Nội dung                                                                                                                                                                                                                                                                                                                                              |
| :--------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Mã yêu cầu (ID)**    | **FR-OVERDUE-002**                                                                                                                                                                                                                                                                                                                                    |
| **Tên yêu cầu**        | Lập biên bản bàn giao điện tử chuyển Phòng CTSV                                                                                                                                                                                                                                                                                                       |
| **Mô tả chi tiết**     | Hệ thống PHẢI cho phép quản lý trạm kết xuất danh sách đồ quá hạn, tạo biên bản bàn giao điện tử kèm mã chứng từ; sau khi Cán bộ CTSV ký xác nhận tiếp nhận trên hệ thống, trạng thái các vật phẩm PHẢI cập nhật sang "Đã bàn giao" (BR-08).                                                                                                          |
| **Use case liên quan** | UC-13                                                                                                                                                                                                                                                                                                                                                 |
| **Tác nhân**           | Quản lý trạm, Cán bộ CTSV                                                                                                                                                                                                                                                                                                                             |
| **Tiền điều kiện**     | Có ít nhất 1 vật phẩm ở trạng thái Quá hạn.                                                                                                                                                                                                                                                                                                           |
| **Hậu điều kiện**      | Biên bản bàn giao CTSV được lưu vĩnh viễn; vật phẩm chuyển sang "Đã bàn giao".                                                                                                                                                                                                                                                                        |
| **Luồng chính**        | 1. Quản lý trạm chọn các món đồ quá hạn và nhấn Lập biên bản bàn giao.<br>2. Hệ thống sinh mã biên bản và xuất danh sách kiểm kê.<br>3. Cán bộ CTSV kiểm tra hiện vật thực tế và bấm Xác nhận tiếp nhận trên tài khoản CTSV.<br>4. Hệ thống cập nhật trạng thái biên bản thành "Đã tiếp nhận" và toàn bộ vật phẩm trong biên bản thành "Đã bàn giao". |
| **Luồng ngoại lệ**     | Cán bộ CTSV từ chối một số món do sai lệch hiện vật: Hệ thống cho phép tách các món sai lệch để trạm kiểm tra lại.                                                                                                                                                                                                                                    |
| **Quy tắc nghiệp vụ**  | BR-08; Phân tích CRUDL (biên bản không bị xóa)                                                                                                                                                                                                                                                                                                        |
| **Nguồn gốc**          | XĐ-01; Biên bản PV02-2; BB-KH-01                                                                                                                                                                                                                                                                                                                      |
| **Độ ưu tiên**         | Essential                                                                                                                                                                                                                                                                                                                                             |
| **Tiêu chí chấp nhận** | Given danh sách 10 món đồ quá hạn, When Cán bộ CTSV bấm xác nhận tiếp nhận biên bản bàn giao, Then trạng thái 10 món đồ đồng loạt chuyển thành Đã bàn giao.                                                                                                                                                                                           |
| **Trạng thái**         | Approved                                                                                                                                                                                                                                                                                                                                              |
| **Phiên bản**          | v1.0 (29/11/2026)                                                                                                                                                                                                                                                                                                                                     |

##### Nhóm RPT, NOTI, MOD, CAT & ROLE (Tóm tắt đặc tả)

```text
[GHI CHÚ HƯỚNG DẪN KHI LÊN WORD]
Đối với các FR còn lại (FR-ROLE-001, FR-POST-003, FR-SEARCH-002, FR-VERIFY-001, FR-VERIFY-004, FR-CHAT-001, FR-STATION-002, FR-RETURN-002, FR-SHIFT-001, FR-SHIFT-002, FR-MOD-001, FR-CAT-001, FR-RPT-001, FR-NOTI-001), anh em kẻ bảng thẻ 14 dòng tương tự như các bảng trên, lấy đúng nội dung từ file CT241_Nhom02_RTM_v1.0.xlsx.
```

---

## 3.3. Yêu cầu hiệu năng

|        Mã        | Yêu cầu                                                                                                                                          | Cách kiểm chứng                                                                |  Ưu tiên  |
| :--------------: | :----------------------------------------------------------------------------------------------------------------------------------------------- | :----------------------------------------------------------------------------- | :-------: |
| **NFR-PERF-001** | Hệ thống PHẢI trả kết quả tra cứu và lọc đồ thất lạc trong vòng 2 giây cho 95% yêu cầu khi có 200 người dùng đồng thời.                          | Kiểm thử tải 200 người dùng ảo trong 15 phút; đo thời gian đáp ứng phân vị 95. | Essential |
| **NFR-PERF-002** | Hệ thống PHẢI hoàn tất việc quét so khớp và gửi thông báo gợi ý tin tương đồng trong vòng 5 giây sau khi có tin đăng mới được lưu.               | Đo thời gian xử lý tác vụ đối soát trên tập dữ liệu mẫu 500 tin đăng.          | Desirable |
| **NFR-PERF-003** | Sau mỗi lần quét mã QR lịch hẹn hoặc mã nhãn vật phẩm tại trạm, hệ thống PHẢI tải và hiển thị hồ sơ đối soát trong vòng 1 giây cho 99% lần quét. | Đo thời gian 200 lần quét thực tế trên thiết bị quầy trạm chuẩn.               | Essential |

---

## 3.4. Ràng buộc thiết kế

- Tuân thủ triệt để các ràng buộc C-01 đến C-06 (Mục 2.4).
- Kiến trúc ứng dụng Web responsive; giao diện hiển thị thích ứng mượt mà trên màn hình di động từ 360 px trở lên, không bị vỡ khung hay tràn ngang (NFR-USA-002).
- Cơ sở dữ liệu quan hệ lưu trữ trên máy chủ trường; tuân thủ nguyên tắc toàn vẹn không xóa vật lý các bản ghi lịch sử theo phân tích CRUDL.

---

## 3.5. Các thuộc tính chất lượng

|        Mã        | Yêu cầu                                                                                                                                                                                                         | Cách kiểm chứng                                                                            |  Ưu tiên  |
| :--------------: | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :----------------------------------------------------------------------------------------- | :-------: |
| **NFR-SEC-001**  | Hệ thống PHẢI kiểm tra quyền ở phía máy chủ cho mọi yêu cầu; sinh viên chỉ xem và sửa được dữ liệu cá nhân của chính mình.                                                                                      | Kiểm thử bảo mật thử truy cập chéo tài nguyên giữa 2 tài khoản sinh viên khác nhau.        | Essential |
| **NFR-SEC-002**  | Phiên đăng nhập trên điện thoại PHẢI hết hạn sau 30 phút không thao tác; phiên làm việc trên máy quầy trạm PHẢI hết hạn sau 10 phút để tránh bị lạm dụng khi vắng mặt.                                          | Để máy rảnh đúng thời gian quy định; kiểm tra thao tác kế tiếp bị yêu cầu đăng nhập lại.   | Essential |
| **NFR-SEC-003**  | Toàn bộ dữ liệu nhạy cảm (số điện thoại, chi tiết đồ giá trị) PHẢI được che mờ công khai; kênh trao đổi in-app PHẢI ẩn số điện thoại người dùng (BR-03).                                                        | Kiểm tra giao diện người dùng công khai và đối chiếu phản hồi JSON từ API.                 | Essential |
| **NFR-SEC-004**  | Mọi thao tác tiếp nhận kho, xác nhận trao trả và lập biên bản bàn giao CTSV PHẢI được ghi nhật ký kiểm toán gồm người thực hiện, thời điểm, trạng thái trước và sau; nhật ký không thể chỉnh sửa qua giao diện. | Thực hiện thao tác tại quầy và đối chiếu bản ghi nhật ký hệ thống; thử xóa/sửa nhật ký.    | Essential |
| **NFR-AVA-001**  | Hệ thống trực tuyến (đăng tin, tra cứu, đặt lịch) PHẢI sẵn sàng tối thiểu 99,5% thời gian mỗi tháng trong khung giờ 06:00–22:00 hằng ngày.                                                                      | Đo bằng công cụ giám sát uptime trong 1 tháng vận hành thử nghiệm.                         | Essential |
| **NFR-REL-001**  | Cơ sở dữ liệu PHẢI được tự động sao lưu hằng ngày lúc 02:00; khi có sự cố, PHẢI khôi phục được hệ thống trong vòng 4 giờ và mất tối đa dữ liệu của 24 giờ.                                                      | Diễn tập khôi phục hệ thống từ bản sao lưu gần nhất trên máy chủ thử nghiệm.               | Essential |
| **NFR-USA-001**  | Sinh viên quản lý trạm mới, sau 15 phút hướng dẫn, PHẢI hoàn thành một lượt quét mã QR và xác nhận giao trả đồ cho sinh viên trong thời gian không quá 60 giây.                                                 | Thử nghiệm bấm giờ với 3 sinh viên tình nguyện lần đầu sử dụng giao diện quầy.             | Essential |
| **NFR-USA-002**  | Toàn bộ giao diện sinh viên PHẢI hiển thị đầy đủ, không bị cuộn ngang trên màn hình điện thoại có độ rộng từ 360 px trở lên.                                                                                    | Kiểm tra trên trình giả lập kích thước 360 px và trên 2 điện thoại thông minh thực tế.     | Essential |
| **NFR-COMP-001** | Giao diện web PHẢI hoạt động chính xác và tương thích trên Chrome, Edge, Safari và Firefox ở 2 phiên bản mới nhất.                                                                                              | Thực hiện bộ kiểm thử chấp nhận trên cả 4 trình duyệt máy tính và di động.                 | Essential |
| **NFR-COMP-002** | Hệ thống PHẢI tương thích và nhận diện chính xác mã QR Code chuẩn ISO/IEC 18004 qua camera điện thoại hoặc máy quét mã vạch 2D cổng USB giả lập bàn phím.                                                       | Quét thử nghiệm 100 mã QR mẫu bằng cả camera điện thoại và máy quét quầy.                  | Essential |
| **NFR-MAIN-001** | Các tham số quy định trạm (thời hạn lưu giữ 30/90 ngày, khung giờ mở cửa trạm) PHẢI thay đổi được qua giao diện quản trị mà không cần sửa mã nguồn, có hiệu lực trong vòng 1 phút.                              | Đổi tham số thời hạn lưu qua giao diện, kiểm tra tác vụ quét quá hạn áp dụng thời hạn mới. | Essential |
