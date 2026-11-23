# TRƯỜNG ĐẠI HỌC CẦN THƠ
## TRƯỜNG CÔNG NGHỆ THÔNG TIN VÀ TRUYỀN THÔNG
Học phần CT241 – Phân tích yêu cầu phần mềm

# ĐẶC TẢ YÊU CẦU PHẦN MỀM (SRS)
## Đề tài: Hệ thống quản lý và kết nối tìm kiếm đồ thất lạc tập trung trong khuôn viên Đại học Cần Thơ (LostLink)

| Thông tin | Chi tiết |
|:---|:---|
| **Nhóm** | Nhóm 02 |
| **Thành viên** | Nguyễn Phước Lộc (B2303828); Võ Thành Nam (B2303829); Trần Trọng Phúc (B2303844) |
| **Mã tài liệu** | `CT241_Nhom02_SRS` |
| **Phiên bản** | v0.9 – 29/11/2026 |
| **Học kỳ** | Học kỳ 1, năm học 2026–2027 |

---

## Lịch sử phiên bản

| Phiên bản | Ngày | Người thực hiện | Nội dung thay đổi |
|:---:|:---:|:---|:---|
| **v0.9** | 29/11/2026 | Cả nhóm | Bản nháp hoàn chỉnh gửi nhóm bạn rà soát chéo theo Bảng 4.8 giáo trình. |
| **v1.0** | 03/12/2026 | Nguyễn Phước Lộc | Sửa các lỗi theo phản hồi rà soát nhận được; đóng baseline 1. |

---

# 1. Giới thiệu

## 1.1. Mục đích
Tài liệu đặc tả các yêu cầu phần mềm của Hệ thống quản lý và kết nối tìm kiếm đồ thất lạc tập trung trong khuôn viên Đại học Cần Thơ (LostLink). Người đọc gồm: nhóm khách hàng (đại diện Phòng CTSV, sinh viên quản lý trạm), nhóm phát triển, nhóm kiểm thử và giảng viên học phần. Cấu trúc tài liệu theo IEEE 830-1998 như giáo trình hướng dẫn; các mục tương ứng với phần SRS của ISO/IEC/IEEE 29148:2018.

## 1.2. Phạm vi
LostLink quản lý tin đăng mất, tin đăng nhặt, vật phẩm lưu kho, xác minh sở hữu qua câu hỏi bí mật, lịch hẹn nhận đồ tại trạm, quét mã QR giao trả và bàn giao đồ quá hạn cho Phòng CTSV. LostLink không quản lý vận chuyển đồ, không thanh toán phí và không thay thế hệ thống camera an ninh. Mục tiêu nghiệp vụ MT-01 đến MT-05 nêu trong tài liệu tầm nhìn – phạm vi v1.1.

## 1.3. Định nghĩa, từ viết tắt

| Thuật ngữ | Định nghĩa |
|:---|:---|
| **LostLink** | Hệ thống quản lý và kết nối tìm kiếm đồ thất lạc tập trung tại Trường Đại học Cần Thơ. |
| **Trạm** | Trạm giữ đồ thất lạc đặt tại khuôn viên Khu II Trường Đại học Cần Thơ. |
| **Vật phẩm lưu kho** | Hiện vật thất lạc được tiếp nhận thực tế tại trạm, có dán nhãn mã QR. |
| **Lịch hẹn** | Lịch đăng ký khung giờ đến trạm nhận lại đồ của sinh viên. |
| **Trao trả** | Trạm giao trả đồ cho sinh viên chủ sở hữu (UC-11). |
| **Bàn giao** | Trạm xuất kho chuyển giao đồ quá hạn về Phòng CTSV xử lý (UC-13). |
| **SSO** | Dịch vụ đăng nhập dùng chung của trường. |
| **PHẢI / NÊN / CÓ THỂ** | Từ khóa theo Bảng 4.5 giáo trình: bắt buộc / khuyến nghị / tùy chọn. |
| **MT, BR, FR, NFR, UC, C, A** | Mục tiêu, Quy tắc nghiệp vụ, Yêu cầu chức năng, Yêu cầu phi chức năng, Use case, Ràng buộc, Giả định. |

## 1.4. Tài liệu tham khảo
- `CT241_Nhom02_TamNhinPhamVi_v1.1`; `CT241_Nhom02_BienBanPhongVan_v1.0`; `CT241_Nhom02_BienBanLamViecKhachHang_v1.0`; `CT241_Nhom02_KhaoSat_v1.0`.
- `CT241_Nhom02_MoHinhUML_v1.0` (thư mục `03_MoHinh`); `CT241_Nhom02_RTM_v1.0` (thư mục `05_QuanLyYeuCau`).
- Giáo trình Phân tích yêu cầu phần mềm, Chương 3 và Chương 4; IEEE Std 830-1998; ISO/IEC/IEEE 29148:2018.

## 1.5. Tổng quan tài liệu
Mục 2 mô tả tổng quan sản phẩm. Mục 3 đặc tả quy tắc nghiệp vụ, use case, yêu cầu chức năng và phi chức năng. Mục 4 là phụ lục mô hình và truy vết.
