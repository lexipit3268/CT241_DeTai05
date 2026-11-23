# 2. Mô tả tổng quan

## 2.1. Bối cảnh sản phẩm
LostLink là hệ thống web độc lập, hỗ trợ kết nối tìm kiếm và quản lý lưu kho đồ thất lạc tại Khu II ĐH Cần Thơ, giao tiếp với cổng SSO trường và dịch vụ email thông báo của trường.

```text
[CHÈN HÌNH ẢNH TẠI ĐÂY KHI LÊN WORD]
File ảnh nguồn: 03_MoHinh/AnhXuat/LuocDoNguCanh_v1.0.png
Tên hình: Hình 2.1. Lược đồ ngữ cảnh
```

## 2.2. Chức năng sản phẩm

| Mã | Use case | Tác nhân |
|:---:|:---|:---|
| **UC-01** | Đăng nhập và xác thực tài khoản | Sinh viên, Quản lý trạm, Cán bộ CTSV |
| **UC-02** | Đăng tin tìm đồ thất lạc | Sinh viên |
| **UC-03** | Đăng tin nhặt được đồ | Sinh viên, Quản lý trạm |
| **UC-04** | Tra cứu và lọc danh sách đồ thất lạc | Sinh viên, Quản lý trạm, Cán bộ CTSV |
| **UC-05** | Tự động so khớp và gợi ý tin tương đồng | Hệ thống, Sinh viên |
| **UC-06** | Nhắn tin ẩn danh trao đổi thông tin nhận đồ | Sinh viên, Quản lý trạm |
| **UC-07** | Xác minh quyền sở hữu đồ thất lạc | Sinh viên, Quản lý trạm |
| **UC-08** | Tiếp nhận và xử lý tranh chấp nhận đồ | Cán bộ CTSV, Quản lý trạm, Sinh viên |
| **UC-09** | Đặt và quản lý lịch hẹn nhận đồ tại trạm | Sinh viên, Quản lý trạm |
| **UC-10** | Tiếp nhận vật phẩm vào kho trạm và cấp mã QR | Quản lý trạm, Sinh viên |
| **UC-11** | Quét mã QR và giao trả đồ trực tiếp tại trạm | Quản lý trạm, Sinh viên |
| **UC-12** | Bàn giao ca trực và kiểm kê kho hiện vật | Quản lý trạm, Cán bộ CTSV |
| **UC-13** | Xử lý đồ quá hạn và lập biên bản bàn giao CTSV | Quản lý trạm, Cán bộ CTSV |
| **UC-14** | Kiểm duyệt tin đăng và xử lý vi phạm nội dung | Quản lý trạm, Cán bộ CTSV |
| **UC-15** | Quản lý danh mục loại đồ, khu vực và quy định trạm | Cán bộ CTSV |
| **UC-16** | Quản lý tài khoản và phân quyền nhân sự trạm | Cán bộ CTSV, Quản lý trạm |
| **UC-17** | Thống kê và kết xuất báo cáo định kỳ | Cán bộ CTSV, Quản lý trạm |
| **UC-18** | Gửi thông báo tự động đa kênh | Hệ thống, Sinh viên, Quản lý trạm |

```text
[CHÈN HÌNH ẢNH TẠI ĐÂY KHI LÊN WORD]
File ảnh nguồn: 03_MoHinh/AnhXuat/UC_TongQuat_v1.0.png
Tên hình: Hình 2.2. Biểu đồ use case tổng quát
```

## 2.3. Đặc điểm người dùng

| Lớp người dùng | Đặc điểm | Kỹ năng |
|:---|:---|:---|
| **Sinh viên** | ≈ 30.000; dùng điện thoại; đăng tin, tra cứu và hẹn nhận đồ | Quen dùng web trên điện thoại |
| **Sinh viên quản lý trạm** | 10–15; làm việc tại bàn trực theo ca; tiếp nhận và giao trả đồ | Quen điện thoại quét QR, web máy tính |
| **Cán bộ Phòng CTSV** | 2–3; xem báo cáo, xử lý tranh chấp, tiếp nhận đồ quá hạn | Kỹ năng văn phòng cơ bản |
| **Quản trị hệ thống** | 1–2; kiểm duyệt, cấu hình danh mục và phân quyền | Chuyên môn CNTT |

## 2.4. Các ràng buộc

| Mã | Ràng buộc |
|:---:|:---|
| **C-01** | Đăng nhập bằng tài khoản dùng chung của trường (SSO); hệ thống không tự quản lý mật khẩu. |
| **C-02** | Dữ liệu sinh viên lấy từ hệ thống quản lý đào tạo hiện có của trường; không nhập tay. |
| **C-03** | Triển khai trên hạ tầng máy chủ của trường; giao diện web responsive, dùng được trên điện thoại từ 360 px. |
| **C-04** | Tuân thủ quy định hiện hành về bảo vệ dữ liệu cá nhân (tự động làm mờ ảnh đồ giá trị, ẩn thông tin liên hệ). |
| **C-05** | Phạm vi địa lý áp dụng tại Khu II; đồ quá hạn bàn giao về Phòng CTSV xử lý ngoài hệ thống. |
| **C-06** | Hoàn thành trong khuôn khổ học phần CT241 (HK1 năm học 2026–2027) trước tuần 15; ngân sách 0 đồng. |

## 2.5. Giả định và phụ thuộc
- A-01 SSO trường sẵn sàng; A-02 hệ thống đào tạo cung cấp thông tin sinh viên; A-03 trạm có vị trí cố định, tủ kho và giờ mở cửa cố định; A-04 quy định thời hạn lưu giữ do Phòng CTSV ban hành; A-05 sinh viên quản lý trạm do Phòng CTSV phân công.
- D-01 Dịch vụ email của trường; D-02 thiết bị camera điện thoại quét mã QR tại trạm.
