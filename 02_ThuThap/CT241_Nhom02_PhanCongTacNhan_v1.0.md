# BẢNG PHÂN CÔNG TÁC NHÂN THEO USE CASE (ACTOR - USE CASE MATRIX)
**Dự án:** Hệ thống quản lý và kết nối tìm kiếm đồ thất lạc tập trung trong khuôn viên Đại học Cần Thơ (LostLink)  
**Môn học:** CT241 – Phân tích yêu cầu phần mềm (Học kỳ 1, Năm học 2026–2027)  
**Đơn vị:** Khoa Công nghệ Thông tin & Truyền thông – Đại học Cần Thơ  
**Nhóm thực hiện:** Nhóm 02 · Đề tài 05  
**Phiên bản:** v1.0 · **Ngày cập nhật:** 14/11/2026  
**Tài liệu tham chiếu:** `CT241_Nhom02_CRUDL_v1.0.xlsx`, `CT241_Nhom02_TamNhinPhamVi_v1.0.docx`, `CT241_Nhom02_BienBanLamViecKhachHang_v1.0.docx`

---

## 1. Danh mục chuẩn hóa các Tác nhân (System Actors)

Để khắc phục tình trạng danh xưng tác nhân không nhất quán giữa các tài liệu, hệ thống LostLink chuẩn hóa duy nhất **4 tác nhân** với định nghĩa, trách nhiệm và quyền hạn rõ ràng như sau:

| Tác nhân (Actor) | Bản chất | Định nghĩa & Trách nhiệm trong LostLink | Phạm vi tài khoản / Xác thực |
|---|---|---|---|
| **Sinh viên** | Con người (*Human Actor*) | Người dùng phổ thông trong khuôn viên trường (bao gồm cả sinh viên, học viên, giảng viên, viên chức nhà trường đóng vai trò người mất đồ hoặc người nhặt được đồ). Đăng tin, tra cứu, nhắn tin xác minh, đặt lịch hẹn nhận lại đồ. | Đăng nhập bắt buộc bằng tài khoản **SSO CTU** (`@ctu.edu.vn` hoặc `@student.ctu.edu.vn`). |
| **Quản lý trạm** | Con người (*Human Actor*) | Tình nguyện viên / Sinh viên trực trạm phụ trách vận hành vật lý tại bàn trực trạm LostLink (Nhà điều hành). Chịu trách nhiệm tiếp nhận đồ vào kho, dán nhãn mã QR, giao trả đồ trực tiếp cho sinh viên, kiểm kê kho và bàn giao đồ quá hạn. *(Lưu ý: Không quản lý nhân sự, không chấm công theo mục loại trừ 3.3)*. | Tài khoản SSO CTU được cấp quyền vai trò `Station_Staff` trên hệ thống. |
| **Cán bộ CTSV** | Con người (*Human Actor*) | Cán bộ đại diện Phòng Công tác Sinh viên (đơn vị chủ quản). Phụ trách giám sát tổng thể, chủ trì tiếp nhận và giải quyết các vụ việc **tranh chấp nhận đồ**, ký nhận biên bản bàn giao đồ quá hạn để xử lý ngoài hệ thống, phê duyệt cấu hình quy định trạm và cấp quyền cho nhân sự trực trạm. | Tài khoản SSO CTU được cấp quyền vai trò `CTSV_Officer` / `Admin`. |
| **Hệ thống** | Tự động (*System / Time Actor*) | Các tác vụ ngầm (*Background Job/Worker*) tự động vận hành theo thời gian hoặc kích hoạt theo sự kiện: tính toán thuật toán so khớp gợi ý tin tương đồng, quét hạn lưu kho vật phẩm, tự động gửi email/thông báo đa kênh. | Dịch vụ nội bộ máy chủ (*Internal Automated Process*). |

---

## 2. Bảng ma trận tổng hợp Tác nhân theo 18 Use Case

> **Quy ước:**  
> • **Chính (Primary Actor):** Tác nhân trực tiếp kích hoạt Use Case để đạt được mục tiêu của mình.  
> • **Phụ / Liên quan (Secondary Actor):** Tác nhân nhận thông tin, tham gia phối hợp hoặc được hệ thống tác động trong quá trình thực hiện Use Case.

| Mã UC | Tên Use Case chuẩn hóa | Tác nhân chính (Primary) | Tác nhân phụ / Liên quan (Secondary) | Mục tiêu chính & Tương tác |
|:---:|---|---|---|---|
| **UC-01** | Đăng nhập và xác thực bằng SSO CTU | Sinh viên, Quản lý trạm, Cán bộ CTSV | — | Xác thực danh tính người dùng thông qua hệ thống Single Sign-On của Đại học Cần Thơ. |
| **UC-02** | Đăng tin tìm đồ thất lạc | Sinh viên | — | Người mất đồ đăng thông tin mô tả, đặc điểm nhận dạng, khu vực thất lạc để tìm lại tài sản. |
| **UC-03** | Đăng tin nhặt được đồ kèm câu hỏi xác minh | Sinh viên | Quản lý trạm | Người nhặt đăng tin báo nhặt được đồ, thiết lập câu hỏi bảo mật chống nhận bừa (trạm có thể hỗ trợ đăng khi tiếp nhận đồ vô danh). |
| **UC-04** | Tra cứu và lọc danh sách đồ thất lạc | Sinh viên | Quản lý trạm, Cán bộ CTSV | Tìm kiếm tin đăng theo danh mục loại đồ, thời gian, khu vực, trạng thái lưu kho tại trạm. |
| **UC-05** | Tự động so khớp và gợi ý tin thất lạc | Hệ thống | Sinh viên | Thuật toán quét và tính điểm tương đồng giữa tin mất và tin nhặt, tự động gửi gợi ý cho sinh viên. |
| **UC-06** | Nhắn tin ẩn danh trao đổi thông tin | Sinh viên | Quản lý trạm | Người mất và người nhặt trao đổi, xác thực thông tin tài sản ẩn danh mà không lộ số điện thoại cá nhân. |
| **UC-07** | Xác minh quyền sở hữu đồ thất lạc | Sinh viên | Quản lý trạm | Người nhận trả lời câu hỏi xác minh; nếu trả lời sai quá 3 lần hệ thống tự động khóa tạm thời 48h. |
| **UC-08** | Tiếp nhận và xử lý tranh chấp nhận đồ | Cán bộ CTSV | Quản lý trạm, Sinh viên | Phòng CTSV đối soát bằng chứng, xác minh thực tế khi phát sinh từ 2 người trở lên cùng nhận 1 món đồ. |
| **UC-09** | Đặt và quản lý lịch hẹn nhận đồ tại trạm | Sinh viên | Quản lý trạm | Sinh viên chủ động chọn khung giờ đến trạm nhận đồ; được phép đổi/hủy lịch hẹn khi có thay đổi đột xuất. |
| **UC-10** | Tiếp nhận vật phẩm vào kho trạm và cấp mã QR | Quản lý trạm | Sinh viên | Nhân sự trạm nhận đồ vật lý từ người nhặt, kiểm tra, chụp ảnh, nhập kho và in/cấp mã QR định danh dán lên đồ. |
| **UC-11** | Quét mã QR và giao trả đồ trực tiếp | Quản lý trạm | Sinh viên | Quét mã QR trên món đồ, đối chiếu mã hẹn/thẻ sinh viên, chụp ảnh xác nhận và hoàn tất giao trả. |
| **UC-12** | Bàn giao ca trực và kiểm kê kho | Quản lý trạm | Cán bộ CTSV | Nhân sự trạm quét kiểm kê toàn bộ hiện vật trong tủ kho, lập biên bản đối soát bàn giao giữa các ca trực. |
| **UC-13** | Xử lý đồ quá hạn và lập biên bản bàn giao CTSV | Quản lý trạm | Cán bộ CTSV | Lọc các món đồ quá hạn lưu giữ (30 ngày/90 ngày), lập biên bản bàn giao vật lý về Phòng CTSV để xử lý ngoài hệ thống. |
| **UC-14** | Kiểm duyệt tin đăng và xử lý vi phạm | Quản lý trạm | Cán bộ CTSV, Sinh viên | Xử lý các báo cáo vi phạm, ẩn tin đăng rác/sai sự thật, cảnh báo hoặc đề xuất khóa tài khoản vi phạm. |
| **UC-15** | Quản lý danh mục loại đồ, khu vực và quy định hệ thống | Cán bộ CTSV | Quản trị viên | Thêm/sửa danh mục loại đồ, khu vực khuôn viên trường, cấu hình thời hạn lưu giữ (30/90 ngày) và khung giờ mở cửa trạm. |
| **UC-16** | Quản lý tài khoản và phân quyền quản lý trạm | Cán bộ CTSV | Quản lý trạm | Phân quyền tài khoản SSO của sinh viên trực trạm (`Station_Staff`) theo kỳ học; thu hồi quyền khi hết ca. |
| **UC-17** | Thống kê và báo cáo định kỳ | Cán bộ CTSV | Quản lý trạm | Xuất báo cáo tổng hợp tỷ lệ tìm thấy đồ, số lượng tồn kho, thời gian lưu kho trung bình theo tháng/học kỳ. |
| **UC-18** | Gửi thông báo tự động đa kênh | Hệ thống | Sinh viên, Quản lý trạm | Tự động kích hoạt phát thông báo (gợi ý so khớp, nhắc lịch hẹn, cảnh báo khóa 48h, thông báo tranh chấp) qua Email CTU / In-app. |

---

## 3. Chi tiết phân công Tác nhân & Quy trình phối hợp (UC-01 đến UC-18)

### Nhóm Chức năng Người dùng & Tìm kiếm (UC-01 → UC-06)
* **UC-01 (Đăng nhập SSO CTU):**  
  * *Tác nhân tham gia:* Mọi người dùng (`Sinh viên`, `Quản lý trạm`, `Cán bộ CTSV`).  
  * *Hành vi:* Hệ thống xác thực qua cổng SSO của Trường ĐH Cần Thơ, phân tách quyền hạn dựa trên vai trò được gán trong hệ thống.
* **UC-02 (Đăng tin tìm đồ thất lạc):**  
  * *Tác nhân chính:* `Sinh viên` (Người mất đồ).  
  * *Hành vi:* Nhập mô tả, chọn danh mục loại đồ, khu vực nghi ngờ đánh rơi, đính kèm hình ảnh mô tả.
* **UC-03 (Đăng tin nhặt được đồ kèm câu hỏi xác minh):**  
  * *Tác nhân chính:* `Sinh viên` (Người nhặt đồ) hoặc `Quản lý trạm` (tiếp nhận đồ vô danh).  
  * *Hành vi:* Nhập đặc điểm bên ngoài, ẩn giấu chi tiết cốt lõi (ảnh/vết xước/số dư) thành **câu hỏi xác minh** bí mật.
* **UC-04 (Tra cứu và lọc danh sách đồ thất lạc):**  
  * *Tác nhân chính:* `Sinh viên`, `Quản lý trạm`.  
  * *Hành vi:* Tìm kiếm theo từ khóa, lọc theo trạng thái ("Đang tìm", "Đã tìm thấy", "Đang lưu kho tại trạm Nhà điều hành").
* **UC-05 (Tự động so khớp và gợi ý tin thất lạc):**  
  * *Tác nhân chính:* `Hệ thống` (Kích hoạt chạy ngầm tự động).  
  * *Tác nhân phụ:* `Sinh viên` (Người nhận được thông báo gợi ý tin so khớp độ chính xác cao).
* **UC-06 (Nhắn tin ẩn danh trao đổi thông tin):**  
  * *Tác nhân chính:* `Sinh viên` (Người mất ↔ Người nhặt).  
  * *Hành vi:* Trò chuyện an toàn qua hệ thống mà không phải cung cấp số điện thoại hoặc mạng xã hội cá nhân.

---

### Nhóm Xác minh, Tranh chấp & Đặt lịch hẹn (UC-07 → UC-09)
* **UC-07 (Xác minh quyền sở hữu đồ thất lạc):**  
  * *Tác nhân chính:* `Sinh viên` (Người tự nhận là chủ đồ).  
  * *Tác nhân phụ:* `Quản lý trạm` (đối soát khi sinh viên đến trạm).  
  * *Quy tắc:* Trả lời đúng câu hỏi xác minh mới được kích hoạt bước đặt lịch hẹn nhận đồ; trả lời sai quá 3 lần bị khóa tạm thời 48h.
* **UC-08 (Tiếp nhận và xử lý tranh chấp nhận đồ):**  
  * *Tác nhân chính:* `Cán bộ CTSV` (Chủ trì giải quyết tranh chấp).  
  * *Tác nhân phối hợp:* `Quản lý trạm` (cung cấp vật phẩm và biên bản đối soát), `Sinh viên` (các bên liên quan xuất trình bằng chứng thực tế).  
  * *Căn cứ:* Giải quyết yêu cầu `FR-VERIFY-003` (từ BB-KH-02 và PV03-12).
* **UC-09 (Đặt và quản lý lịch hẹn nhận đồ tại trạm):**  
  * *Tác nhân chính:* `Sinh viên`.  
  * *Tác nhân phụ:* `Quản lý trạm` (tiếp nhận danh sách lịch hẹn để sắp xếp đồ sẵn sàng).  
  * *Hành vi:* Sinh viên chọn khung giờ trạm mở cửa; có quyền chủ động hủy hoặc đổi lịch hẹn khi bận đột xuất trước giờ hẹn (`FR-APPT-002`, PT-01).

---

### Nhóm Nghiệp vụ Vận hành Kho & Quản lý Trạm (UC-10 → UC-14)
* **UC-10 (Tiếp nhận vật phẩm vào kho trạm và cấp mã QR):**  
  * *Tác nhân chính:* `Quản lý trạm`.  
  * *Tác nhân liên quan:* `Sinh viên` (người mang đồ nhặt được đến gửi tại trạm).  
  * *Hành vi:* Kiểm tra đồ thực tế, nhập mã định danh, in mã QR dán vào vật phẩm và đưa vào tủ bảo quản.
* **UC-11 (Quét mã QR và giao trả đồ trực tiếp):**  
  * *Tác nhân chính:* `Quản lý trạm`.  
  * *Tác nhân phụ:* `Sinh viên` (người đến nhận lại đồ).  
  * *Hành vi:* Quét mã QR trên vật phẩm, kiểm tra thẻ sinh viên, đối chiếu mã hẹn nhận đồ, xác nhận trạng thái "Đã trao trả".
* **UC-12 (Bàn giao ca trực và kiểm kê kho):**  
  * *Tác nhân chính:* `Quản lý trạm` (Nhân sự trực giữa 2 ca).  
  * *Tác nhân giám sát:* `Cán bộ CTSV` (xem báo cáo đối soát kho).  
  * *Hành vi:* Quét toàn bộ mã QR đồ đang có trong kho để đối chiếu số lượng thực tế với phần mềm trước khi giao ca.
* **UC-13 (Xử lý đồ quá hạn và lập biên bản bàn giao CTSV):**  
  * *Tác nhân chính:* `Quản lý trạm`.  
  * *Tác nhân tiếp nhận:* `Cán bộ CTSV`.  
  * *Hành vi:* Lọc danh sách đồ vượt quá hạn lưu giữ (30 ngày/90 ngày), đóng gói và bàn giao thực tế cho Cán bộ CTSV kèm biên bản có chữ ký hai bên (`FR-OVERDUE-002`). *(Xử lý thanh lý diễn ra ngoài hệ thống)*.
* **UC-14 (Kiểm duyệt tin đăng và xử lý vi phạm):**  
  * *Tác nhân chính:* `Quản lý trạm`, `Cán bộ CTSV`.  
  * *Tác nhân bị ảnh hưởng:* `Sinh viên` (tài khoản vi phạm bị nhắc nhở hoặc khóa).

---

### Nhóm Quản trị Hệ thống & Dịch vụ Nền tảng (UC-15 → UC-18)
* **UC-15 (Quản lý danh mục loại đồ, khu vực và quy định hệ thống):**  
  * *Tác nhân chính:* `Cán bộ CTSV`.  
  * *Hành vi:* Quản trị danh mục loại tài sản, sơ đồ vị trí các khoa/giảng đường trong CTU; thiết lập thời hạn lưu giữ và khung giờ mở cửa của trạm theo từng học kỳ.
* **UC-16 (Quản lý tài khoản và phân quyền quản lý trạm):**  
  * *Tác nhân chính:* `Cán bộ CTSV`.  
  * *Tác nhân tiếp nhận:* `Quản lý trạm`.  
  * *Hành vi:* Cấp quyền vai trò `Station_Staff` cho danh sách tình nguyện viên/sinh viên trực trạm; thu hồi quyền khi hết thời gian làm nhiệm vụ *(Tuyệt đối không chấm công ca trực hay quản lý nhân sự)*.
* **UC-17 (Thống kê và báo cáo định kỳ):**  
  * *Tác nhân chính:* `Cán bộ CTSV`, `Quản lý trạm`.  
  * *Hành vi:* Xem biểu đồ thống kê, xuất file Excel báo cáo phục vụ họp giao ban công tác sinh viên.
* **UC-18 (Gửi thông báo tự động đa kênh):**  
  * *Tác nhân kích hoạt:* `Hệ thống`.  
  * *Tác nhân thụ hưởng:* `Sinh viên`, `Quản lý trạm`.  
  * *Hành vi:* Đẩy thông báo qua Email trường và Notification trên ứng dụng khi có biến động trạng thái tài sản/lịch hẹn.

---

## 4. Các nguyên tắc phân định ranh giới (Boundaries & Constraints)

1. **Tuân thủ triệt để phạm vi loại trừ (Mục 3.3 - `TamNhinPhamVi_v1.0`):**
   * Hệ thống **không** xây dựng phân hệ quản lý nhân sự, không xếp lịch ca trực và không chấm công tính lương. Tác nhân `Quản lý trạm` chỉ thao tác với các chức năng nghiệp vụ đồ vật và kho. `UC-16` chỉ thuần túy là phân quyền đăng nhập (*RBAC - Role-Based Access Control*).
2. **Quy chuẩn Tác nhân UML (UML Actor Standards):**
   * Các thuật toán nội bộ (so khớp ảnh, nhận diện từ khóa) không được định nghĩa là "Tác nhân AI" riêng biệt; toàn bộ quy về tác nhân **`Hệ thống`** (*Internal System Agent*).
3. **Phân biệt rạch ròi giữa `Quản lý trạm` và `Cán bộ CTSV`:**
   * `Quản lý trạm` chỉ có quyền tại trạm vật lý (tiếp nhận, bảo quản, trả đồ, kiểm kê).
   * Mọi quyết định mang tính pháp lý hoặc tranh chấp tài sản lớn (`UC-08`), tiếp nhận đồ quá hạn để xử lý bên ngoài (`UC-13`), cấu hình thời hạn/khung giờ (`UC-15`) và phân quyền nhân sự (`UC-16`) đều thuộc thẩm quyền độc quyền của **`Cán bộ CTSV`**.
