# CT241_Chuong4_DacTaVaQuanLyYeuCau
**Tổng số slide:** 59

## Slide 1
TRƯỜNG CÔNG NGHỆ THÔNG TIN & TRUYỀN THÔNG  •  CT241
PHÂN TÍCH YÊU CẦU PHẦN MỀM
Chương 4
Đặc tả và
Quản lý Yêu cầu
Software Requirements Specification & Requirements Management

## Slide 2
C H Ư Ơ N G  4
Chương này nói về điều gì?
Chương này trình bày chi tiết quy trình đặc tả yêu cầu phần mềm (SRS) và các phương pháp quản lý yêu cầu hiệu quả trong 
suốt vòng đời phát triển: cấu trúc tài liệu SRS theo chuẩn IEEE, kỹ thuật viết đặc tả chuyên nghiệp, quy trình rà soát – thẩm 
định, cùng các công cụ và metrics đánh giá chất lượng yêu cầu.
① SRS = “hợp đồng kỹ thuật”
Xác định rõ phạm vi và kỳ vọng giữa khách hàng và đội ngũ 
phát triển.
② Chi phí sửa lỗi tăng theo CẤP SỐ NHÂN
Lỗi yêu cầu phát hiện sau triển khai có thể tốn kém gấp 
100–1000 lần.
③ Chuẩn IEEE 830-1998 & 29148:2018
Cấu trúc tài liệu, 8 đặc tính của SRS tốt và quy trình kỹ 
nghệ yêu cầu.
④ Quản lý yêu cầu = truy xuất + thay đổi
RTM, Change Control Board, baseline, version control và 
các metrics đánh giá.
2

## Slide 3
L E A R N I N G  O U T C O M E S
Mục tiêu của chương
Sau khi hoàn thành chương này, người học có khả năng:
1 Hiểu khái niệm, vai trò và tầm quan trọng của tài liệu đặc tả yêu cầu phần mềm (SRS).
2 Nắm vững cấu trúc và các thành phần của một tài liệu SRS chuẩn theo IEEE 830-1998 và IEEE 29148:2018.
3 Áp dụng các kỹ thuật viết đặc tả yêu cầu chuyên nghiệp, rõ ràng và có thể kiểm chứng.
4 Thực hiện quy trình rà soát và thẩm định tài liệu yêu cầu.
5 Xây dựng và duy trì ma trận truy xuất yêu cầu (Requirements Traceability Matrix).
6 Thiết lập và vận hành quy trình quản lý thay đổi yêu cầu hiệu quả.
7 Sử dụng các công cụ quản lý yêu cầu phổ biến trong công nghiệp.
8 Áp dụng các metrics để đo lường và đánh giá chất lượng yêu cầu.
3

## Slide 4
A G E N D A
Nội dung chương 4
4.1 Tài liệu đặc tả yêu cầu (SRS)
Khái niệm & vai trò · Cấu trúc · Chuẩn IEEE · Kỹ thuật viết · Rà soát & thẩm định · Case study
4.2 Quản lý yêu cầu
Truy xuất yêu cầu · Quản lý thay đổi · Công cụ · Metrics · Thực hành tốt nhất · Theo phương pháp phát triển
4.3 Tóm tắt chương
Sơ đồ tổng hợp quy trình đặc tả và quản lý yêu cầu · Các điểm chính cần lưu ý
Câu hỏi ôn tập (15 câu) & 5 bài tập thực hành cuối chương
4

## Slide 5
4.1
Tài liệu đặc tả
yêu cầu (SRS)
Tài liệu chính thức mô tả đầy đủ và chi tiết những gì hệ thống phần mềm cần thực hiện —
“hợp đồng kỹ thuật” giữa khách hàng và đội ngũ phát triển.

## Slide 6
4 . 1 . 1
SRS là gì?
SRS (Software Requirements Specification) là tài liệu CHÍNH THỨC mô tả đầy đủ và chi tiết những gì hệ thống phần 
mềm cần thực hiện: chức năng, hành vi, ràng buộc và các thuộc tính chất lượng. SRS đóng vai trò như một “HỢP 
ĐỒNG KỸ THUẬT” giữa khách hàng và đội ngũ phát triển.
IEEE 830-1998
“Một tài liệu mô tả những gì phần mềm sẽ làm và cách thức hoạt 
động mong đợi.”
Tiêu chuẩn NỀN TẢNG, tập trung chủ yếu vào CẤU TRÚC và NỘI 
DUNG của tài liệu đặc tả.
ISO/IEC/IEEE 29148:2018
“Một thuộc tính hoặc đặc điểm mà một sản phẩm phần mềm 
được yêu cầu phải có.”
Bản CẬP NHẬT và MỞ RỘNG: bao quát toàn bộ quy trình từ yêu 
cầu Nghiệp vụ đến yêu cầu Phần mềm.
SRS không chỉ là danh sách tính năng, mà còn gồm ngữ cảnh sử dụng, ràng buộc kỹ thuật, yêu cầu phi chức năng và các tiêu chí đánh giá 
mức độ hoàn thành của hệ thống.
6

## Slide 7
4 . 1 . 1
Tám vai trò của SRS trong phát triển phần mềm
1
Cơ sở cho thiết kế và phát triển
Đầu vào chính xác cho thiết kế kiến trúc và thiết kế chi tiết.
 2
Thống nhất hiểu biết giữa các bên
Tạo ngôn ngữ chung cho khách hàng, BA, dev, tester và PM.
3
Cơ sở ước lượng chi phí & thời gian
Ước lượng khối lượng công việc, nguồn lực, tiến độ và ngân sách.
 4
Nền tảng cho kiểm thử & QA
Mỗi yêu cầu cần ít nhất một test case tương ứng để xác minh.
5
Hỗ trợ quản lý thay đổi
Cung cấp BASELINE để đánh giá tác động của mỗi thay đổi.
 6
Giảm thiểu rủi ro dự án
Phát hiện sớm mâu thuẫn, yêu cầu không khả thi hoặc còn thiếu.
7
Tài liệu pháp lý và hợp đồng
Thường được đính kèm phụ lục hợp đồng, xác định tiêu chí nghiệm 
thu.
8
Hỗ trợ bảo trì và phát triển tiếp
Tài liệu tham khảo quan trọng cho đội ngũ bảo trì sau vận hành.
7

## Slide 8
B Ả N G  4 . 1
Chi phí sửa lỗi yêu cầu theo giai đoạn phát hiện
Theo CHAOS Report của Standish Group: khoảng 40–60% lỗi phần mềm có nguồn gốc từ GIAI ĐOẠN YÊU CẦU.
Giai đoạn phát hiện lỗi Hệ số chi phí Chi phí ước tính
Phân tích yêu cầu 1× $100 – $200
Thiết kế 5× $500 – $1.000
Lập trình 10× $1.000 – $2.000
Kiểm thử đơn vị 20× $2.000 – $4.000
Kiểm thử tích hợp 50× $5.000 – $10.000
Kiểm thử hệ thống 100× $10.000 – $20.000
Sau khi triển khai 200× – 1000× $20.000 – $200.000+
→ Đầu tư vào xây dựng SRS chất lượng cao ngay từ đầu là hoàn toàn xứng đáng về mặt kinh tế.
8

## Slide 9
B Ả N G  4 . 2
Cấu trúc chuẩn của tài liệu SRS theo IEEE 830-1998
1
Giới thiệu (Introduction)
Mục đích · Phạm vi · Định nghĩa thuật ngữ · Tài liệu tham khảo · Tổng quan tài liệu
2
Mô tả tổng quan (Overall Description)
Bối cảnh sản phẩm · Chức năng sản phẩm · Đặc điểm người dùng · Các ràng buộc · Giả định và phụ thuộc
3
Yêu cầu cụ thể (Specific Requirements)
Yêu cầu giao diện · Yêu cầu chức năng · Yêu cầu hiệu năng · Ràng buộc thiết kế · Thuộc tính chất lượng
4
Phụ lục (Appendices)
Mô hình phân tích · Danh mục thuật ngữ · Chỉ mục · Lịch sử thay đổi
Cấu trúc này có thể được điều chỉnh cho phù hợp với đặc thù từng dự án, nhưng cần bảo đảm đầy đủ các thông tin thiết yếu.
9

## Slide 10
4 . 1 . 2
Phần 1 — Giới thiệu (Introduction)
Cung cấp tổng quan về tài liệu SRS và dự án, giúp người đọc nắm bối cảnh trước khi đi vào các yêu cầu chi tiết.
1.1 Mục đích (Purpose) Mô tả mục đích của tài liệu SRS, xác định đối tượng đọc (developers, testers, stakeholders) và phạm vi áp dụng.
1.2 Phạm vi (Scope) Định nghĩa tên phần mềm, giải thích phần mềm SẼ LÀM GÌ và KHÔNG LÀM GÌ, mô tả lợi ích, mục tiêu của hệ thống.
1.3 Định nghĩa, từ viết tắt và thuật ngữ Cung cấp định nghĩa cho tất cả thuật ngữ kỹ thuật, từ viết tắt và ký hiệu được dùng trong tài liệu.
1.4 Tài liệu tham khảo (References) Liệt kê tất cả tài liệu được tham chiếu trong SRS, bao gồm tiêu chuẩn và các tài liệu dự án khác.
1.5 Tổng quan tài liệu (Overview) Mô tả cấu trúc phần còn lại của SRS, giúp người đọc định hướng trong tài liệu.
10

## Slide 11
4 . 1 . 2
Phần 2 — Mô tả tổng quan (Overall Description)
Cung cấp cái nhìn tổng thể về sản phẩm và môi trường hoạt động của nó.
2.1 Bối cảnh sản phẩm (Product Perspective) Mô tả mối quan hệ của sản phẩm với các hệ thống khác.
2.2 Chức năng sản phẩm (Product Functions) Tóm tắt các chức năng chính của sản phẩm ở MỨC CAO.
2.3 Đặc điểm người dùng (User Characteristics) Mô tả các nhóm người dùng dự kiến của hệ thống.
2.4 Các ràng buộc (Constraints) Liệt kê các ràng buộc ảnh hưởng đến thiết kế và triển khai.
2.5 Giả định và phụ thuộc Liệt kê các giả định và các yếu tố bên ngoài mà dự án phụ thuộc.
11

## Slide 12
4 . 1 . 2
Phần 3 — Yêu cầu cụ thể: Yêu cầu giao diện
Phần 3 là phần QUAN TRỌNG NHẤT và CHI TIẾT NHẤT của SRS, chứa đặc tả đầy đủ các yêu cầu của hệ thống.
3.1 Yêu cầu giao diện (External Interface Requirements)
Giao diện người dùng
User Interfaces
Mô tả màn hình, báo cáo, menu và các phương thức tương tác.
Giao diện phần cứng
Hardware Interfaces
Mô tả các thiết bị phần cứng mà hệ thống tương tác.
Giao diện phần mềm
Software Interfaces
Mô tả các hệ thống phần mềm khác mà hệ thống tương tác.
Giao diện truyền thông
Communications Interfaces
Mô tả các giao thức và định dạng truyền thông.
Yêu cầu chức năng (3.2) có thể tổ chức theo: đối tượng người dùng · tính năng · use case · đối tượng dữ liệu. 12

## Slide 13
4 . 1 . 2
Phần 3 — Hiệu năng, Ràng buộc thiết kế, Chất lượng
3.3 Yêu cầu hiệu năng
Xác định các yêu cầu về tốc độ, thông lượng, dung lượng và thời 
gian phản hồi của hệ thống.
3.4 Ràng buộc thiết kế
Các ràng buộc kỹ thuật ảnh hưởng đến thiết kế như tiêu chuẩn 
phải tuân thủ, giới hạn phần cứng.
3.5 Các thuộc tính chất lượng (Software System Attributes)
Độ tin cậy Reliability Xác suất hoạt động không lỗi trong một khoảng thời gian.
Tính sẵn sàng Availability Tỷ lệ thời gian hệ thống hoạt động.
Bảo mật Security Yêu cầu về xác thực, phân quyền, mã hoá, audit.
Khả năng bảo trì Maintainability Mức độ dễ dàng sửa đổi và nâng cấp hệ thống.
Khả năng di chuyển Portability Khả năng chạy trên nhiều môi trường khác nhau.
13

## Slide 14
B Ả N G  4 . 3
Tám đặc tính của SRS tốt theo IEEE 830-1998
1 Correct Đúng đắn Mỗi yêu cầu phản ánh chính xác một nhu cầu thực sự và được KHÁCH HÀNG xác nhận.
2 Unambiguous Rõ ràng Mỗi yêu cầu chỉ có MỘT cách giải thích duy nhất; không dùng ngôn ngữ mơ hồ.
3 Complete Đầy đủ Bao gồm tất cả yêu cầu quan trọng: chức năng, hiệu năng, ràng buộc, thuộc tính, giao diện.
4 Consistent Nhất quán Không mâu thuẫn giữa các yêu cầu; thuật ngữ dùng nhất quán trong toàn tài liệu.
5 Ranked Có độ ưu tiên Mỗi yêu cầu được gán mức quan trọng (Essential, Desirable, Optional) hoặc độ ổn định.
6 Verifiable Kiểm chứng được Tồn tại quy trình hữu hạn, chi phí hợp lý để kiểm tra phần mềm đáp ứng yêu cầu.
7 Modifiable Dễ sửa đổi Cấu trúc và định dạng cho phép thay đổi dễ dàng mà không phá vỡ tính nhất quán.
8 Traceable Truy xuất được Nguồn gốc mỗi yêu cầu rõ ràng, theo dõi được đến thiết kế, code và test case.
Tám đặc tính này là bộ tiêu chí kiểm tra chất lượng SRS trước khi thiết lập baseline. 14

## Slide 15
4 . 1 . 3
IEEE 29148:2018 — điểm mới và cải tiến
ISO/IEC/IEEE 29148:2018 là tiêu chuẩn MỚI HƠN, TOÀN DIỆN HƠN, thay thế và mở rộng IEEE 830-1998 — cung cấp hướng 
dẫn về kỹ nghệ yêu cầu trong toàn bộ vòng đời hệ thống và phần mềm.
① Phạm vi mở rộng
Áp dụng cho cả HỆ THỐNG và phần mềm, không chỉ giới hạn ở phần mềm như IEEE 830.
② Tích hợp với các tiêu chuẩn khác
Thiết kế để làm việc cùng ISO/IEC/IEEE 15288 và ISO/IEC/IEEE 12207.
③ Quy trình chi tiết hơn
Định nghĩa các hoạt động và nhiệm vụ cụ thể cho từng quy trình yêu cầu.
④ Mẫu tài liệu chi tiết
Cung cấp các mẫu cụ thể cho StRS (Stakeholder), SyRS (System) và SRS (Software).
⑤ Hỗ trợ Agile
Thừa nhận yêu cầu có thể được phát triển theo nhiều cách khác nhau, bao gồm cả phương pháp Agile.
Giáo trình hướng dẫn chi tiết theo IEEE 830-1998 (cấp độ phần mềm); sinh viên được hướng dẫn mở rộng sang ISO/IEC/IEEE 29148:2018 ở 
cấp độ hệ thống lớn. 15

## Slide 16
B Ả N G  4 . 4
So sánh IEEE 830-1998 và IEEE 29148:2018
Tiêu chí IEEE 830-1998 IEEE 29148:2018
Phạm vi Chỉ phần mềm Hệ thống và phần mềm
Loại tài liệu SRS StRS, SyRS, SRS
Quy trình Tập trung vào tài liệu Định nghĩa quy trình chi tiết
Tích hợp Độc lập Tích hợp ISO 15288, 12207
Phương pháp Truyền thống (Waterfall) Linh hoạt (nhiều phương pháp)
Trạng thái Vẫn được sử dụng rộng rãi Khuyến nghị cho dự án mới

## Slide 17
4 . 1 . 4
Nguyên tắc 1 — Sử dụng ngôn ngữ chuẩn hoá
Bảng 4.5. Từ khoá chuẩn trong đặc tả yêu cầu — xác định MỨC ĐỘ BẮT BUỘC của mỗi yêu cầu.
SHALL PHẢI Bắt buộc (Mandatory) Yêu cầu bắt buộc phải thực hiện.
SHOULD NÊN Khuyến nghị (Recommended) Nên thực hiện trừ khi có lý do hợp lệ.
MAY CÓ THỂ Tuỳ chọn (Optional) Tính năng tuỳ chọn, có thể bỏ qua.
WILL SẼ Tuyên bố (Declaration) Mô tả hành vi của hệ thống.
Ví dụ: “Hệ thống PHẢI cho phép người dùng đăng nhập bằng email và mật khẩu.” — dùng SHALL vì đây là yêu cầu bắt buộc.
17

## Slide 18
4 . 1 . 4
Nguyên tắc 2 & 3 — Đánh số và cấu trúc yêu cầu
Nguyên tắc 2 — Đánh số & phân loại
Mỗi yêu cầu cần có mã định danh duy nhất để dễ theo dõi và 
tham chiếu.
FR-xxx Functional Requirement
NFR-xxx Non-Functional Requirement
IR-xxx Interface Requirement
BR-xxx Business Rule
UC-xxx Use Case
Nguyên tắc 3 — Cấu trúc mỗi yêu cầu
1 Mã yêu cầu (Requirement ID)
2 Mô tả (Description)
3 Nguồn gốc (Source)
4 Độ ưu tiên (Priority)
5 Tiêu chí chấp nhận (Acceptance Criteria)
6 Trạng thái (Proposed → Verified)
7 Phiên bản (Version)
Vì sao phải đánh mã?
Mã định danh là “chìa khoá” cho toàn bộ ma trận truy xuất (RTM): nó liên kết yêu cầu với use case, thiết kế, mã nguồn và test case; đồng 
thời cho phép phân tích tác động khi có Change Request.
18

## Slide 19
B Ả N G  4 . 6
Ví dụ đặc tả yêu cầu chức năng “Đăng nhập hệ thống”
Mã yêu cầu FR-UC01-001
Tên yêu cầu Đăng nhập hệ thống.
Mô tả Hệ thống PHẢI cho phép người dùng đăng nhập bằng tài khoản (email hoặc tên đăng nhập) và mật khẩu. Hệ thống PHẢI xác thực thông tin đăng nhập và cấp quyền truy cập phù hợp với vai trò của người dùng.
Use Case liên quan UC-01: Đăng nhập.
Nguồn gốc Stakeholder Interview — Phòng IT, ngày 15/10/2024.
Độ ưu tiên Cao (Essential).
Tiêu chí chấp nhận ① Người dùng đăng nhập thành công với thông tin hợp lệ trong vòng 3 giây · ② Hệ thống hiển thị thông báo lỗi cụ thể khi thông tin không hợp lệ · ③ Tài khoản bị khoá sau 5 lần đăng nhập sai liên tiếp.
Trạng thái Approved.
Phiên bản 1.0 (15/10/2024).
19

## Slide 20
B Ả N G  4 . 7
Ví dụ đặc tả yêu cầu phi chức năng “Hiệu năng”
Mã yêu cầu NFR-PERF-001
Tên yêu cầu Thời gian phản hồi trang web.
Mô tả Hệ thống PHẢI bảo đảm thời gian tải trang không vượt quá 3 giây đối với 95% các yêu cầu trong điều kiện tải bình thường (lên đến 1.000 người dùng đồng thời).
Loại Yêu cầu hiệu năng (Performance Requirement).
Phương pháp đo lường Sử dụng công cụ load testing (JMeter, LoadRunner) để đo thời gian phản hồi với các kịch bản tải khác nhau.
Độ ưu tiên Cao (Essential).
Trạng thái Approved.

## Slide 21
4 . 1 . 5
Năm kỹ thuật rà soát yêu cầu
1 Thanh tra (Inspection)
Rà soát CHÍNH THỨC, cấu trúc chặt chẽ với các vai 
trò rõ ràng: Moderator, Reader, Recorder, 
Inspectors.
Tỷ lệ phát hiện lỗi CAO NHẤT (60–90%) nhưng 
tốn nhiều thời gian và nguồn lực.
2 Duyệt qua (Walkthrough) Rà soát BÁN CHÍNH THỨC, do tác giả tài liệu trình bày và dẫn dắt nhóm đi qua nội dung. Phù hợp cho chia sẻ kiến thức và đào tạo thành viên mới.
3 Đánh giá đồng cấp (Peer Review) Một hoặc nhiều đồng nghiệp xem xét tài liệu ĐỘC LẬP và cung cấp phản hồi. Linh hoạt, không cần cuộc họp chính thức — phù hợp dự án Agile.
4 Kiểm tra tại bàn (Desk Check) Tác giả TỰ kiểm tra tài liệu của mình theo một checklist định sẵn. Nhanh, đơn giản — bước đầu tiên trước khi gửi cho người khác rà soát.
5 Rà soát bằng bản mẫu (Prototype Review) Sử dụng prototype để xác nhận yêu cầu với khách hàng. Giúp khách hàng hiểu rõ sản phẩm cuối, phát hiện yêu cầu còn thiếu hoặc hiểu sai.
21

## Slide 22
B Ả N G  4 . 8
Checklist rà soát yêu cầu
Checklist là công cụ hữu hiệu để bảo đảm không bỏ sót các vấn đề quan trọng khi rà soát.
1 Tính đầy đủ Tất cả các yêu cầu đã được ghi nhận? Có yêu cầu nào còn thiếu?
2 Tính rõ ràng Mỗi yêu cầu có thể được hiểu theo một cách duy nhất? Có từ ngữ mơ hồ không?
3 Tính nhất quán Có mâu thuẫn giữa các yêu cầu? Thuật ngữ có được dùng nhất quán?
4 Tính kiểm chứng được Mỗi yêu cầu có thể được kiểm thử? Tiêu chí chấp nhận có rõ ràng?
5 Tính khả thi Yêu cầu có thể thực hiện được trong giới hạn công nghệ, ngân sách và thời gian?
6 Tính cần thiết Mỗi yêu cầu có thực sự cần thiết? Có yêu cầu nào dư thừa?
7 Khả năng truy xuất Nguồn gốc mỗi yêu cầu có được ghi nhận? Có thể truy xuất đến thiết kế và test?
8 Độ ưu tiên Mỗi yêu cầu đã được gán độ ưu tiên phù hợp?
22

## Slide 23
4 . 1 . 5
Quy trình thẩm định yêu cầu — 6 bước
Thẩm định (Validation) nhằm xác nhận rằng các yêu cầu đã đặc tả ĐÚNG là những gì khách hàng và người dùng mong 
muốn.
1 Lập kế hoạch thẩm định Xác định phạm vi, người tham gia, tiêu chí thành công, lịch trình.
2 Chuẩn bị tài liệu Hoàn thiện SRS, chuẩn bị prototype (nếu có), checklist thẩm định.
3 Tổ chức phiên thẩm định Trình bày yêu cầu cho stakeholders, thu thập phản hồi và ý kiến.
4 Ghi nhận kết quả Ghi lại các vấn đề phát hiện, các yêu cầu thay đổi hoặc bổ sung.
5 Cập nhật SRS Sửa đổi SRS theo kết quả thẩm định.
6 Phê duyệt Stakeholders ký xác nhận BASELINE của SRS.
Verification kiểm tra “chúng ta xây dựng sản phẩm ĐÚNG CÁCH”; Validation xác nhận “chúng ta xây dựng ĐÚNG sản phẩm”. 23

## Slide 24
4 . 1 . 5
Sáu vấn đề thường gặp khi rà soát yêu cầu
✗ Yêu cầu mơ hồ Sử dụng các từ như “nhanh”, “thân thiện”, “dễ sử dụng” mà không có định nghĩa cụ thể.
✗ Yêu cầu không hoàn chỉnh Thiếu thông tin về điều kiện biên, xử lý lỗi, hoặc các trường hợp ngoại lệ.
✗ Yêu cầu mâu thuẫn Hai yêu cầu khác nhau yêu cầu hành vi đối lập nhau.
✗ Yêu cầu không khả thi Vượt quá khả năng công nghệ hoặc nguồn lực hiện tại của dự án.
✗ Yêu cầu không cần thiết Gold plating — thêm tính năng không ai yêu cầu.
✗ Thiếu khả năng truy xuất Không rõ nguồn gốc hoặc mục đích của yêu cầu.
24

## Slide 25
B Ả N G  4 . 9
Template đặc tả yêu cầu chức năng (1/2)
Mã yêu cầu (ID) Định dạng: FR-[Module]-[Số thứ tự]. Ví dụ: FR-AUTH-001, FR-SEARCH-005.
Tên yêu cầu Tên ngắn gọn, mô tả chức năng chính. Ví dụ: “Đăng nhập bằng email”.
Mô tả chi tiết Dùng cấu trúc: “Hệ thống PHẢI [hành động] khi [điều kiện] để [mục đích]”. Mô tả rõ ràng, không mơ hồ.
Use Case liên quan Liệt kê các Use Case ID mà yêu cầu này thuộc về. Ví dụ: UC-001, UC-002.
Tác nhân (Actor) Ai sẽ thực hiện / sử dụng chức năng này. Ví dụ: Sinh viên, Thủ thư, Hệ thống.
Tiền điều kiện Các điều kiện phải thoả mãn trước khi thực hiện. Ví dụ: Người dùng đã đăng nhập.
Hậu điều kiện Trạng thái hệ thống sau khi thực hiện xong. Ví dụ: Phiên mượn được tạo trong CSDL.
Luồng chính Các bước thực hiện theo trình tự 1, 2, 3… Mô tả tương tác giữa actor và hệ thống.
25

## Slide 26
B Ả N G  4 . 9
Template đặc tả yêu cầu chức năng (2/2)
Luồng ngoại lệ Các trường hợp lỗi / ngoại lệ và cách xử lý. Ví dụ: “Nếu sách hết, hiển thị thông báo…”.
Quy tắc nghiệp vụ Các ràng buộc nghiệp vụ áp dụng. Ví dụ: “Sinh viên chỉ được mượn tối đa 5 cuốn”.
Nguồn gốc Ai / tài liệu nào cung cấp yêu cầu này. Ví dụ: “Phỏng vấn Thủ thư, 15/10/2024”.
Độ ưu tiên Essential (bắt buộc) / Desirable (nên có) / Optional (tuỳ chọn).
Tiêu chí chấp nhận Danh sách điều kiện để xác nhận yêu cầu được thực hiện đúng. Sử dụng cấu trúc Given – When – Then.
Trạng thái Draft → Review → Approved → Implemented → Verified.
Phiên bản Số phiên bản và ngày cập nhật. Ví dụ: v1.2 (20/10/2024).
Ghi chú Thông tin bổ sung, tham chiếu đến tài liệu khác nếu cần.
26

## Slide 27
4 . 1 . 5
Năm mẫu câu đặc tả chuẩn
1
Yêu cầu chức năng cơ bản
“Hệ thống PHẢI [hành động] để [mục đích / kết quả].”
“Hệ thống PHẢI hiển thị danh sách sách theo thứ tự alphabet để người dùng 
dễ tìm kiếm.”
2
Yêu cầu có điều kiện
“Khi [điều kiện], hệ thống PHẢI [hành động].”
“Khi người dùng nhập sai mật khẩu 5 lần liên tiếp, hệ thống PHẢI khoá tài 
khoản trong 30 phút.”
3
Yêu cầu hiệu năng
“Hệ thống PHẢI [hành động] trong vòng [thời gian] với [điều kiện 
tải].”
“Hệ thống PHẢI trả về kết quả tìm kiếm trong vòng 2 giây với 1.000 người 
dùng đồng thời.”
4
Yêu cầu giao diện
“[Thành phần giao diện] PHẢI [đặc điểm / hành vi].”
“Nút ‘Mượn sách’ PHẢI hiển thị màu xanh lá và có kích thước tối thiểu 44×44 
pixel.”
5
Yêu cầu bảo mật
“Hệ thống PHẢI [cơ chế bảo mật] để [mục đích bảo vệ].”
“Hệ thống PHẢI mã hoá mật khẩu bằng thuật toán bcrypt để bảo vệ thông tin 
người dùng.”
27

## Slide 28
B Ả N G  4 . 1 0
Các từ cần tránh trong đặc tả yêu cầu
Từ cần tránh Vấn đề Thay thế bằng
Nhanh, nhanh chóng Mơ hồ, không đo lường được “trong vòng X giây”, “dưới Y mili giây”
Dễ sử dụng Chủ quan, khó kiểm chứng “người dùng mới hoàn thành trong X phút”
Thân thiện Mơ hồ “tuân thủ hướng dẫn Material Design”
Hiệu quả Không cụ thể “sử dụng dưới X% CPU, Y MB RAM”
Linh hoạt Quá rộng Liệt kê cụ thể các tuỳ chọn cần hỗ trợ
Tốt, tốt hơn Chủ quan Định nghĩa tiêu chí cụ thể
Phù hợp Mơ hồ Định nghĩa rõ tiêu chí “phù hợp”
Thường xuyên Không định lượng “hàng ngày”, “mỗi 5 phút”, “X lần/giờ”
Hầu hết Không chính xác “95% requests”, “tất cả trường hợp trừ…”
28

## Slide 29
4 . 1 . 6  C A S E  S T U D Y
Đặc tả yêu cầu cho hệ thống Quản lý Thư viện
Bối cảnh: Trường Đại học ABC cần xây dựng hệ thống quản lý thư viện mới thay thế hệ thống cũ đã lỗi thời — đáp ứng yêu 
cầu quản lý sách, độc giả, mượn/trả sách và tích hợp với hệ thống đào tạo hiện có.
1.2 Phạm vi — TRONG phạm vi
• Quản lý tài liệu (sách, tạp chí, luận văn)
• Quản lý độc giả
• Quản lý mượn / trả
• Báo cáo thống kê
NGOÀI phạm vi
• Quản lý nhân sự thư viện
• Quản lý tài chính
2.1 Bối cảnh sản phẩm — LMS là ứng dụng web tích hợp với
• Hệ thống quản lý đào tạo — để lấy thông tin sinh viên, giảng viên
• Cổng thanh toán — để xử lý phạt nếu có
• Hệ thống email — để gửi thông báo
29

## Slide 30
B Ả N G  4 . 1 1
Các nhóm người dùng hệ thống thư viện
Người dùng Mô tả Chức năng chính
Sinh viên Sinh viên đang theo học tại trường Tìm kiếm, mượn/trả sách, xem lịch sử mượn, gia hạn.
Giảng viên Cán bộ giảng dạy và nghiên cứu Giống sinh viên + mượn số lượng nhiều hơn, thời gian dài hơn.
Thủ thư Nhân viên thư viện Quản lý sách, xử lý mượn/trả, quản lý độc giả, báo cáo.
Quản trị viên Quản lý hệ thống Cấu hình hệ thống, quản lý người dùng, phân quyền.
Xác định rõ các nhóm người dùng giúp đặc tả yêu cầu phù hợp với từng đối tượng và phân quyền chính xác.
30

## Slide 31
B Ả N G  4 . 1 2
Ví dụ các yêu cầu chức năng hệ thống thư viện
Mã Tên Mô tả Ưu tiên
FR-001 Đăng nhập Hệ thống PHẢI cho phép người dùng đăng nhập bằng mã số và mật khẩu Thiết yếu
FR-002 Tìm kiếm sách Hệ thống PHẢI cho phép tìm kiếm theo: tên sách, tác giả, ISBN, chủ đề Thiết yếu
FR-003 Xem chi tiết sách Hệ thống PHẢI hiển thị: thông tin sách, vị trí kệ, số lượng còn, trạng thái Thiết yếu
FR-004 Đặt mượn sách Hệ thống PHẢI cho phép đặt trước sách đang được mượn Mong muốn
FR-005 Mượn sách Thủ thư có thể ghi nhận mượn sách, hệ thống cập nhật số lượng và lịch sử Thiết yếu
FR-006 Trả sách Thủ thư có thể ghi nhận trả sách, hệ thống tính phạt nếu trả trễ Thiết yếu
FR-007 Gia hạn mượn Độc giả có thể gia hạn tối đa 2 lần nếu sách không có người đặt trước Mong muốn
FR-008 Thông báo đến hạn Hệ thống PHẢI gửi email thông báo trước 3 ngày đến hạn trả Mong muốn
Trạng thái của cả 8 yêu cầu trên: Thông qua (Approved). 31

## Slide 32
B Ả N G  4 . 1 3
Ví dụ các yêu cầu phi chức năng hệ thống thư viện
Mã Loại Mô tả Ưu tiên
NFR-001 Hiệu năng Thời gian tìm kiếm sách PHẢI dưới 2 giây với 95% các yêu cầu. Thiết yếu
NFR-002 Hiệu năng Hệ thống PHẢI hỗ trợ ít nhất 500 người dùng đồng thời. Thiết yếu
NFR-003 Khả dụng Hệ thống PHẢI đạt uptime 99,5% trong giờ làm việc (7:00–22:00). Thiết yếu
NFR-004 Bảo mật Mật khẩu PHẢI được mã hoá bằng bcrypt với cost ≥ 10. Thiết yếu
NFR-005 Bảo mật Phiên đăng nhập PHẢI hết hạn sau 30 phút không hoạt động. Thiết yếu
NFR-006 Khả năng sử dụng Người dùng mới NÊN hoàn thành tìm kiếm và mượn sách trong 5 phút. Mong muốn
NFR-007 Tương thích Hệ thống PHẢI hoạt động trên Chrome, Firefox, Safari, Edge bản mới nhất. Thiết yếu
Chú ý cách dùng từ khoá chuẩn: PHẢI (bắt buộc) cho NFR-001…005, 007 và NÊN (khuyến nghị) cho NFR-006. 32

## Slide 33
4 . 1 . 6
Bài học rút ra từ Case Study
① Cấu trúc rõ ràng
Tuân thủ cấu trúc IEEE 830-1998 giúp tài liệu dễ đọc và đầy đủ thông tin.
② Phân loại người dùng
Xác định rõ các nhóm người dùng giúp đặc tả yêu cầu phù hợp với từng đối tượng.
③ Sử dụng từ khoá chuẩn
PHẢI, NÊN, CÓ THỂ giúp phân biệt rõ mức độ bắt buộc của mỗi yêu cầu.
④ Định lượng cụ thể
Thay vì “nhanh”, hãy viết “dưới 2 giây với 95% các yêu cầu”.
⑤ Truy xuất đầy đủ
Mỗi yêu cầu có mã định danh rõ ràng để theo dõi xuyên suốt vòng đời dự án.
33

## Slide 34
4.2
Quản lý yêu cầu
Tập hợp các hoạt động nhằm kiểm soát, theo dõi và duy trì các yêu cầu trong suốt vòng đời 
dự án — bảo đảm yêu cầu được thực hiện đúng và mọi thay đổi được kiểm soát chặt chẽ.

## Slide 35
4 . 2 . 1
Truy xuất yêu cầu (Requirements Traceability)
Truy xuất yêu cầu là khả năng theo dõi MỐI LIÊN HỆ giữa các yêu cầu và các thành phần khác của dự án — bảo đảm mọi yêu 
cầu đều được thực hiện và có thể xác minh được.
Truy xuất NGƯỢC
Backward Traceability
Từ yêu cầu truy về NGUỒN GỐC: 
stakeholder, tài liệu nghiệp vụ, luật định.
“Yêu cầu này đến từ đâu? Ai yêu cầu điều 
này?”
Truy xuất XUÔI
Forward Traceability
Từ yêu cầu đến thiết kế, code, test case.
“Yêu cầu này được thực hiện như thế nào? 
Test nào kiểm tra nó?”
Truy xuất HAI CHIỀU
Bi-directional
Kết hợp cả hai hướng trên, cho phép di 
chuyển linh hoạt giữa các tạo phẩm.
Là mức độ truy xuất mà CMMI và các chuẩn 
nghiêm ngặt yêu cầu.
Ma trận truy xuất yêu cầu (RTM) là công cụ CHÍNH để quản lý truy xuất.
35

## Slide 36
B Ả N G  4 . 1 4
Ví dụ Ma trận Truy xuất Yêu cầu (RTM)
Req ID Mô tả yêu cầu Nguồn gốc Design ID Module Test Case
FR-001 Đăng nhập hệ thống SI-001 DD-001 Auth TC-001, TC-002
FR-002 Đăng ký tài khoản SI-001 DD-002 Auth TC-003, TC-004
FR-003 Quên mật khẩu SI-002 DD-003 Auth TC-005
FR-004 Tìm kiếm sách SI-003 DD-010 Search TC-020, TC-021
FR-005 Mượn sách SI-003 DD-020 Borrow TC-030, TC-031
NFR-001 Thời gian phản hồi < 3s SI-005 — All TC-P01
SI = Stakeholder Interview  ·  DD = Design Document  ·  TC = Test Case  ·  TC-P = Performance Test Case
36

## Slide 37
4 . 2 . 1
Năm lợi ích của truy xuất yêu cầu
1 Bảo đảm độ bao phủ Xác nhận mọi yêu cầu đều được thiết kế, lập trình và kiểm thử.
2 Phân tích tác động Khi có thay đổi, dễ dàng xác định các thành phần bị ảnh hưởng.
3 Hỗ trợ kiểm toán Chứng minh rằng dự án đã tuân thủ các yêu cầu ban đầu.
4 Quản lý rủi ro Xác định các yêu cầu quan trọng chưa được thực hiện.
5 Giao tiếp hiệu quả Giúp các bên liên quan hiểu rõ trạng thái của từng yêu cầu.
Truy xuất chỉ có giá trị khi RTM được CẬP NHẬT LIÊN TỤC — cập nhật ngay khi có thay đổi, không để dồn vào cuối sprint.
37

## Slide 38
4 . 2 . 2
Vì sao cần quản lý thay đổi yêu cầu?
Yêu cầu thay đổi là điều KHÔNG THỂ TRÁNH KHỎI trong hầu hết các dự án phần mềm. Nguyên nhân có thể đến từ:
1 Thay đổi môi trường kinh doanh hoặc thị trường
 2 Hiểu sai hoặc hiểu chưa đầy đủ yêu cầu ban đầu
3 Phản hồi từ người dùng sau khi xem prototype hoặc phiên bản beta
 4 Thay đổi quy định pháp luật hoặc tiêu chuẩn ngành
5 Phát hiện lỗi hoặc vấn đề kỹ thuật trong quá trình phát triển
 6 Yêu cầu mới từ các bên liên quan
Nếu KHÔNG kiểm soát thay đổi…
Dự án gặp hiện tượng “SCOPE CREEP” — phạm vi mở rộng không kiểm soát, dẫn đến vượt ngân sách, trễ tiến độ và chất lượng kém.
38

## Slide 39
B Ả N G  4 . 1 5
Quy trình quản lý thay đổi yêu cầu — 5 bước
1 Tiếp nhận yêu cầu thay đổi Ghi nhận yêu cầu thay đổi từ stakeholder vào Change Request (CR) form: mô tả thay đổi, lý do, người yêu cầu, ngày yêu cầu, độ ưu tiên đề xuất.
2 Phân tích tác động Đánh giá ảnh hưởng đến: phạm vi dự án, lịch trình, ngân sách, chất lượng, các yêu cầu liên quan, thiết kế và code hiện tại. Sử dụng RTM để xác định phạm vi ảnh hưởng.
3 Đánh giá và phê duyệt Change Control Board (CCB) xem xét phân tích tác động và quyết định: Approve · Reject · Defer. CCB gồm PM, BA, Tech Lead và đại diện khách hàng.
4 Thực hiện thay đổi Nếu được phê duyệt: cập nhật SRS, điều chỉnh thiết kế, lập trình, kiểm thử. Cập nhật RTM và các tài liệu liên quan.
5 Xác minh và đóng Xác minh thay đổi đã được thực hiện đúng. Cập nhật trạng thái CR thành Closed. Thông báo cho các bên liên quan.
39

## Slide 40
B Ả N G  4 . 1 6
Ví dụ Change Request Form (1/2)
CR ID CR-2024-0015
Ngày yêu cầu 25/10/2024
Người yêu cầu Nguyễn Văn A — Phòng Đào tạo
Yêu cầu liên quan FR-005: Mượn sách.
Loại thay đổi Sửa đổi yêu cầu hiện có.
Mô tả thay đổi Tăng số lượng sách tối đa mà sinh viên năm cuối được mượn từ 5 cuốn lên 10 cuốn để hỗ trợ làm đồ án tốt nghiệp.
Lý do thay đổi Sinh viên năm cuối cần nhiều tài liệu tham khảo hơn cho đồ án. Khảo sát cho thấy 78% sinh viên năm cuối gặp khó khăn vì giới hạn số sách mượn.
Độ ưu tiên đề xuất Cao
40

## Slide 41
B Ả N G  4 . 1 6
Ví dụ Change Request Form (2/2)
Tác động đến yêu cầu khác FR-007 (Gia hạn mượn): cần cập nhật logic gia hạn. NFR-002 (Hiệu năng): có thể tăng tải hệ thống.
Tác động đến thiết kế Cần sửa đổi: bảng BorrowPolicy, module BorrowService, stored procedure sp_CheckBorrowLimit.
Tác động đến test Cập nhật: TC-030, TC-031, TC-032. Thêm mới: TC-033 (test giới hạn 10 cuốn cho SV năm cuối).
Ước lượng effort Development: 2 ngày · Testing: 1 ngày · Documentation: 0,5 ngày.  Tổng: 3,5 ngày.
Tác động đến timeline Không ảnh hưởng milestone chính. Có thể hoàn thành trong Sprint 5.
Tác động đến budget Chi phí phát sinh: ~$500 (3,5 ngày × $150/ngày).
Quyết định CCB ☑ Approve    ☐ Reject    ☐ Defer          Ngày quyết định: 28/10/2024
Ghi chú CCB Phê duyệt. Thực hiện trong Sprint 5. Cần thông báo cho team QA về test case mới.
41

## Slide 42
B Ả N G  4 . 1 7
Chi tiết các bước xử lý một Change Request
Bước Hoạt động Mô tả Người thực hiện Thời gian
1 Submit CR Điền biểu mẫu CR, mô tả rõ yêu cầu thay đổi và lý do Stakeholder, BA, PM 1 ngày
2 Validate CR Kiểm tra CR hợp lệ, đầy đủ thông tin, không trùng lặp BA, CM Manager 0,5 ngày
3 Impact Analysis Phân tích tác động đến yêu cầu, thiết kế, code, test, timeline, budget BA, Tech Lead, QA Lead 1–3 ngày
4 CCB Review CCB họp xem xét báo cáo phân tích, thảo luận và biểu quyết CCB Members 1 ngày
5 Decision CCB quyết định Approve / Reject / Defer, ghi nhận lý do CCB —
6 Communicate Thông báo quyết định đến tất cả các bên liên quan CM Manager, PM 0,5 ngày
7 Implement Nếu Approve: cập nhật SRS, thiết kế, lập trình, kiểm thử Dev Team, QA Team Theo ước lượng
8 Verify Kiểm tra thay đổi đã được thực hiện đúng như CR mô tả QA, BA 1 ngày
9 Close CR Cập nhật trạng thái CR thành Closed, lưu vào hồ sơ dự án CM Manager 0,5 ngày
42

## Slide 43
4 . 2 . 2
Thành phần Change Control Board (CCB)
CCB là cơ quan có THẨM QUYỀN phê duyệt hoặc từ chối các yêu cầu thay đổi.
◆ Project Manager Đánh giá tác động đến timeline và ngân sách, điều phối nguồn lực.
◆ Business Analyst Đánh giá tác động đến yêu cầu và phạm vi, bảo đảm thay đổi phù hợp mục tiêu dự án.
◆ Technical Lead / Architect Đánh giá tác động kỹ thuật, tính khả thi về mặt công nghệ.
◆ QA Lead Đánh giá tác động đến kế hoạch kiểm thử và chất lượng.
◆ Customer / Product Owner Đại diện phía khách hàng, xác nhận GIÁ TRỊ NGHIỆP VỤ của thay đổi.
◆ Configuration Manager Quản lý version control, bảo đảm traceability sau thay đổi.
43

## Slide 44
4 . 2 . 2
Đường cơ sở (Baseline) và Kiểm soát phiên bản
Baseline (Đường cơ sở)
Một phiên bản ỔN ĐỊNH của SRS đã được phê duyệt. Sau khi 
baseline được thiết lập, mọi thay đổi PHẢI đi qua quy trình kiểm 
soát thay đổi chính thức.
• Initial Baseline: bản SRS đầu tiên được phê duyệt trước khi 
thiết kế
• Intermediate Baselines: sau mỗi lần cập nhật quan trọng
• Final Baseline: bản cuối khi dự án hoàn thành
Version Control
Mỗi thay đổi trong SRS cần được ghi nhận với:
• Số phiên bản theo quy ước Major.Minor (1.0, 1.1, 2.0)
• Ngày thay đổi
• Người thực hiện thay đổi
• Mô tả và lý do thay đổi
• Trạng thái phê duyệt
Bảng 4.18. Ví dụ lịch sử thay đổi tài liệu SRS
Phiên bản Ngày Tác giả Mô tả thay đổi
1.0 15/10/2024 Nguyễn Văn A Phiên bản ban đầu, baseline đầu tiên.
1.1 22/10/2024 Trần Thị B Bổ sung yêu cầu FR-010 đến FR-015 (module báo cáo).
1.2 01/11/2024 Nguyễn Văn A Cập nhật NFR-001 (thời gian phản hồi từ 5s xuống 3s).
2.0 15/11/2024 Trần Thị B Baseline lần 2, bao gồm tất cả CR đã phê duyệt. 44

## Slide 45
B Ả N G  4 . 1 9
Các công cụ quản lý yêu cầu phổ biến
Công cụ Đặc điểm nổi bật Phù hợp với
JIRA + Confluence Tích hợp Agile, quản lý backlog, wiki, tuỳ chỉnh workflow, kho plugin phong phú Dự án Agile/Scrum, đội ngũ vừa và lớn
Azure DevOps Tích hợp CI/CD, quản lý Work Items, Boards, Repos, Test Plans trong một nền tảng Dự án Microsoft stack, DevOps teams
IBM DOORS Công cụ enterprise, truy xuất mạnh mẽ, tuân thủ chuẩn DO-178C, ISO 26262 Dự án lớn: hàng không, ô tô, y tế
Helix RM Quản lý yêu cầu end-to-end, tích hợp công cụ ALM khác, hỗ trợ compliance Dự án chuyên ngành có quy định nghiêm ngặt
Trello / Asana Đơn giản, trực quan, dễ sử dụng, quản lý công việc và backlog đơn giản Dự án nhỏ, khởi nghiệp, nhóm mới bắt đầu
ReqView Chuyên biệt cho phân tích yêu cầu, hỗ trợ ghi vết, kết xuất đa dạng, giá hợp lý Dự án vừa, cần công cụ chuyên biệt
Polarion ALM platform đầy đủ: yêu cầu, kiểm thử, xử lý lỗi, quản lý tuân thủ, báo cáo Doanh nghiệp, công nghiệp ô tô, hàng không
Modern Requirements Tích hợp sâu Azure DevOps, SmartDocs, quy trình rà soát, xác lập đường cơ sở Đội ngũ đã dùng Azure DevOps
45

## Slide 46
4 . 2 . 3
Tám tiêu chí lựa chọn công cụ quản lý yêu cầu
1
Khả năng truy xuất
Liên kết yêu cầu – thiết kế – mã nguồn – test case; truy xuất một 
chiều hoặc hai chiều.
2
Quản lý thay đổi
Workflow phê duyệt, theo dõi lịch sử thay đổi, hỗ trợ thiết lập 
baseline.
3
Cộng tác
Comment, thảo luận, phân công và thông báo (notification) cho 
nhóm.
4
Báo cáo
Báo cáo về trạng thái, mức độ bao phủ (coverage), chất lượng và tiến 
độ.
5
Tích hợp
Kết nối IDE, CI/CD, công cụ quản lý kiểm thử và hệ thống quản lý mã 
nguồn.
6
Khả năng mở rộng
Đáp ứng tốt khi quy mô dự án, số người dùng và lượng tạo phẩm 
tăng lên.
7
Chi phí
Bản quyền (license), đào tạo, triển khai và bảo trì.
 8
Dễ sử dụng
Độ dễ học (learning curve), trải nghiệm người dùng và mức thân 
thiện với người mới.
46

## Slide 47
B Ả N G  4 . 2 0
Các chỉ số đo lường đánh giá yêu cầu
Chỉ số đo lường Công thức Ý nghĩa
Độ ổn định của yêu cầu (Số YC không thay đổi / Tổng số YC) × 100% Giá trị CAO cho thấy yêu cầu ít thay đổi.
Độ bao phủ yêu cầu (Số YC được test / Tổng số YC) × 100% Đo mức độ kiểm thử — mục tiêu 100%.
Mật độ lỗi Số lỗi tìm được / Số yêu cầu Đo chất lượng yêu cầu — giá trị THẤP là tốt.
Tỷ lệ yêu cầu thay đổi (Số CR / Tổng số YC) × 100% Đo tần suất thay đổi — giá trị cao cần xem xét 
nguyên nhân.
Độ bao phủ truy xuất (Số YC có trace / Tổng số YC) × 100% Đo mức độ truy xuất — mục tiêu 100%.
Thời gian chu kỳ phê duyệt Thời gian từ lúc submit đến approved Đo hiệu quả quy trình phê duyệt.
Độ biến động của yêu cầu (YC thêm + sửa + xoá) / Tổng YC ban đầu Đo mức độ biến động của yêu cầu.
Tỷ lệ hoàn thành (Số YC được cài đặt / Tổng số YC) × 100% Đo tiến độ thực hiện yêu cầu.
47

## Slide 48
4 . 2 . 4
Cách sử dụng metrics & ví dụ báo cáo
Dashboard theo dõi Hiển thị các metrics quan trọng, cập nhật tự động từ công cụ quản lý yêu cầu.
Trend analysis Theo dõi xu hướng metrics theo thời gian để phát hiện vấn đề sớm.
Benchmarking So sánh với dự án trước hoặc tiêu chuẩn ngành để đánh giá hiệu suất.
Root cause analysis Khi metrics cho thấy vấn đề, phân tích nguyên nhân gốc để cải tiến.
Goal setting Đặt mục tiêu cụ thể cho từng metric và theo dõi việc đạt được mục tiêu.
Bảng 4.21. Ví dụ báo cáo chỉ số đo lường — dự án thư viện
Chỉ số đo lường Sprint 1 Sprint 2 Mục tiêu
Tổng số yêu cầu 45 52 —
Phạm vi yêu cầu 85% 92% ≥ 95%
Độ bao phủ truy xuất 78% 88% 100%
Tỷ lệ yêu cầu thay đổi 12% 8% ≤ 10%
Mật độ lỗi 0,15 0,11 ≤ 0,10
Tỷ lệ hoàn thành 65% 78% ≥ 80%
48

## Slide 49
4 . 2 . 5
Các thực hành tốt nhất trong quản lý yêu cầu
a) Giai đoạn Thu thập và Đặc tả
• Involve stakeholders SỚM và THƯỜNG XUYÊN qua 
workshop, interview định kỳ
• Sử dụng PROTOTYPE để validate yêu cầu, đặc biệt cho 
UI/UX
• Đặc tả theo TEMPLATE CHUẨN, nhất quán cho tất cả yêu 
cầu
• Peer review TẤT CẢ yêu cầu trước khi đưa vào baseline
• Tránh GOLD PLATING — chỉ đặc tả những gì thực sự cần 
thiết
b) Giai đoạn Quản lý và Theo dõi
• Thiết lập BASELINE SỚM, trước khi bắt đầu thiết kế
• Chọn công cụ PHÙ HỢP quy mô — không cần công cụ phức 
tạp cho dự án nhỏ
• Duy trì RTM LIÊN TỤC, không để dồn vào cuối sprint
• Review metrics ĐỊNH KỲ hàng tuần/sprint để phát hiện vấn 
đề sớm
• Giao tiếp thay đổi RÕ RÀNG đến tất cả các bên liên quan
Nguyên tắc chung: quản lý yêu cầu là hoạt động LIÊN TỤC, không phải một mốc trong dự án.
49

## Slide 50
B Ả N G  4 . 2 2
Các lỗi thường gặp và cách khắc phục
✗ Yêu cầu mơ hồ, không kiểm chứng được →  Sử dụng ngôn ngữ cụ thể, định lượng. Rà soát bằng checklist để bảo đảm mỗi yêu cầu có tiêu chí chấp nhận rõ ràng.
✗ Thiếu sự tham gia của bên liên quan →  Lập kế hoạch tham gia rõ ràng, đặt lịch họp định kỳ, dùng prototype để thu hút sự quan tâm.
✗ Scope creep không kiểm soát →  Thiết lập quy trình quản lý thay đổi chặt chẽ, có CCB đánh giá mọi thay đổi, từ chối yêu cầu không hợp lý.
✗ RTM không được cập nhật →  Tích hợp RTM vào quy trình làm việc hằng ngày, sử dụng công cụ tự động liên kết.
✗ Không có baseline rõ ràng →  Định nghĩa rõ các mốc baseline, có quy trình phê duyệt chính thức trước khi thiết lập.
✗ Thiếu bằng chứng kiểm thử →  Đòi hỏi mỗi yêu cầu phải có ít nhất một test case trước khi đóng; đưa vào Definition of Done.
50

## Slide 51
B Ả N G  4 . 2 3
Quản lý yêu cầu theo phương pháp phát triển
Khía cạnh Waterfall Agile Hybrid
Tài liệu yêu cầu SRS đầy đủ User Stories, Acceptance Criteria SRS + User Stories
Thời điểm đặc tả Đầu dự án Just-in-time Kết hợp
Quản lý thay đổi CCB chính thức Product Owner quyết định CCB cho core, PO cho chi tiết
Traceability RTM thủ công / công cụ Công cụ tự động Công cụ tự động
Baseline Baseline chính thức Product Backlog Baseline + Backlog
Phù hợp với Yêu cầu ổn định Yêu cầu thay đổi thường xuyên Đa dạng
Hybrid: SRS high-level cho yêu cầu cốt lõi + User Stories cho tính năng chi tiết; baseline cho phần ổn định, linh hoạt cho phần còn lại.
51

## Slide 52
B Ả N G  4 . 2 4
Tổng hợp quy trình đặc tả và quản lý yêu cầu
Giai đoạn Hoạt động chính Sản phẩm đầu ra Công cụ hỗ trợ
1. Thu thập Phỏng vấn, khảo sát, workshop, phân tích tài liệu Danh sách yêu cầu thô Interview forms, Mind maps
2. Phân tích Phân loại, ưu tiên, phát hiện mâu thuẫn, giải quyết xung đột Yêu cầu đã phân tích Spreadsheet, UML tools
3. Đặc tả Viết SRS theo chuẩn IEEE, tạo RTM ban đầu Tài liệu SRS, RTM Word, RM tools
4. Rà soát Review, inspection, validation với stakeholder SRS đã rà soát Checklist, Review forms
5. Phê duyệt CCB review, thiết lập baseline SRS baseline v1.0 RM tools, Version control
6. Quản lý Theo dõi trạng thái, xử lý thay đổi, cập nhật RTM RTM cập nhật, CR logs JIRA, Azure DevOps
7. Đánh giá Thu thập metrics, phân tích, cải tiến quy trình Báo cáo metrics Dashboards, BI tools
52

## Slide 53
4 . 3 . 2
Các điểm chính cần lưu ý (1/2)
Về tài liệu đặc tả yêu cầu (SRS)
• SRS là tài liệu chính thức mô tả đầy đủ những gì hệ thống cần thực hiện — “hợp đồng kỹ thuật” giữa các bên liên quan
• Chi phí sửa lỗi yêu cầu tăng theo cấp số nhân, có thể lên đến 100–1000 lần nếu phát hiện sau khi triển khai
• Cấu trúc SRS chuẩn IEEE 830-1998: Giới thiệu · Mô tả tổng quan · Yêu cầu cụ thể · Phụ lục
• Tám đặc tính của SRS tốt: Correct, Unambiguous, Complete, Consistent, Ranked, Verifiable, Modifiable, Traceable
• IEEE 29148:2018 toàn diện hơn, hỗ trợ cả hệ thống và phần mềm, tích hợp với các tiêu chuẩn ISO
Về kỹ thuật viết đặc tả
• Ngôn ngữ chuẩn hoá: SHALL (bắt buộc) · SHOULD (khuyến nghị) · MAY (tuỳ chọn) · WILL (tuyên bố)
• Đánh số và phân loại rõ ràng: FR · NFR · IR · BR · UC
• Mỗi yêu cầu cần có: Mã · Mô tả · Nguồn gốc · Độ ưu tiên · Tiêu chí chấp nhận · Trạng thái · Phiên bản
53

## Slide 54
4 . 3 . 2
Các điểm chính cần lưu ý (2/2)
Về rà soát và thẩm định
• Các kỹ thuật rà soát: Inspection · Walkthrough · Peer Review · Desk Check · Prototype Review
• Sử dụng checklist để bảo đảm không bỏ sót các vấn đề quan trọng
• Quy trình thẩm định: Lập kế hoạch → Chuẩn bị → Tổ chức phiên → Ghi nhận kết quả → Cập nhật SRS → Phê duyệt
Về quản lý yêu cầu
• Truy xuất yêu cầu giúp theo dõi mối liên hệ giữa yêu cầu và các thành phần khác: Forward · Backward · Bi-directional
• Ma trận truy xuất yêu cầu (RTM) là công cụ chính để quản lý truy xuất
• Quy trình quản lý thay đổi: Tiếp nhận CR → Phân tích tác động → Đánh giá & phê duyệt → Thực hiện → Xác minh & đóng
• Baseline và Version Control giúp kiểm soát các phiên bản của SRS
• Công cụ phổ biến: JIRA · Azure DevOps · IBM DOORS · Helix RM · Polarion
• Metrics quan trọng: Requirements Stability · Coverage · Defect Density · Change Request Rate · Traceability Coverage
54

## Slide 55
C Â U  H Ỏ I  Ô N  T Ậ P  C H Ư Ơ N G  4
Câu 1 – 8
1 Trình bày khái niệm và vai trò của tài liệu SRS. Tại sao việc đầu tư vào SRS chất lượng cao lại quan trọng?
2 Mô tả cấu trúc chuẩn của tài liệu SRS theo IEEE 830-1998. Liệt kê các thành phần chính của mỗi phần.
3 Giải thích tám đặc tính của một SRS tốt theo IEEE 830-1998. Cho ví dụ minh hoạ cho mỗi đặc tính.
4 So sánh IEEE 830-1998 và IEEE 29148:2018. Những điểm mới và cải tiến trong IEEE 29148:2018 là gì?
5 Trình bày các từ khoá chuẩn (SHALL, SHOULD, MAY, WILL). Cho ví dụ sử dụng mỗi từ khoá.
6 Một yêu cầu chức năng đầy đủ cần gồm những thành phần nào? Viết một ví dụ hoàn chỉnh cho chức năng “Tìm kiếm sách”.
7 Phân biệt các kỹ thuật rà soát: Inspection, Walkthrough, Peer Review, Desk Check. Khi nào nên dùng mỗi kỹ thuật?
8 Giải thích khái niệm truy xuất yêu cầu. Phân biệt Forward, Backward và Bi-directional Traceability.
55

## Slide 56
C Â U  H Ỏ I  Ô N  T Ậ P  C H Ư Ơ N G  4
Câu 9 – 15
9 Ma trận truy xuất yêu cầu (RTM) là gì? Nêu các thành phần chính và lợi ích của việc sử dụng RTM trong dự án.
10 Trình bày quy trình quản lý thay đổi yêu cầu. Vai trò của Change Control Board (CCB) là gì?
11 Giải thích khái niệm Baseline. Tại sao cần thiết lập baseline và quản lý version control cho SRS?
12 So sánh các công cụ quản lý yêu cầu: JIRA, Azure DevOps, IBM DOORS. Mỗi công cụ phù hợp với loại dự án nào?
13 Liệt kê và giải thích các metrics đánh giá yêu cầu. Cách tính và ý nghĩa của Requirements Stability, Coverage, Defect Density.
14 Scope creep là gì? Nguyên nhân và cách phòng tránh scope creep trong dự án phần mềm.
15 Trình bày các vấn đề thường gặp khi viết đặc tả (mơ hồ, không hoàn chỉnh, mâu thuẫn…). Đề xuất cách khắc phục cho mỗi vấn đề.
56

## Slide 57
B À I  T Ậ P  T H Ự C  H À N H
Bài 1 – 3  (làm theo nhóm 3–4 người)
1 Viết tài liệu SRS Thời gian dự kiến: 4–6 giờ
Viết SRS cho hệ thống “Quản lý Thư viện Trường Đại học” theo cấu trúc IEEE 830-1998. Chức năng: quản lý sách · quản lý độc giả · mượn/trả · gia hạn · 
xử lý vi phạm · thống kê báo cáo.
Nộp: SRS đầy đủ theo template IEEE 830-1998; ít nhất 15 FR và 5 NFR; mỗi yêu cầu có Mã, Mô tả, Nguồn gốc, Độ ưu tiên, Tiêu chí chấp nhận.
2 Xây dựng Ma trận Truy xuất (RTM)
Dựa trên SRS ở Bài 1, xây dựng RTM gồm các cột: Requirement ID · Description · Source · Priority · Use Case ID (liên kết Chương 3) · Design Component 
· Test Case ID · Status.
Nộp: file RTM dạng Excel hoặc trên công cụ quản lý yêu cầu; bảo đảm 100% yêu cầu đều có lưu vết.
3 Rà soát SRS (Peer Review)
Nhận SRS từ nhóm khác → dùng checklist Bảng 4.8 để kiểm tra → ghi nhận vấn đề → phân loại theo mức nghiêm trọng (Critical, Major, Minor) → đề 
xuất khắc phục → viết báo cáo rà soát.
Nộp: báo cáo rà soát với danh sách vấn đề phát hiện và đề xuất cải tiến cho từng vấn đề.
57

## Slide 58
B À I  T Ậ P  T H Ự C  H À N H
Bài 4 – 5
4 Sử dụng công cụ quản lý yêu cầu
Dùng JIRA, Azure DevOps hoặc Trello để quản lý yêu cầu cho dự án thư viện.
• Tạo dự án mới · Import các yêu cầu từ SRS vào công cụ
• Thiết lập workflow: Draft → Review → Approved → Implemented → Verified
• Tạo liên kết giữa các yêu cầu (dependencies, parent-child)
• Tạo một Change Request và xử lý theo quy trình · Tạo báo cáo/dashboard trạng thái yêu cầu
5 Phân tích tác động thay đổi Thời gian dự kiến: 2–3 giờ
Tình huống: khách hàng yêu cầu thay đổi — “Hệ thống phải hỗ trợ đăng nhập bằng tài khoản Google và Facebook (SSO)” thay vì chỉ 
đăng nhập bằng email/password như yêu cầu ban đầu.
• Viết Change Request (CR) cho yêu cầu thay đổi này
• Dùng RTM để xác định các yêu cầu, thiết kế và test case bị ảnh hưởng
• Ước lượng effort cần thiết · Đánh giá tác động đến thời hạn và kinh phí
• Đề xuất quyết định: Approve, Reject hoặc Defer — kèm lý giải
58

## Slide 59
HẾT CHƯƠNG 4 — HOÀN THÀNH GIÁO TRÌNH
Phân tích Yêu cầu Phần mềm
Chương 1 → Chương 4
Tài liệu tham khảo chính: IEEE 830-1998 · ISO/IEC/IEEE 29148:2018 · Dean Leffingwell (2011) [7] · DSDM Project 
Framework (2014) [1] · Buschmann và cộng sự (1996) [5]
CT241 — Phân tích Yêu cầu Phần mềm
