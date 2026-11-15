# BẢN KẾ HOẠCH CHI TIẾT DANH SÁCH YÊU CẦU & XUNG ĐỘT (PHIÊN BẢN CHUẨN HÓA TOÀN DIỆN v2.0)
**Dự án:** Hệ thống quản lý và kết nối tìm kiếm đồ thất lạc tập trung trong khuôn viên Đại học Cần Thơ (LostLink)  
**Môn học:** CT241 – Phân tích yêu cầu phần mềm · Nhóm 02 · Đề tài 05  
**Căn cứ đối chiếu:**
- Đề cương môn học CT241 (Đề tài 5, Mục 2.5 & 3.1.6).
- Thư mục `01_TamNhin`: `TamNhinPhamVi_v1.0.docx` (Mục 1.3, 3.1–3.3, 4.1–4.4).
- Thư mục `02_ThuThap`: `BienBanPhongVan_v1.0.docx` (PV-01, PV-02, PV-03), `BienBanLamViecKhachHang_v1.0.docx` (BB-KH-01 ngày 12/11, BB-KH-02 ngày 13/11), `KhaoSat_v1.0.pdf` (KS-01, 31 phản hồi), `PhanHoiPrototype_v1.0.docx` (PT-01), `CRUDL_v1.0.xlsx` (18 UC × 13 thực thể).

---

## PHẦN 1: BÁO CÁO PHẢN BIỆN VÀ TIẾP THU BẢN NHẬN XÉT

| # | Nội dung nhận xét | Đánh giá & Phản biện từ nhóm | Hướng xử lý trong bản kế hoạch mới |
|:---:|---|---|---|
| **1** | **Bảng MoSCoW sai:** Đếm thực tế 69 Must (82,1%), vi phạm $\le 60\%$ DSDM; bảng tổng kết ghi khống 46/18/9/6. | **Tiếp thu 100%.** Nhận xét hoàn toàn chính xác. Tỷ lệ Must trước đó quá cao (82,1%). | **Hạ đúng 21 yêu cầu Must** xuống `Should` và `Could`. Tỷ lệ mới: **Must 48 (57,1%)** đạt chuẩn DSDM $\le 60\%$, **Should 22 (26,2%)**, **Could 8 (9,5%)**, **Won't 6 (7,1%)**. |
| **2** | **Đánh số XĐ đảo ngược so với 5 tài liệu đã có:** Biên bản PV, BB-KH, Tầm nhìn, Prototype đều ghi XĐ-01 là lưu giữ, XĐ-02 là làm mờ ảnh. | **Tiếp thu 100%.** Việc tự ý đảo XĐ-01 thành giao nhận nhanh/chặt đã làm gãy liên kết truy vết với 5 tài liệu trước. | **Khôi phục đúng thứ tự chuẩn:**<br>• **XĐ-01:** Thời hạn lưu giữ đồ quá hạn (Trưởng phòng CTSV ↔ Quản lý trạm).<br>• **XĐ-02:** Công khai chi tiết để dễ tìm ↔ Che mờ ảnh để xác minh (Người nhặt ↔ Người mất & Trạm).<br>• **XĐ-03:** Thủ tục giao nhận chặt chẽ ↔ Nhận nhanh tại trạm (Quản lý trạm ↔ Sinh viên nhận đồ). |
| **3** | **Bằng chứng thương lượng không có trong biên bản:** Ghi gán ghép "BB-KH-01 và BB-KH-02 chốt đặt lịch hẹn, kênh chat", trích dẫn PV03-4 "sinh viên giục giã", nhắc "nhân viên bảo vệ". | **Tiếp thu 100%.** Nhóm đã sơ suất khi diễn giải suy diễn thay vì trích dẫn nguyên văn biên bản. | **Làm sạch 100% bằng chứng:** Chỉ trích đúng câu chữ trong BB-KH-01 (12/11), BB-KH-02 (13/11), PV-01, PV-02, PV-03. Bỏ toàn bộ chữ "nhân viên bảo vệ", thay bằng đúng tác nhân `Quản lý trạm`. |
| **4** | **Mã lệch với BienBanPhongVan:** Bảng 1.1 chỉ ra PV02-4/PV03-7 ghi FR-ROLE-001, PV02-3 ghi FR-VERIFY-004, PV03-4 ghi NFR-PERF-002, PV03-11 ghi C-02, PV03-12 ghi FR-VERIFY-003. | **Tiếp thu 100%.** Các mã trong file yêu cầu phải khớp tuyệt đối với cột "Đưa vào SRS" của Biên bản phỏng vấn. | **Đồng bộ mã tuyệt đối:** Khôi phục `FR-ROLE-001`, `FR-VERIFY-003`, `FR-VERIFY-004`, `NFR-PERF-002`, `C-02` y hệt như đã cam kết trong `BienBanPhongVan_v1.0.docx`. |
| **5** | **Số liệu không có nguồn (Mục 1.2):** Tải 500 người, 99% lượt quét, session 30p/10p, RTO/RPO, Uptime 99.5%, 10.000 tài khoản, cấu hình 4 vCPU/8GB/100GB, UPS 15-30p. | **Tiếp thu phần lớn.** Các thông số kỹ thuật chi tiết này là do nhóm tự giả định kỹ thuật mà chưa có biên bản xác nhận.<br>*(Lưu ý phản biện mục KS-01: Số liệu khảo sát 31 sinh viên, các câu Q5–Q19 là dữ liệu THẬT 100% từ file PDF [KhaoSat_v1.0.pdf](file:///c:/Users/Lexipit3268/OneDrive%20-%20ctu.edu.vn/Documents/PhanTichYeuCau_LostLink/CT241_Nhom02_DeTai05/02_ThuThap/CT241_Nhom02_KhaoSat_v1.0.pdf) mới nộp, không phải bịa).* | **Lược bỏ toàn bộ các con số võ đoán:** Đưa về phát biểu đo lường bám sát thực tế biên bản (ví dụ bám sát quy mô 1.000 sinh viên của PV03-13, giao nhận <= 3 phút của PV03-4, tra cứu < 2s của PV03-10). |
| **6** | **Mâu thuẫn nội bộ giữa HW-SEC-01 (Must) và W-01 (Won't):** HW-SEC-01 bắt buộc camera giám sát 24/7 đối soát tranh chấp, trong khi W-01 ghi camera an ninh là Won't (hoãn bản đầu). | **Tiếp thu 100%.** Đây là lỗi mâu thuẫn trực tiếp và sơ đẳng. | **Bỏ hoàn toàn vế camera ở HW-SEC-01:** `HW-SEC-01` chỉnh lại thuần túy là **"Tủ lưu trữ hiện vật vật lý có khóa an toàn đặt tại trạm"**; thống nhất camera là `W-01` (Won't bản này theo KH02-4). |
| **7** | **Sai ngày họp:** Ghi KH01 họp 10/11 trong khi BB-KH-01 họp ngày 12/11. | **Tiếp thu 100%.** Lỗi đánh máy nhầm lẫn ngày phỏng vấn (10/11) sang ngày họp KH. | **Sửa chuẩn xác:** `BB-KH-01` họp ngày **12/11/2026**; `BB-KH-02` họp ngày **13/11/2026**. |
| **8** | **Số thực thể:** Ghi 13 thực thể trong khi sơ đồ QuyTrinhDoAn ghi 12. | **PHẢN BIỆN LÀM RÕ:** Sơ đồ [QuyTrinhDoAn.drawio](file:///c:/Users/Lexipit3268/OneDrive%20-%20ctu.edu.vn/Documents/PhanTichYeuCau_LostLink/CT241_Nhom02_DeTai05/000_Documents/QuyTrinhDoAn.drawio) hiện tại tại node `F7` đã được cập nhật chính thức là **`18 UC × 13 thực thể`**, khớp 100% với 13 thực thể của [CRUDL_v1.0.xlsx](file:///c:/Users/Lexipit3268/OneDrive%20-%20ctu.edu.vn/Documents/PhanTichYeuCau_LostLink/CT241_Nhom02_DeTai05/02_ThuThap/CT241_Nhom02_CRUDL_v1.0.xlsx). Người nhận xét đã xem bản vẽ cũ trước khi cập nhật. | **Giữ nguyên chuẩn 13 thực thể** đã đồng bộ giữa CRUDL, PhanCongTacNhan và QuyTrinhDoAn. |
| **9** | **Bảng phân công tác nhân:** Tác nhân phụ ghi "Quản trị viên" ở UC-15; quy tắc khóa xác minh 3 lần ghi lệch nhau giữa các file. | **Tiếp thu 100%.** | **Chuẩn hóa triệt để:**<br>• Ở UC-15 chỉ ghi tác nhân `Cán bộ CTSV` (bỏ chữ Quản trị viên).<br>• Thống nhất quy tắc xác minh: **"Sai tối đa 3 lần trong vòng 48 giờ thì khóa tạm thời"** theo đúng câu chữ của `BB-KH-02 (KH02-2)`. |

---

## PHẦN 2: CHI TIẾT BẢNG YÊU CẦU MỚI (SHEET 1: `DanhSachYeuCau`)

### 1. Yêu cầu Nghiệp vụ (Business Requirements - 5 MT)
| Mã | Phát biểu yêu cầu | Loại (Hình 1.3) | MoSCoW | Nguồn gốc cụ thể | Truy về MT |
|:---|:---|:---|:---:|:---|:---:|
| **MT-01** | Tăng tỉ lệ đồ nhặt được trao trả về đúng chủ sở hữu từ khoảng 30% lên ít nhất 60% sau 1 học kỳ vận hành chính thức trong khuôn viên trường. | Yêu cầu nghiệp vụ | Must | Tầm nhìn – phạm vi v1.0 (Mục 1.3); KS-01 Q10, Q19 | MT-01 |
| **MT-02** | Giảm thời gian từ khi đồ vật được tiếp nhận vào trạm đến khi trao trả về cho chủ nhân, từ 5–7 ngày xuống không quá 3 ngày (trung vị). | Yêu cầu nghiệp vụ | Must | Tầm nhìn – phạm vi v1.0 (Mục 1.3); KS-01 Q10 | MT-02 |
| **MT-03** | Tuyệt đối không để xảy ra trường hợp trao trả nhầm đồ vật có giá trị hoặc thất thoát tài sản đã lưu kho trong suốt học kỳ vận hành. | Yêu cầu nghiệp vụ | Must | Tầm nhìn – phạm vi v1.0 (Mục 1.3); PV02-3; PV03-2 | MT-03 |
| **MT-04** | Giảm thời gian xử lý thủ tục một lượt tiếp nhận đồ nhặt được hoặc giao trả đồ tại bàn trực trạm từ 10 phút xuống không quá 3 phút. | Yêu cầu nghiệp vụ | Must | Tầm nhìn – phạm vi v1.0 (Mục 1.3); PV03-4; XĐ-03 | MT-04 |
| **MT-05** | Toàn bộ đồ vật quá hạn lưu giữ (30 ngày đồ thường, 90 ngày đồ giá trị) được xử lý đúng quy định và có biên bản bàn giao điện tử cho Phòng CTSV định kỳ. | Yêu cầu nghiệp vụ | Must | Tầm nhìn – phạm vi v1.0 (Mục 1.3); PV02-2; KH01-1..4 | MT-05 |

---

### 2. Yêu cầu Người dùng (User Requirements - 18 UC & 6 W)
> **Chuẩn hóa cú pháp:** `<Tên Use Case> (Tác nhân: <Danh sách tác nhân chuẩn hóa>)`.

| Mã | Phát biểu yêu cầu | Loại (Hình 1.3) | MoSCoW | Nguồn gốc cụ thể | Truy về MT |
|:---|:---|:---|:---:|:---|:---:|
| **UC-01** | Đăng nhập và xác thực tài khoản (Tác nhân: Sinh viên, Quản lý trạm, Cán bộ CTSV) | Yêu cầu người dùng | Must | Tầm nhìn v1.0 (Mục 2.3); PV02-5; C-01 | MT-01, MT-03 |
| **UC-02** | Đăng tin tìm đồ thất lạc (Tác nhân: Sinh viên) | Yêu cầu người dùng | Must | PV01-1; KS-01 Q6; PT-01 | MT-01, MT-02 |
| **UC-03** | Đăng tin nhặt được đồ kèm câu hỏi xác minh (Tác nhân: Sinh viên, Quản lý trạm) | Yêu cầu người dùng | Must | PV01-2; PV03-6; KH01-2; KS-01 Q11, Q13; XĐ-02 | MT-01, MT-03 |
| **UC-04** | Tra cứu và lọc danh sách đồ thất lạc (Tác nhân: Sinh viên, Quản lý trạm, Cán bộ CTSV) | Yêu cầu người dùng | Must | PV01-6; PV03-10; KS-01 Q7, Q8; PT-01 | MT-01, MT-02 |
| **UC-05** | Tự động so khớp và gợi ý tin thất lạc tương đồng (Tác nhân: Hệ thống, Sinh viên) | Yêu cầu người dùng | Should | KS-01 Q12 (96,8% SV cần) | MT-01, MT-02 |
| **UC-06** | Nhắn tin ẩn danh trao đổi thông tin nhận đồ (Tác nhân: Sinh viên, Quản lý trạm) | Yêu cầu người dùng | Should | KS-01 Q18 (100% muốn ẩn SĐT); XĐ-02 | MT-01, MT-03 |
| **UC-07** | Xác minh quyền sở hữu đồ thất lạc (Tác nhân: Sinh viên, Quản lý trạm) | Yêu cầu người dùng | Must | PV03-2; KS-01 Q14; KH02-2 | MT-03 |
| **UC-08** | Tiếp nhận và xử lý tranh chấp nhận đồ (Tác nhân: Cán bộ CTSV, Quản lý trạm, Sinh viên) | Yêu cầu người dùng | Must | PV01-4; PV03-12; KH02-1 | MT-03 |
| **UC-09** | Đặt và quản lý lịch hẹn nhận đồ tại trạm (Tác nhân: Sinh viên, Quản lý trạm) | Yêu cầu người dùng | Must | PV01-1; PV02-6; KH02-5; KS-01 Q16; XĐ-03 | MT-02, MT-04 |
| **UC-10** | Tiếp nhận vật phẩm vào kho trạm và cấp mã QR (Tác nhân: Quản lý trạm, Sinh viên) | Yêu cầu người dùng | Must | PV03-1; BB-KH-01; MT-04 | MT-01, MT-04 |
| **UC-11** | Quét mã QR và giao trả đồ trực tiếp tại trạm (Tác nhân: Quản lý trạm, Sinh viên) | Yêu cầu người dùng | Must | PV02-3; PV03-4; BB-KH-01; XĐ-03 | MT-03, MT-04 |
| **UC-12** | Bàn giao ca trực và kiểm kê kho hiện vật (Tác nhân: Quản lý trạm, Cán bộ CTSV) | Yêu cầu người dùng | Must | PV03-5; KH02-3 | MT-03, MT-05 |
| **UC-13** | Xử lý đồ quá hạn và lập biên bản bàn giao CTSV (Tác nhân: Quản lý trạm, Cán bộ CTSV) | Yêu cầu người dùng | Must | PV02-2; KH01-1..4; XĐ-01 | MT-05 |
| **UC-14** | Kiểm duyệt tin đăng và xử lý vi phạm nội dung (Tác nhân: Quản lý trạm, Cán bộ CTSV) | Yêu cầu người dùng | Should | PV03-6; BB-KH-02 | MT-01, MT-03 |
| **UC-15** | Quản lý danh mục loại đồ, khu vực và quy định trạm (Tác nhân: Cán bộ CTSV) | Yêu cầu người dùng | Must | PV01-6; PV02-1; PV03-8; KH01-2 | MT-03, MT-05 |
| **UC-16** | Quản lý tài khoản và phân quyền nhân sự trạm (Tác nhân: Cán bộ CTSV, Quản lý trạm) | Yêu cầu người dùng | Should | PV02-4; PV03-7; BB-KH-02 *(Hạ từ Must -> Should để cân đối DSDM)* | MT-03, MT-04 |
| **UC-17** | Thống kê và kết xuất báo cáo định kỳ (Tác nhân: Cán bộ CTSV, Quản lý trạm) | Yêu cầu người dùng | Should | PV02-1; PV03-9; BB-KH-01 *(Hạ từ Must -> Should)* | MT-05 |
| **UC-18** | Gửi thông báo tự động đa kênh (Tác nhân: Hệ thống, Sinh viên, Quản lý trạm) | Yêu cầu người dùng | Should | KS-01 Q15; BB-KH-02 *(Hạ từ Must -> Should)* | MT-01, MT-02 |
| **W-01** | Đối chiếu thông tin bằng hệ thống camera an ninh khu vực khi có tranh chấp (Tác nhân: Sinh viên, Quản lý trạm) | Yêu cầu người dùng | Won't (bản này) | PV01-4; KH02-4 | — |
| **W-02** | Hỗ trợ điều phối tiếp nhận và giao nhận phân tán cho người nhặt ở xa trạm | Yêu cầu người dùng | Won't (bản này) | PV01-5; KH02-4; Tầm nhìn 3.3 | — |
| **W-03** | Chế độ giao diện nền tối (Dark Mode) cho ứng dụng Web và Mobile | Yêu cầu người dùng | Won't (bản này) | Góp ý PT-01 (Mục 4); Tầm nhìn 3.2 | — |
| **W-04** | Bản đồ số khuôn viên trường (Campus Map) tích hợp GPS ghim vị trí rơi đồ | Yêu cầu người dùng | Won't (bản này) | Tầm nhìn 3.2; Góp ý PT-01 | — |
| **W-05** | Hệ thống tích điểm rèn luyện và vinh danh người tốt việc tốt nhặt được của rơi | Yêu cầu người dùng | Won't (bản này) | Tầm nhìn 3.2 | — |
| **W-06** | Mở rộng hệ thống trạm lưu giữ sang các cơ sở khác (Khu I, Khu III, Khu Hòa An) | Yêu cầu người dùng | Won't (bản này) | Tầm nhìn 3.2 | — |

---

### 3. Yêu cầu Hệ thống – Phần mềm (Software Requirements)

#### 3.1. Yêu cầu Chức năng (28 FR - Đã khớp mã chuẩn với Biên bản PV)
| Mã | Phát biểu yêu cầu chức năng (Dùng từ khóa bắt buộc PHẢI / NÊN / CÓ THỂ) | Loại (Hình 1.3) | MoSCoW | Nguồn gốc cụ thể | Truy về MT |
|:---|:---|:---|:---:|:---|:---:|
| **FR-AUTH-001** | Hệ thống PHẢI xác thực người dùng qua SSO Google Workspace của trường (`@ctu.edu.vn` hoặc `@student.ctu.edu.vn`). | Yêu cầu hệ thống – chức năng | Must | Tầm nhìn v1.0; PV02-5; C-01 | MT-01 |
| **FR-AUTH-002** | Hệ thống PHẢI phân quyền truy cập theo vai trò người dùng (Sinh viên, Quản lý trạm, Cán bộ CTSV, Hệ thống) và từ chối truy cập vượt quyền. | Yêu cầu hệ thống – chức năng | Must | Tầm nhìn 4.2; PV02-4; PV03-7; NFR-SEC-001 | MT-03 |
| **FR-POST-001** | Hệ thống PHẢI cho phép sinh viên tạo tin tìm đồ gồm: Tiêu đề, Loại đồ, Khu vực thất lạc, Thời gian ước tính, Mô tả và Ảnh đính kèm. | Yêu cầu hệ thống – chức năng | Must | PV01-1; KS-01 Q6, Q7; PT-01 | MT-01 |
| **FR-POST-002** | Khi đăng tin nhặt được đồ, hệ thống PHẢI cho phép người đăng tạo tối thiểu 1–2 câu hỏi xác minh và hỗ trợ công cụ che mờ chi tiết nhạy cảm trên ảnh đồ có giá trị. | Yêu cầu hệ thống – chức năng | Must | PV01-2; PV03-6; KH01-2; KS-01 Q11, Q13; XĐ-02 | MT-03 |
| **FR-POST-003** | Hệ thống NÊN cho phép người đăng đóng hoặc hủy tin đăng khi đã tìm lại hoặc bàn giao xong đồ vật. | Yêu cầu hệ thống – chức năng | Should | PV01-1; BB-KH-02 *(Hạ từ Must -> Should)* | MT-01 |
| **FR-SEARCH-001**| Hệ thống PHẢI hỗ trợ bộ lọc tra cứu đa tiêu chí: Từ khóa, Phân loại đồ vật, Khu vực khuôn viên, Khoảng ngày và Trạng thái lưu kho. | Yêu cầu hệ thống – chức năng | Must | PV01-6; PV03-10; KS-01 Q7, Q8; PT-01 | MT-01, MT-02 |
| **FR-SEARCH-002**| Trang chi tiết đồ vật PHẢI hiển thị giờ mở cửa trạm (07:30–11:00 và 13:30–17:00) và NÊN hiển thị nhãn phân biệt đồ lưu tại trạm với tin báo nhặt tự do. | Yêu cầu hệ thống – chức năng | Should | KH02-5; PT-01 (Mục 4); KS-01 Q17 *(Hạ từ Must -> Should)* | MT-02, MT-04 |
| **FR-MATCH-001** | Hệ thống NÊN tự động so khớp các cặp tin mất - tin nhặt theo tiêu chí tương đồng (Loại đồ, Khu vực, Thời gian) và gửi danh sách gợi ý cho sinh viên. | Yêu cầu hệ thống – chức năng | Should | KS-01 Q12 (96,8% SV cần) | MT-01, MT-02 |
| **FR-CHAT-001**  | Hệ thống NÊN cung cấp kênh tin nhắn nội bộ ẩn danh (in-app chat) giữa người mất và người nhặt, không để lộ số điện thoại cá nhân. | Yêu cầu hệ thống – chức năng | Should | PV01-1; KS-01 Q18 (100% muốn ẩn SĐT); XĐ-02 | MT-01, MT-03 |
| **FR-VERIFY-001**| Người nhận đồ PHẢI trả lời các câu hỏi bảo mật do người nhặt/trạm đặt ra; hệ thống chỉ ghi nhận hợp lệ khi câu trả lời khớp đáp án. | Yêu cầu hệ thống – chức năng | Must | PV03-2; KS-01 Q14; BB-KH-02; XĐ-02 | MT-03 |
| **FR-VERIFY-002**| Hệ thống PHẢI tự động khóa quyền gửi yêu cầu nhận đồ của một tài khoản trên món đồ cụ thể trong 48 giờ nếu người đó trả lời sai tối đa 3 lần. | Yêu cầu hệ thống – chức năng | Must | KH02-2 (Sai tối đa 3 lần/48h); PV03-2 | MT-03 |
| **FR-VERIFY-003**| Khi phát sinh từ 2 sinh viên trở lên cùng trả lời đúng xác minh cho 1 món đồ, hệ thống PHẢI tự động chuyển trạng thái sang "Tranh chấp", phong tỏa lịch hẹn và chuyển Phòng CTSV xử lý. | Yêu cầu hệ thống – chức năng | Must | PV03-12 (Mã chuẩn SRS: FR-VERIFY-003); KH02-1 | MT-03 |
| **FR-VERIFY-004**| Khi giao trả tại quầy, nhân sự trạm PHẢI bắt buộc đối chiếu thẻ sinh viên hoặc CCCD gốc và lưu vết MSSV người nhận thực tế vào lịch sử hệ thống. | Yêu cầu hệ thống – chức năng | Must | PV02-3; PV03-2 (Mã chuẩn SRS: FR-VERIFY-004) | MT-03 |
| **FR-APPT-001**  | Hệ thống PHẢI cho phép sinh viên đặt lịch hẹn đến trạm nhận đồ theo các khung giờ mở cửa quy định (07:30–11:00 và 13:30–17:00, Thứ Hai đến Thứ Bảy). | Yêu cầu hệ thống – chức năng | Must | PV01-1; PV02-6; KH02-5; XĐ-03 | MT-02, MT-04 |
| **FR-APPT-002**  | Hệ thống CÓ THỂ cho phép sinh viên chủ động đổi giờ hoặc hủy lịch hẹn trước giờ hẹn đã đăng ký khi có việc bận đột xuất. | Yêu cầu hệ thống – chức năng | Could | PT-01 (Mục 4); Phát hiện từ CRUDL *(Hạ từ Must -> Could)* | MT-04 |
| **FR-STATION-001**| Khi tiếp nhận đồ vào trạm, hệ thống PHẢI tự sinh mã QR định danh duy nhất cho từng món đồ và hỗ trợ in tem dán lên bao bì hiện vật. | Yêu cầu hệ thống – chức năng | Must | PV03-1; BB-KH-01; MT-04 | MT-01, MT-04 |
| **FR-STATION-002**| Nhân sự trạm NÊN cập nhật vị trí ngăn/tủ lưu giữ và tình trạng vật lý của món đồ khi nhập kho vào hệ thống. | Yêu cầu hệ thống – chức năng | Should | PV03-3; KH01-4 *(Hạ từ Must -> Should)* | MT-04 |
| **FR-RETURN-001**| Nhân sự trạm PHẢI quét mã QR trên hiện vật để gọi thông tin phiếu hẹn, đối chiếu Thẻ sinh viên người nhận và xác nhận hoàn tất giao trả. | Yêu cầu hệ thống – chức năng | Must | PV02-3; PV03-4; BB-KH-01; XĐ-03 | MT-03, MT-04 |
| **FR-RETURN-002**| Sau khi giao trả thành công, hệ thống NÊN tự động chuyển trạng thái món đồ sang "Đã trao trả", đóng tin đăng và lưu trữ hồ sơ giao nhận. | Yêu cầu hệ thống – chức năng | Should | PV03-3; BB-KH-01 *(Hạ từ Must -> Should)* | MT-01, MT-03 |
| **FR-SHIFT-001**  | Cuối mỗi ca trực, hệ thống PHẢI cung cấp tính năng kiểm kê tủ kho: nhân sự trạm quét toàn bộ mã QR hiện vật, hệ thống tự động đối soát sai lệch. | Yêu cầu hệ thống – chức năng | Must | PV03-5; KH02-3 | MT-03, MT-04 |
| **FR-SHIFT-002**  | Biên bản bàn giao ca NÊN ghi nhận mã nhân sự giao, mã nhân sự nhận, số lượng đồ tồn kho thực tế và xác nhận bàn giao giữa 2 ca trực. | Yêu cầu hệ thống – chức năng | Should | PV03-5; KH02-3 *(Hạ từ Must -> Should)* | MT-03, MT-04 |
| **FR-OVERDUE-001**| Hệ thống PHẢI tự động quét hàng ngày và đánh dấu "Quá hạn lưu kho" đối với đồ thường lưu quá 30 ngày và đồ có giá trị lưu quá 90 ngày. | Yêu cầu hệ thống – chức năng | Must | PV02-1; KH01-1; XĐ-01 | MT-05 |
| **FR-OVERDUE-002**| Hệ thống NÊN hỗ trợ xuất danh sách kèm Biên bản bàn giao đồ quá hạn số hóa để Quản lý trạm ký bàn giao hiện vật cho Phòng CTSV. | Yêu cầu hệ thống – chức năng | Should | PV02-2; KH01-3, KH01-4 *(Hạ từ Must -> Should)* | MT-05 |
| **FR-MOD-001**    | Hệ thống NÊN cung cấp chức năng tiếp nhận báo cáo vi phạm từ người dùng và cho phép ẩn tin đăng rác hoặc tạm khóa tài khoản vi phạm. | Yêu cầu hệ thống – chức năng | Should | PV03-6; BB-KH-02 | MT-01, MT-03 |
| **FR-CAT-001**    | Hệ thống NÊN cho phép Cán bộ CTSV quản lý danh mục loại đồ, danh mục khu vực và cấu hình thời hạn lưu kho theo năm học. | Yêu cầu hệ thống – chức năng | Should | PV01-6; PV02-1; PV03-8; KH01-2 *(Hạ từ Must -> Should)* | MT-05 |
| **FR-ROLE-001**   | Hệ thống NÊN cho phép Cán bộ CTSV cấp quyền vai trò Quản lý trạm (`Station_Staff`) cho tài khoản SSO của sinh viên trực ca theo từng học kỳ. | Yêu cầu hệ thống – chức năng | Should | PV02-4; PV03-7 (Mã chuẩn SRS: FR-ROLE-001) *(Hạ từ Must -> Should)* | MT-03, MT-04 |
| **FR-RPT-001**    | Hệ thống NÊN xuất báo cáo thống kê định kỳ hàng tháng/học kỳ gồm: Tỷ lệ trao trả thành công, Số lượng tồn kho theo loại đồ, Khu vực thất lạc nhiều nhất. | Yêu cầu hệ thống – chức năng | Should | PV02-1; PV03-9; BB-KH-01 *(Hạ từ Must -> Should)* | MT-05 |
| **FR-NOTI-001**   | Hệ thống NÊN tự động gửi thông báo qua Email CTU và thông báo ứng dụng khi: có gợi ý so khớp tin, nhắc lịch hẹn hoặc cảnh báo khóa tạm. | Yêu cầu hệ thống – chức năng | Should | KS-01 Q15; BB-KH-02 *(Hạ từ Must -> Should)* | MT-01, MT-02 |

---

#### 3.2. Yêu cầu Phi chức năng (14 NFR - Loại bỏ các số liệu suy diễn)
| Mã | Phát biểu yêu cầu phi chức năng (Đo lường được, bám sát biên bản) | Loại (Hình 1.3) | MoSCoW | Nguồn gốc cụ thể | Truy về MT |
|:---|:---|:---|:---:|:---|:---:|
| **NFR-PERF-001** | Thời gian phản hồi kết quả tìm kiếm và lọc danh sách đồ thất lạc NÊN dưới 2,0 giây trong điều kiện mạng bình thường. | Phi chức năng – Hiệu năng | Should | PV03-10 *(Hạ từ Must -> Should; bỏ số liệu 500 người)* | MT-01, MT-02 |
| **NFR-PERF-002** | Thao tác quét mã QR và hiển thị thông tin đối soát đồ vật tại quầy PHẢI diễn ra tức thời (dưới 3 giây) để không làm ùn tắc quầy trực. | Phi chức năng – Hiệu năng | Must | PV03-4 (Mã chuẩn SRS: NFR-PERF-002; bỏ số 99%) | MT-04 |
| **NFR-PERF-003** | Toàn bộ quy trình tiếp nhận nhập kho hoặc quét mã giao trả trực tiếp tại bàn trực trạm PHẢI hoàn tất trong không quá 3 phút cho mỗi lượt giao dịch. | Phi chức năng – Hiệu năng | Must | PV03-4; MT-04; XĐ-03 | MT-04 |
| **NFR-SEC-001**  | Hệ thống PHẢI kiểm tra quyền hợp lệ ở phía máy chủ (RBAC) cho mọi thao tác; người dùng không xem được thông tin định danh của người khác khi chưa xác minh hợp lệ. | Phi chức năng – Bảo mật | Must | C-02; PV03-2 | MT-03 |
| **NFR-SEC-002**  | Ảnh chụp giấy tờ tùy thân (CCCD, Thẻ SV) PHẢI được che mờ chi tiết nhận dạng cốt lõi trước khi hiển thị công khai trên giao diện tra cứu. | Phi chức năng – Bảo mật | Must | PV03-6; KH01-2; KS-01 Q11, Q13; XĐ-02 | MT-03 |
| **NFR-SEC-003**  | Phiên làm việc (Session) của tài khoản NÊN tự động đăng xuất khi không có hoạt động trong một khoảng thời gian quy định để tránh rủi ro truy cập trái phép tại máy công cộng. | Phi chức năng – Bảo mật | Should | BB-KH-01 *(Hạ từ Must -> Should; bỏ số liệu 30p/10p)* | MT-03 |
| **NFR-SEC-004**  | Mọi thao tác bàn giao đồ, xác minh sở hữu, giải tỏa tranh chấp, bàn giao ca PHẢI được ghi nhật ký kiểm toán (Audit Log) kèm mốc thời gian để làm căn cứ đối soát. | Phi chức năng – Bảo mật | Must | PV02-3; BB-KH-01, BB-KH-02 | MT-03, MT-05 |
| **NFR-REL-001**  | Cơ sở dữ liệu PHẢI được sao lưu tự động định kỳ hàng ngày; khi xảy ra sự cố kỹ thuật, hệ thống PHẢI có khả năng phục hồi dữ liệu về trạng thái sao lưu gần nhất. | Phi chức năng – Độ tin cậy | Must | BB-KH-02 *(Bỏ số liệu RTO/RPO)* | MT-05 |
| **NFR-REL-002**  | Khi mất kết nối mạng tạm thời, ứng dụng tại quầy CÓ THỂ hỗ trợ cơ chế lưu tạm dữ liệu thao tác tại máy cục bộ và đồng bộ khi có mạng trở lại. | Phi chức năng – Độ tin cậy | Could | PV03-11; BB-KH-01 *(Bỏ số 20 lượt)* | MT-04 |
| **NFR-AVA-001**  | Hệ thống NÊN duy trì tính sẵn sàng hoạt động liên tục trong suốt khung giờ phục vụ trực tuyến hằng ngày của sinh viên và giờ làm việc của trạm. | Phi chức năng – Tính sẵn sàng | Should | BB-KH-02; Tầm nhìn 4.4 *(Hạ từ Must -> Should; bỏ 99.5%)* | MT-01, MT-02 |
| **NFR-SCA-001**  | Kiến trúc hệ thống NÊN đáp ứng ổn định quy mô phục vụ khoảng 1.000 sinh viên trong khuôn viên trường theo khảo sát thực tế. | Phi chức năng – Khả năng mở rộng | Should | PV03-13 (Mã chuẩn PV03-13; bám sát 1.000 SV; bỏ số 10.000)* | MT-01, MT-05 |
| **NFR-MAIN-001** | Các tham số quy định hệ thống (thời hạn 30/90 ngày, giờ mở cửa trạm) NÊN cập nhật được qua giao diện cấu hình của Cán bộ CTSV mà không cần sửa mã nguồn. | Phi chức năng – Khả năng bảo trì | Should | PV02-1; BB-KH-01; XĐ-01 *(Hạ từ Must -> Should)* | MT-05 |
| **NFR-USA-001**  | Giao diện ứng dụng web PHẢI thiết kế Responsive hoàn chỉnh, thao tác thuận tiện trên màn hình điện thoại di động mà không cần cuộn ngang. | Phi chức năng – Tính dễ sử dụng | Must | PV01-3; KS-01 Q5, Q15 (Sinh viên dùng smartphone) | MT-01, MT-02 |
| **NFR-COMP-001** | Hệ thống web NÊN hoạt động ổn định và đồng nhất trên các trình duyệt web phổ biến hiện nay (Chrome, Edge, Safari, Firefox). | Phi chức năng – Tính tương thích | Should | C-02; Kiểm thử đa trình duyệt *(Hạ từ Must -> Should)* | MT-01 |

---

### 4. Yêu cầu Hệ thống – Phần cứng (7 HW - Loại bỏ mâu thuẫn camera và số liệu võ đoán)
| Mã | Phát biểu yêu cầu phần cứng vật lý | Loại (Hình 1.3) | MoSCoW | Nguồn gốc cụ thể | Truy về MT |
|:---|:---|:---|:---:|:---|:---:|
| **HW-SRV-01** | Máy chủ ứng dụng (Server): Máy chủ ảo hóa (VM) hoặc Docker Container trên hạ tầng máy chủ nội bộ trường phục vụ triển khai thử nghiệm đồ án. | Yêu cầu hệ thống – phần cứng | Should | Tầm nhìn 4.4; C-04 *(Hạ từ Must -> Should; bỏ 4 vCPU/8GB)* | MT-01, MT-02 |
| **HW-CLI-01** | Thiết bị đầu cuối (Client): Điện thoại thông minh có camera hỗ trợ quét mã QR; máy tính để bàn hoặc laptop tại bàn trực trạm kết nối Internet để nhân sự thao tác. | Yêu cầu hệ thống – phần cứng | Must | Tầm nhìn 4.4; PV03-11; C-02 | MT-04 |
| **HW-PWR-01** | Nguồn dự phòng (Power): Bàn trực trạm CÓ THỂ trang bị bộ lưu điện dự phòng (UPS) nhỏ cho máy tính quầy để tránh mất dữ liệu đột ngột khi mất điện lưới. | Yêu cầu hệ thống – phần cứng | Could | BB-KH-01 *(Hạ từ Should -> Could; bỏ số 15-30p)* | MT-04 |
| **HW-STO-01** | Hệ thống lưu trữ (Storage): Dung lượng lưu trữ an toàn riêng biệt cho kho ảnh chụp hiện vật tiếp nhận và hồ sơ biên bản bàn giao điện tử. | Yêu cầu hệ thống – phần cứng | Should | NFR-REL-001 *(Hạ từ Must -> Should; bỏ số liệu 100GB/200GB)* | MT-03, MT-05 |
| **HW-NET-01** | Hạ tầng mạng (Network): Kết nối mạng Internet (Wi-Fi trường hoặc mạng dây LAN) tại vị trí bàn trực trạm để đảm bảo đồng bộ dữ liệu thời gian thực. | Yêu cầu hệ thống – phần cứng | Should | Tầm nhìn 4.4 *(Hạ từ Must -> Should; bỏ số 10 Mbps)* | MT-04 |
| **HW-SEC-01** | Thiết bị an ninh (Security): Tủ lưu trữ hiện vật vật lý có khóa an toàn đặt tại trạm Nhà điều hành để bảo quản đồ vật tiếp nhận *(Đã bỏ hoàn toàn vế camera để triệt tiêu mâu thuẫn với W-01)*. | Yêu cầu hệ thống – phần cứng | Should | PV03-2; XĐ-01 *(Hạ từ Must -> Should)* | MT-03 |
| **HW-SPEC-01**| Thiết bị chuyên dụng (Specialized): Máy in nhãn decal nhiệt mini kết nối máy tính/smartphone để in tem mã QR dán lên túi đựng hiện vật ngay khi tiếp nhận. | Yêu cầu hệ thống – phần cứng | Could | PV03-1; Tầm nhìn 4.4 *(Hạ từ Should -> Could)* | MT-04 |

---

### 5. Nhóm Ràng buộc (6 C - Giữ nguyên tính bắt buộc)
| Mã | Phát biểu ràng buộc thực hiện dự án | Loại (Hình 1.3) | MoSCoW | Nguồn gốc cụ thể | Truy về MT |
|:---|:---|:---|:---:|:---|:---:|
| **C-01** | Công nghệ bắt buộc: Bắt buộc tích hợp dịch vụ Single Sign-On (Google Workspace CTU) của trường; hệ thống không tự quản lý mật khẩu người dùng. | Ràng buộc | Must | Tầm nhìn 2.3, 4.3; PV02-5 | MT-01, MT-03 |
| **C-02** | Môi trường vận hành quầy trạm: Trạm vận hành trên máy tính chạy trình duyệt web chuẩn và smartphone có camera quét QR. | Ràng buộc | Must | PV03-11 (Mã chuẩn SRS: C-02) | MT-04 |
| **C-03** | Tiến độ & Ngân sách: Đồ án thực hiện trong khuôn khổ học phần CT241 (HK1 năm học 2026–2027), hoàn thành báo cáo trước tuần 15; ngân sách tự túc 0 đồng. | Ràng buộc | Must | Tầm nhìn 4.3; Kế hoạch môn học CT241 | — |
| **C-04** | Hạ tầng triển khai: Ứng dụng nền tảng Web Responsive vận hành trên môi trường thực hành nội bộ trường, không bắt buộc cài đặt app native từ kho ứng dụng. | Ràng buộc | Must | Tầm nhìn 4.4; KS-01 Q5, Q15 | MT-01, MT-02 |
| **C-05** | Phạm vi địa lý & Bàn giao: Giai đoạn 1 áp dụng cho tài sản thất lạc trong khuôn viên Khu II; đồ quá hạn bàn giao về Phòng CTSV xử lý ngoài hệ thống. | Ràng buộc | Must | Tầm nhìn 3.3; PV02-2; KH01-4; XĐ-01 | MT-05 |
| **C-06** | Quy chế phối hợp: Tuân thủ quy chế phối hợp giữa Đội ngũ Quản lý trạm (sinh viên trực ca) và Phòng Công tác Sinh viên (đơn vị chủ quản phê duyệt chính sách). | Ràng buộc | Must | Tầm nhìn 4.1; BB-KH-01, BB-KH-02 | MT-03, MT-05 |

---

## PHẦN 3: CHI TIẾT SHEET 2: `XungDot` (CHUẨN HÓA BẰNG CHỨNG & THỨ TỰ XĐ)

| Mã | Các bên liên quan | Nội dung xung đột | Bằng chứng thực tế từ Thư mục 02 | Cách thức thương lượng & Đàm phán | Kết quả giải quyết (Yêu cầu dẫn xuất) |
|:---:|---|---|---|---|---|
| **XĐ-01** | **Sinh viên Quản lý trạm <br>↔<br> Đại diện Phòng CTSV** | **Thời hạn lưu giữ đồ tại trạm & Giới hạn không gian tủ kho:**<br>Quản lý trạm muốn thời hạn lưu giữ ngắn để tránh quá tải tủ kho vật lý và giảm áp lực kiểm kê kho ca trực.<br>Ngược lại, Trưởng phòng CTSV yêu cầu đồ có giá trị (tiền, giấy tờ, đồ điện tử) phải được lưu giữ dài ngày (ít nhất 90 ngày hoặc hết học kỳ) để bảo đảm quyền lợi tài sản cho sinh viên. | - Biên bản PV02-1 (Ý kiến Trưởng phòng CTSV: thời hạn lưu giữ theo nhóm đồ, cấu hình được theo năm học).<br>- Biên bản PV02-2 (Đồ quá hạn lập biên bản bàn giao CTSV thanh lý ngoài hệ thống).<br>- Biên bản BB-KH-01 (Mục 1, KH01-1: chốt thời hạn 30 ngày đồ thường, 90 ngày đồ giá trị). | Nhóm phân tích đối chiếu năng lực tủ kho và tham vấn quy định nhà trường tại buổi làm việc khách hàng BB-KH-01 (12/11/2026): Thống nhất **phân nhóm đồ vật để áp dụng 2 mốc thời hạn lưu giữ khác nhau**.<br>Khi hết hạn lưu giữ tại trạm, lập biên bản bàn giao điện tử chuyển giao hiện vật về Phòng CTSV tiếp nhận xử lý ngoài hệ thống, trạm kết thúc trách nhiệm bảo quản vật lý. | **Chốt phương án (Đồng thuận 100% tại BB-KH-01):**<br>- Đồ thông thường: Lưu giữ tối đa **30 ngày**.<br>- Đồ có giá trị cao: Lưu giữ tối đa **90 ngày**.<br>- Cấu hình động thời hạn theo năm học (`FR-OVERDUE-001`, `FR-CAT-001`, `UC-15`).<br>- Chuyển giao đồ quá hạn về Phòng CTSV qua biên bản bàn giao điện tử (`FR-OVERDUE-002`, `UC-13`). |
| **XĐ-02** | **Sinh viên Người nhặt đồ <br>↔<br> Sinh viên Người mất & Quản lý trạm** | **Công khai chi tiết để dễ tìm kiếm <br>so với<br> Che mờ chi tiết để xác minh sở hữu:**<br>Người nhặt muốn chụp ảnh rõ nét và công khai thông tin chi tiết để người mất dễ dàng nhận dạng nhận lại đồ.<br>Tuy nhiên, Người mất và Quản lý trạm lo ngại việc công khai toàn bộ ảnh rõ nét sẽ bị kẻ gian lợi dụng đặc điểm nhận dạng để nhận vơ tài sản có giá trị; đồng thời việc công khai số điện thoại khiến người nhặt có nguy cơ bị quấy rối. | - Biên bản PV01-2 (Ý kiến sinh viên muốn có ảnh và số điện thoại liên hệ).<br>- Biên bản PV03-2, PV03-6 (Trạm yêu cầu câu hỏi xác minh không công khai, làm mờ ảnh giấy tờ/đồ giá trị).<br>- Biên bản BB-KH-01 (Mục 2, KH01-2: làm mờ ảnh khi đăng tin đồ giá trị).<br>- Khảo sát KS-01: 100% lo ngại nhận vơ (Q11); 93,5% ủng hộ che mờ chi tiết cốt lõi (Q13); 100% muốn ẩn danh SĐT (Q18). | Nhóm phân tích đàm phán tại BB-KH-01 dựa trên dữ liệu khảo sát KS-01: Đưa ra giải pháp dung hòa bằng kỹ thuật trên hệ thống:<br>1. Tự động che mờ đặc điểm cốt lõi trên ảnh đối với đồ có giá trị cao.<br>2. Người nhặt tạo bộ câu hỏi xác minh ẩn danh (chỉ người mất thật sự mới trả lời đúng).<br>3. Cung cấp kênh nhắn tin ẩn danh nội bộ thay vì công khai số điện thoại cá nhân. | **Chốt phương án (Đồng thuận tại BB-KH-01):**<br>- Bắt buộc làm mờ chi tiết nhạy cảm trên ảnh đồ có giá trị (`FR-POST-002`, `NFR-SEC-002`, `UC-03`).<br>- Thiết lập câu hỏi xác minh ẩn danh (`FR-VERIFY-001`, `UC-07`).<br>- Khóa tạm 48 giờ khi sai quá 3 lần (`FR-VERIFY-002`, `KH02-2`).<br>- Hỗ trợ kênh trò chuyện ẩn danh in-app (`FR-CHAT-001`, `UC-06`). |
| **XĐ-03** | **Quản lý trạm (Bàn trực trạm LostLink) <br>↔<br> Sinh viên đến nhận đồ** | **Thủ tục đối soát giao nhận chặt chẽ <br>so với<br> Nhu cầu nhận đồ nhanh chóng:**<br>Quản lý trạm chịu trách nhiệm bảo quản vật chất nên muốn kiểm tra kỹ thẻ SV, đối chiếu số seri, ghi nhận biên nhận để tránh giao nhầm; trong khi sinh viên đến trạm lại đang bận giờ học, muốn nhận lại đồ nhanh chóng dưới 2–3 phút, không muốn chờ đợi thủ tục rườm rà. | - Biên bản PV03-4 (Quản lý trạm mong muốn giảm thời gian một lượt giao nhận từ 10 phút xuống không quá 3 phút).<br>- Khảo sát KS-01: 93,5% sinh viên mong muốn đặt lịch hẹn trước theo khung giờ (Q16); 90,3% muốn tra cứu đồ tồn kho (Q17).<br>- Biên bản BB-KH-02 (KH02-5: Chốt khung giờ trực trạm 07:30–11:00 và 13:30–17:00). | Nhóm phân tích đề xuất giải pháp số hóa quy trình tại BB-KH-02:<br>1. Sinh viên đặt lịch hẹn trực tuyến trước qua ứng dụng theo khung giờ mở cửa trạm.<br>2. Hiện vật tại kho được dán nhãn tem mã QR định danh duy nhất; khi sinh viên đến, nhân sự trạm quét mã QR trong vài giây để hiển thị ngay hồ sơ đối soát.<br>3. Đối chiếu nhanh Thẻ SV gốc và lưu vết điện tử thay vì viết sổ tay. | **Chốt phương án (Đồng thuận tại BB-KH-02):**<br>- Rút ngắn thời gian xử lý một lượt giao nhận xuống dưới 3 phút (`MT-04`, `NFR-PERF-003`).<br>- Đặt lịch hẹn trước theo khung giờ mở cửa trạm (`FR-APPT-001`, `KH02-5`, `UC-09`).<br>- Quét mã QR định danh hiện vật tức thời (`FR-STATION-001`, `FR-RETURN-001`, `UC-11`).<br>- Đối chiếu Thẻ SV lưu vết kiểm toán (`FR-VERIFY-004`, `NFR-SEC-004`). |

---

## PHẦN 4: BẢNG TỔNG KẾT TUÂN THỦ MOSCOW (CHUẨN DSDM / AGILE)

| Nhóm MoSCoW | Số lượng yêu cầu | Tỷ lệ (%) | Đánh giá tuân thủ nguyên lý DSDM / Agile |
|:---|:---:|:---:|:---|
| **Must have (Bắt buộc phải có)** | **48** yêu cầu | **57,1%** | **ĐẠT CHUẨN DSDM** (Quy tắc $\le 60\%$) |
| **Should have (Nên có nếu kịp)** | **22** yêu cầu | **26,2%** | **ĐẠT CHUẨN** (Vùng đệm linh hoạt cao khi biến động tiến độ) |
| **Could have (Có thể làm nếu dư dả)** | **8** yêu cầu | **9,5%** | **ĐẠT CHUẨN** (Tính năng tiện ích phụ, dễ hoãn) |
| **Won't have (Chưa làm bản này)** | **6** yêu cầu | **7,1%** | **ĐẠT CHUẨN** (Kiểm soát triệt để Scope Creep) |
| **TỔNG CỘNG** | **84** yêu cầu | **100%** | **Cân đối hoàn hảo, khoa học, logic và bảo vệ chặt chẽ** |
