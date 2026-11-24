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

| Mã | Tên yêu cầu chức năng | Độ ưu tiên | Use case liên quan |
|:---:|:---|:---:|:---:|
| **FR-AUTH-001** | Đăng nhập bằng tài khoản trường qua SSO | Essential | UC-01 |
| **FR-AUTH-002** | Phân quyền truy cập theo vai trò | Essential | UC-01 |
| **FR-ROLE-001** | Quản lý và phân quyền nhân sự trạm | Essential | UC-16 |
| **FR-POST-001** | Đăng tin tìm đồ thất lạc | Essential | UC-02 |
| **FR-POST-002** | Đăng tin nhặt được đồ kèm câu hỏi xác minh | Essential | UC-03 |
| **FR-POST-003** | Quản lý và chỉnh sửa tin đăng cá nhân | Desirable | UC-02, UC-03 |
| **FR-SEARCH-001** | Tra cứu và lọc danh sách đồ thất lạc đa tiêu chí | Essential | UC-04 |
| **FR-SEARCH-002** | Xem thông tin chi tiết vật phẩm và làm mờ ảnh đồ giá trị | Essential | UC-04 |
| **FR-MATCH-001** | Tự động so khớp và gợi ý tin tương đồng | Desirable | UC-05 |
| **FR-VERIFY-001** | Thiết lập câu hỏi xác minh ẩn danh | Essential | UC-03, UC-07 |
| **FR-VERIFY-002** | Trả lời câu hỏi xác minh sở hữu | Essential | UC-07 |
| **FR-VERIFY-003** | Khóa tạm thời 48h khi trả lời sai quá 3 lần | Essential | UC-07 |
| **FR-VERIFY-004** | Đối chiếu thông tin giấy tờ tùy thân tại quầy | Essential | UC-11 |
| **FR-CHAT-001** | Nhắn tin trao đổi ẩn danh in-app | Desirable | UC-06 |
| **FR-APPT-001** | Đặt lịch hẹn nhận đồ trực tuyến theo ca trực | Essential | UC-09 |
| **FR-APPT-002** | Điều chỉnh và hủy lịch hẹn nhận đồ | Desirable | UC-09 |
| **FR-STATION-001** | Tiếp nhận hiện vật vào kho trạm và in/cấp mã QR | Essential | UC-10 |
| **FR-STATION-002** | Quản lý vị trí ngăn tủ và trạng thái vật phẩm lưu kho | Essential | UC-10, UC-12 |
| **FR-RETURN-001** | Quét mã QR tra cứu hồ sơ và xác nhận trao trả đồ | Essential | UC-11 |
| **FR-RETURN-002** | Chụp ảnh lưu bằng chứng giao nhận điện tử | Essential | UC-11 |
| **FR-SHIFT-001** | Điểm danh nhận ca và bàn giao ca trực trạm | Essential | UC-12 |
| **FR-SHIFT-002** | Kiểm kê kho hiện vật đối soát thực tế theo ca | Desirable | UC-12 |
| **FR-OVERDUE-001** | Tự động quét và cảnh báo vật phẩm quá hạn lưu trữ | Essential | UC-13 |
| **FR-OVERDUE-002** | Lập biên bản bàn giao điện tử chuyển Phòng CTSV | Essential | UC-13 |
| **FR-MOD-001** | Tiếp nhận báo cáo vi phạm và phong tỏa đồ tranh chấp | Essential | UC-08, UC-14 |
| **FR-CAT-001** | Cấu hình tham số quy định trạm và danh mục loại đồ | Essential | UC-15 |
| **FR-RPT-001** | Thống kê số liệu và xuất báo cáo định kỳ | Essential | UC-17 |
| **FR-NOTI-001** | Gửi thông báo tự động đa kênh (Web, Email) | Essential | UC-18 |

---

#### Bảng thẻ đặc tả chi tiết 28 yêu cầu chức năng (Template Bảng 4.9 giáo trình)

##### Nhóm 1: AUTH & ROLE – Xác thực, phân quyền và nhân sự

| Mục | Nội dung |
|:---|:---|
| **Mã yêu cầu (ID)** | **FR-AUTH-001** |
| **Tên yêu cầu** | Đăng nhập bằng tài khoản trường qua SSO |
| **Mô tả chi tiết** | Hệ thống PHẢI xác thực người dùng qua dịch vụ đăng nhập dùng chung (SSO) của Trường Đại học Cần Thơ khi truy cập các chức năng cần định danh, để không phải quản lý mật khẩu riêng (C-01). |
| **Use case liên quan** | UC-01 |
| **Tác nhân** | Sinh viên, Quản lý trạm, Cán bộ CTSV |
| **Tiền điều kiện** | Người dùng có tài khoản email trường Đại học Cần Thơ còn hiệu lực. |
| **Hậu điều kiện** | Phiên làm việc được khởi tạo đúng vai trò tương ứng. |
| **Luồng chính** | 1. Người dùng chọn Đăng nhập.<br>2. Hệ thống chuyển hướng sang cổng SSO của trường.<br>3. SSO xác thực thành công và trả về định danh; hệ thống cấp quyền theo vai trò. |
| **Luồng ngoại lệ** | SSO báo lỗi hoặc tài khoản bị khóa: Hệ thống hiển thị thông báo lỗi và giữ người dùng ở trang công khai. |
| **Quy tắc nghiệp vụ** | C-01; Phiên làm việc tự động hết hạn sau 30 phút rảnh (NFR-SEC-002). |
| **Nguồn gốc** | Tầm nhìn 2.3; Biên bản PV02-5 |
| **Độ ưu tiên** | Essential (Bắt buộc) |
| **Tiêu chí chấp nhận** | Given sinh viên có tài khoản trường hợp lệ, When đăng nhập qua SSO, Then trang chủ hiển thị họ tên, MSSV và vai trò Sinh viên. |
| **Trạng thái** | Approved |
| **Phiên bản** | v1.0 (29/11/2026) |

| Mục | Nội dung |
|:---|:---|
| **Mã yêu cầu (ID)** | **FR-AUTH-002** |
| **Tên yêu cầu** | Phân quyền truy cập theo vai trò |
| **Mô tả chi tiết** | Hệ thống PHẢI giới hạn quyền truy cập menu và chức năng theo 4 vai trò (Sinh viên, Quản lý trạm, Cán bộ CTSV, Quản trị hệ thống) để bảo đảm an toàn dữ liệu. |
| **Use case liên quan** | UC-01, UC-16 |
| **Tác nhân** | Hệ thống |
| **Tiền điều kiện** | Người dùng đã đăng nhập. |
| **Hậu điều kiện** | Menu và API chỉ mở các chức năng thuộc thẩm quyền của vai trò. |
| **Luồng chính** | 1. Hệ thống đọc vai trò người dùng sau khi xác thực.<br>2. Hệ thống tải menu giao diện tương ứng.<br>3. Mọi truy cập vào chức năng ngoài phạm vi vai trò đều bị chặn từ máy chủ. |
| **Luồng ngoại lệ** | Truy cập trái phép qua URL: Hệ thống trả mã lỗi 403, từ chối truy cập và ghi nhật ký kiểm toán. |
| **Quy tắc nghiệp vụ** | Phân quyền do Quản trị hoặc Cán bộ CTSV cấu hình (UC-16). |
| **Nguồn gốc** | Biên bản PV02-5; NFR-SEC-001 |
| **Độ ưu tiên** | Essential |
| **Tiêu chí chấp nhận** | Given sinh viên đã đăng nhập, When cố ý mở đường dẫn trang quản lý kho trạm, Then hệ thống từ chối và ghi log vi phạm. |
| **Trạng thái** | Approved |
| **Phiên bản** | v1.0 (29/11/2026) |

| Mục | Nội dung |
|:---|:---|
| **Mã yêu cầu (ID)** | **FR-ROLE-001** |
| **Tên yêu cầu** | Quản lý và phân quyền nhân sự trạm |
| **Mô tả chi tiết** | Hệ thống PHẢI cho phép Cán bộ CTSV tìm kiếm tài khoản sinh viên theo MSSV, gán hoặc thu hồi vai trò "Quản lý trạm" theo từng học kỳ, nhằm bảo đảm chỉ sinh viên có phân công chính thức mới được truy cập nghiệp vụ kho. |
| **Use case liên quan** | UC-16 |
| **Tác nhân** | Cán bộ CTSV |
| **Tiền điều kiện** | Sinh viên đã từng đăng nhập hệ thống qua SSO (đã có hồ sơ tài khoản trong CSDL). |
| **Hậu điều kiện** | Phân quyền mới được cập nhật; tài khoản được cấp quyền truy cập phân hệ kho quầy trạm. |
| **Luồng chính** | 1. Cán bộ CTSV tìm kiếm sinh viên bằng MSSV.<br>2. Chọn gán vai trò Quản lý trạm.<br>3. Chọn học kỳ áp dụng.<br>4. Hệ thống cập nhật quyền và kích hoạt menu quản lý quầy trạm cho tài khoản sinh viên đó. |
| **Luồng ngoại lệ** | Hết học kỳ hoặc sinh viên nghỉ trực: Cán bộ CTSV bấm Thu hồi quyền; hệ thống đưa tài khoản về vai trò Sinh viên thông thường. |
| **Quy tắc nghiệp vụ** | C-06; Phân tích CRUDL (tài khoản không bị xóa mà chỉ cập nhật quyền). |
| **Nguồn gốc** | Biên bản PV02-4; PV03-7 |
| **Độ ưu tiên** | Essential |
| **Tiêu chí chấp nhận** | Given sinh viên B2303828 có vai trò Sinh viên, When Cán bộ CTSV gán quyền Quản lý trạm, Then tài khoản đăng nhập lại sẽ xuất hiện menu Quản lý kho và Quét mã giao trả. |
| **Trạng thái** | Approved |
| **Phiên bản** | v1.0 (29/11/2026) |

##### Nhóm 2: POST – Đăng tin thất lạc và nhặt được

| Mục | Nội dung |
|:---|:---|
| **Mã yêu cầu (ID)** | **FR-POST-001** |
| **Tên yêu cầu** | Đăng tin tìm đồ thất lạc |
| **Mô tả chi tiết** | Hệ thống PHẢI cho phép sinh viên đăng tin tìm đồ thất lạc gồm danh mục, khu vực rơi, thời gian, mô tả đặc điểm chi tiết và ảnh đính kèm (nếu có). |
| **Use case liên quan** | UC-02 |
| **Tác nhân** | Sinh viên |
| **Tiền điều kiện** | Sinh viên đã đăng nhập qua SSO trường. |
| **Hậu điều kiện** | Tin đăng được lưu ở trạng thái "Chờ xác nhận". |
| **Luồng chính** | 1. Sinh viên nhập thông tin theo biểu mẫu.<br>2. Hệ thống kiểm tra tính hợp lệ của dữ liệu.<br>3. Hệ thống kiểm tra giới hạn $\le 5$ tin đang mở (BR-01).<br>4. Hệ thống lưu tin đăng và hiển thị thông báo thành công. |
| **Luồng ngoại lệ** | Thiếu trường bắt buộc hoặc vượt quá 5 tin đang mở: Hệ thống từ chối lưu bài viết và thông báo lý do cụ thể. |
| **Quy tắc nghiệp vụ** | BR-01 |
| **Nguồn gốc** | Biên bản PV01-1; Khảo sát KS-01 Q6 |
| **Độ ưu tiên** | Essential |
| **Tiêu chí chấp nhận** | Given sinh viên có dưới 5 tin đang mở, When gửi biểu mẫu đăng tin hợp lệ, Then hệ thống lưu bài viết ở trạng thái Chờ xác nhận. |
| **Trạng thái** | Approved |
| **Phiên bản** | v1.0 (29/11/2026) |

| Mục | Nội dung |
|:---|:---|
| **Mã yêu cầu (ID)** | **FR-POST-002** |
| **Tên yêu cầu** | Đăng tin nhặt được đồ kèm câu hỏi xác minh |
| **Mô tả chi tiết** | Hệ thống PHẢI cho phép người nhặt đăng tin nhặt được đồ; PHẢI bắt buộc thiết lập ít nhất 1 câu hỏi xác minh ẩn danh và TỰ ĐỘNG làm mờ ảnh nếu đồ thuộc danh mục giá trị cao (BR-03). |
| **Use case liên quan** | UC-03 |
| **Tác nhân** | Sinh viên, Quản lý trạm |
| **Tiền điều kiện** | Người nhặt đã đăng nhập. |
| **Hậu điều kiện** | Tin nhặt được lưu trữ và hiển thị công khai dạng bảo mật (ẩn SĐT và mờ ảnh đồ giá trị). |
| **Luồng chính** | 1. Người nhặt nhập thông tin món đồ nhặt được và tải ảnh lên.<br>2. Người nhặt thiết lập câu hỏi và đáp án xác minh bí mật.<br>3. Hệ thống kiểm tra loại đồ; nếu là đồ giá trị (ví, laptop, tiền, điện thoại), tự động áp dụng bộ lọc làm mờ chi tiết cốt lõi.<br>4. Hệ thống lưu tin đăng công khai. |
| **Luồng ngoại lệ** | Chưa nhập câu hỏi xác minh bí mật: Hệ thống báo lỗi và yêu cầu nhập câu hỏi trước khi cho phép đăng tin. |
| **Quy tắc nghiệp vụ** | BR-03 |
| **Nguồn gốc** | XĐ-02; BB-KH-01 KH01-2; KS-01 Q13, Q14 |
| **Độ ưu tiên** | Essential |
| **Tiêu chí chấp nhận** | Given người nhặt đăng ảnh một chiếc ví nhặt được, When lưu tin đăng thành công, Then ảnh ví trên trang công khai bị làm mờ chi tiết và hiển thị câu hỏi xác minh ẩn danh. |
| **Trạng thái** | Approved |
| **Phiên bản** | v1.0 (29/11/2026) |

| Mục | Nội dung |
|:---|:---|
| **Mã yêu cầu (ID)** | **FR-POST-003** |
| **Tên yêu cầu** | Quản lý và chỉnh sửa tin đăng cá nhân |
| **Mô tả chi tiết** | Hệ thống NÊN cho phép người đăng đóng, ẩn hoặc cập nhật thông tin bài viết khi đã tìm lại được đồ hoặc đã hoàn tất trao trả, nhằm giảm tải dữ liệu tìm kiếm hiển thị trên hệ thống. |
| **Use case liên quan** | UC-02, UC-03 |
| **Tác nhân** | Sinh viên, Quản lý trạm |
| **Tiền điều kiện** | Người dùng đã đăng nhập và là chủ sở hữu của tin đăng. |
| **Hậu điều kiện** | Trạng thái tin đăng chuyển sang "Đã đóng" hoặc cập nhật thông tin mới. |
| **Luồng chính** | 1. Người dùng vào mục Quản lý tin đăng cá nhân.<br>2. Chọn một tin đăng đang hoạt động và chọn Đóng tin đăng.<br>3. Hệ thống yêu cầu xác nhận lý do (đã tìm thấy đồ / hủy tìm kiếm).<br>4. Người dùng xác nhận; hệ thống cập nhật trạng thái tin sang "Đã đóng" và ẩn khỏi trang tìm kiếm công khai. |
| **Luồng ngoại lệ** | Tin đăng đã có đồ nhập kho trạm: Hệ thống không cho phép tự ý đóng bài mà hướng dẫn liên hệ trạm để xuất kho theo quy trình. |
| **Quy tắc nghiệp vụ** | Phân tích CRUDL (tin đăng không bị xóa vật lý mà chuyển trạng thái). |
| **Nguồn gốc** | Biên bản PV01-1; BB-KH-02 |
| **Độ ưu tiên** | Desirable (Nên có) |
| **Tiêu chí chấp nhận** | Given sinh viên có tin đăng đang hiển thị công khai, When chọn Đóng tin đăng và xác nhận, Then tin đăng chuyển sang trạng thái Đã đóng và không còn xuất hiện trong kết quả tìm kiếm. |
| **Trạng thái** | Approved |
| **Phiên bản** | v1.0 (29/11/2026) |

##### Nhóm 3: SEARCH & MATCH – Tra cứu và gợi ý đối soát

| Mục | Nội dung |
|:---|:---|
| **Mã yêu cầu (ID)** | **FR-SEARCH-001** |
| **Tên yêu cầu** | Tra cứu và lọc danh sách đồ thất lạc đa tiêu chí |
| **Mô tả chi tiết** | Hệ thống PHẢI cho phép tìm kiếm từ khóa và lọc danh sách đồ theo loại đồ, khu vực rơi/nhặt, mốc thời gian và trạng thái tồn kho trạm trong thời gian $\le 2$ giây (NFR-PERF-001). |
| **Use case liên quan** | UC-04 |
| **Tác nhân** | Sinh viên, Quản lý trạm, Cán bộ CTSV |
| **Tiền điều kiện** | Không có (chức năng công khai). |
| **Hậu điều kiện** | Danh sách kết quả phù hợp được hiển thị. |
| **Luồng chính** | 1. Người dùng chọn các tiêu chí lọc và nhấn Tìm kiếm.<br>2. Hệ thống truy vấn CSDL và trả về danh sách kết quả phù hợp.<br>3. Kết quả tự động phân trang (mỗi trang 12 mục). |
| **Luồng ngoại lệ** | Không có kết quả: Hệ thống hiển thị thông báo không tìm thấy kết quả và gợi ý đăng tin mới. |
| **Quy tắc nghiệp vụ** | Mặc định ẩn các tin đã trao trả thành công. |
| **Nguồn gốc** | Biên bản PV01-6; KS-01 Q7, Q8 |
| **Độ ưu tiên** | Essential |
| **Tiêu chí chấp nhận** | Given có 500 tin đăng trong hệ thống, When người dùng lọc theo loại "Thẻ sinh viên" và khu vực "Nhà học C1", Then kết quả trả về trong vòng dưới 2 giây. |
| **Trạng thái** | Approved |
| **Phiên bản** | v1.0 (29/11/2026) |

| Mục | Nội dung |
|:---|:---|
| **Mã yêu cầu (ID)** | **FR-SEARCH-002** |
| **Tên yêu cầu** | Xem thông tin chi tiết vật phẩm và làm mờ ảnh đồ giá trị |
| **Mô tả chi tiết** | Hệ thống PHẢI hiển thị đầy đủ thông tin chi tiết của món đồ thất lạc gồm mã tin, danh mục, thời gian, khu vực, giờ mở cửa trạm (07:30–11:00 và 13:30–17:00); đồng thời PHẢI tự động làm mờ chi tiết nhận dạng cốt lõi trên ảnh đồ giá trị và ẩn thông tin liên hệ cá nhân (BR-03). |
| **Use case liên quan** | UC-04 |
| **Tác nhân** | Sinh viên, Quản lý trạm, Cán bộ CTSV |
| **Tiền điều kiện** | Người dùng chọn một món đồ từ danh sách tìm kiếm. |
| **Hậu điều kiện** | Màn hình chi tiết vật phẩm được tải hiển thị đúng quy tắc bảo mật. |
| **Luồng chính** | 1. Người dùng chọn xem một món đồ.<br>2. Hệ thống kiểm tra phân loại đồ vật.<br>3. Nếu là đồ giá trị cao: Hệ thống hiển thị ảnh dạng làm mờ, ẩn số điện thoại người nhặt và hiển thị câu hỏi xác minh ẩn danh kèm giờ mở cửa phục vụ của quầy trạm.<br>4. Nếu là đồ thông thường: Hệ thống hiển thị ảnh rõ nét để sinh viên nhận diện. |
| **Luồng ngoại lệ** | Món đồ đã được trao trả xong: Hệ thống hiển thị nhãn "Đã trao trả" và vô hiệu hóa nút gửi yêu cầu nhận đồ. |
| **Quy tắc nghiệp vụ** | BR-03; BR-05 |
| **Nguồn gốc** | BB-KH-02 KH02-5; Khảo sát KS-01 Q17; Prototype PT-01 |
| **Độ ưu tiên** | Essential |
| **Tiêu chí chấp nhận** | Given người dùng mở xem chi tiết một tin nhặt ví tiền, When trang chi tiết tải xong, Then ảnh chụp ví bị làm mờ chi tiết nhạy cảm và hiển thị khung câu hỏi xác minh bí mật. |
| **Trạng thái** | Approved |
| **Phiên bản** | v1.0 (29/11/2026) |

| Mục | Nội dung |
|:---|:---|
| **Mã yêu cầu (ID)** | **FR-MATCH-001** |
| **Tên yêu cầu** | Tự động so khớp và gợi ý tin tương đồng |
| **Mô tả chi tiết** | Hệ thống NÊN tự động so sánh mức độ tương đồng giữa tin đăng mất và tin đăng nhặt (loại đồ, địa điểm, thời gian, từ khóa mô tả); khi độ tương đồng $\ge 70\%$, hệ thống tự động phát thông báo gợi ý cho sinh viên trong $\le 5$ giây (NFR-PERF-002). |
| **Use case liên quan** | UC-05 |
| **Tác nhân** | Hệ thống, Sinh viên |
| **Tiền điều kiện** | Có tin đăng mới được tạo thành công. |
| **Hậu điều kiện** | Thông báo gợi ý được gửi vào hòm thư nội bộ của sinh viên có tin tương đồng. |
| **Luồng chính** | 1. Hệ thống kích hoạt tác vụ nền sau khi có tin đăng mới.<br>2. Giải thuật quét đối soát độ khớp dữ liệu.<br>3. Khi phát hiện các cặp tin khớp nhau $\ge 70\%$, hệ thống gửi thông báo kèm đường dẫn xem chi tiết. |
| **Luồng ngoại lệ** | Độ tương đồng $< 70\%$: Hệ thống không phát thông báo gợi ý. |
| **Quy tắc nghiệp vụ** | NFR-PERF-002 |
| **Nguồn gốc** | Khảo sát KS-01 Q12 (87,9% sinh viên cần); AD-03 |
| **Độ ưu tiên** | Desirable (Nên có) |
| **Tiêu chí chấp nhận** | Given sinh viên A đăng mất thẻ sinh viên tại Khoa CNTT&TT, When người nhặt B đăng nhặt thẻ tại cùng địa điểm, Then hệ thống gửi thông báo gợi ý cho A trong vòng 5 giây. |
| **Trạng thái** | Approved |
| **Phiên bản** | v1.0 (29/11/2026) |

##### Nhóm 4: VERIFY & CHAT – Xác minh sở hữu và trao đổi ẩn danh

| Mục | Nội dung |
|:---|:---|
| **Mã yêu cầu (ID)** | **FR-VERIFY-001** |
| **Tên yêu cầu** | Thiết lập câu hỏi xác minh ẩn danh |
| **Mô tả chi tiết** | Hệ thống PHẢI bắt buộc người nhặt đồ hoặc nhân sự trạm thiết lập ít nhất 1–2 câu hỏi xác minh bí mật kèm đáp án đối chiếu khi tạo tin nhặt đồ; đáp án PHẢI được mã hóa bảo mật phía máy chủ và không công khai ra giao diện (NFR-SEC-001). |
| **Use case liên quan** | UC-03, UC-07 |
| **Tác nhân** | Sinh viên (Người nhặt), Quản lý trạm |
| **Tiền điều kiện** | Người dùng đang thực hiện biểu mẫu đăng tin nhặt đồ. |
| **Hậu điều kiện** | Câu hỏi và đáp án bí mật được liên kết với bản ghi vật phẩm trong CSDL. |
| **Luồng chính** | 1. Người đăng nhập câu hỏi xác minh (ví dụ: "Màu sắc ốp lưng điện thoại là gì?").<br>2. Người đăng nhập câu trả lời chính xác.<br>3. Hệ thống lưu câu hỏi để hiển thị công khai và mã hóa lưu đáp án bảo mật phía server. |
| **Luồng ngoại lệ** | Người đăng bỏ trống câu hỏi hoặc câu trả lời: Hệ thống cảnh báo đỏ và ngăn không cho hoàn tất đăng bài. |
| **Quy tắc nghiệp vụ** | BR-03 |
| **Nguồn gốc** | Biên bản PV03-2; Khảo sát KS-01 Q14; XĐ-02 |
| **Độ ưu tiên** | Essential |
| **Tiêu chí chấp nhận** | Given người nhặt tạo tin đăng nhặt chìa khóa, When nhập câu hỏi "Chùm chìa khóa có móc khóa hình gì?", Then câu hỏi xuất hiện trên trang chi tiết còn đáp án được bảo mật tuyệt đối. |
| **Trạng thái** | Approved |
| **Phiên bản** | v1.0 (29/11/2026) |

| Mục | Nội dung |
|:---|:---|
| **Mã yêu cầu (ID)** | **FR-VERIFY-002** |
| **Tên yêu cầu** | Trả lời câu hỏi xác minh sở hữu |
| **Mô tả chi tiết** | Hệ thống PHẢI cho phép sinh viên gửi câu trả lời xác minh đặc điểm đồ vật và tự động đối soát với đáp án của người nhặt. |
| **Use case liên quan** | UC-07 |
| **Tác nhân** | Sinh viên |
| **Tiền điều kiện** | Sinh viên đã đăng nhập; tài khoản không bị khóa 48h. |
| **Hậu điều kiện** | Nếu đúng: mở khóa đặt lịch hẹn; nếu sai: ghi nhận số lần sai. |
| **Luồng chính** | 1. Sinh viên nhập câu trả lời xác minh.<br>2. Hệ thống so khớp đáp án.<br>3. Đáp án chính xác: Hệ thống mở quyền đặt lịch hẹn nhận đồ tại trạm. |
| **Luồng ngoại lệ** | Trả lời sai: Hệ thống báo lỗi câu trả lời không khớp, tăng biến đếm số lần sai và thông báo số lần còn lại. |
| **Quy tắc nghiệp vụ** | BR-04 |
| **Nguồn gốc** | XĐ-02; BB-KH-02 KH02-2 |
| **Độ ưu tiên** | Essential |
| **Tiêu chí chấp nhận** | Given câu hỏi xác minh có đáp án là "màu đỏ", When sinh viên nhập đúng "màu đỏ", Then hệ thống mở quyền chuyển sang màn hình Đặt lịch hẹn. |
| **Trạng thái** | Approved |
| **Phiên bản** | v1.0 (29/11/2026) |

| Mục | Nội dung |
|:---|:---|
| **Mã yêu cầu (ID)** | **FR-VERIFY-003** |
| **Tên yêu cầu** | Khóa tạm thời 48h khi trả lời sai quá 3 lần |
| **Mô tả chi tiết** | Hệ thống PHẢI tự động khóa quyền gửi yêu cầu nhận đồ của tài khoản sinh viên trong vòng 48 giờ nếu người dùng trả lời sai câu hỏi xác minh liên tiếp quá 3 lần, nhằm ngăn chặn hành vi dò đoán để nhận vơ tài sản (BR-04). |
| **Use case liên quan** | UC-07 |
| **Tác nhân** | Hệ thống |
| **Tiền điều kiện** | Sinh viên trả lời sai lần thứ 3 liên tiếp. |
| **Hậu điều kiện** | Tài khoản bị gắn cờ khóa tạm thời 48 giờ; gửi thông báo cảnh báo. |
| **Luồng chính** | 1. Hệ thống ghi nhận lần trả lời sai thứ 3.<br>2. Hệ thống cập nhật trạng thái tài khoản sang Khóa xác minh 48h.<br>3. Hệ thống hiển thị thông báo thời gian khóa và đồng hồ đếm ngược.<br>4. Mọi yêu cầu nhận đồ từ tài khoản bị từ chối cho đến khi hết 48 giờ. |
| **Luồng ngoại lệ** | Hết 48 giờ: Hệ thống tự động mở khóa và reset số lần thử về 0. |
| **Quy tắc nghiệp vụ** | BR-04 |
| **Nguồn gốc** | XĐ-02; BB-KH-02 KH02-2; SD-03 |
| **Độ ưu tiên** | Essential |
| **Tiêu chí chấp nhận** | Given tài khoản sinh viên đã trả lời sai 2 lần, When nhập sai tiếp lần thứ 3, Then tài khoản bị khóa quyền nhận đồ trong 48 giờ và hiển thị thông báo khóa. |
| **Trạng thái** | Approved |
| **Phiên bản** | v1.0 (29/11/2026) |

| Mục | Nội dung |
|:---|:---|
| **Mã yêu cầu (ID)** | **FR-VERIFY-004** |
| **Tên yêu cầu** | Đối chiếu thông tin giấy tờ tùy thân tại quầy |
| **Mô tả chi tiết** | Khi giao trả đồ tại quầy trạm, nhân sự trạm PHẢI bắt buộc đối chiếu Thẻ sinh viên hoặc CCCD gốc với thông tin tài khoản người nhận trên hệ thống và lưu vết MSSV người nhận thực tế vào nhật ký kiểm toán (BR-06, NFR-SEC-004). |
| **Use case liên quan** | UC-11 |
| **Tác nhân** | Quản lý trạm |
| **Tiền điều kiện** | Sinh viên đã xuất trình mã QR lịch hẹn hợp lệ tại bàn trực trạm. |
| **Hậu điều kiện** | Thông tin đối soát giấy tờ được lưu vết kèm biên bản giao nhận điện tử. |
| **Luồng chính** | 1. Quản lý trạm quét mã QR lịch hẹn của sinh viên.<br>2. Hệ thống hiển thị họ tên, MSSV của chủ tài khoản đã đặt hẹn.<br>3. Quản lý trạm yêu cầu xuất trình Thẻ sinh viên hoặc CCCD gốc và kiểm tra tính trùng khớp.<br>4. Thông tin khớp: Bấm xác nhận đối soát thành công để chuyển sang bước bàn giao hiện vật. |
| **Luồng ngoại lệ** | Giấy tờ không trùng khớp hoặc sinh viên không xuất trình được giấy tờ gốc: Quản lý trạm từ chối trao trả, ghi nhận lý do nghi vấn vào hệ thống (BR-06). |
| **Quy tắc nghiệp vụ** | BR-06 |
| **Nguồn gốc** | Biên bản PV02-3; PV03-2; XĐ-03 |
| **Độ ưu tiên** | Essential |
| **Tiêu chí chấp nhận** | Given sinh viên đến trạm nhận đồ, When quản lý trạm đối chiếu Thẻ sinh viên hoặc CCCD gốc trùng khớp với thông tin trên hệ thống, Then hệ thống kích hoạt nút Xác nhận trao trả. |
| **Trạng thái** | Approved |
| **Phiên bản** | v1.0 (29/11/2026) |

| Mục | Nội dung |
|:---|:---|
| **Mã yêu cầu (ID)** | **FR-CHAT-001** |
| **Tên yêu cầu** | Nhắn tin trao đổi ẩn danh in-app |
| **Mô tả chi tiết** | Hệ thống NÊN cung cấp kênh nhắn tin nội bộ ẩn danh trực tiếp giữa người mất và người nhặt đồ để trao đổi thêm đặc điểm nhận diện mà tuyệt đối không để lộ số điện thoại cá nhân (NFR-SEC-003). |
| **Use case liên quan** | UC-06 |
| **Tác nhân** | Sinh viên (Người mất / Người nhặt), Quản lý trạm |
| **Tiền điều kiện** | Cả hai tài khoản đã đăng nhập qua SSO trường. |
| **Hậu điều kiện** | Đoạn hội thoại được lưu vết lịch sử trong hệ thống để phục vụ đối soát khi cần. |
| **Luồng chính** | 1. Sinh viên bấm nút "Nhắn tin ẩn danh" tại bài đăng đồ nhặt được.<br>2. Hệ thống mở cửa sổ hội thoại nội bộ, ẩn thông tin số điện thoại của cả 2 bên.<br>3. Hai bên gửi tin nhắn trao đổi đặc điểm nhận diện món đồ.<br>4. Tin nhắn được chuyển phát theo thời gian thực. |
| **Luồng ngoại lệ** | Một trong hai bên có hành vi quấy rối hoặc gửi nội dung phản cảm: Cho phép bấm nút "Báo cáo vi phạm" để khóa hội thoại và chuyển quản trị viên xử lý (UC-14). |
| **Quy tắc nghiệp vụ** | Phân tích CRUDL (tin nhắn không bị xóa vật lý để làm bằng chứng tranh chấp). |
| **Nguồn gốc** | Khảo sát KS-01 Q18 (91,6% sinh viên muốn ẩn SĐT); XĐ-02 |
| **Độ ưu tiên** | Desirable |
| **Tiêu chí chấp nhận** | Given người mất nhắn tin cho người nhặt qua hệ thống, When tin nhắn gửi đi thành công, Then giao diện hội thoại chỉ hiển thị tên ẩn danh và số điện thoại hoàn toàn được giấu kín. |
| **Trạng thái** | Approved |
| **Phiên bản** | v1.0 (29/11/2026) |

##### Nhóm 5: APPT – Lịch hẹn nhận đồ tại trạm

| Mục | Nội dung |
|:---|:---|
| **Mã yêu cầu (ID)** | **FR-APPT-001** |
| **Tên yêu cầu** | Đặt lịch hẹn nhận đồ trực tuyến theo ca trực |
| **Mô tả chi tiết** | Hệ thống PHẢI cho phép sinh viên chọn ngày và khung giờ hẹn đến trạm theo đúng giờ mở cửa trực bàn (07:30–11:00 và 13:30–17:00, thứ Hai đến thứ Sáu); sau khi lưu, hệ thống PHẢI cấp mã QR lịch hẹn duy nhất (BR-05). |
| **Use case liên quan** | UC-09 |
| **Tác nhân** | Sinh viên |
| **Tiền điều kiện** | Yêu cầu nhận đồ đã được xác minh sở hữu hợp lệ. |
| **Hậu điều kiện** | Phiếu hẹn được tạo trạng thái "Chờ xác nhận"; mã QR lịch hẹn được gửi về tài khoản. |
| **Luồng chính** | 1. Sinh viên chọn ngày và khung giờ trực còn trống.<br>2. Hệ thống kiểm tra khung giờ hợp lệ.<br>3. Hệ thống lưu phiếu hẹn và cấp mã QR lịch hẹn. |
| **Luồng ngoại lệ** | Chọn ngoài khung giờ trực trạm: Hệ thống từ chối và báo lỗi ngoài giờ phục vụ. |
| **Quy tắc nghiệp vụ** | BR-05 |
| **Nguồn gốc** | XĐ-03; BB-KH-02 KH02-5; KS-01 Q16 (93,5% SV ủng hộ) |
| **Độ ưu tiên** | Essential |
| **Tiêu chí chấp nhận** | Given sinh viên xác minh đúng món đồ, When chọn khung giờ "08:00 - 08:30 sáng Thứ Tư", Then phiếu hẹn được tạo và hiển thị mã QR lịch hẹn. |
| **Trạng thái** | Approved |
| **Phiên bản** | v1.0 (29/11/2026) |

| Mục | Nội dung |
|:---|:---|
| **Mã yêu cầu (ID)** | **FR-APPT-002** |
| **Tên yêu cầu** | Điều chỉnh và hủy lịch hẹn nhận đồ |
| **Mô tả chi tiết** | Hệ thống NÊN cho phép sinh viên tự đổi khung giờ hoặc hủy lịch hẹn trước giờ hẹn tối thiểu 2 giờ để giải phóng chỗ cho người khác (phát hiện từ phân tích CRUDL). |
| **Use case liên quan** | UC-09 |
| **Tác nhân** | Sinh viên |
| **Tiền điều kiện** | Lịch hẹn đang ở trạng thái Chờ xác nhận hoặc Đã xác nhận; còn trước giờ hẹn $\ge 2$ giờ. |
| **Hậu điều kiện** | Lịch hẹn được cập nhật khung giờ mới hoặc chuyển trạng thái sang "Đã hủy". |
| **Luồng chính** | 1. Sinh viên chọn Đổi lịch hoặc Hủy hẹn tại danh sách lịch hẹn cá nhân.<br>2. Chọn Hủy hẹn: Hệ thống xác nhận và cập nhật trạng thái phiếu hẹn sang "Đã hủy".<br>3. Chọn Đổi giờ: Sinh viên chọn khung giờ mới; hệ thống cập nhật lịch và phát hành mã QR mới. |
| **Luồng ngoại lệ** | Thao tác cận giờ hẹn ($< 2$ giờ): Hệ thống thông báo không thể đổi lịch trực tuyến và yêu cầu liên hệ trực tiếp bàn trực trạm. |
| **Quy tắc nghiệp vụ** | Phân tích CRUDL (giải phóng vị trí hẹn). |
| **Nguồn gốc** | Phân tích CRUDL; Phản hồi PT-01 #3 |
| **Độ ưu tiên** | Desirable |
| **Tiêu chí chấp nhận** | Given sinh viên có lịch hẹn lúc 14:00 ngày mai, When chọn Hủy lịch hẹn lúc 09:00 hôm nay, Then trạng thái lịch hẹn chuyển sang Đã hủy và ô lịch được giải phóng. |
| **Trạng thái** | Approved |
| **Phiên bản** | v1.0 (29/11/2026) |

##### Nhóm 6: STATION & RETURN – Tiếp nhận kho và giao trả đồ

| Mục | Nội dung |
|:---|:---|
| **Mã yêu cầu (ID)** | **FR-STATION-001** |
| **Tên yêu cầu** | Tiếp nhận hiện vật vào kho trạm và in/cấp mã QR |
| **Mô tả chi tiết** | Hệ thống PHẢI cho phép quản lý trạm nhập thông tin tiếp nhận hiện vật thực tế, gán vị trí ngăn tủ kho và cấp mã QR định danh duy nhất in dán lên nhãn đồ vật. |
| **Use case liên quan** | UC-10 |
| **Tác nhân** | Quản lý trạm |
| **Tiền điều kiện** | Quản lý trạm đã đăng nhập trên máy bàn trực. |
| **Hậu điều kiện** | Bản ghi vật phẩm được tạo trạng thái "Đang lưu kho"; mã QR được sinh ra. |
| **Luồng chính** | 1. Quản lý trạm nhập đặc điểm món đồ tiếp nhận và chọn ngăn tủ lưu giữ.<br>2. Hệ thống tạo bản ghi VatPhamLuuKho.<br>3. Hệ thống sinh mã QR định danh vật phẩm để in nhãn dán. |
| **Luồng ngoại lệ** | Ngăn tủ đã đầy: Hệ thống cảnh báo sức chứa và gợi ý chọn ngăn tủ khác. |
| **Quy tắc nghiệp vụ** | Phân tích CRUDL (không xóa vật lý bản ghi lưu kho). |
| **Nguồn gốc** | XĐ-03; Biên bản PV03-1 |
| **Độ ưu tiên** | Essential |
| **Tiêu chí chấp nhận** | Given trạm tiếp nhận một chiếc tai nghe, When quản lý trạm lưu kho vào ngăn T1-02, Then hệ thống cấp mã QR nhãn và cập nhật trạng thái Đang lưu kho. |
| **Trạng thái** | Approved |
| **Phiên bản** | v1.0 (29/11/2026) |

| Mục | Nội dung |
|:---|:---|
| **Mã yêu cầu (ID)** | **FR-STATION-002** |
| **Tên yêu cầu** | Quản lý vị trí ngăn tủ và trạng thái vật phẩm lưu kho |
| **Mô tả chi tiết** | Hệ thống PHẢI cho phép quản lý trạm tra cứu danh mục đồ vật đang lưu giữ theo từng ngăn tủ kho (ví dụ: T1-01, T1-02), theo dõi số lượng tồn và cập nhật chuyển đổi trạng thái vòng đời vật phẩm (Đang lưu kho $ightarrow$ Chờ nhận $ightarrow$ Đã trao trả / Quá hạn). |
| **Use case liên quan** | UC-10, UC-12 |
| **Tác nhân** | Quản lý trạm |
| **Tiền điều kiện** | Quản lý trạm đã đăng nhập trên máy bàn trực quầy. |
| **Hậu điều kiện** | Vị trí ngăn tủ và trạng thái vật phẩm được cập nhật chính xác trong CSDL. |
| **Luồng chính** | 1. Quản lý trạm vào phân hệ Quản lý kho trạm.<br>2. Chọn xem sơ đồ ngăn tủ lưu trữ.<br>3. Hệ thống hiển thị danh sách các món đồ hiện có trong từng ngăn tủ kèm mã QR và ngày nhập kho.<br>4. Quản lý trạm có thể cập nhật điều chuyển món đồ sang ngăn tủ khác khi cần sắp xếp lại kho. |
| **Luồng ngoại lệ** | Quét mã QR hiện vật không khớp với ngăn tủ khai báo: Hệ thống hiển thị cảnh báo sai lệch vị trí để kiểm tra thực tế. |
| **Quy tắc nghiệp vụ** | Phân tích CRUDL (không xóa vật lý bản ghi lưu kho). |
| **Nguồn gốc** | Biên bản PV03-3; BB-KH-01; ST-01 |
| **Độ ưu tiên** | Essential |
| **Tiêu chí chấp nhận** | Given quản lý trạm mở danh mục ngăn tủ T1, When chọn xem chi tiết, Then hệ thống hiển thị chính xác danh sách các món đồ và trạng thái lưu kho của từng món trong ngăn T1. |
| **Trạng thái** | Approved |
| **Phiên bản** | v1.0 (29/11/2026) |

| Mục | Nội dung |
|:---|:---|
| **Mã yêu cầu (ID)** | **FR-RETURN-001** |
| **Tên yêu cầu** | Quét mã QR tra cứu hồ sơ và xác nhận trao trả đồ |
| **Mô tả chi tiết** | Hệ thống PHẢI cho phép quản lý trạm quét mã QR lịch hẹn để tải hồ sơ đối soát trong $\le 3$ giây (NFR-PERF-002); sau khi đối chiếu Thẻ sinh viên/CCCD gốc khớp, quản lý trạm bấm xác nhận và hệ thống PHẢI cập nhật trạng thái vật phẩm thành "Đã trao trả" (BR-06). |
| **Use case liên quan** | UC-11 |
| **Tác nhân** | Quản lý trạm |
| **Tiền điều kiện** | Quản lý trạm đã đăng nhập; vật phẩm ở trạng thái Đang lưu kho. |
| **Hậu điều kiện** | Vật phẩm chuyển sang trạng thái "Đã trao trả"; xuất khỏi danh sách tồn kho trạm. |
| **Luồng chính** | 1. Quản lý trạm quét mã QR lịch hẹn của sinh viên.<br>2. Hệ thống hiển thị hồ sơ đối soát kèm ảnh và thông tin người hẹn.<br>3. Quản lý trạm đối chiếu Thẻ sinh viên/CCCD gốc.<br>4. Thông tin khớp: Bấm Xác nhận trao trả.<br>5. Hệ thống chuyển trạng thái vật phẩm sang "Đã trao trả" và gửi thông báo hoàn tất. |
| **Luồng ngoại lệ** | Quét mã QR của đồ đang tranh chấp (UC-08): Hệ thống cảnh báo đỏ và khóa nút xác nhận trao trả (BR-07). |
| **Quy tắc nghiệp vụ** | BR-06, BR-07; Mục tiêu MT-04 |
| **Nguồn gốc** | XĐ-03; Biên bản PV02-3; AD-02, SD-02 |
| **Độ ưu tiên** | Essential |
| **Tiêu chí chấp nhận** | Given sinh viên xuất trình mã QR hợp lệ và Thẻ sinh viên trùng khớp, When quản lý trạm bấm Xác nhận trao trả, Then trạng thái vật phẩm cập nhật thành Đã trao trả trong vòng dưới 3 giây. |
| **Trạng thái** | Approved |
| **Phiên bản** | v1.0 (29/11/2026) |

| Mục | Nội dung |
|:---|:---|
| **Mã yêu cầu (ID)** | **FR-RETURN-002** |
| **Tên yêu cầu** | Chụp ảnh lưu bằng chứng giao nhận điện tử |
| **Mô tả chi tiết** | Khi hoàn tất thủ tục trao trả đồ tại quầy, hệ thống PHẢI hỗ trợ quản lý trạm dùng camera thiết bị chụp ảnh biên nhận bàn giao thực tế (hoặc ảnh người nhận cầm hiện vật) và lưu trữ kèm hồ sơ giao nhận điện tử để chống khiếu nại về sau. |
| **Use case liên quan** | UC-11 |
| **Tác nhân** | Quản lý trạm |
| **Tiền điều kiện** | Sinh viên đã kiểm tra hiện vật và đồng ý nhận lại đồ tại quầy. |
| **Hậu điều kiện** | Tệp ảnh chụp biên nhận được tải lên máy chủ và liên kết vĩnh viễn với hồ sơ bàn giao. |
| **Luồng chính** | 1. Sau khi đối chiếu giấy tờ khớp, quản lý trạm kích hoạt chức năng Chụp ảnh xác nhận.<br>2. Quản lý trạm chụp ảnh khoảnh khắc trao trả hoặc ảnh sinh viên cầm hiện vật kèm phiếu ký nhận.<br>3. Hệ thống tải ảnh lên CSDL lưu trữ kiểm toán.<br>4. Quản lý trạm bấm Hoàn tất trao trả. |
| **Luồng ngoại lệ** | Lỗi camera hoặc không chụp được ảnh: Hệ thống cho phép nhập mã xác thực OTP gửi qua email sinh viên để thay thế bằng chứng ảnh chụp. |
| **Quy tắc nghiệp vụ** | NFR-SEC-004 |
| **Nguồn gốc** | Biên bản PV02-3; BB-KH-02; AD-02 |
| **Độ ưu tiên** | Essential |
| **Tiêu chí chấp nhận** | Given quản lý trạm thực hiện thủ tục trao trả đồ tại quầy, When chụp ảnh xác nhận bàn giao, Then ảnh được đính kèm vào hồ sơ giao nhận và không thể bị sửa đổi hoặc xóa bỏ. |
| **Trạng thái** | Approved |
| **Phiên bản** | v1.0 (29/11/2026) |

##### Nhóm 7: SHIFT & OVERDUE – Ca trực và bàn giao đồ quá hạn

| Mục | Nội dung |
|:---|:---|
| **Mã yêu cầu (ID)** | **FR-SHIFT-001** |
| **Tên yêu cầu** | Điểm danh nhận ca và bàn giao ca trực trạm |
| **Mô tả chi tiết** | Hệ thống PHẢI cho phép tình nguyện viên quản lý trạm đăng nhập điểm danh khi bắt đầu ca trực và lập biên bản bàn giao điện tử khi kết thúc ca (tổng kết số đồ tiếp nhận mới, số đồ đã trao trả, số đồ tồn kho bàn giao cho ca tiếp theo) (MT-04). |
| **Use case liên quan** | UC-12 |
| **Tác nhân** | Quản lý trạm |
| **Tiền điều kiện** | Quản lý trạm có phân công lịch trực trong ngày. |
| **Hậu điều kiện** | Biên bản bàn giao ca trực được tạo và ghi nhận mốc thời gian chuyển giao. |
| **Luồng chính** | 1. Tình nguyện viên hết ca trực chọn Lập biên bản bàn giao ca.<br>2. Hệ thống tự động thống kê số lượt tiếp nhận, số lượt trao trả và số hiện vật đang lưu trong kho trong phiên trực.<br>3. Tình nguyện viên ca sau đăng nhập xác nhận tiếp nhận bàn giao kho và thiết bị.<br>4. Hệ thống lưu biên bản ca trực vào nhật ký kiểm toán. |
| **Luồng ngoại lệ** | Số lượng hiện vật thực tế sai lệch so với hệ thống: Cho phép ghi chú giải trình lý do sai lệch vào biên bản bàn giao ca để Cán bộ CTSV kiểm tra. |
| **Quy tắc nghiệp vụ** | NFR-SEC-004 |
| **Nguồn gốc** | Biên bản PV03-5; BB-KH-02; MT-04 |
| **Độ ưu tiên** | Essential |
| **Tiêu chí chấp nhận** | Given quản lý trạm ca sáng kết thúc phiên trực lúc 11:00, When bấm Tạo biên bản bàn giao ca, Then hệ thống tự động tổng hợp số liệu giao dịch trong ca và yêu cầu người nhận ca chiều ký xác nhận. |
| **Trạng thái** | Approved |
| **Phiên bản** | v1.0 (29/11/2026) |

| Mục | Nội dung |
|:---|:---|
| **Mã yêu cầu (ID)** | **FR-SHIFT-002** |
| **Tên yêu cầu** | Kiểm kê kho hiện vật đối soát thực tế theo ca |
| **Mô tả chi tiết** | Hệ thống NÊN hỗ trợ chế độ kiểm kê kho nhanh bằng cách quét mã QR liên tục các món đồ thực tế trong tủ kho; hệ thống tự động đối chiếu với danh sách tồn kho trên CSDL và hiển thị danh sách các món bị thất lạc hoặc sai vị trí. |
| **Use case liên quan** | UC-12 |
| **Tác nhân** | Quản lý trạm, Cán bộ CTSV |
| **Tiền điều kiện** | Quản lý trạm mở chế độ Kiểm kê kho. |
| **Hậu điều kiện** | Phiếu kiểm kê kho được lập, ghi nhận tình trạng khớp/lệch kho. |
| **Luồng chính** | 1. Quản lý trạm kích hoạt chức năng Kiểm kê kho.<br>2. Quản lý trạm cầm máy quét/smartphone quét lần lượt mã QR các món đồ trong tủ.<br>3. Hệ thống tự động đánh dấu "Đã kiểm kê" cho các món quét được.<br>4. Sau khi kết thúc, hệ thống hiển thị danh sách các món đồ chưa được quét (nguy cơ thất thoát) hoặc các món đồ nằm sai ngăn tủ. |
| **Luồng ngoại lệ** | Phát hiện đồ vật không có mã QR trong kho: Cho phép in cấp lại tem mã QR bổ sung ngay tại quầy. |
| **Quy tắc nghiệp vụ** | Mục tiêu MT-03 (không để xảy ra thất thoát tài sản). |
| **Nguồn gốc** | Biên bản PV03-5; PV02-3 |
| **Độ ưu tiên** | Desirable |
| **Tiêu chí chấp nhận** | Given trong kho có 20 món đồ, When quản lý trạm quét được 19 món, Then hệ thống hiển thị cảnh báo đỏ món thứ 20 chưa được kiểm kê kèm vị trí ngăn tủ cần tìm. |
| **Trạng thái** | Approved |
| **Phiên bản** | v1.0 (29/11/2026) |

| Mục | Nội dung |
|:---|:---|
| **Mã yêu cầu (ID)** | **FR-OVERDUE-001** |
| **Tên yêu cầu** | Tự động quét và cảnh báo vật phẩm quá hạn lưu trữ |
| **Mô tả chi tiết** | Hệ thống PHẢI chạy tác vụ quét định kỳ hằng ngày lúc 00:00 để tự động lọc các hiện vật vượt quá thời hạn lưu kho (30 ngày đối với đồ thường, 90 ngày đối với đồ giá trị), chuyển trạng thái sang "Quá hạn" và cảnh báo nhân sự trạm (BR-02). |
| **Use case liên quan** | UC-13 |
| **Tác nhân** | Hệ thống |
| **Tiền điều kiện** | Có đồ vật lưu kho vượt quá số ngày quy định. |
| **Hậu điều kiện** | Vật phẩm chuyển sang trạng thái "Quá hạn"; thêm vào danh sách chờ bàn giao CTSV. |
| **Luồng chính** | 1. Hệ thống quét ngày nhập kho của các vật phẩm Đang lưu kho.<br>2. Tính số ngày lưu = Ngày hiện tại - Ngày nhập kho.<br>3. Nếu số ngày lưu vượt hạn quy định: Chuyển trạng thái sang "Quá hạn" và đưa vào danh sách chờ bàn giao. |
| **Luồng ngoại lệ** | Đồ vật đang có lịch hẹn nhận trong ngày: Tạm hoãn chuyển quá hạn thêm 24 giờ. |
| **Quy tắc nghiệp vụ** | BR-02; Mục tiêu MT-05 |
| **Nguồn gốc** | XĐ-01; BB-KH-01 KH01-1; ST-01 |
| **Độ ưu tiên** | Essential |
| **Tiêu chí chấp nhận** | Given một cuốn giáo trình đã lưu kho 31 ngày, When hệ thống quét tác vụ nửa đêm, Then trạng thái cuốn sách chuyển sang Quá hạn. |
| **Trạng thái** | Approved |
| **Phiên bản** | v1.0 (29/11/2026) |

| Mục | Nội dung |
|:---|:---|
| **Mã yêu cầu (ID)** | **FR-OVERDUE-002** |
| **Tên yêu cầu** | Lập biên bản bàn giao điện tử chuyển Phòng CTSV |
| **Mô tả chi tiết** | Hệ thống PHẢI cho phép quản lý trạm kết xuất danh sách đồ quá hạn, tạo biên bản bàn giao điện tử kèm mã chứng từ; sau khi Cán bộ CTSV ký xác nhận tiếp nhận trên hệ thống, trạng thái các vật phẩm PHẢI cập nhật sang "Đã bàn giao" (BR-08). |
| **Use case liên quan** | UC-13 |
| **Tác nhân** | Quản lý trạm, Cán bộ CTSV |
| **Tiền điều kiện** | Có ít nhất 1 vật phẩm ở trạng thái Quá hạn. |
| **Hậu điều kiện** | Biên bản bàn giao CTSV được lưu vĩnh viễn; vật phẩm chuyển sang "Đã bàn giao". |
| **Luồng chính** | 1. Quản lý trạm chọn các món đồ quá hạn và nhấn Lập biên bản bàn giao.<br>2. Hệ thống sinh mã biên bản và xuất danh sách kiểm kê.<br>3. Cán bộ CTSV kiểm tra hiện vật thực tế và bấm Xác nhận tiếp nhận trên tài khoản CTSV.<br>4. Hệ thống cập nhật trạng thái biên bản thành "Đã tiếp nhận" và toàn bộ vật phẩm trong biên bản thành "Đã bàn giao". |
| **Luồng ngoại lệ** | Cán bộ CTSV từ chối một số món do sai lệch hiện vật: Hệ thống cho phép tách các món sai lệch để trạm kiểm tra lại. |
| **Quy tắc nghiệp vụ** | BR-08; Phân tích CRUDL (biên bản không bị xóa) |
| **Nguồn gốc** | XĐ-01; Biên bản PV02-2; BB-KH-01 |
| **Độ ưu tiên** | Essential |
| **Tiêu chí chấp nhận** | Given danh sách 10 món đồ quá hạn, When Cán bộ CTSV bấm xác nhận tiếp nhận biên bản bàn giao, Then trạng thái 10 món đồ đồng loạt chuyển thành Đã bàn giao. |
| **Trạng thái** | Approved |
| **Phiên bản** | v1.0 (29/11/2026) |

##### Nhóm 8: MOD & CAT – Kiểm duyệt và cấu hình quy định

| Mục | Nội dung |
|:---|:---|
| **Mã yêu cầu (ID)** | **FR-MOD-001** |
| **Tên yêu cầu** | Tiếp nhận báo cáo vi phạm và phong tỏa đồ tranh chấp |
| **Mô tả chi tiết** | Hệ thống PHẢI cho phép người dùng gửi báo cáo tin đăng vi phạm (sai sự thật, lừa đảo, phản cảm); khi một món đồ có từ 2 yêu cầu nhận trở lên hoặc nhận được báo cáo tranh chấp, hệ thống PHẢI tự động khóa quyền đặt lịch hẹn và chuyển Phòng CTSV xử lý (BR-07). |
| **Use case liên quan** | UC-08, UC-14 |
| **Tác nhân** | Sinh viên, Quản lý trạm, Cán bộ CTSV |
| **Tiền điều kiện** | Người dùng đã đăng nhập vào hệ thống. |
| **Hậu điều kiện** | Tin đăng hoặc món đồ bị chuyển trạng thái sang "Tranh chấp" hoặc "Bị ẩn". |
| **Luồng chính** | 1. Người dùng chọn Báo cáo vi phạm tại bài đăng hoặc món đồ.<br>2. Nhập lý do vi phạm và đính kèm bằng chứng (nếu có).<br>3. Hệ thống ghi nhận báo cáo vào danh sách kiểm duyệt.<br>4. Nếu là tranh chấp nhận đồ: Hệ thống tự động chuyển trạng thái vật phẩm sang "Tranh chấp" và phong tỏa toàn bộ lịch hẹn liên quan. |
| **Luồng ngoại lệ** | Cán bộ CTSV phân xử xong tranh chấp: Cán bộ CTSV chọn người nhận hợp lệ trên hệ thống, giải tỏa phong tỏa để trạm tiến hành trao trả. |
| **Quy tắc nghiệp vụ** | BR-07 |
| **Nguồn gốc** | Biên bản PV03-8; BB-KH-01; KH02-1 |
| **Độ ưu tiên** | Essential |
| **Tiêu chí chấp nhận** | Given một chiếc laptop có 2 sinh viên cùng yêu cầu nhận, When hệ thống ghi nhận yêu cầu thứ 2, Then trạng thái món đồ tự động chuyển thành Tranh chấp và nút đặt lịch hẹn bị phong tỏa. |
| **Trạng thái** | Approved |
| **Phiên bản** | v1.0 (29/11/2026) |

| Mục | Nội dung |
|:---|:---|
| **Mã yêu cầu (ID)** | **FR-CAT-001** |
| **Tên yêu cầu** | Cấu hình tham số quy định trạm và danh mục loại đồ |
| **Mô tả chi tiết** | Hệ thống PHẢI cho phép Cán bộ CTSV cập nhật các tham số quy định động của trạm (thời hạn lưu giữ đồ thường 30 ngày, đồ giá trị 90 ngày, khung giờ trạm mở cửa, danh mục loại đồ, danh mục khu vực tòa nhà) qua giao diện web mà không cần sửa mã nguồn (NFR-MAIN-001). |
| **Use case liên quan** | UC-15 |
| **Tác nhân** | Cán bộ CTSV |
| **Tiền điều kiện** | Cán bộ CTSV đã đăng nhập với quyền quản trị chính sách. |
| **Hậu điều kiện** | Các tham số quy định mới được lưu vào thực thể ThamSoQuyDinh và có hiệu lực tức thời. |
| **Luồng chính** | 1. Cán bộ CTSV vào phân hệ Cấu hình quy định.<br>2. Thay đổi giá trị tham số (ví dụ: đổi thời hạn lưu đồ thường hoặc cập nhật giờ mở cửa trạm đợt thi cử).<br>3. Nhấn Lưu cấu hình.<br>4. Hệ thống cập nhật CSDL và áp dụng ngay cho các tác vụ kiểm tra nghiệp vụ trong vòng 1 phút. |
| **Luồng ngoại lệ** | Nhập giá trị tham số không hợp lệ (ví dụ thời hạn $\le 0$): Hệ thống báo lỗi và không cho lưu. |
| **Quy tắc nghiệp vụ** | NFR-MAIN-001; Phân tích CRUDL (thực thể ThamSoQuyDinh đầy đủ 5 thao tác CRUDL). |
| **Nguồn gốc** | Biên bản PV02-1; BB-KH-01; XĐ-01 |
| **Độ ưu tiên** | Essential |
| **Tiêu chí chấp nhận** | Given Cán bộ CTSV thay đổi thời hạn lưu đồ thường từ 30 ngày sang 45 ngày trên giao diện cấu hình, When bấm Lưu, Then hệ thống áp dụng mốc 45 ngày cho tác vụ quét quá hạn ngay lập tức. |
| **Trạng thái** | Approved |
| **Phiên bản** | v1.0 (29/11/2026) |

##### Nhóm 9: RPT & NOTI – Thống kê, báo cáo và thông báo

| Mục | Nội dung |
|:---|:---|
| **Mã yêu cầu (ID)** | **FR-RPT-001** |
| **Tên yêu cầu** | Thống kê số liệu và xuất báo cáo định kỳ |
| **Mô tả chi tiết** | Hệ thống PHẢI cung cấp báo cáo thống kê trực quan (biểu đồ và bảng số liệu) về: Tỷ lệ đồ trao trả thành công (MT-01), số lượng đồ tồn kho theo danh mục, khu vực có tần suất rơi đồ cao nhất, danh sách đồ quá hạn bàn giao; hỗ trợ xuất báo cáo sang tệp Excel và PDF (MT-05). |
| **Use case liên quan** | UC-17 |
| **Tác nhân** | Cán bộ CTSV, Quản lý trạm |
| **Tiền điều kiện** | Người dùng có vai trò Quản lý trạm hoặc Cán bộ CTSV. |
| **Hậu điều kiện** | Báo cáo thống kê được hiển thị hoặc tệp báo cáo được tải về máy. |
| **Luồng chính** | 1. Người dùng chọn khoảng thời gian cần thống kê (tháng, học kỳ, năm học).<br>2. Hệ thống tổng hợp số liệu và hiển thị các biểu đồ trực quan.<br>3. Người dùng chọn nút Xuất báo cáo (Excel hoặc PDF).<br>4. Hệ thống kết xuất và tải tệp báo cáo hoàn chỉnh về máy tính. |
| **Luồng ngoại lệ** | Khoảng thời gian không có dữ liệu: Hệ thống thông báo không có số liệu phát sinh trong mốc thời gian đã chọn. |
| **Quy tắc nghiệp vụ** | Mục tiêu MT-01, MT-05 |
| **Nguồn gốc** | Biên bản PV02-1; PV03-9; BB-KH-01 |
| **Độ ưu tiên** | Essential |
| **Tiêu chí chấp nhận** | Given Cán bộ CTSV chọn xuất báo cáo Học kỳ 1, When bấm Xuất Excel, Then hệ thống tải về tệp bảng tính có đầy đủ tỷ lệ trao trả thành công và danh sách phân loại đồ tồn kho. |
| **Trạng thái** | Approved |
| **Phiên bản** | v1.0 (29/11/2026) |

| Mục | Nội dung |
|:---|:---|
| **Mã yêu cầu (ID)** | **FR-NOTI-001** |
| **Tên yêu cầu** | Gửi thông báo tự động đa kênh (Web, Email) |
| **Mô tả chi tiết** | Hệ thống NÊN tự động phát thông báo trên ứng dụng web và gửi thư điện tử qua máy chủ SMTP của trường khi phát sinh các sự kiện: có tin nhặt tương đồng (so khớp AI), có người đặt lịch hẹn mới, nhắc lịch hẹn trước 2 giờ, hoặc cảnh báo tài khoản bị tạm khóa 48h. |
| **Use case liên quan** | UC-18 |
| **Tác nhân** | Hệ thống, Sinh viên, Quản lý trạm |
| **Tiền điều kiện** | Phát sinh sự kiện nghiệp vụ trong hệ thống. |
| **Hậu điều kiện** | Bản ghi thông báo được lưu vào thực thể ThongBao; email được chuyển tới hàng đợi gửi. |
| **Luồng chính** | 1. Hệ thống phát hiện sự kiện (ví dụ: sinh viên đặt lịch hẹn thành công).<br>2. Hệ thống tạo thông báo in-app gửi tới tài khoản sinh viên và quản lý trạm trực ca.<br>3. Hệ thống tạo nội dung thư điện tử và gửi qua máy chủ SMTP trường.<br>4. Người dùng nhận được chuông thông báo trên web và email trong hòm thư trường. |
| **Luồng ngoại lệ** | Máy chủ email trường gặp sự cố tạm thời: Hệ thống lưu trạng thái thư vào hàng đợi thử lại (tối đa 3 lần) và bảo đảm thông báo in-app vẫn hiển thị bình thường. |
| **Quy tắc nghiệp vụ** | Phân tích CRUDL (thông báo không bị xóa vật lý để giữ vết kiểm toán). |
| **Nguồn gốc** | Khảo sát KS-01 Q15; BB-KH-02 |
| **Độ ưu tiên** | Desirable |
| **Tiêu chí chấp nhận** | Given sinh viên A được gợi ý một món đồ thất lạc, When hệ thống kích hoạt sự kiện đối soát, Then sinh viên A nhận được thông báo trên thanh thông báo web và email trong vòng 5 giây. |
| **Trạng thái** | Approved |
| **Phiên bản** | v1.0 (29/11/2026) |

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
