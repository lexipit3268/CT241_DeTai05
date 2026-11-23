Ran kiểm tra file trong 01_TamNhin
Ran đọc nội dung đầu file TamNhinPhamVi_v1.1.docx · Exited with code 1
Ran đọc lịch sử thay đổi TamNhinPhamVi_v1.1 · Exited with code 1
Ran đọc đoạn đầu TamNhinPhamVi_v1.1 bằng python · Exited with code 1
Ran đọc XML docx TamNhinPhamVi_v1.1 bằng python
Ran xem cấu trúc DanhSachYeuCau_v1.0.xlsx
Ran liệt kê danh sách UC trong Excel
Ran thống kê FR và NFR trong DanhSachYeuCau
Ran kiểm tra ảnh xuất UML hiện có
Ran kiểm tra prototype screenshots
Ran liệt kê các thư mục Prototype HTML
Ran tìm danh sách BR trong PhanLoaiYeuCau · Exited with code 1
Ran đọc BR từ XML PhanLoaiYeuCau
Ran tìm BR trong Excel DanhSachYeuCau
Ran kiểm tra CRUDL sheets
Ran đọc sheet PhanTich trong CRUDL
Ran đọc sheet XungDot trong DanhSachYeuCau
Ran xem chi tiết mục 3.1 của SRS mẫu
Ran xem ghi chú CRUDL trong SRS mẫu
Ran xem các mục 3.3 đến 4.2 của SRS mẫu

Dưới đây là **Bản thiết kế mục lục chi tiết và kế hoạch nội dung chuẩn chỉ 100%** cho tài liệu **SRS v1.0 (LostLink)** của Nhóm 02:

---

# MỤC LỤC CHI TIẾT TÀI LIỆU SRS v1.0 (LOSTLINK)

```text
TRANG BÌA (Theo mẫu chuẩn Trường CNTT&TT – ĐHCT)
LỊCH SỬ PHIÊN BẢN (v0.9 bản nháp rà soát chéo; v1.0 baseline)
MỤC LỤC TỰ ĐỘNG
DANH MỤC HÌNH ẢNH & DANH MỤC BẢNG BIỂU

1. GIỚI THIỆU
   1.1. Mục đích
   1.2. Phạm vi
   1.3. Định nghĩa, từ viết tắt
   1.4. Tài liệu tham khảo
   1.5. Tổng quan tài liệu

2. MÔ TẢ TỔNG QUAN
   2.1. Bối cảnh sản phẩm
        Hình 2.1. Lược đồ ngữ cảnh
   2.2. Chức năng sản phẩm
        Hình 2.2. Biểu đồ use case tổng quát
   2.3. Đặc điểm người dùng
   2.4. Các ràng buộc
   2.5. Giả định và phụ thuộc

3. YÊU CẦU CỤ THỂ
   3.1. Yêu cầu giao diện
        Bảng Yêu cầu giao diện (IR-01 đến IR-04)
        Hình 3.1. Prototype trang tra cứu và danh sách đồ thất lạc
        Hình 3.2. Prototype màn hình chi tiết vật phẩm và câu hỏi xác minh
   3.2. Yêu cầu chức năng
        3.2.1. Quy tắc nghiệp vụ
               Bảng Quy tắc nghiệp vụ (BR-01 đến BR-08)
               Ghi chú từ phân tích CRUDL (bảo toàn lịch sử, không xóa vật lý)
        3.2.2. Đặc tả use case chính
               UC-02. Đăng tin tìm đồ thất lạc
               UC-04. Tra cứu và lọc danh sách đồ thất lạc
               UC-07. Xác minh quyền sở hữu đồ thất lạc
               UC-09. Đặt và quản lý lịch hẹn nhận đồ tại trạm
               UC-11. Quét mã QR và giao trả đồ trực tiếp tại trạm
        3.2.3. Danh sách yêu cầu chức năng
               Bảng tổng hợp 28 yêu cầu chức năng (FR)
               Nhóm AUTH – Đăng nhập và phân quyền (FR-AUTH-001, FR-AUTH-002, FR-ROLE-001)
               Nhóm POST – Đăng tin thất lạc và nhặt được (FR-POST-001, FR-POST-002, FR-POST-003)
               Nhóm SEARCH – Tra cứu và gợi ý so khớp (FR-SEARCH-001, FR-SEARCH-002, FR-MATCH-001)
               Nhóm VERIFY & CHAT – Xác minh sở hữu và trao đổi (FR-VERIFY-001..004, FR-CHAT-001)
               Nhóm APPT – Lịch hẹn nhận đồ tại trạm (FR-APPT-001, FR-APPT-002)
               Nhóm STATION – Tiếp nhận kho và giao trả đồ (FR-STATION-001, FR-STATION-002, FR-RETURN-001, FR-RETURN-002)
               Nhóm SHIFT & DISPUTE – Ca trực và tranh chấp (FR-SHIFT-001, FR-SHIFT-002, FR-MOD-001)
               Nhóm OVERDUE & CAT – Xử lý đồ quá hạn và cấu hình (FR-OVERDUE-001, FR-OVERDUE-002, FR-CAT-001)
               Nhóm RPT & NOTI – Báo cáo và thông báo (FR-RPT-001, FR-NOTI-001)
   3.3. Yêu cầu hiệu năng
        Bảng Yêu cầu hiệu năng (NFR-PERF-001 đến NFR-PERF-003)
   3.4. Ràng buộc thiết kế
   3.5. Các thuộc tính chất lượng
        Bảng tổng hợp NFR (Bảo mật, Sẵn sàng, Tin cậy, Dễ sử dụng, Tương thích, Khả năng bảo trì)

4. PHỤ LỤC
   4.1. Mô hình phân tích
        Hình 4.1. Biểu đồ lớp mức phân tích (CD_Lop_v1.0)
   4.2. Truy vết
```

---

# CHI TIẾT NỘI DUNG TỪNG MỤC, HÌNH ẢNH & TÀI LIỆU NGUỒN

### 1. PHẦN 1: GIỚI THIỆU
* **1.1. Mục đích:** Đặc tả các yêu cầu phần mềm cho Hệ thống LostLink – quản lý và kết nối tìm kiếm đồ thất lạc tập trung tại Khu II ĐH Cần Thơ. Đối tượng đọc: Khách hàng (Phòng CTSV, Sinh viên, Quản lý trạm), Nhóm phát triển, Nhóm kiểm thử và Giảng viên. Cấu trúc theo chuẩn IEEE 830-1998 / ISO/IEC/IEEE 29148:2018.
* **1.2. Phạm vi:** Quản lý vòng đời đồ thất lạc: đăng tin, tìm kiếm, ghép đôi AI, xác minh câu hỏi bí mật, đặt hẹn nhận đồ, quản lý kho trạm bằng mã QR, bàn giao đồ quá hạn cho Phòng CTSV. Hệ thống không vận chuyển đồ, không thanh toán tiền, không thay camera an ninh. Nêu rõ mục tiêu nghiệp vụ **MT-01 đến MT-05** trích từ `TamNhinPhamVi_v1.1`.
* **1.3. Định nghĩa, từ viết tắt:** Bảng thuật ngữ: *Vật phẩm lưu kho, Tin đăng mất, Trạm LostLink, Lịch hẹn, Mã QR hẹn, Phòng CTSV, Trao trả (cho sinh viên), Bàn giao (cho CTSV), BR, FR, NFR, UC, C, A, PHẢI/NÊN/CÓ THỂ*.
* **1.4. Tài liệu tham khảo:** 
  - `CT241_Nhom02_TamNhinPhamVi_v1.1` *(đã cập nhật ngày 15/11)*, `BienBanPhongVan_v1.0`, `BienBanLamViecKhachHang_v1.0`, `KhaoSat_v1.0`.
  - `CT241_Nhom02_MoHinhUML_v1.0` (thư mục `03_MoHinh`), `CT241_Nhom02_RTM_v1.0` (thư mục `05_QuanLyYeuCau`).
  - Giáo trình CT241 Chương 3, 4; IEEE Std 830-1998.
* **1.5. Tổng quan tài liệu:** Đoạn văn ngắn tóm tắt nội dung các mục 2, 3 và 4.

---

### 2. PHẦN 2: MÔ TẢ TỔNG QUAN
* **2.1. Bối cảnh sản phẩm:** Mô tả hệ thống web responsive độc lập, kết nối với Cổng đăng nhập dùng chung (SSO ĐH Cần Thơ), dịch vụ thông báo qua email trường.
  * **Hình ảnh nhúng:** `Hình 2.1. Lược đồ ngữ cảnh` (Lấy từ `03_MoHinh/AnhXuat/LuocDoNguCanh_v1.0.png`).
* **2.2. Chức năng sản phẩm:** Bảng phân chia 18 Use Case (`UC-01` đến `UC-18`) theo 4 nhóm tác nhân (Sinh viên, Quản lý trạm, Cán bộ CTSV, Hệ thống).
  * **Hình ảnh nhúng:** `Hình 2.2. Biểu đồ use case tổng quát` (Lấy từ `03_MoHinh/AnhXuat/UC_TongQuat_v1.0.png`).
  * **Tài liệu nguồn CHÍNH THỨC:** Sheet `DanhSachYeuCau` trong `02_ThuThap/CT241_Nhom02_DanhSachYeuCau_v1.0.xlsx` (đã chuẩn hóa tên tác nhân & 18 UC chuẩn) và biểu đồ `03_MoHinh/AnhXuat/UC_TongQuat_v1.0.png`. Tuyệt đối không dùng file nháp cũ trong thư mục `000_Documents/`.
* **2.3. Đặc điểm người dùng:** Bảng phân tích 4 lớp người dùng (Sinh viên: ~30.000, Quản lý trạm trực bàn: ~15-20, Cán bộ CTSV: ~3-5, Quản trị hệ thống: 1-2).
* **2.4. Các ràng buộc:** Bảng ràng buộc `C-01` đến `C-06` (SSO trường, web responsive di động, bảo vệ thông tin cá nhân theo NĐ 13/2023, quy định lưu kho của trường).
* **2.5. Giả định và phụ thuộc:** Bảng giả định `A-01` đến `A-04` (Hạ tầng máy chủ trường sẵn sàng, dịch vụ SMTP trường, người dùng cung cấp thông tin trung thực).

---

### 3. PHẦN 3: YÊU CẦU CỤ THỂ

#### 3.1. Yêu cầu giao diện (Đúng chuẩn Mục 3.1 đồ án mẫu)
* **Bảng Yêu cầu giao diện (IR-01 đến IR-04):**
  * `IR-01 (Người dùng):` Giao diện sinh viên theo prototype PT-01 (Hình 3.1, Hình 3.2); giao diện quản lý trạm quét mã QR thao tác trực quan, hiển thị rõ ảnh và thông tin đối soát; mọi thông báo lỗi nêu lý do cụ thể và cách khắc phục.
  * `IR-02 (Phần cứng):` Camera điện thoại thông minh hoặc máy quét mã vạch 2D (QR Code) qua cổng USB giả lập bàn phím để tra cứu nhanh hồ sơ lưu kho (NFR-COMP-002).
  * `IR-03 (Phần mềm):` Tích hợp hệ thống SSO của Trường Đại học Cần Thơ để xác thực danh tính sinh viên và nhân sự trạm.
  * `IR-04 (Truyền thông):` HTTPS mã hóa TLS 1.3 cho toàn bộ kết nối; gửi thông báo tự động qua giao thức WSS và SMTP máy chủ thư điện tử của trường.
* **Hình ảnh nhúng:**
  * `Hình 3.1. Prototype trang tra cứu và danh sách đồ thất lạc` (Lấy từ `02_ThuThap/Prototype/HTML/TraCuu/screen.png`).
  * `Hình 3.2. Prototype màn hình chi tiết vật phẩm và câu hỏi xác minh` (Lấy từ `02_ThuThap/Prototype/HTML/ChiTietVatPham/screen.png`).

#### 3.2. Yêu cầu chức năng

##### 3.2.1. Quy tắc nghiệp vụ (Business Rules - BR)
* **Bảng Quy tắc nghiệp vụ (BR-01 đến BR-08):**
  * `BR-01:` Mỗi sinh viên chỉ được duy trì tối đa 5 tin đăng đang ở trạng thái xử lý/chờ xác nhận cùng một thời điểm. *(Nguồn: BB-KH-02, PV-01)*.
  * `BR-02:` Thời hạn lưu trữ đồ vật tại trạm: Đồ thông thường tối đa 30 ngày; Đồ có giá trị cao (tiền, ví, laptop, giấy tờ) tối đa 90 ngày. *(Nguồn: XĐ-01, BB-KH-01)*.
  * `BR-03:` Tự động che mờ đặc điểm nhận dạng cốt lõi trên ảnh chụp và ẩn thông tin liên hệ đối với đồ vật có giá trị cao. *(Nguồn: XĐ-02, BB-KH-01)*.
  * `BR-04:` Người mất trả lời sai câu hỏi xác minh sở hữu quá 3 lần sẽ bị khóa tạm thời quyền yêu cầu nhận đồ trong 48 giờ. *(Nguồn: XĐ-02, BB-KH-02)*.
  * `BR-05:` Sinh viên chỉ được đặt lịch hẹn nhận đồ trong khung giờ trạm mở cửa trực (07:30–11:00 và 13:30–17:00, Thứ Hai đến Thứ Sáu). *(Nguồn: XĐ-03, BB-KH-02)*.
  * `BR-06:` Bắt buộc đối chiếu Thẻ SV/CCCD gốc và quét mã QR lịch hẹn trước khi xác nhận trao trả đồ tại quầy. *(Nguồn: XĐ-03, PV02-3)*.
  * `BR-07:` Khi đồ vật phát sinh từ 2 yêu cầu nhận trở lên hoặc có báo cáo tranh chấp, hệ thống tự động phong tỏa giao dịch và chuyển Phòng CTSV xử lý. *(Nguồn: FR-MOD-001, UC-08)*.
  * `BR-08:` Đồ vật quá hạn lưu trữ tại trạm phải được xuất khỏi kho kèm biên bản bàn giao điện tử gửi về Phòng CTSV. *(Nguồn: XĐ-01, PV02-2)*.
* **Dòng ghi chú CRUDL chuẩn đồ án mẫu:**
  > *"Ghi chú từ phân tích CRUDL: Vật phẩm lưu kho, tài khoản người dùng, tin nhắn ẩn danh, yêu cầu nhận đồ, biên bản bàn giao CTSV và nhật ký thông báo không bị xóa vật lý; sử dụng các trạng thái Đã trao trả, Quá hạn / Đã bàn giao CTSV, Vô hiệu hóa để bảo toàn lịch sử và đối soát khi có khiếu nại."*

##### 3.2.2. Đặc tả use case chính (5 Use Case cốt lõi)
Mỗi Use Case lập một bảng khung chi tiết gồm: *Mã/Tên, Mô tả, Tác nhân, Độ ưu tiên, Kích hoạt, Tiền điều kiện, Hậu điều kiện, Luồng chính, Luồng thay thế, Luồng ngoại lệ, Quy tắc nghiệp vụ, NFR, FR và Mô hình liên quan*.
1. **UC-02. Đăng tin tìm đồ thất lạc:** Dựa trên `BaiTH03.docx` (mục 1.2.1), cập nhật chuẩn hóa tên trạng thái **"Chờ xác nhận"**; luồng kiểm tra $\le 5$ tin (BR-01); liên kết AD-01, SD-01.
2. **UC-04. Tra cứu và lọc danh sách đồ thất lạc:** Dựa trên `BaiTH03.docx` (mục 1.2.2), lọc theo phân loại, khu vực nhặt, ngày mất; gợi ý so khớp tương đồng; liên kết AD-03.
3. **UC-07. Xác minh quyền sở hữu đồ thất lạc:** Sinh viên trả lời câu hỏi bảo mật; luồng kiểm tra đúng/sai $\ge 3$ lần kích hoạt khóa 48h (BR-04); liên kết SD-03.
4. **UC-09. Đặt và quản lý lịch hẹn nhận đồ tại trạm:** Chọn khung giờ trực; sinh viên có thể đổi/hủy hẹn trước giờ hẹn; liên kết ST-02 (Vòng đời lịch hẹn).
5. **UC-11. Quét mã QR và giao trả đồ trực tiếp tại trạm:** Quản lý trạm quét QR; đối chiếu Thẻ SV; alt đối chiếu khớp $\rightarrow$ cập nhật **"Đã trao trả"**; alt tranh chấp $\rightarrow$ phong tỏa; liên kết AD-02, SD-02.

##### 3.2.3. Danh sách yêu cầu chức năng (28 FR)
* **Bảng tổng hợp 28 FR:** Cột *Mã, Tên, Ưu tiên (Essential/Desirable/Optional), Use Case*.
* **Bảng thẻ chi tiết từng FR theo template Bảng 4.9:**
  * Chia thành 9 nhóm nghiệp vụ: `AUTH`, `POST`, `SEARCH`, `VERIFY`, `APPT`, `STATION`, `SHIFT`, `OVERDUE`, `RPT/NOTI`.
  * Mỗi FR gồm: *Mã, Tên, Mô tả chi tiết (dùng PHẢI/NÊN/CÓ THỂ), UC liên quan, Tác nhân, Tiền/Hậu điều kiện, Luồng chính, Ngoại lệ, BR liên quan, Nguồn gốc, Tiêu chí chấp nhận (Given/When/Then), Trạng thái (Approved), Phiên bản (v1.0)*.

#### 3.3. Yêu cầu hiệu năng
* **Bảng Yêu cầu hiệu năng:**
  * `NFR-PERF-001:` Hệ thống PHẢI trả kết quả tìm kiếm và lọc đồ thất lạc trong vòng $\le 2$ giây với 200 người dùng đồng thời. *(Kiểm chứng: Kiểm thử tải 200 virtual users trong 15 phút, đo phân vị 95)*.
  * `NFR-PERF-002:` Thời gian tự động so khớp và gợi ý tin tương đồng PHẢI hoàn tất trong vòng $\le 5$ giây sau khi tin mới được duyệt lưu. *(Kiểm chứng: Đo thời gian chạy giải thuật đối soát 100 tin mẫu)*.
  * `NFR-PERF-003:` Sau khi quét mã QR hiện vật/lịch hẹn tại trạm, hệ thống PHẢI tải và hiển thị hồ sơ đối soát trong vòng $\le 1$ giây cho 99% lần quét. *(Kiểm chứng: Đo thời gian 200 lần quét trên thiết bị bàn trực chuẩn)*.

#### 3.4. Ràng buộc thiết kế
* Ràng buộc từ `C-01` đến `C-06`.
* Kiến trúc ứng dụng Web responsive; giao diện hiển thị trơn tru, không vỡ khung từ độ rộng màn hình 360 px trở lên (NFR-USA-002).
* CSDL quan hệ lưu trữ trên máy chủ trường; tuân thủ quy tắc toàn vẹn không xóa vật lý các bản ghi lịch sử theo phân tích CRUDL.

#### 3.5. Các thuộc tính chất lượng
* **Bảng tổng hợp NFR:** Bao phủ đủ các thuộc tính:
  * `NFR-SEC-001..004 (Bảo mật):` Kiểm soát quyền phía server; mã hóa dữ liệu cá nhân; hết hạn phiên làm việc sau 30 phút rảnh (trên máy bàn trực là 10 phút); ghi nhật ký giao nhận không thể sửa.
  * `NFR-AVA-001 (Tính sẵn sàng):` Sẵn sàng tối thiểu 99,5% trong khung giờ hoạt động của trường (06:00–22:00 hằng ngày).
  * `NFR-REL-001 (Độ tin cậy):` Sao lưu tự động CSDL lúc 02:00 hằng ngày; khôi phục hệ thống trong vòng 4 giờ khi có sự cố.
  * `NFR-USA-001..002 (Khả dụng):` Tình nguyện viên mới hoàn thành thao tác quét mã và giao trả đồ trong $\le 60$ giây sau 15 phút hướng dẫn; giao diện thích ứng màn hình di động 360 px.
  * `NFR-COMP-001..002 (Tương thích):` Hoạt động chuẩn xác trên các trình duyệt di động và máy tính phổ biến (Chrome, Safari, Edge); máy trạm đọc tốt chuẩn QR Code ISO/IEC 18004.
  * `NFR-MAIN-001 (Khả năng bảo trì):` Cho phép Cán bộ CTSV thay đổi tham số quy định (thời hạn giữ đồ 30/90 ngày, khung giờ trạm trực) qua giao diện quản trị mà không cần sửa mã nguồn.

---

### 4. PHẦN 4: PHỤ LỤC
* **4.1. Mô hình phân tích:** Giới thiệu ngắn về 5 loại biểu đồ UML đã hoàn thiện trong `CT241_Nhom02_MoHinhUML_v1.0.pdf` (thư mục `03_MoHinh`).
  * **Hình ảnh nhúng:** `Hình 4.1. Biểu đồ lớp mức phân tích` (Lấy từ `03_MoHinh/AnhXuat/CD_Lop_v1.0.png`).
* **4.2. Truy vết:** Tóm tắt ma trận truy vết hai chiều: `MT (Mục tiêu) → FR/NFR → UC → Biểu đồ UML → Ca kiểm thử chấp nhận`. Trích dẫn tới file `CT241_Nhom02_RTM_v1.0.xlsx` trong thư mục `05_QuanLyYeuCau`.

---