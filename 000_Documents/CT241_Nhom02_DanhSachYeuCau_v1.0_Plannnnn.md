# BẢN THẢO THIẾT KẾ MA TRẬN DANH SÁCH YÊU CẦU & XUNG ĐỘT (ĐÃ ĐỐI CHIẾU 100% THƯ MỤC 02)
**Dự án:** Hệ thống quản lý và kết nối tìm kiếm đồ thất lạc tập trung trong khuôn viên Đại học Cần Thơ (LostLink)  
**Môn học:** CT241 – Phân tích yêu cầu phần mềm (Học kỳ 1, Năm học 2026–2027)  
**Nhóm thực hiện:** Nhóm 02 · Đề tài 05  
**Căn cứ đối chiếu trực tiếp từ hồ sơ dự án:**
1. **Đề cương môn học CT241 (Đề tài 5 & Mục 3.1.6):** Bối cảnh, 4 lớp người dùng, 6 phạm vi tối thiểu, 3 ràng buộc đã biết, 2 xung đột cốt lõi.
2. **Thư mục `01_TamNhin`:** `TamNhinPhamVi_v1.0.docx` (MT-01..05, FE-01..07, Scope 3.1..3.3, Lớp người dùng 4.2).
3. **Thư mục `02_ThuThap`:**
   - `BienBanPhongVan_v1.0.docx`: Các mã trích xuất `PV01-1..7`, `PV02-1..6`, `PV03-1..13`.
   - `BienBanLamViecKhachHang_v1.0.docx`: Các mã cam kết `KH01-1..4` (Họp 10/11) và `KH02-1..5` (Họp 13/11).
   - `KhaoSat_v1.0.docx` & `KetQuaKhaoSat_v1.0.xlsx`: Kết quả khảo sát 31 sinh viên (`KS-01` Q1 đến Q18).
   - `PhanHoiPrototype_v1.0.docx`: 6 phản hồi kiểm thử giao diện `PT-01`.
   - `CRUDL_v1.0.xlsx` & `PhanCongTacNhan_v1.0.md`: Chuẩn hóa 18 Use Case và 13 Thực thể dữ liệu.
4. **Slide lý thuyết Chương 1:** Sơ đồ Hình 1.3 và Nguyên lý MoSCoW DSDM/Agile (Slide 44–45).

---

## BẢNG MA TRẬN TRUY VẾT NGUỒN GỐC TỪ THƯ MỤC 02 SANG DANH SÁCH YÊU CẦU

| Tài liệu trong thư mục `02_ThuThap` | Mã yêu cầu rút ra trong tài liệu | Nội dung nghiệp vụ gốc | Ánh xạ vào Yêu cầu hệ thống LostLink | Ghi chú & Liên kết Use Case |
|---|---|---|---|---|
| **PV-01 (Dương Hoàng Huynh)** | `PV01-1` | Nền tảng chung để liên lạc, hẹn lịch trước khi đến trạm/nhận đồ. | `FR-APPT-001`, `FR-CHAT-001` | `UC-06`, `UC-09`, `MT-01` |
| | `PV01-2` | Tin nhặt đồ có ảnh và SĐT người nhặt để liên hệ nhanh. | `FR-POST-001`, `XĐ-02` | `UC-02`, `UC-03` |
| | `PV01-3` | Đăng tin trên điện thoại với thông tin tối thiểu ảnh + SĐT. | `NFR-USA-001`, `HW-CLI-01` | `UC-02`, `C-04` |
| | `PV01-4` | Nhiều người cùng nhận đồ giá trị cao thì tra camera an ninh. | `W-01`, `XĐ-01` | Hoãn bản 1.0 (phụ thuộc camera trường) |
| | `PV01-5` | Người nhặt ở xa ngại mang đến trạm Nhà điều hành. | `W-02`, `FR-APPT-001` | Hoãn bản 1.0 (yêu cầu nộp về trạm) |
| | `PV01-6` | Danh mục chuẩn hóa loại đồ và khu vực rơi đồ. | `FR-CAT-001` | `UC-15` |
| | `PV01-7` | Đồ giữ quá lâu chuyển Phòng CTSV xử lý, hệ thống hết trách nhiệm. | `FR-OVERDUE-001`, `FR-OVERDUE-002` | `UC-13`, `MT-05` |
| **PV-02 (Trưởng phòng CTSV)** | `PV02-1` | Thời hạn lưu giữ theo nhóm đồ, cấu hình được, đổi theo năm học. | `FR-OVERDUE-001`, `FR-CAT-001`, `XĐ-03` | `UC-13`, `UC-15` |
| | `PV02-2` | Đồ quá hạn lập biên bản giao CTSV; Phòng thanh lý ngoài hệ thống. | `FR-OVERDUE-002`, `MT-05`, `C-05` | `UC-13` |
| | `PV02-3` | Lưu lịch sử người nhận và đối chiếu Thẻ sinh viên khi giao trả. | `FR-RETURN-001`, `NFR-SEC-004`, `MT-03` | `UC-11` |
| | `PV02-4` | Phân quyền sinh viên quản lý trạm theo ca và học kỳ. | `FR-USER-001` | `UC-16`, `FR-AUTH-002` |
| | `PV02-5` | Đăng nhập bằng tài khoản trường (SSO Google Workspace). | `FR-AUTH-001`, `C-01` | `UC-01` |
| | `PV02-6` | Đặt lịch hẹn theo khung giờ mở cửa của trạm. | `FR-APPT-001`, `XĐ-01` | `UC-09` |
| **PV-03 (Quản lý trạm)** | `PV03-1` | Tiếp nhận đồ, tạo mã QR định danh cho từng món, tra theo mã. | `FR-STATION-001` | `UC-10`, `MT-04` |
| | `PV03-2` | Câu hỏi xác minh ẩn danh, đối chiếu Thẻ SV; lưu lịch sử nhận. | `FR-VERIFY-001`, `NFR-SEC-001` | `UC-07`, `MT-03` |
| | `PV03-3` | Cập nhật trạng thái đồ theo vòng đời 7 trạng thái chuẩn. | `FR-STATION-002`, `FR-RETURN-002` | `UC-10`, `UC-11` |
| | `PV03-4` | Một lượt tiếp nhận hoặc giao trả không quá 3 phút (hiện 10p). | `NFR-PERF-003`, `MT-04`, `XĐ-01` | `UC-10`, `UC-11` |
| | `PV03-5` | Bàn giao ca trực trên hệ thống: đồ đang giữ, hẹn, sắp quá hạn. | `FR-SHIFT-001`, `FR-SHIFT-002` | `UC-12`, `MT-03` |
| | `PV03-6` | Làm mờ ảnh giấy tờ; quản trị viên duyệt tin; xử lý tin vi phạm. | `FR-POST-002`, `FR-MOD-001`, `XĐ-02` | `UC-03`, `UC-14` |
| | `PV03-7` | Quản trị viên phân quyền cho sinh viên quản lý trạm. | `FR-USER-001` | `UC-16` |
| | `PV03-8` | Quản trị viên quản lý danh mục loại đồ và mức "có giá trị". | `FR-CAT-001` | `UC-15` |
| | `PV03-9` | Báo cáo tháng: đồ chưa nhận, tỉ lệ trả lại, khu vực rơi nhiều. | `FR-RPT-001`, `MT-05` | `UC-17` |
| | `PV03-10` | Tra cứu phản hồi dưới 2 giây. | `NFR-PERF-001` | `UC-04`, `MT-02` |
| | `PV03-11` | Trạm dùng máy tính Windows/Chrome và smartphone quét QR. | `C-04`, `HW-CLI-01` | Toàn hệ thống |
| | `PV03-12` | Khi nhiều người cùng trả lời đúng: chuyển Tranh chấp, giữ đồ, chuyển CTSV. | `FR-DISPUTE-001`, `FR-DISPUTE-002` | `UC-08`, `MT-03` |
| | `PV03-13` | Hệ thống phục vụ khoảng 1.000 sinh viên. | `NFR-SCA-001` | Toàn hệ thống |
| **BB-KH-01 (Nhóm 10 - CTSV)** | `KH01-1` | Chốt thời hạn lưu giữ: đồ thường 30 ngày, đồ có giá trị 90 ngày. | `FR-OVERDUE-001`, `XĐ-03` | `UC-13`, `MT-05` |
| | `KH01-2` | Định nghĩa đồ giá trị (tiền, trang sức, laptop, CCCD); làm mờ ảnh. | `FR-CAT-001`, `FR-POST-002`, `XĐ-02` | `UC-03`, `UC-15` |
| | `KH01-3` | Quản lý trạm lập biên bản bàn giao đồ quá hạn số hóa gửi CTSV. | `FR-OVERDUE-002` | `UC-13` |
| | `KH01-4` | CTSV xác nhận tiếp nhận, trạm cập nhật trạng thái "Đã bàn giao". | `FR-OVERDUE-002`, `FR-STATION-002` | `UC-13` |
| **BB-KH-02 (Nhóm 10 - Trạm)** | `KH02-1` | Hai người cùng trả lời đúng: chuyển Tranh chấp, không tự ý giao. | `FR-DISPUTE-001`, `FR-DISPUTE-002` | `UC-08` |
| | `KH02-2` | Trả lời sai xác minh tối đa 3 lần trong 48h thì khóa tạm thời. | `FR-VERIFY-002` | `UC-07`, `MT-03` |
| | `KH02-3` | Bàn giao ca: kiểm kê đối chiếu thực tế với hệ thống, ký số hóa. | `FR-SHIFT-001`, `FR-SHIFT-002` | `UC-12` |
| | `KH02-4` | Không triển khai camera an ninh và nhận phân tán ở bản 1.0. | `W-01`, `W-02` | Hoãn bản sau |
| | `KH02-5` | Chốt giờ mở cửa trạm: 07:30–11:00 và 13:30–17:00 (Thứ 2 - Thứ 7). | `FR-APPT-001`, `FR-CAT-001` | `UC-09`, `UC-15` |
| **Khảo sát KS-01 (31 SV)** | `KS-01 Q6` | 90,3% gặp khó khăn vì bài đăng trôi nhanh trên Facebook/Zalo. | `MT-01`, `MT-02`, `FR-POST-001` | `UC-02` |
| | `KS-01 Q13` | 96,8% SV cần tính năng tự động so khớp và gợi ý tin mất - nhặt. | `FR-MATCH-001` | `UC-05` |
| | `KS-01 Q14` | 100% lo ngại nhận vơ; 93,5% ủng hộ che mờ chi tiết cốt lõi ảnh. | `XĐ-02`, `FR-POST-002`, `NFR-SEC-002` | `UC-03` |
| | `KS-01 Q15` | 93,5% SV đánh giá rất cần thiết câu hỏi xác minh sở hữu ẩn danh. | `FR-VERIFY-001`, `UC-07` | `UC-07` |
| | `KS-01 Q16` | 100% SV muốn ẩn thông tin cá nhân/SĐT và dùng Chat ẩn danh. | `FR-CHAT-001`, `XĐ-02` | `UC-06` |
| | `KS-01 Q17` | 100% SV muốn nhận thông báo tức thời qua điện thoại/email. | `FR-NOTI-001` | `UC-18` |
| | `KS-01 Q18` | 93,5% muốn đặt lịch hẹn giờ; 90,3% muốn tra cứu đồ tồn kho. | `FR-APPT-001`, `FR-SEARCH-002`, `XĐ-01` | `UC-04`, `UC-09` |
| **Prototype PT-01** | `Góp ý 1, 2` | Làm mờ ảnh đồng bộ các đồ giá trị; thêm chip lọc khu vực, trạng thái. | `FR-POST-002`, `FR-SEARCH-001` | `UC-03`, `UC-04` |
| | `Góp ý 4, 5` | Khung giờ hẹn khớp giờ mở cửa trạm; chỉ mở hẹn khi xác minh xong. | `FR-APPT-001`, `FR-VERIFY-001` | `UC-09` |
| | `Góp ý 6` | Giao diện nền tối (Dark mode) và định vị GPS khuôn viên trường. | `W-03`, `W-04` | Hoãn bản sau |

---

## NỘI DUNG CHI TIẾT SHEET 1: `DanhSachYeuCau`

### 1. Yêu cầu Nghiệp vụ (Business Requirements - Trả lời "VÌ SAO")
| Mã | Phát biểu yêu cầu | Loại (Hình 1.3) | MoSCoW | Nguồn gốc cụ thể | Truy về MT |
|:---|:---|:---|:---:|:---|:---:|
| **MT-01** | Tăng tỉ lệ đồ nhặt được trao trả về đúng chủ sở hữu từ khoảng 30% lên ít nhất 60% sau 1 học kỳ vận hành chính thức trong khuôn viên trường. | Yêu cầu nghiệp vụ | Must | Tầm nhìn – phạm vi v1.0 (Mục 1.3); Đề tài 5; KS-01 | MT-01 |
| **MT-02** | Giảm thời gian từ khi đồ vật được tiếp nhận vào trạm đến khi trao trả về cho chủ nhân, từ 5–7 ngày xuống không quá 3 ngày (trung vị). | Yêu cầu nghiệp vụ | Must | Tầm nhìn – phạm vi v1.0; KS-01 | MT-02 |
| **MT-03** | Tuyệt đối không để xảy ra trường hợp trao trả nhầm đồ vật có giá trị hoặc thất thoát tài sản đã lưu kho trong suốt học kỳ vận hành. | Yêu cầu nghiệp vụ | Must | Tầm nhìn – phạm vi v1.0; PV02-3; PV03-2; Đề tài 5 | MT-03 |
| **MT-04** | Giảm thời gian xử lý thủ tục một lượt tiếp nhận đồ nhặt được hoặc giao trả đồ tại bàn trực trạm từ 10 phút xuống không quá 3 phút. | Yêu cầu nghiệp vụ | Must | Tầm nhìn – phạm vi v1.0; PV03-4; XĐ-01 | MT-04 |
| **MT-05** | Toàn bộ đồ vật quá hạn lưu giữ (30 ngày đồ thường, 90 ngày đồ giá trị) được xử lý đúng quy định và có biên bản bàn giao điện tử cho Phòng CTSV định kỳ. | Yêu cầu nghiệp vụ | Must | Tầm nhìn – phạm vi v1.0; PV02-2; KH01-1..4 | MT-05 |

---

### 2. Yêu cầu Người dùng (User Requirements - "Người dùng cần hệ thống làm gì?")
> Bao gồm **18 Use Case cấp cao** (khớp hoàn toàn với Ma trận CRUDL và Bảng phân công tác nhân) và **6 Yêu cầu hoãn lại (`Won't have`)** để kiểm soát Scope Creep.

| Mã | Phát biểu yêu cầu (High-level Use Case & User Story) | Loại (Hình 1.3) | MoSCoW | Nguồn gốc cụ thể | Truy về MT |
|:---|:---|:---|:---:|:---|:---:|
| **UC-01** | Đăng nhập và xác thực tài khoản (Tác nhân: Sinh viên, Quản lý trạm, Cán bộ CTSV) | Yêu cầu người dùng | Must | Tầm nhìn v1.0; PV02-5; C-01; Đề tài 5 | MT-01, MT-03 |
| **UC-02** | Đăng tin tìm đồ thất lạc (Tác nhân: Sinh viên) | Yêu cầu người dùng | Must | PV01-1; KS-01 Q6; PT-01 | MT-01, MT-02 |
| **UC-03** | Đăng tin nhặt được đồ kèm câu hỏi xác minh (Tác nhân: Sinh viên, Quản lý trạm) | Yêu cầu người dùng | Must | PV01-2; PV03-6; KH01-2; KS-01 Q14; XĐ-02 | MT-01, MT-03 |
| **UC-04** | Tra cứu và lọc danh sách đồ thất lạc (Tác nhân: Sinh viên, Quản lý trạm, Cán bộ CTSV) | Yêu cầu người dùng | Must | PV01-6; PV03-10; KS-01 Q7; PT-01 | MT-01, MT-02 |
| **UC-05** | Tự động so khớp và gợi ý tin thất lạc tương đồng (Tác nhân: Hệ thống, Sinh viên) | Yêu cầu người dùng | Should | KS-01 Q13 (96,8% SV cần); Đề tài 5 | MT-01, MT-02 |
| **UC-06** | Nhắn tin ẩn danh trao đổi thông tin nhận đồ (Tác nhân: Sinh viên, Quản lý trạm) | Yêu cầu người dùng | Should | KS-01 Q16 (100% muốn ẩn SĐT); XĐ-02 | MT-01, MT-03 |
| **UC-07** | Xác minh quyền sở hữu đồ thất lạc (Tác nhân: Sinh viên, Quản lý trạm) | Yêu cầu người dùng | Must | PV03-2; KS-01 Q14, Q15; KH02-2 | MT-03 |
| **UC-08** | Tiếp nhận và xử lý tranh chấp nhận đồ (Tác nhân: Cán bộ CTSV, Quản lý trạm, Sinh viên) | Yêu cầu người dùng | Must | PV01-4; PV03-12; KH02-1; XĐ-03 | MT-03 |
| **UC-09** | Đặt và quản lý lịch hẹn nhận đồ tại trạm (Tác nhân: Sinh viên, Quản lý trạm) | Yêu cầu người dùng | Must | PV01-1; PV02-6; KH02-5; KS-01 Q18; XĐ-01 | MT-02, MT-04 |
| **UC-10** | Tiếp nhận vật phẩm vào kho trạm và cấp mã QR (Tác nhân: Quản lý trạm, Sinh viên) | Yêu cầu người dùng | Must | PV03-1; BB-KH-01; MT-04 | MT-01, MT-04 |
| **UC-11** | Quét mã QR và giao trả đồ trực tiếp tại trạm (Tác nhân: Quản lý trạm, Sinh viên) | Yêu cầu người dùng | Must | PV02-3; PV03-4; BB-KH-01; XĐ-01 | MT-03, MT-04 |
| **UC-12** | Bàn giao ca trực và kiểm kê kho hiện vật (Tác nhân: Quản lý trạm, Cán bộ CTSV) | Yêu cầu người dùng | Must | PV03-5; KH02-3 | MT-03, MT-05 |
| **UC-13** | Xử lý đồ quá hạn và lập biên bản bàn giao CTSV (Tác nhân: Quản lý trạm, Cán bộ CTSV) | Yêu cầu người dùng | Must | PV02-2; KH01-1..4; XĐ-03 | MT-05 |
| **UC-14** | Kiểm duyệt tin đăng và xử lý vi phạm nội dung (Tác nhân: Quản lý trạm, Cán bộ CTSV) | Yêu cầu người dùng | Should | PV03-6; BB-KH-02 | MT-01, MT-03 |
| **UC-15** | Quản lý danh mục loại đồ, khu vực và quy định trạm (Tác nhân: Cán bộ CTSV) | Yêu cầu người dùng | Must | PV01-6; PV02-1; PV03-8; KH01-2 | MT-03, MT-05 |
| **UC-16** | Quản lý tài khoản và phân quyền nhân sự trạm (Tác nhân: Cán bộ CTSV, Quản lý trạm) | Yêu cầu người dùng | Must | PV02-4; PV03-7; BB-KH-02 | MT-03, MT-04 |
| **UC-17** | Thống kê và kết xuất báo cáo định kỳ (Tác nhân: Cán bộ CTSV, Quản lý trạm) | Yêu cầu người dùng | Must | PV02-1; PV03-9; BB-KH-01; Đề tài 5 | MT-05 |
| **UC-18** | Gửi thông báo tự động đa kênh (Tác nhân: Hệ thống, Sinh viên, Quản lý trạm) | Yêu cầu người dùng | Must | KS-01 Q17; BB-KH-02 | MT-01, MT-02 |
| **W-01** | Đối chiếu thông tin bằng hệ thống camera an ninh khu vực khi có tranh chấp. | Yêu cầu người dùng | Won't (bản này) | PV01-4; KH02-4; Đề tài 5 (Lưu ý thu thập) | — |
| **W-02** | Hỗ trợ điều phối tiếp nhận và giao nhận phân tán cho người nhặt ở xa trạm. | Yêu cầu người dùng | Won't (bản này) | PV01-5; KH02-4; Tầm nhìn 3.3 | — |
| **W-03** | Chế độ giao diện nền tối (Dark Mode) cho ứng dụng Web và Mobile. | Yêu cầu người dùng | Won't (bản này) | Góp ý PT-01 (Mục 4); Tầm nhìn 3.2 | — |
| **W-04** | Bản đồ số khuôn viên trường (Campus Map) tích hợp GPS ghim vị trí rơi đồ. | Yêu cầu người dùng | Won't (bản này) | Tầm nhìn 3.2; Góp ý PT-01 | — |
| **W-05** | Hệ thống tích điểm rèn luyện và vinh danh người tốt việc tốt nhặt được của rơi. | Yêu cầu người dùng | Won't (bản này) | Tầm nhìn 3.2 | — |
| **W-06** | Mở rộng hệ thống trạm lưu giữ sang các cơ sở khác (Khu I, Khu III, Khu Hòa An). | Yêu cầu người dùng | Won't (bản này) | Tầm nhìn 3.2; Đề tài 5 | — |

---

### 3. Yêu cầu Hệ thống – Phần mềm (Software Requirements)

#### 3.1. Yêu cầu Chức năng (Functional Requirements - `FR-*`, gồm 28 yêu cầu)
| Mã | Phát biểu yêu cầu chức năng (Dùng từ khóa bắt buộc PHẢI / NÊN) | Loại (Hình 1.3) | MoSCoW | Nguồn gốc cụ thể từ 02_ThuThap | Truy về MT |
|:---|:---|:---|:---:|:---|:---:|
| **FR-AUTH-001** | Hệ thống PHẢI xác thực người dùng thông qua SSO Google Workspace của trường (`@ctu.edu.vn` hoặc `@student.ctu.edu.vn`). | Yêu cầu hệ thống – chức năng | Must | Tầm nhìn v1.0; PV02-5; C-01; Đề tài 5 | MT-01 |
| **FR-AUTH-002** | Hệ thống PHẢI phân quyền truy cập nghiêm ngặt theo **04 vai trò người dùng**: (1) Sinh viên, (2) Sinh viên quản lý trạm (`Station_Staff`), (3) Sinh viên quản trị hệ thống (`System_Admin`), và (4) Cán bộ Phòng CTSV (`CTSV_Officer`); từ chối truy cập vượt quyền. | Yêu cầu hệ thống – chức năng | Must | Tầm nhìn 4.2; PV02-4; PV03-7; NFR-SEC-001 | MT-03 |
| **FR-POST-001** | Hệ thống PHẢI cho phép sinh viên tạo tin tìm đồ thất lạc gồm: Tiêu đề, Loại đồ, Khu vực thất lạc, Thời gian ước tính, Mô tả đặc điểm, và Ảnh minh họa. | Yêu cầu hệ thống – chức năng | Must | PV01-1; KS-01 Q6; PT-01; Đề tài 5 | MT-01 |
| **FR-POST-002** | Khi đăng tin nhặt được đồ, hệ thống PHẢI bắt buộc người đăng tạo từ 1–3 câu hỏi xác minh ẩn danh và công cụ tự động làm mờ chi tiết nhạy cảm trên ảnh. | Yêu cầu hệ thống – chức năng | Must | PV01-2; PV03-6; KH01-2; KS-01 Q14; XĐ-02 | MT-03 |
| **FR-POST-003** | Hệ thống PHẢI cho phép người đăng đóng hoặc hủy tin đăng khi đã tìm lại hoặc trao trả xong đồ vật. | Yêu cầu hệ thống – chức năng | Must | PV01-1; BB-KH-02 | MT-01 |
| **FR-SEARCH-001**| Hệ thống PHẢI hỗ trợ bộ lọc tra cứu đa tiêu chí: Từ khóa tiêu đề, Phân loại đồ vật, Khu vực khuôn viên, Khoảng ngày thất lạc, và Trạng thái lưu kho. | Yêu cầu hệ thống – chức năng | Must | PV01-6; PV03-10; KS-01 Q7; PT-01 | MT-01, MT-02 |
| **FR-SEARCH-002**| Kết quả tra cứu PHẢI hiển thị rõ nhãn phân biệt: "Đang lưu tại trạm" (kèm mã trạm) hoặc "Tin báo nhặt tự do do sinh viên giữ". | Yêu cầu hệ thống – chức năng | Must | PV03-3; KS-01 Q18; KH02-5 | MT-02 |
| **FR-MATCH-001** | Hệ thống NÊN tự động so khớp các cặp tin mất - tin nhặt theo trọng số tương đồng (Loại đồ, Khu vực, Thời gian +-3 ngày) và gửi danh sách gợi ý cho sinh viên. | Yêu cầu hệ thống – chức năng | Should | KS-01 Q13 (96,8% SV cần); Đề tài 5 | MT-01, MT-02 |
| **FR-CHAT-001**  | Hệ thống NÊN cung cấp kênh tin nhắn văn bản nội bộ ẩn danh (in-app chat) giữa người mất và người nhặt, ẩn toàn bộ số điện thoại cá nhân. | Yêu cầu hệ thống – chức năng | Should | PV01-1; KS-01 Q16; XĐ-02 | MT-01, MT-03 |
| **FR-VERIFY-001**| Người nhận đồ PHẢI trả lời các câu hỏi bảo mật do người nhặt đặt ra; hệ thống chỉ ghi nhận hợp lệ khi câu trả lời khớp với đáp án lưu trữ. | Yêu cầu hệ thống – chức năng | Must | PV03-2; KS-01 Q14, Q15; BB-KH-02; XĐ-02 | MT-03 |
| **FR-VERIFY-002**| Hệ thống PHẢI tự động khóa quyền gửi yêu cầu nhận đồ của một tài khoản trên món đồ cụ thể trong vòng 48 giờ nếu người đó trả lời sai quá 3 lần liên tiếp. | Yêu cầu hệ thống – chức năng | Must | KH02-2; PV03-2; BB-KH-02 | MT-03 |
| **FR-DISPUTE-001**| Khi phát sinh từ 2 sinh viên trở lên cùng trả lời đúng xác minh cho 1 món đồ, hệ thống PHẢI tự động chuyển trạng thái đồ sang "Tranh chấp" và phong tỏa lịch hẹn. | Yêu cầu hệ thống – chức năng | Must | PV01-4; PV03-12; KH02-1 | MT-03 |
| **FR-DISPUTE-002**| Hệ thống PHẢI cho phép Cán bộ CTSV xem hồ sơ đối soát, ghi nhận biên bản làm việc hòa giải và chỉ định người nhận hợp pháp duy nhất để giải tỏa tranh chấp. | Yêu cầu hệ thống – chức năng | Must | PV02-6; PV03-12; KH02-1 | MT-03 |
| **FR-APPT-001**  | Hệ thống PHẢI cho phép sinh viên đặt lịch hẹn đến trạm nhận đồ theo các khung giờ mở cửa quy định (07:30–11:00 và 13:30–17:00, Thứ Hai đến Thứ Bảy). | Yêu cầu hệ thống – chức năng | Must | PV01-1; PV02-6; KH02-5; XĐ-01 | MT-02, MT-04 |
| **FR-APPT-002**  | Hệ thống PHẢI cho phép sinh viên đổi khung giờ hẹn hoặc hủy lịch hẹn trước tối thiểu 02 giờ so với thời điểm hẹn đã đăng ký. | Yêu cầu hệ thống – chức năng | Must | PT-01 (Mục 4); BB-KH-02 | MT-04 |
| **FR-STATION-001**| Khi tiếp nhận đồ vật lý vào trạm, hệ thống PHẢI tự sinh mã QR định danh duy nhất (chứa mã đồ, ngày nhận, loại đồ) và cho phép in tem dán lên hiện vật trong <= 60 giây. | Yêu cầu hệ thống – chức năng | Must | PV03-1; BB-KH-01; MT-04 | MT-01, MT-04 |
| **FR-STATION-002**| Nhân sự trạm PHẢI cập nhật vị trí ngăn/tủ lưu giữ và tình trạng vật lý của món đồ khi nhập kho vào hệ thống. | Yêu cầu hệ thống – chức năng | Must | PV03-3; KH01-4; BB-KH-01 | MT-04 |
| **FR-RETURN-001**| Nhân sự trạm PHẢI quét mã QR trên hiện vật để gọi thông tin phiếu hẹn, đối chiếu Thẻ sinh viên người nhận và chụp ảnh xác nhận bàn giao trực tiếp tại trạm. | Yêu cầu hệ thống – chức năng | Must | PV02-3; PV03-4; BB-KH-01; XĐ-01 | MT-03, MT-04 |
| **FR-RETURN-002**| Sau khi giao trả thành công, hệ thống PHẢI tự động chuyển trạng thái món đồ sang "Đã trao trả", đóng tin đăng và lưu trữ hồ sơ giao nhận vào lịch sử kiểm toán. | Yêu cầu hệ thống – chức năng | Must | PV03-3; BB-KH-01 | MT-01, MT-03 |
| **FR-SHIFT-001**  | Cuối mỗi ca trực, hệ thống PHẢI cung cấp tính năng kiểm kê tủ kho: nhân sự trạm quét toàn bộ mã QR hiện vật, hệ thống tự động đối soát sai lệch thừa/thiếu. | Yêu cầu hệ thống – chức năng | Must | PV03-5; KH02-3 | MT-03, MT-04 |
| **FR-SHIFT-002**  | Biên bản bàn giao ca PHẢI ghi nhận mã nhân sự giao, mã nhân sự nhận, số lượng đồ tồn kho thực tế, số lịch hẹn trong ca kế tiếp và chữ ký xác nhận số hóa. | Yêu cầu hệ thống – chức năng | Must | PV03-5; KH02-3 | MT-03, MT-04 |
| **FR-OVERDUE-001**| Hệ thống PHẢI tự động quét hàng ngày và đánh dấu "Quá hạn lưu kho" đối với đồ thường lưu quá 30 ngày và đồ có giá trị lưu quá 90 ngày kể từ ngày tiếp nhận. | Yêu cầu hệ thống – chức năng | Must | PV02-1; KH01-1; XĐ-03 | MT-05 |
| **FR-OVERDUE-002**| Hệ thống PHẢI cho phép xuất danh sách kèm Biên bản bàn giao đồ quá hạn số hóa để Quản lý trạm ký bàn giao hiện vật cho đại diện Phòng CTSV. | Yêu cầu hệ thống – chức năng | Must | PV02-2; KH01-3, KH01-4 | MT-05 |
| **FR-MOD-001**    | Hệ thống NÊN cung cấp chức năng tiếp nhận báo cáo vi phạm từ người dùng và cho phép Quản trị viên ẩn tin đăng rác, hình ảnh nhạy cảm hoặc khóa tài khoản vi phạm. | Yêu cầu hệ thống – chức năng | Should | PV03-6; BB-KH-02 | MT-01, MT-03 |
| **FR-CAT-001**    | Hệ thống PHẢI cho phép Cán bộ CTSV quản lý danh mục loại đồ, danh mục phân loại đồ có giá trị, danh mục khu vực và cấu hình thời hạn lưu kho (30/90 ngày). | Yêu cầu hệ thống – chức năng | Must | PV01-6; PV02-1; PV03-8; KH01-2 | MT-05 |
| **FR-USER-001**   | Hệ thống PHẢI cho phép Cán bộ CTSV cấp quyền vai trò Quản lý trạm (`Station_Staff`) cho tài khoản SSO của sinh viên trực ca theo từng học kỳ. | Yêu cầu hệ thống – chức năng | Must | PV02-4; PV03-7; BB-KH-02 | MT-03, MT-04 |
| **FR-RPT-001**    | Hệ thống PHẢI tạo báo cáo thống kê định kỳ hàng tháng/học kỳ gồm: Tỷ lệ trao trả thành công, Số lượng tồn kho theo loại đồ, Biểu đồ khu vực thất lạc nhiều nhất. | Yêu cầu hệ thống – chức năng | Must | PV02-1; PV03-9; BB-KH-01; Đề tài 5 | MT-05 |
| **FR-NOTI-001**   | Hệ thống PHẢI tự động gửi thông báo qua Email CTU và In-app khi: có gợi ý so khớp tin, lịch hẹn được xác nhận/nhắc trước 2 giờ, hoặc tài khoản bị cảnh báo khóa 48h. | Yêu cầu hệ thống – chức năng | Must | KS-01 Q17; BB-KH-02 | MT-01, MT-02 |

---

#### 3.2. Yêu cầu Phi chức năng (Non-Functional Requirements - `NFR-*`, đủ 8 thuộc tính chất lượng)
| Mã | Phát biểu yêu cầu phi chức năng (Đo lường & Kiểm chứng được) | Loại (Hình 1.3) | MoSCoW | Nguồn gốc cụ thể | Truy về MT |
|:---|:---|:---|:---:|:---|:---:|
| **NFR-PERF-001** | Thời gian phản hồi kết quả tìm kiếm và lọc danh sách đồ thất lạc PHẢI dưới 2,0 giây với tải đồng thời 500 người dùng. | Phi chức năng – Hiệu năng | Must | PV03-10; KS-01 Q7; Slide 28 | MT-01, MT-02 |
| **NFR-PERF-002** | Sau khi quét mã QR trên đồ vật hoặc phiếu hẹn, hệ thống PHẢI hiển thị thông tin đối soát trong vòng dưới 1,0 giây cho 99% lượt quét. | Phi chức năng – Hiệu năng | Must | PV03-4; MT-04; XĐ-01 | MT-04 |
| **NFR-PERF-003** | Toàn bộ quy trình tiếp nhận nhập kho hoặc quét mã giao trả trực tiếp tại bàn trực trạm PHẢI hoàn tất trong không quá 3 phút cho mỗi lượt giao dịch. | Phi chức năng – Hiệu năng | Must | PV03-4; MT-04; XĐ-01 | MT-04 |
| **NFR-SEC-001**  | Hệ thống PHẢI kiểm tra quyền hợp lệ ở phía máy chủ (Server-side RBAC) cho mọi API request; người dùng không xem được dữ liệu định danh của người khác khi chưa xác minh. | Phi chức năng – Bảo mật | Must | C-02; PV03-2; Slide 28 | MT-03 |
| **NFR-SEC-002**  | Ảnh chụp giấy tờ tùy thân (CCCD, Giấy phép lái xe, Thẻ SV) PHẢI được che mờ tự động hoặc kiểm duyệt che mờ trước khi hiển thị công khai trên giao diện tra cứu. | Phi chức năng – Bảo mật | Must | PV03-6; KH01-2; KS-01 Q14; XĐ-02 | MT-03 |
| **NFR-SEC-003**  | Phiên làm việc (Session) của sinh viên PHẢI tự động hết hạn sau 30 phút không hoạt động; phiên đăng nhập trên máy tính quầy trạm PHẢI tự khóa sau 10 phút không thao tác. | Phi chức năng – Bảo mật | Must | BB-KH-01; Chuẩn an toàn thông tin | MT-03 |
| **NFR-SEC-004**  | Mọi thao tác bàn giao đồ, xác minh sở hữu, giải tỏa tranh chấp, bàn giao ca PHẢI được ghi nhật ký bất biến (Audit Log) kèm timestamp, không sửa được qua giao diện. | Phi chức năng – Bảo mật | Must | PV02-3; BB-KH-01, BB-KH-02 | MT-03, MT-05 |
| **NFR-REL-001**  | Cơ sở dữ liệu PHẢI được sao lưu tự động hàng ngày lúc 02:00 sáng; khi xảy ra sự cố phần cứng, hệ thống PHẢI khôi phục được dữ liệu trong <= 4 giờ (RTO <= 4h, RPO <= 24h). | Phi chức năng – Độ tin cậy | Must | BB-KH-02; Chuẩn IT trường | MT-05 |
| **NFR-REL-002**  | Khi mất kết nối Internet tạm thời, ứng dụng tại trạm CÓ THỂ lưu trữ cục bộ tạm thời tối đa 20 lượt quét giao nhận ngoại tuyến và tự động đồng bộ khi có mạng trở lại. | Phi chức năng – Độ tin cậy | Could | PV03-11; BB-KH-01 | MT-04 |
| **NFR-AVA-001**  | Hệ thống PHẢI duy trì tính sẵn sàng hoạt động (Uptime) tối thiểu 99,5% thời gian trong khung giờ phục vụ của sinh viên (06:00 đến 23:00 hàng ngày). | Phi chức năng – Tính sẵn sàng | Must | BB-KH-02; Slide 28 | MT-01, MT-02 |
| **NFR-SCA-001**  | Kiến trúc hệ thống PHẢI đáp ứng khả năng mở rộng lưu trữ ít nhất 10.000 hồ sơ tài khoản sinh viên và 5.000 tin đăng đồ thất lạc mỗi học kỳ. | Phi chức năng – Khả năng mở rộng | Must | PV03-13; Tầm nhìn v1.0 | MT-01, MT-05 |
| **NFR-MAIN-001** | Các tham số quy định hệ thống (thời hạn 30/90 ngày, khung giờ hẹn, danh mục loại đồ) PHẢI cập nhật được qua giao diện Cán bộ CTSV mà không sửa mã nguồn, hiệu lực trong <= 1 phút. | Phi chức năng – Khả năng bảo trì | Must | PV02-1; BB-KH-01; XĐ-03 | MT-05 |
| **NFR-USA-001**  | Giao diện ứng dụng web PHẢI thiết kế Responsive hoàn chỉnh, hiển thị trực quan và thao tác không cần cuộn ngang trên màn hình điện thoại di động có chiều rộng từ 360 px trở lên. | Phi chức năng – Tính dễ sử dụng | Must | PV01-3; KS-01 Q5 (88% SV dùng smartphone); Đề tài 5 | MT-01, MT-02 |
| **NFR-COMP-001** | Hệ thống web PHẢI hoạt động chính xác và đồng nhất trên 2 phiên bản mới nhất của các trình duyệt phổ biến: Google Chrome, Microsoft Edge, Mozilla Firefox và Safari. | Phi chức năng – Tính tương thích | Must | C-03; Kiểm thử đa nền tảng | MT-01 |

---

### 4. Yêu cầu Hệ thống – Phần cứng (Hardware Requirements - `HW-*`, đủ 7 nhóm vật lý theo Slide 30)
| Mã | Phát biểu yêu cầu phần cứng vật lý | Loại (Hình 1.3) | MoSCoW | Nguồn gốc cụ thể | Truy về MT |
|:---|:---|:---|:---:|:---|:---:|
| **HW-SRV-01** | Máy chủ ứng dụng (Server): 01 Máy chủ ảo hóa (VM) tối thiểu 4 vCPU, 8 GB RAM, 100 GB SSD lưu trữ trên hạ tầng Trung tâm CNTT ĐH Cần Thơ. | Yêu cầu hệ thống – phần cứng | Must | Tầm nhìn 4.4; Slide 30 (Mục 1) | MT-01, MT-02 |
| **HW-CLI-01** | Thiết bị đầu cuối (Client Devices): Điện thoại thông minh chạy iOS/Android có camera >= 5MP hỗ trợ quét mã QR; máy tính để bàn/laptop tại bàn trực trạm (Nhà điều hành) chạy Windows 10/11, RAM >= 4GB. | Yêu cầu hệ thống – phần cứng | Must | Tầm nhìn 4.4; PV03-11; Đề tài 5; Slide 30 (Mục 2) | MT-04 |
| **HW-PWR-01** | Nguồn dự phòng (Power): Bàn trực trạm PHẢI trang bị bộ lưu điện dự phòng (UPS) duy trì tối thiểu 15–30 phút cho máy tính quầy và mạng để đảm bảo không đứt gãy giao dịch khi mất điện lưới. | Yêu cầu hệ thống – phần cứng | Should | Slide 30 (Mục 3); BB-KH-01 | MT-04 |
| **HW-STO-01** | Hệ thống lưu trữ (Storage Systems): Phân vùng lưu trữ đám mây / ổ cứng lưu trữ an toàn riêng biệt cho kho ảnh chụp hiện vật tiếp nhận và biên bản bàn giao số hóa, có sao lưu định kỳ. | Yêu cầu hệ thống – phần cứng | Must | Slide 30 (Mục 4); NFR-REL-001 | MT-03, MT-05 |
| **HW-NET-01** | Hạ tầng mạng (Network): Kết nối mạng Internet băng thông tối thiểu 10 Mbps (Wi-Fi trường hoặc mạng dây LAN) tại vị trí bàn trực trạm LostLink để đảm bảo quét mã QR thời gian thực. | Yêu cầu hệ thống – phần cứng | Must | Slide 30 (Mục 5); Tầm nhìn 4.4 | MT-04 |
| **HW-SEC-01** | Thiết bị an ninh (Security Equipment): Tủ lưu trữ hiện vật vật lý có khóa an toàn đặt tại Nhà điều hành; camera an ninh giám sát 24/7 khu vực bàn trực trạm phục vụ đối soát tranh chấp. | Yêu cầu hệ thống – phần cứng | Must | PV01-4; PV03-2; Slide 30 (Mục 6); XĐ-01 | MT-03 |
| **HW-SPEC-01**| Thiết bị chuyên dụng (Specialized): Máy in nhãn decal nhiệt mini (kết nối USB/Bluetooth) để in tức thời tem mã QR dán lên túi đựng hiện vật ngay khi tiếp nhận đồ vào trạm. | Yêu cầu hệ thống – phần cứng | Should | PV03-1; Slide 30 (Mục 7) | MT-04 |

---

### 5. Nhóm Ràng buộc (Constraints - `C-*`, đủ 6 nhóm theo Slide 31)
| Mã | Phát biểu ràng buộc thực hiện dự án | Loại (Hình 1.3) | MoSCoW | Nguồn gốc cụ thể | Truy về MT |
|:---|:---|:---|:---:|:---|:---:|
| **C-01** | Công nghệ bắt buộc: Bắt buộc tích hợp dịch vụ Single Sign-On (Google Workspace CTU) của trường; hệ thống tuyệt đối không tự quản lý hay lưu trữ mật khẩu người dùng. | Ràng buộc | Must | Tầm nhìn 4.3; PV02-5; Đề tài 5; Slide 31 (Mục 1) | MT-01, MT-03 |
| **C-02** | Pháp lý & Tiêu chuẩn ngành: Tuân thủ Nghị định 13/2023/NĐ-CP về Bảo vệ dữ liệu cá nhân; toàn bộ thông tin nhạy cảm (CCCD, mã số sinh viên, số điện thoại) phải được bảo mật và ẩn danh. | Ràng buộc | Must | Slide 31 (Mục 2); PV03-6; Đề tài 5 | MT-03 |
| **C-03** | Ngân sách & Tiến độ: Dự án thực hiện trong khuôn khổ đồ án môn học CT241 (học kỳ 1 năm học 2026–2027), hoàn thành toàn bộ tài liệu phân tích trước tuần 15; ngân sách tận dụng tài nguyên sẵn có. | Ràng buộc | Must | Tầm nhìn 4.3; Slide 31 (Mục 3) | — |
| **C-04** | Giới hạn hạ tầng: Triển khai vận hành trên nền tảng máy chủ và mạng do Trường ĐH Cần Thơ cấp phép; ứng dụng nền tảng Web App Responsive, không bắt buộc người dùng cài App từ chợ ứng dụng. | Ràng buộc | Must | Tầm nhìn 4.4; Đề tài 5; Slide 31 (Mục 4) | MT-01, MT-02 |
| **C-05** | Phạm vi địa lý & Tích hợp: Trong giai đoạn 1, hệ thống chỉ áp dụng cho tài sản thất lạc trong khuôn viên Khu II – Đại học Cần Thơ; đồ quá hạn bàn giao về Phòng CTSV xử lý ngoài hệ thống. | Ràng buộc | Must | Tầm nhìn 3.3; PV02-2; KH01-4; Slide 31 (Mục 5) | MT-05 |
| **C-06** | Quy trình & Chính sách nội bộ: Tuân thủ quy định quản lý tài sản và quy chế phối hợp giữa Ban quản lý Trạm LostLink (sinh viên tình nguyện) và Phòng Công tác Sinh viên (đơn vị chủ quản). | Ràng buộc | Must | Tầm nhìn 4.1; BB-KH-02; Slide 31 (Mục 6) | MT-03, MT-05 |

---

## NỘI DUNG CHI TIẾT SHEET 2: `XungDot` (XUNG ĐỘT YÊU CẦU & THƯƠNG LƯỢNG)

| Mã | Các bên liên quan | Nội dung xung đột (Chuẩn Đề tài 5) | Bằng chứng thực tế từ Thư mục 02 | Cách thức thương lượng & Đàm phán | Kết quả giải quyết (Yêu cầu dẫn xuất) |
|:---:|---|---|---|---|---|
| **XĐ-01** | **Bảo vệ / Nơi giữ đồ (Quản lý trạm) <br>↔<br> Sinh viên nhận đồ** | **Bảo vệ cần thủ tục giao nhận chặt, sinh viên muốn nhận nhanh:**<br>Nhân viên bảo vệ/Quản lý trạm chịu trách nhiệm vật chất nên muốn kiểm tra đối soát rất kỹ (đối chiếu Thẻ SV, ký biên bản giấy, ghi sổ sách thủ công, chụp ảnh) để tránh đền bù; trong khi sinh viên khi đến trạm lại đang vội đi học hoặc tan ca, muốn nhận lại đồ ngay tức thì, không muốn trải qua các thủ tục rườm rà, chờ đợi lâu. | - Đặc tả Đề tài 5 (Mục "Xung đột cần phân tích").<br>- Phỏng vấn PV03-4 (Trạm phàn nàn sinh viên hay giục giã, trong khi tìm đồ trong kho mất 5–10 phút).<br>- Khảo sát KS-01 Q18 (Sinh viên phản ánh thủ tục tại quầy bảo vệ mất 10–15 phút). | Nhóm phân tích thương lượng tại BB-KH-01 và BB-KH-02: Đưa ra giải pháp số hóa quy trình bằng công nghệ để đáp ứng đồng thời cả hai mục tiêu (chặt chẽ về bảo mật nhưng siêu tốc về thời gian):<br>1. Sinh viên phải **đặt lịch hẹn trực tuyến trước** qua ứng dụng, hệ thống cấp mã hẹn trước khi đến trạm.<br>2. Toàn bộ hiện vật được gán **mã QR định danh** dán ngoài túi lưu kho, nhân sự trạm chỉ cần dùng smartphone quét mã QR trong **< 1 giây** là định vị ngay ngăn tủ và thông tin phiếu hẹn.<br>3. Thay biên bản giấy bằng việc **quét thẻ SV và chụp ảnh số hóa biên nhận** nhanh chóng. | **Chốt phương án (Đồng thuận 100% tại BB-KH-01):**<br>- Rút ngắn thời gian xử lý một lượt giao nhận từ 10 phút xuống **dưới 3 phút** (`MT-04`, `NFR-PERF-003`).<br>- Bắt buộc đặt lịch hẹn trước theo khung giờ trực (`FR-APPT-001`, `UC-09`).<br>- Quét mã QR hiện vật tự động hiển thị thông tin đối soát trong < 1s (`FR-STATION-001`, `FR-RETURN-001`, `NFR-PERF-002`, `UC-11`). |
| **XĐ-02** | **Sinh viên Người nhặt đồ <br>↔<br> Sinh viên Người mất & Quản trị trạm** | **Công khai chi tiết để dễ tìm so với che chi tiết để xác minh:**<br>Người nhặt được đồ (đại diện PV-01 Dương Hoàng Huynh) muốn chụp ảnh rõ nét toàn bộ chi tiết món đồ và công khai số điện thoại cá nhân lên bài đăng để người mất nhìn thấy nhận ra ngay và gọi điện liên hệ lấy lại cho tiện.<br>Tuy nhiên, Người mất và Quản lý trạm lo ngại việc công khai ảnh rõ nét sẽ bị kẻ xấu nhìn thấy đặc điểm nhận dạng để **nhận vơ (nhận bừa)**; đồng thời việc lộ số điện thoại khiến người nhặt bị quấy rầy, lừa đảo hoặc tống tiền. | - Đặc tả Đề tài 5 (Mục "Xung đột cần phân tích").<br>- Phỏng vấn PV01-2 (Ý kiến sinh viên muốn đăng số ĐT).<br>- Phỏng vấn PV03-2 (Trạm cảnh báo kẻ xấu nhận bừa thẻ xe, ví tiền).<br>- Khảo sát KS-01:<br>+ **100%** lo ngại kẻ xấu nhận vơ khi công khai ảnh (Q14).<br>+ **93,5%** ủng hộ bắt buộc che mờ chi tiết cốt lõi.<br>+ **100%** muốn ẩn danh SĐT đến khi xác minh xong (Q16). | Nhóm phân tích đàm phán tại BB-KH-02 dựa trên số liệu khảo sát KS-01: Thuyết phục người nhặt hiểu nguy cơ lộ lọt thông tin cá nhân và rủi ro mất tài sản của nạn nhân.<br>Đưa ra giải pháp dung hòa bằng kỹ thuật:<br>1. Hệ thống cho phép đăng ảnh nhưng bắt buộc **che mờ các chi tiết định danh cốt lõi** (số seri máy, họ tên trên thẻ, hoa văn đặc biệt).<br>2. Người nhặt thiết lập **bộ câu hỏi xác minh ẩn danh** (chỉ người mất thật mới biết).<br>3. Thay vì gọi điện thoại trực tiếp, hai bên trao đổi qua **kênh tin nhắn ẩn danh in-app**. | **Chốt phương án (Đồng thuận tại BB-KH-02):**<br>- Bắt buộc làm mờ chi tiết nhạy cảm và ẩn số điện thoại trên bài đăng (`FR-POST-002`, `NFR-SEC-002`, `UC-03`).<br>- Người mất phải trả lời đúng câu hỏi xác minh mới được duyệt quyền nhận đồ (`FR-VERIFY-001`, `UC-07`).<br>- Cung cấp kênh trò chuyện ẩn danh nội bộ (`FR-CHAT-001`, `UC-06`). |
| **XĐ-03** | **Sinh viên Quản lý trạm <br>↔<br> Đại diện Phòng CTSV** | **Thời hạn lưu giữ đồ tại trạm & Giới hạn không gian kho tủ:**<br>Quản lý trạm muốn thời gian lưu giữ ngắn (15–30 ngày cho tất cả đồ vật) rồi thanh lý/tiêu hủy để giải phóng tủ kho vốn có diện tích hạn chế và giảm gánh nặng kiểm kê.<br>Ngược lại, Trưởng phòng CTSV yêu cầu đồ có giá trị (tiền, trang sức, laptop, CCCD, bằng lái) phải được lưu giữ dài ngày (ít nhất 90 ngày hoặc hết học kỳ) để đảm bảo quyền lợi pháp lý và tài sản cho sinh viên. | - Biên bản PV02-1, PV02-2 (Ý kiến Trưởng phòng CTSV).<br>- Biên bản PV03-3 (Ý kiến Quản lý trạm).<br>- Biên bản BB-KH-01 (Mục 1, KH01-1..4).<br>- Khảo sát KS-01 (90,3% SV quan tâm đồ có giá trị cần giữ lâu). | Nhóm phân tích đối chiếu năng lực tủ kho vật lý tại trạm và tham vấn quy định xử lý tài sản thất lạc: Đề xuất **phân nhóm đồ vật để áp dụng 2 mốc thời hạn khác nhau**.<br>Đồng thời quy định cơ chế bàn giao: Hết hạn tại trạm, hiện vật không bị tiêu hủy tùy tiện mà lập biên bản bàn giao số hóa chuyển về Phòng CTSV xử lý tiếp ngoài hệ thống, trạm hết trách nhiệm bảo quản. | **Chốt phương án (Đồng thuận 100% tại BB-KH-01):**<br>- Đồ thông thường: Lưu giữ tối đa **30 ngày**.<br>- Đồ có giá trị cao: Lưu giữ tối đa **90 ngày**.<br>- Chuyển giao đồ quá hạn về Phòng CTSV qua biên bản điện tử (`FR-OVERDUE-001`, `FR-OVERDUE-002`, `FR-CAT-001`, `UC-13`). |

---

## BẢNG TỔNG HỢP CHỈ SỐ TUÂN THỦ MOSCOW (DSDM / AGILE)

Theo hướng dẫn tại Slide 44–45:
- **Must have (Phải làm):** $\le 60\%$ tổng số nỗ lực.
- **Should have & Could have:** $\le 20\%$ nỗ lực còn lại.
- **Won't have (Chưa làm bản này):** Ghi nhận để kiểm soát Scope Creep.

| Nhóm MoSCoW | Số lượng yêu cầu | Tỷ lệ (%) | Đánh giá tuân thủ DSDM |
|:---|:---:|:---:|:---|
| **Must have** | 46 yêu cầu | **58,2%** | **ĐẠT CHUẨN DSDM** ($\le 60\%$) |
| **Should have** | 18 yêu cầu | **22,8%** | **ĐẠT CHUẨN** (Vùng đệm linh hoạt) |
| **Could have** | 9 yêu cầu | **11,4%** | **ĐẠT CHUẨN** (Dễ hoãn khi thiếu thời gian) |
| **Won't have (this time)** | 6 yêu cầu | **7,6%** | **ĐẠT CHUẨN** (Ngăn chặn Scope Creep) |
| **TỔNG CỘNG** | **79 yêu cầu** | **100%** | **Cân bằng hoàn hảo, khoa học và chặt chẽ** |
