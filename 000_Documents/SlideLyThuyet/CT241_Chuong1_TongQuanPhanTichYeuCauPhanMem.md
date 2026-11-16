# CT241_Chuong1_TongQuanPhanTichYeuCauPhanMem
**Tổng số slide:** 52

## Slide 1
*(Slide hình ảnh / không có văn bản)*

## Slide 2
TRƯỜNG CÔNG NGHỆ THÔNG TIN & TRUYỀN THÔNG  •  CT241
PHÂN TÍCH YÊU CẦU PHẦN MỀM
Chương 1
Tổng quan về Phân tích
Yêu cầu Phần mềm
Software Requirements Analysis — Fundamentals & Overview

## Slide 3
C H Ư Ơ N G  1
Chương này nói về điều gì?
Chương này cung cấp cái nhìn tổng quan và nền tảng về lĩnh vực Phân tích Yêu cầu Phần mềm (Software Requirements 
Analysis – SRA): định nghĩa vai trò và tầm quan trọng chiến lược của việc “thấu hiểu” yêu cầu, các loại yêu cầu, đặc tính 
của một yêu cầu tốt, quy trình phân tích yêu cầu tổng thể và các thách thức thường gặp trong thực tế dự án.
? Vì sao cần phân tích yêu cầu?
Hiểu sai nhu cầu → làm lại tốn kém, vượt chi phí, trễ hạn, 
thậm chí thất bại dự án.
! Từ khoá then chốt: THẤU HIỂU
Không chỉ “hiểu” yêu cầu, mà phải thấu hiểu vấn đề thực 
sự của người dùng.
→ Tư duy hệ thống (CMM → CMMI)
Phần mềm là một thành phần trong hệ thống gồm phần 
cứng, dữ liệu, con người, quy trình.
✓ Làm đúng sản phẩm & đúng cách
Design Thinking xác định “xây cái gì”; Agile quyết định “xây 
như thế nào”.
3

## Slide 4
L E A R N I N G  O U T C O M E S
Mục tiêu của chương
Sau khi hoàn thành chương này, người học có khả năng:
1 Hiểu khái niệm và vai trò chiến lược của Phân tích Yêu cầu Phần mềm trong vòng đời phát triển phần mềm.
2 Phân biệt và phân loại các nhóm yêu cầu: Nghiệp vụ, Người dùng, Hệ thống (chức năng & phi chức năng) và Ràng buộc.
3 Nắm vững các đặc tính chất lượng của một yêu cầu tốt: đúng đắn, nhất quán, rõ ràng, khả thi, kiểm chứng, truy vết.
4 Mô tả các bước chính trong quy trình phân tích yêu cầu: Inception, Elicitation, Elaboration, Negotiation, Specification, Validation, Management.
5 Nhận diện và phân tích các thách thức, rủi ro phổ biến liên quan đến yêu cầu phần mềm (Scope creep, xung đột yêu cầu…).
4

## Slide 5
A G E N D A
Nội dung chương 1
1.1 Công nghệ phần mềm và lịch sử phát triển
Từ Fortran/COBOL đến CMM, CMMI và tư duy hệ thống 
hiện đại.
1.2 Khái niệm và vai trò của yêu cầu phần mềm
Định nghĩa, tầm quan trọng, vị trí trong vòng đời & quy 
trình 7 bước.
1.3 Các loại yêu cầu phần mềm
Nghiệp vụ – Người dùng – Hệ thống (phần mềm/phần 
cứng) – Ràng buộc.
1.4 Các đặc tính của yêu cầu tốt
Đúng đắn, nhất quán, đầy đủ, rõ ràng, khả thi, kiểm 
chứng, truy vết.
1.5 Thách thức trong phân tích yêu cầu
Giao tiếp, yêu cầu thay đổi liên tục, xung đột giữa các yêu 
cầu.
? Câu hỏi ôn tập & bài tập thực hành
6 câu hỏi lý thuyết và 2 bài tập vận dụng cuối chương.
5

## Slide 6
1.1
Công nghệ phần mềm
và lịch sử phát triển
Từ những ngôn ngữ lập trình đầu tiên đến tư duy hệ thống toàn diện — vì sao yêu cầu phần 
mềm ngày càng trở nên phức tạp và quan trọng.

## Slide 7
1 . 1  L Ị C H  S Ử  P H Á T  T R I Ể N
Những cột mốc hình thành ngành Kỹ nghệ phần mềm
1950s Ngôn ngữ lập trình đầu tiên Fortran, ALGOL, PL/I, COBOL ra đời — nhu cầu áp dụng nguyên tắc kỹ thuật có hệ thống.
1960s Thuật ngữ “Software Engineering” Được sử dụng rộng rãi từ giữa thập niên 1960, đánh dấu sự trưởng thành của lĩnh vực.
1972 David Parnas Tính mô-đun (modularity) và ẩn thông tin (information hiding) — nền tảng cho hệ thống lớn.
1990s Mô hình CMM Phần mềm là sản phẩm độc lập, được xây dựng qua các quy trình bảo đảm chất lượng.
2006 Mô hình CMMI Phần mềm là một thành phần trong hệ thống hoàn chỉnh: phần cứng, dữ liệu, con người, quy trình.
7

## Slide 8
1 . 1  B Ố I  C Ả N H
Yêu cầu đặt lên phần mềm không ngừng gia tăng
TRƯỚC ĐÂY
Chương trình đơn nhiệm
chạy trên một máy đơn lẻ
NGÀY NAY
Môi trường phân tán, dữ liệu lớn,
hiệu năng – an toàn – mở rộng – UX
▲ Số lượng yêu cầu
Nhiều hơn, đến từ nhiều bên liên 
quan khác nhau.
◆ Độ đa dạng
Chức năng, hiệu năng, bảo mật, 
tương thích, trải nghiệm.
✱ Mức độ phức tạp
Ràng buộc kỹ thuật, pháp lý và tổ 
chức đan xen nhau.
→ Không phân tích và quản lý tốt yêu cầu ngay từ đầu, dự án dễ đi chệch mục tiêu, phát sinh chi phí lớn hoặc thất bại.
8

## Slide 9
1 . 1  C H U Y Ể N  D Ị C H  T Ư  D U Y
Từ CMM đến CMMI: từ phần mềm đến hệ thống
M CMM (giữa thập niên 1990)
Capability Maturity Model
• Xem phần mềm như một sản phẩm độc lập
• Xây dựng qua các quy trình cụ thể
• Mục tiêu: bảo đảm chất lượng và tính ổn định
• Trọng tâm: quy trình phát triển phần mềm
I CMMI (từ 2006)
Capability Maturity Model Integration
• Phần mềm là thành phần của một hệ thống hoàn 
chỉnh
• Bao gồm phần cứng, dữ liệu, con người, quy trình vận 
hành
• Phạm vi mở rộng: tư duy hệ thống toàn diện
• Phần mềm vừa là sản phẩm, vừa là phương tiện, vừa 
là nền tảng
Hệ quả: Phân tích yêu cầu không còn dừng ở việc xác định chức năng cần lập trình, mà phải tiếp cận theo tư duy hệ thống — hiểu 
mục tiêu nghiệp vụ, nhu cầu người dùng, môi trường triển khai, tương tác phần cứng và các ràng buộc kỹ thuật, pháp lý, tổ chức.
9

## Slide 10
1.2
Khái niệm và vai trò
của yêu cầu phần mềm
Yêu cầu phần mềm là gì, vì sao “thấu hiểu” yêu cầu quyết định thành bại của dự án, và quy 
trình 7 bước của kỹ nghệ yêu cầu.

## Slide 11
1 . 2 . 1  Đ Ị N H  N G H Ĩ A
Yêu cầu phần mềm là gì?
“Yêu cầu phần mềm là sự mô tả về một dịch vụ mà hệ thống phải cung cấp, một ràng buộc về hiệu năng mà 
hệ thống phải tuân thủ, hoặc một điều kiện mà hệ thống phải đáp ứng.”
1 Một DỊCH VỤ
Hệ thống phải cung cấp chức 
năng gì cho người dùng.
2 Một RÀNG BUỘC
Về hiệu năng, chất lượng mà hệ 
thống phải tuân thủ.
3 Một ĐIỀU KIỆN
Hệ thống phải đáp ứng để được 
chấp nhận / vận hành.
Kỹ nghệ yêu cầu (Requirements Engineering – RE)
Là một quy trình có cấu trúc bao gồm các hoạt động: khai thác → phân tích → đặc tả → thẩm định → quản lý yêu cầu. Mọi dự án 
phần mềm đều bắt đầu bằng việc hiểu rõ vấn đề cần giải quyết và xác định kết quả quan trọng đối với các bên liên quan.
11

## Slide 12
1 . 2 . 1  V Ì  S A O  Q U A N  T R Ọ N G
Cái giá phải trả khi không đầu tư đủ cho yêu cầu
✗
Làm lại tốn kém
Rework
✗
Vượt chi phí
Cost overrun
✗
Chất lượng kém
Poor quality
✗
Giao hàng trễ
Late delivery
✗
Khách hàng không hài lòng
Dissatisfaction
✗
Tinh thần nhóm giảm sút
Low morale
Cân bằng cần thiết:  Kỹ nghệ yêu cầu không được kéo dài vô tận — phải chuyển sang giai đoạn xây dựng sản phẩm đúng 
thời điểm. Đây chính là tinh thần của EDUF (Enough Design Up Front).
12

## Slide 13
1 . 2 . 2  T Ầ M  Q U A N  T R Ọ N G
Thực hành theo ngữ cảnh & Thiết kế vừa đủ
Scott Ambler: khái niệm “thực hành tốt nhất” (best practices) thường không thực tế, thậm chí dẫn đến giải pháp sai lầm. Ông 
đề xuất “thực hành theo ngữ cảnh” (contextual practice) — phù hợp với tư duy Design Thinking.
BDUF
Big Design Up Front
Thiết kế quá kỹ ở giai đoạn đầu — nặng 
nề, chậm thích ứng với thay đổi.
EDUF
Enough Design Up Front
Thiết kế VỪA ĐỦ ở giai đoạn đầu —
quan điểm được thống nhất trong giáo 
trình.
NDUF
No Design Up Front
Không thiết kế gì cả — rủi ro sai hướng, 
chi phí sửa chữa rất lớn.
“Thiết kế quá chi tiết là ngốc nghếch, nhưng không thiết kế gì cả thậm chí còn ngốc nghếch hơn.” — Dave Thomas (Agile 
Manifesto)
Vấn đề không phải là CÓ thực hiện phân tích yêu cầu hay không, mà là THỰC HIỆN NÓ NHƯ THẾ NÀO.
13

## Slide 14
1 . 2 . 3  V Ị  T R Í  T R O N G  V Ò N G  Đ Ờ I
“Hiểu” là chưa đủ — phải THẤU HIỂU
Bốn câu hỏi tưởng chừng đơn giản nhưng quyết định thành bại của dự án:
• Khách hàng (customer) có thực sự biết những gì họ đang yêu cầu hay không?
• Người dùng cuối (end-user) có hiểu rõ tính năng nào sẽ mang lại lợi ích cho họ?
• Phần mềm chúng ta tạo ra có thực sự cần thiết, hay chỉ phô diễn các chức năng mơ hồ?
• Các chức năng đó có gây thêm khó khăn (thậm chí gây hại) cho người sử dụng không?
Nói một cách đơn giản: phân tích yêu cầu phần mềm là xác định cho bằng được ĐÂU LÀ YÊU CẦU CẦN THIẾT để xây 
dựng, và đâu là các yêu cầu kém cần thiết hơn trong giai đoạn hiện tại.
Xây dựng công cụ phần mềm có chức năng phù hợp, dễ sử dụng luôn là tiêu chí hàng đầu, đứng trên các tiêu chí khác khi bàn về 
chuẩn mực của một phần mềm tốt.
14

## Slide 15
H Ì N H  1 . 2
Quy trình 07 bước trong phân tích yêu cầu phần mềm
Nguồn: Pressman [3], [4] — quy trình mang tính tượng trưng, được thực hiện theo tiếp cận lặp (iterative) và tiến hoá không ngừng.
15

## Slide 16
Q U Y  T R Ì N H  7  B Ư Ớ C
Bước 1 – Khởi đầu & Bước 2 – Khai thác
1 Khởi đầu (Inception)
Câu hỏi đặt ra:
• Dự án phần mềm bắt đầu như thế nào?
• Có sự kiện đơn lẻ nào là chất xúc tác, hay nhu cầu tiến 
triển theo thời gian?
Kết quả cần đạt:
• Hiểu biết cơ bản về vấn đề và người muốn có giải pháp
• Bản chất của giải pháp mong muốn
• Giao tiếp & hợp tác sơ bộ giữa các bên
2 Khai thác (Elicitation)
Hỏi khách hàng & người dùng:
• Mục tiêu của hệ thống/sản phẩm là gì?
• Cần hoàn thành những gì?
• Phù hợp với nhu cầu kinh doanh ra sao?
• Sẽ được sử dụng hàng ngày như thế nào?
Kết quả cần đạt:
• Thiết lập mục tiêu nghiệp vụ (business goals)
• Cơ chế ưu tiên (prioritization mechanism)
• Cơ sở lý luận thiết kế (design rationale)
16

## Slide 17
Q U Y  T R Ì N H  7  B Ư Ớ C
Bước 3 – Xây dựng chi tiết & Bước 4 – Đàm phán
3 Xây dựng chi tiết (Elaboration)
Thông tin thu thập từ Inception và Elicitation được MỞ RỘNG 
và TINH CHỈNH. Được thúc đẩy bởi việc tạo ra và tinh chỉnh các 
kịch bản người dùng (user scenarios) mô tả cách người dùng 
cuối và các tác nhân khác tương tác với hệ thống.
4 Đàm phán (Negotiation)
Sử dụng phương pháp lặp (iterative) để ưu tiên yêu cầu, đánh 
giá chi phí và rủi ro, giải quyết xung đột nội bộ. Các yêu cầu 
được LOẠI BỎ, KẾT HỢP hoặc ĐIỀU CHỈNH sao cho mỗi bên đạt 
được mức độ hài lòng nhất định.
Ghi nhớ: Phân tích yêu cầu KHÔNG chỉ là giai đoạn đầu của mô hình thác nước
Đây là một quá trình xuyên suốt theo tiếp cận Agile kết hợp Design Thinking. Quy trình 7 bước mang tính tượng trưng, không phải là 
duy nhất — nó được thực hiện theo tiếp cận LẶP (iterative) và tiến hoá không ngừng, với công cụ mô hình hoá trọng tâm là UML.
17

## Slide 18
Q U Y  T R Ì N H  7  B Ư Ớ C
Bước 5 – Đặc tả & Bước 6 – Xác nhận
5 Đặc tả (Specification)
Bản đặc tả có thể là:
• Một tài liệu viết
• Một tập hợp các mô hình đồ hoạ
• Một mô hình toán học hình thức
• Một bộ sưu tập các kịch bản sử dụng
• Một bản thử nghiệm (prototype)
• Hoặc bất kỳ sự kết hợp nào
SRS (Software Requirements Specification): mô tả chi tiết mọi khía 
cạnh của phần mềm, được xác định rõ trước khi dự án bắt đầu.
6 Xác nhận (Validation)
Kiểm tra bản đặc tả để bảo đảm:
1 Tất cả yêu cầu phần mềm đã được nêu rõ ràng, không mơ hồ (unambiguously).
2 Các mâu thuẫn (inconsistencies), thiếu sót (omissions) và lỗi đã được phát hiện và sửa chữa.
3 Các sản phẩm công việc phù hợp với tiêu chuẩn đã thiết lập cho quy trình, dự án và sản phẩm.
18

## Slide 19
Q U Y  T R Ì N H  7  B Ư Ớ C
Bước 7 – Quản lý yêu cầu (Requirements Management)
Yêu cầu đối với các hệ thống dựa trên máy tính luôn thay đổi, và mong muốn thay đổi tồn tại trong SUỐT VÒNG ĐỜI của hệ 
thống. Quản lý yêu cầu là tập hợp các hoạt động giúp đội dự án xác định, kiểm soát và theo dõi yêu cầu cùng các thay đổi tại 
bất kỳ thời điểm nào.
Áp dụng Quản lý cấu hình phần mềm (SCM) vào yêu cầu
① Nhận dạng
Identification — Gán ID/mã số 
duy nhất cho mỗi yêu cầu để dễ 
dàng theo dõi.
② Kiểm soát phiên bản
Version Control — Ghi lại lịch sử: 
ai thay đổi, thay đổi khi nào và 
thay đổi cái gì.
③ Kiểm soát thay đổi
Change Control — Mọi thay đổi 
phải qua quy trình phê duyệt 
chính thức (Change Control 
Board).
SCM là kỹ thuật được thiết lập vững chắc trong kỹ nghệ phần mềm, chuyên kiểm soát các phiên bản của thành phần phần mềm: mã nguồn, 
tài liệu, dữ liệu.
19

## Slide 20
V Í  D Ụ  M I N H  H O Ạ
Áp dụng quy trình 7 bước: App đặt lịch cắt tóc
1 Inception Chủ chuỗi salon nhận thấy khách phải chờ lâu, muốn có app đặt lịch. Xác định bên liên quan: chủ chuỗi, quản lý cửa hàng, thợ, khách hàng.
2 Elicitation Phỏng vấn 5 quản lý cửa hàng, khảo sát 200 khách, quan sát quy trình tại 2 salon vào giờ cao điểm.
3 Elaboration Xây kịch bản: “Khách chọn cửa hàng → chọn thợ → chọn khung giờ → xác nhận → nhận nhắc lịch”.
4 Negotiation Chủ muốn thanh toán online ngay bản 1.0; ngân sách không đủ → chuyển sang bản 1.1 (Should have).
5 Specification Viết SRS: 24 use case, 8 yêu cầu phi chức năng, kèm wireframe và mô hình UML.
6 Validation Rà soát SRS cùng khách hàng: phát hiện thiếu quy tắc huỷ lịch trước 2 giờ → bổ sung.
7 Management Mỗi yêu cầu có mã REQ-xxx trên Jira, mọi thay đổi qua Change Control Board của dự án.
20

## Slide 21
1.3
Các loại yêu cầu
phần mềm
Bốn nhóm yêu cầu: Nghiệp vụ – Người dùng – Hệ thống – Ràng buộc; và mối quan hệ phân 
cấp giữa chúng.

## Slide 22
1 . 3  M Ở  Đ Ầ U
Vì sao phải phân loại yêu cầu?
① Giúp giao tiếp và xác nhận dễ dàng hơn
Tránh nhầm lẫn giữa chức năng, phi chức năng, nghiệp vụ và ràng buộc; các bên liên quan dễ trao đổi, hạn chế hiểu sai hoặc bỏ sót 
yêu cầu quan trọng.
② Giúp thiết kế và phát triển chính xác, có định hướng
Chức năng quyết định logic xử lý; phi chức năng chi phối kiến trúc và hiệu năng; ràng buộc định hình những giới hạn phải tuân theo.
③ Giúp quản lý dự án hiệu quả hơn
Ưu tiên yêu cầu, ước lượng chính xác, thiết kế ca kiểm thử phù hợp → giảm rủi ro, kiểm soát phạm vi, đáp ứng đúng nhu cầu.
Phát triển hệ thống không chỉ cần hiểu “cần làm gì”, mà còn phải nắm rõ “vì sao cần làm”, “làm như thế nào tốt nhất” 
và “những giới hạn phải tuân theo”.
22

## Slide 23
H Ì N H  1 . 3
Sơ đồ phân loại các yêu cầu phần mềm
1 Yêu cầu nghiệp vụ
Business requirements — vì sao dự án được thực hiện.
2 Yêu cầu người dùng
User requirements — người dùng cần hệ thống làm gì 
cho họ.
3 Yêu cầu hệ thống
System requirements — phần mềm & phần cứng phải 
làm gì.
4 Các ràng buộc
Constraints — điều kiện môi trường để đưa phần mềm 
vào vận hành.
3 nhóm đầu phân loại theo mức độ nắm bắt sâu về hệ thống; 
nhóm thứ 4 liên quan đến điều kiện môi trường vận hành.
23

## Slide 24
1 . 3 . 1  B U S I N E S S  R E Q U I R E M E N T S
Yêu cầu nghiệp vụ — trả lời câu hỏi “VÌ SAO”
Tập trung trả lời: vì sao dự án được thực hiện, lợi ích mong muốn là gì, và những quy tắc vận hành mà hệ thống phải tuân theo. 
Đây là nền tảng định hướng toàn bộ giải pháp.
1 Business Objectives — Mục tiêu nghiệp vụ
Mục tiêu cụ thể doanh nghiệp muốn đạt: cải thiện hiệu suất, giảm chi phí, tăng doanh thu, nâng cao trải nghiệm khách hàng. Giúp 
xác định phạm vi, ưu tiên và giá trị cốt lõi.
2 Business Rules / Policies — Quy tắc & chính sách
Quy định, chuẩn mực, luật lệ chi phối hoạt động: quy tắc nghiệp vụ, chính sách nội bộ, quy trình phê duyệt, tuân thủ pháp lý, chuẩn 
ngành. Hệ thống KHÔNG được vi phạm.
3 Business Value Expected — Giá trị mong đợi
Hữu hình: tăng năng suất, tăng doanh thu, tối ưu chi phí. Vô hình: nâng tầm thương hiệu, cải thiện trải nghiệm, ra quyết định dựa 
trên dữ liệu. Là căn cứ đánh giá thành công.
Thường hình thành ngay từ giai đoạn đầu — thậm chí trước khi dự án ra đời: thuyết minh/đề cương (dự án nghiên cứu) hoặc bản đề xuất ý 
tưởng (dự án kinh tế). 24

## Slide 25
1 . 3 . 2  U S E R  R E Q U I R E M E N T S
Yêu cầu người dùng — “Họ cần hệ thống làm gì cho họ?”
Khác với yêu cầu nghiệp vụ (tập trung vào mục tiêu tổ chức), yêu cầu người dùng phản ánh góc nhìn của người sử dụng thực tế —
bảo đảm hệ thống thân thiện, dễ dùng, giải quyết đúng vấn đề của họ.
1
User Goals
Mục tiêu người dùng
Người dùng cần làm gì
Lợi ích họ muốn nhận được
Vấn đề muốn được hỗ trợ giải quyết
→ Định hướng thiết kế trải nghiệm và xác 
định chức năng cốt lõi.
2
User Stories
Câu chuyện người dùng
Mô tả ngắn gọn nhu cầu theo mẫu:
“Ở vai trò ..., tôi muốn ..., do vậy tôi cần 
phần mềm làm cho tôi ...”
→ Linh hoạt, dễ ưu tiên, phù hợp Agile.
3
High-level Use Cases
Use case cấp cao
Các tác nhân (actors)
Mục tiêu tương tác
Luồng hoạt động chính
Quan hệ người dùng – chức năng
→ Rõ ràng hơn User Story, vẫn ở mức 
tổng quan.
Ví dụ User Story: “Ở vai trò khách hàng, tôi muốn xem các khung giờ còn trống của thợ mình yêu thích, để đặt lịch mà không phải gọi điện tới 
cửa hàng.”
25

## Slide 26
1 . 3 . 3  S Y S T E M  R E Q U I R E M E N T S
Yêu cầu hệ thống — biến nhu cầu thành giải pháp
Mô tả hệ thống PHẢI LÀM GÌ và CÁCH NÓ VẬN HÀNH, dựa trên mục tiêu nghiệp vụ và nhu cầu người dùng. Là cơ sở cho thiết 
kế, phát triển và kiểm thử phần mềm.
Yêu cầu phần mềm
Software Requirements
• Yêu cầu chức năng (Functional Requirements)
• Yêu cầu phi chức năng (Non-functional Requirements)
• Mô tả tính năng, hành vi, dữ liệu và thuộc tính chất 
lượng
• Cầu nối giữa yêu cầu hệ thống và thiết kế kỹ thuật
Yêu cầu phần cứng
Hardware Requirements
• Các thành phần vật lý cần thiết để triển khai
• Bảo đảm vận hành ổn định và đạt hiệu năng mong 
muốn
• Quan trọng với hệ thống cần hạ tầng riêng, dữ liệu lớn
• Hoặc kết nối với thiết bị chuyên dụng
26

## Slide 27
Y Ê U  C Ầ U  P H Ầ N  M Ề M
Yêu cầu chức năng (Functional Requirements)
Mô tả những hành vi và chức năng cụ thể hệ thống phải thực hiện — quyết định phần mềm sẽ “LÀM GÌ” và “VẬN HÀNH NHƯ THẾ 
NÀO” trong từng tình huống.
1 Business Functions — Chức năng nghiệp vụ
Tác vụ hệ thống hỗ trợ người dùng / bộ phận nghiệp vụ · 
Các màn hình, module, nhóm tính năng · Các hành động 
nghiệp vụ. Đây là “xương sống” của giải pháp.
2 Processing Logic / Workflow — Quy trình xử lý
Luồng xử lý chính và phụ · Điều kiện rẽ nhánh, ngoại lệ · 
Quy tắc kiểm tra nghiệp vụ · Cách hệ thống phản hồi theo 
từng tình huống.
3 Data Management — Quản lý dữ liệu
Tạo, đọc, cập nhật, xoá (CRUD) · Quy tắc xác thực và kiểm 
tra dữ liệu · Quản lý trạng thái, lịch sử, nhật ký · Danh mục, 
bảng dữ liệu, hồ sơ, đối tượng nghiệp vụ.
4 System Interactions — Tương tác hệ thống
Tích hợp API (RESTful, MCP AI Agents…) · Gửi/nhận dữ liệu 
với phần mềm nội bộ hoặc bên ngoài · Tương tác thiết bị 
(máy quét, cảm biến, POS) · Đồng bộ dữ liệu, gọi dịch vụ.
27

## Slide 28
Y Ê U  C Ầ U  P H Ầ N  M Ề M
Yêu cầu phi chức năng (Non-functional Requirements)
Không nói hệ thống LÀM GÌ, mà mô tả MỨC ĐỘ TỐT khi hệ thống thực hiện chức năng của mình — quyết định tính tin cậy, hiệu quả 
và khả năng vận hành lâu dài.
1
Hiệu năng  ·  Performance
Thời gian phản hồi, số người dùng đồng thời, giao dịch/giây, tối ưu 
CPU–RAM.
2
Bảo mật  ·  Security
Xác thực, phân quyền, mã hoá, kiểm soát truy cập, phòng chống tấn 
công.
3
Độ tin cậy  ·  Reliability
Tỷ lệ lỗi cho phép, khả năng tự phục hồi, tính nhất quán của dữ liệu.
 4
Tính sẵn sàng  ·  Availability
Thời gian uptime, khả năng dự phòng, phục hồi sau sự cố (24/7).
5
Khả năng mở rộng  ·  Scalability
Mở rộng người dùng, dữ liệu, giao dịch — theo chiều ngang hoặc 
dọc.
6
Khả năng bảo trì  ·  Maintainability
Mã rõ ràng, tách lớp/module hoá, log–giám sát–cảnh báo, dễ debug.
7
Tính dễ sử dụng  ·  Usability & UI/UX
Giao diện thân thiện, dễ học dễ nhớ, nhất quán, hỗ trợ đa thiết bị.
 8
Khả năng tương thích  ·  Compatibility
Hệ điều hành, trình duyệt, thiết bị, chuẩn API và chuẩn dữ liệu.
28

## Slide 29
Q U A N  H Ệ  F R  ↔ N F R
Chức năng và phi chức năng ảnh hưởng trực tiếp lẫn nhau
Hai nhóm yêu cầu này có quan hệ RẤT CHẶT CHẼ: một thay đổi ở yêu cầu phi chức năng có thể ảnh hưởng đến cả kiến 
trúc phần mềm và phát sinh thêm các yêu cầu chức năng mới.
Ví dụ minh hoạ
NFR
Yêu cầu bảo mật:
“Tài khoản có số dư > 50 triệu phải 
được bảo vệ nhiều lớp”
FR mới
Phát sinh chức năng:
Chứng thực hai lớp bằng mã OTP hoặc 
sinh trắc học
Kiến trúc
Ảnh hưởng thiết kế:
Thêm dịch vụ OTP, hàng đợi tin nhắn, 
lưu trữ sinh trắc học
→ Khi phân tích, không bao giờ tách rời chức năng khỏi các thuộc tính chất lượng: mỗi ràng buộc chất lượng đều có “cái giá” về 
chức năng và kiến trúc.
29

## Slide 30
1 . 3 . 3  H A R D W A R E  R E Q U I R E M E N T S
Yêu cầu phần cứng — 7 nhóm thành phần vật lý
1
Máy chủ (CPU/RAM/Storage)
Công suất CPU, RAM, dung lượng & tốc độ lưu trữ; vật lý hoặc ảo 
(on-premise/cloud); phân cụm, dự phòng, cân bằng tải.
2
Thiết bị đầu cuối (Client Devices)
PC, laptop, điện thoại, máy tính bảng, POS, kiosk, máy quét; yêu cầu 
tối thiểu về CPU, RAM, độ phân giải.
3
Yêu cầu điện năng (Power)
Nguồn dự phòng UPS/máy phát, ổn định điện áp, công suất thiết bị, 
chống mất điện đột ngột.
4
Hệ thống lưu trữ (Storage Systems)
NAS, SAN hoặc lưu trữ phân tán; tốc độ đọc/ghi; dung lượng & khả 
năng mở rộng; sao lưu – phục hồi.
5
Hạ tầng mạng (Network)
Router, switch, firewall; đường truyền Internet/LAN/WAN; băng 
thông, độ trễ; cân bằng tải, mạng dự phòng.
6
Thiết bị an ninh (Security)
Firewall phần cứng, IDS/IPS, camera giám sát, khoá phòng server, 
thiết bị kiểm soát ra vào.
7
Thiết bị chuyên dụng (Specialized)
Máy quét mã vạch/RFID, thiết bị IoT, cảm biến, camera AI, máy đo – máy theo dõi (y tế, công nghiệp).
30

## Slide 31
1 . 3 . 4  C O N S T R A I N T S
Các ràng buộc — giới hạn cách thức thực hiện dự án
Không mô tả chức năng hay chất lượng hệ thống, nhưng ảnh hưởng TRỰC TIẾP đến việc lựa chọn giải pháp và cách thực hiện dự án.
1 Công nghệ bắt buộc
Ngôn ngữ lập trình, framework, hệ điều hành, CSDL được chỉ định; nền tảng 
cloud cố định (AWS/Azure/GCP); tương thích hệ thống hiện có.
2 Pháp lý & tiêu chuẩn ngành
GDPR, HIPAA; quy định kế toán – tài chính – ngân hàng; chuẩn ISO, PCI-DSS, 
HL7, SOC2; yêu cầu lưu trữ, kiểm toán, minh bạch.
3 Ngân sách & tiến độ
Ngân sách tối đa được phê duyệt; deadline cố định; sprint/timebox hạn chế; 
giới hạn nguồn lực (nhân sự, thiết bị).
4 Giới hạn hạ tầng
Băng thông và thiết bị mạng sẵn có; máy chủ cũ, cấu hình hạn chế; không 
gian lưu trữ giới hạn; bắt buộc on-premise hoặc cloud.
5 Tích hợp hệ thống cũ
API cũ / giao thức lỗi thời; CSDL cũ cần duy trì; giới hạn định dạng dữ liệu; 
không được thay đổi hệ thống gốc; kế thừa logic cũ.
6 Quy trình & chính sách nội bộ
Quy trình phê duyệt, báo cáo, kiểm thử; chính sách bảo mật nội bộ; quản lý 
thay đổi; SLA nội bộ; chuẩn coding, guideline thiết kế.
31

## Slide 32
V Í  D Ụ  M I N H  H O Ạ
Phân loại yêu cầu: Hệ thống Thư viện điện tử của Trường
Nghiệp vụ Giảm 50% thời gian sinh viên chờ mượn/trả sách trong năm học 2026–2027; mọi giao dịch mượn phải được ghi nhận theo quy chế thư viện.
Người dùng “Ở vai trò sinh viên, tôi muốn tra cứu và giữ chỗ sách qua điện thoại, để không phải đến thư viện mới biết sách còn hay hết.”
Chức năng Hệ thống cho phép sinh viên giữ chỗ tối đa 3 đầu sách trong 24 giờ; tự động huỷ giữ chỗ và thông báo nếu quá hạn.
Phi chức năng Kết quả tra cứu trả về dưới 2 giây với 500 người dùng đồng thời; mật khẩu được mã hoá; hệ thống sẵn sàng 99,5% trong giờ hành chính.
Phần cứng 02 máy chủ ảo 8 vCPU / 16 GB RAM; 05 máy quét mã vạch tại quầy; UPS bảo đảm 30 phút khi mất điện.
Ràng buộc Phải tích hợp với hệ thống quản lý sinh viên hiện có qua API cũ; triển khai trên hạ tầng on-premise của Trường; hoàn thành trong 6 tháng.
32

## Slide 33
1.4
Các đặc tính của
yêu cầu tốt
Design Thinking và Agile giúp tạo ra yêu cầu; các đặc tính chất lượng là chuẩn mực mà mọi 
yêu cầu phải đáp ứng.

## Slide 34
1 . 4  N Ề N  T Ả N G  P H Ư Ơ N G  P H Á P
Design Thinking & Agile — hai nửa của một bài toán
Design Thinking
“Làm ĐÚNG sản phẩm” — Chúng ta nên xây dựng cái gì?
• Empathize — Thấu hiểu người dùng
• Define — Xác định đúng vấn đề
• Ideate — Sáng tạo ý tưởng
• Prototype — Tạo mẫu thử
• Test — Kiểm thử với người dùng thật
Agile
“Làm sản phẩm ĐÚNG CÁCH” — Xây nó như thế nào cho 
hiệu quả?
• Phát triển lặp lại qua các sprint ngắn
• Liên tục mang lại giá trị cho khách hàng
• Giao sản phẩm hoạt động được thường xuyên
• Hợp tác chặt chẽ với khách hàng
• Thích nghi nhanh với thay đổi
Design Thinking và Agile đóng vai trò KIẾN TẠO (hình thành, thu thập, tinh chỉnh yêu cầu); các đặc tính của yêu cầu tốt là CHUẨN
CHẤT LƯỢNG mà mọi yêu cầu phải đáp ứng.
34

## Slide 35
1 . 4  C Ầ U  N Ố I  K Ỹ  T H U Ậ T
Design Pattern & Architectural Pattern
Để chuyển các yêu cầu kinh doanh và người dùng thành một hệ thống hoạt động thực sự — đặc biệt là đáp ứng các Yêu 
cầu Phi chức năng (NFR) như hiệu năng, bảo mật, khả năng mở rộng — chúng ta cần một công cụ ở mức độ THIẾT KẾ.
◆ Design Pattern (Mẫu Thiết kế)
Khuôn mẫu giải pháp kỹ thuật đã được kiểm chứng và tái 
sử dụng cho các vấn đề thiết kế phổ biến ở mức thành 
phần.
▣ Architectural Pattern (Mẫu Kiến trúc)
Khuôn mẫu ở mức kiến trúc hệ thống, được hệ thống hoá 
trong “Pattern-Oriented Software Architecture” 
(Buschmann và cộng sự) [5].
Vai trò: Design Pattern là CẦU NỐI KỸ THUẬT, giúp kiến trúc sư biến các NFR trừu tượng thành một cấu trúc hệ thống vững 
chắc — bảo đảm hệ thống được xây trên nền tảng kiến trúc tốt, thoả mãn các yêu cầu chất lượng cao ngay từ đầu.
35

## Slide 36
1 . 4 . 1  – 1 . 4 . 2
Đúng đắn & Nhất quán · Đầy đủ & Rõ ràng
Tính ĐÚNG ĐẮN Design Thinking
Qua Empathize và Test, đội ngũ tiếp cận trực tiếp người dùng để xác 
nhận yêu cầu có phản ánh đúng vấn đề. Prototype giúp kiểm chứng 
sớm các giả định → giảm nguy cơ “xây nhầm thứ người dùng không 
cần”.
Tính NHẤT QUÁN Agile
Duy trì qua nhịp lặp và giao tiếp liên tục: Daily Scrum, Sprint 
Planning, Sprint Review. User Stories thay cho tài liệu dài dòng → 
yêu cầu rõ ràng, nhỏ gọn, dễ điều chỉnh; mâu thuẫn được phát hiện 
sớm.
Tính RÕ RÀNG Design Thinking
Công cụ trực quan: Persona, Customer Journey Map, Storyboard, 
mô hình ngữ cảnh — mô tả hành vi, mục tiêu, cảm xúc của người 
dùng trong từng bước tương tác → giảm mơ hồ, thống nhất hình 
dung.
Tính ĐẦY ĐỦ Agile
User Story nhỏ, độc lập theo tiêu chí INVEST; kèm Acceptance 
Criteria và Definition of Done; mô hình 3C (Card – Conversation –
Confirmation) bảo đảm mọi chi tiết được làm rõ trước khi thực 
hiện.
36

## Slide 37
1 . 4 . 3
Tính khả thi và kiểm chứng
Một yêu cầu tốt không chỉ “hay trên giấy” — nó phải KHẢ THI để thực hiện và KIỂM CHỨNG ĐƯỢC bằng các tiêu chí rõ ràng, khách 
quan.
Tính KHẢ THI
Design Thinking — thử nghiệm sớm
• Prototype kiểm tra trước khi đầu tư phát triển thật
• Khả thi KỸ THUẬT — có làm được không?
• Khả thi KINH DOANH — có tạo giá trị đủ lớn không?
• Mức độ chấp nhận của người dùng
• Loại bỏ ý tưởng không khả thi từ sớm
Tính KIỂM CHỨNG
Agile — tiêu chí chấp nhận rõ ràng
• Mỗi User Story kèm Acceptance Criteria cụ thể, đo 
lường được
• Là cơ sở để QA và các bên xác định yêu cầu đã đạt 
hay chưa
• Yêu cầu trở nên verifiable và minh bạch khi nghiệm 
thu
• Ngăn ngừa diễn giải sai lệch giữa các bên
Phản ví dụ: “Hệ thống phải chạy thật nhanh” — không kiểm chứng được.  Viết lại: “95% yêu cầu tra cứu trả kết quả dưới 2 giây với 500 
người dùng đồng thời.”
37

## Slide 38
1 . 4 . 4
Tính truy vết (Traceability)
Cho phép theo dõi yêu cầu từ nguồn gốc ban đầu → thiết kế → phát triển → kiểm thử → nghiệm thu; giúp kiểm soát phạm vi, quản 
lý thay đổi và bảo đảm sản phẩm đáp ứng đúng nhu cầu.
Agile — truy vết trực tiếp và rõ ràng
• Product Backlog & Sprint Backlog theo dõi toàn bộ vòng đời yêu cầu
• Jira / Trello / Azure DevOps: User Story ↔ Task ↔ Test Case ↔ Defect
• Artifact rõ ràng: Backlog, User Story, Acceptance Criteria
• Checkpoint định kỳ: Sprint Planning, Review, Retrospective
• Sprint Backlog cố định trong iteration → kiểm soát thay đổi
Design Thinking — tác động gián 
tiếp
Không tạo ra công cụ truy vết kỹ thuật, nhưng 
hình thành NGUỒN GỐC (source) của yêu cầu: 
thấu hiểu người dùng, xác định vấn đề, thử 
nghiệm sớm → yêu cầu dựa trên dữ liệu thực tế 
và bối cảnh rõ ràng, làm quá trình truy vết về sau 
dễ dàng và có giá trị hơn.
Agile kết hợp được với CMM/CMMI — đáp ứng các Vùng Quy trình: REQM (Quản lý yêu cầu), RD (Phát triển yêu cầu), VER/VAL (Kiểm 
chứng & Xác thực) với truy vết hai chiều.
38

## Slide 39
1 . 4  T Ổ N G  K Ế T
Checklist: một yêu cầu tốt cần đạt những gì?
✓
Đúng đắn  ·  Correct
Phản ánh chính xác nhu cầu thực sự của các bên liên quan.
 ✓
Nhất quán  ·  Consistent
Không mâu thuẫn nội bộ hoặc giữa các thành viên dự án.
✓
Rõ ràng  ·  Unambiguous
Chỉ có một cách hiểu duy nhất; gắn với tình huống sử dụng thực 
tế.
✓
Đầy đủ  ·  Complete
Đủ chi tiết và phạm vi để triển khai; có Acceptance Criteria và 
DoD.
✓
Khả thi  ·  Feasible
Thực hiện được về kỹ thuật, kinh doanh và trong ràng buộc dự 
án.
✓
Kiểm chứng được  ·  Verifiable
Có tiêu chí đo lường khách quan để nghiệm thu.
✓
Truy vết được  ·  Traceable
Theo dõi được từ nguồn gốc đến thiết kế, mã nguồn và kiểm thử.
39

## Slide 40
1.5
Thách thức trong
phân tích yêu cầu
Ba nhóm vấn đề tiêu biểu: giao tiếp với các bên liên quan, yêu cầu thay đổi liên tục và xung 
đột giữa các yêu cầu.

## Slide 41
T H Á C H  T H Ứ C  1
Vấn đề giao tiếp với các bên liên quan
Vấn đề
• Khách hàng, người dùng và đội phát triển có mức độ 
hiểu biết khác nhau về hệ thống
• Người dùng diễn đạt bằng ngôn ngữ tự nhiên → dễ mơ 
hồ
• Đội kỹ thuật quen cách diễn đạt chính xác
Hướng giải quyết
• Quy trình giao tiếp rõ ràng, tài liệu hoá đầy đủ
• Xác nhận yêu cầu liên tục với các bên
• Vai trò trung tâm của Nhà phân tích yêu cầu 
(Requirement Analyst)
Nếu không xử lý tốt…
Yêu cầu bị truyền đạt sai lệch → phát triển không đúng mong muốn → phát sinh lỗi và chi phí sửa đổi rất tốn kém. Đây là lý do Bảng 
1.1 (giáo trình) cho thấy vai trò của nhà phân tích trải dài SUỐT VÒNG ĐỜI dự án — từ Khởi động, Phân tích & Thiết kế, Thiết kế 
thành phần, Cài đặt, Kiểm thử & Đánh giá đến Vận hành & Hỗ trợ — chứ không chỉ ở giai đoạn ban đầu.
41

## Slide 42
B Ả N G  1 . 1
Vai trò của Nhà phân tích yêu cầu (Requirement Analyst)
1 Cộng tác với khách hàng, người dùng, kiến trúc sư và nhà thiết kế để xác định yêu cầu thực sự của hệ thống Toàn vòng đời
2 Làm việc với khách hàng và người dùng để thiết đặt cơ chế kiểm soát thay đổi Từ Thiết kế thành phần
3 Nhận diện những công nghệ mới hữu ích Phân tích – Thiết kế – Vận hành
4 Tạo điều kiện tái sử dụng tài nguyên sẵn có và khả năng nhân bản công nghệ Khởi động → Cài đặt
5 Hỗ trợ hình dung lộ trình tăng trưởng từ phiên bản đầu đến sản phẩm cuối Toàn vòng đời
6 Tư vấn phương pháp, kỹ thuật và công cụ tự động hỗ trợ công việc liên quan đến yêu cầu Khởi động, Phân tích, Vận hành
7 Sử dụng các thước đo để đo lường, theo dõi và kiểm soát hoạt động liên quan đến yêu cầu Toàn vòng đời
8 Thiết đặt môi trường cho các cuộc thảo luận và hoà giải xung đột Toàn vòng đời
9 Nghiên cứu kỹ lưỡng lĩnh vực chuyên môn và các hệ thống đang được sử dụng Khởi động, Phân tích, Vận hành
→ Vai trò của nhà phân tích không kết thúc sau giai đoạn phân tích: đó là một vai trò xuyên suốt dự án. 42

## Slide 43
T H Á C H  T H Ứ C  2
Yêu cầu thay đổi liên tục → nguy cơ Scope Creep
① Biến động thị trường
Đối thủ, khách hàng và công nghệ 
thay đổi trong khi dự án đang 
chạy.
② Thay đổi chiến lược
Doanh nghiệp điều chỉnh mục 
tiêu → yêu cầu đã chốt không còn 
phù hợp.
③ Nhận ra nhu cầu muộn
Người dùng chỉ nhận ra nhu cầu 
thật sau khi trải nghiệm bản mẫu.
Khi thay đổi không được kiểm soát tốt, phạm vi dự án mở rộng vượt khỏi kế hoạch ban đầu — hiện tượng “SCOPE 
CREEP” — ảnh hưởng lớn đến thời gian, chi phí và chất lượng phát triển.
Giải pháp: cơ chế quản lý thay đổi + ưu tiên yêu cầu hợp lý + phương pháp linh hoạt (Agile)
Nguyên lý MoSCoW trong tiếp cận DSDM (Dynamic System Development Method) — một trường phái của Agile — được 
xem là giải pháp tốt nhất cho khả năng ứng xử trước các thay đổi.
43

## Slide 44
H Ì N H  1 . 5
Nguyên lý MoSCoW trong tiếp cận DSDM (Agile)
● Must have
Phải làm — yêu cầu bắt buộc để hệ thống hoạt động đúng mục 
tiêu. Chiếm không quá 60% nỗ lực.
● Should have
Nên làm — quan trọng nhưng không nhất thiết có ở phiên bản 
đầu tiên.
● Could have
Có thể làm — nếu còn đủ thời gian và nguồn lực. Cùng Should 
have chiếm không quá 20% nỗ lực.
● Won't have (this time)
Không thực hiện trong giai đoạn này — được ghi nhận, xem xét 
ở phiên bản sau.
44

## Slide 45
M O S C O W
Vì sao MoSCoW khắc phục được vấn đề thay đổi yêu cầu?
1 Giúp xác định điều gì thật sự quan trọng
Khi yêu cầu thay đổi, nhóm Must have làm rõ phần cốt lõi phải giữ vững — dù thêm hay bớt yêu cầu phụ.
2 Dễ điều chỉnh kế hoạch mà không phá vỡ cấu trúc dự án
Should have và Could have tạo “vùng linh hoạt” để thêm/bớt yêu cầu mà không ảnh hưởng tiến độ và chất lượng phần quan trọng.
3 Ngăn ngừa scope creep
Nhóm Won't have (this time) lưu lại yêu cầu nhưng không thực hiện ngay → thay đổi được quản lý có kiểm soát.
4 Giảm tranh luận cảm tính giữa các bên
Mọi bên hiểu rõ mức độ quan trọng của từng yêu cầu → tránh việc thêm yêu cầu mới tuỳ hứng.
Tóm lại: MoSCoW giúp quản lý yêu cầu một cách có hệ thống — linh hoạt trong thay đổi nhưng vẫn giữ ổn định cho 
phạm vi và tiến độ dự án.
45

## Slide 46
T H Á C H  T H Ứ C  3
Xung đột giữa các yêu cầu — ba “căn bệnh” cần tránh
Buschmann [5] mô tả ba sai lầm mà nhóm phát triển cần tránh — đều bắt nguồn từ sự QUÁ THIÊN LỆCH, dẫn đến mất cân bằng 
nghiêm trọng giữa các yêu cầu.
Featuritis
Hội chứng tham chức năng
Đánh đổi chất lượng tổng thể để lấy phạm 
vi chức năng rộng hơn. Lập trình viên có 
xu hướng triển khai nhanh các chức năng 
dễ, không chú trọng chất lượng.
Hậu quả: Sản phẩm nhiều chức năng nhưng 
hầu hết chất lượng kém.
Flexibilitis
Hội chứng quá linh hoạt
Nhồi nhét quá nhiều khả năng tùy biến và 
cấu hình vào sản phẩm. Hệ thống quá linh 
hoạt thường khó cấu hình và hiệu năng 
kém.
Hậu quả: Hệ thống cồng kềnh, chậm chạp —
“dùng dao mổ trâu giết ruồi”.
Performitis
Hội chứng ám ảnh hiệu năng
Tập trung quá mức vào hiệu năng mà bỏ 
qua các thuộc tính chất lượng khác như 
bảo trì, độ tin cậy, bảo mật.
Hậu quả: Thiếu cân bằng, phát sinh chi phí 
cao không cần thiết.
Giải pháp: Design Thinking — lấy người dùng làm trung tâm, lấy giá trị làm ưu tiên, liên tục thử nghiệm và điều chỉnh → sản 
phẩm cân bằng, thực tế và phù hợp nhu cầu hơn.
46

## Slide 47
T Ổ N G  K Ế T
Tóm tắt Chương 1
1.1
Phần mềm ngày nay là thành phần của một hệ thống hoàn chỉnh (CMM → CMMI) → phân tích yêu cầu phải theo tư duy hệ 
thống.
1.2
Yêu cầu = dịch vụ / ràng buộc hiệu năng / điều kiện hệ thống phải đáp ứng. Quy trình 7 bước: Inception → Elicitation → 
Elaboration → Negotiation → Specification → Validation → Management.
1.3
Bốn nhóm: Nghiệp vụ (vì sao) – Người dùng (cần gì) – Hệ thống (làm gì & vận hành ra sao: phần mềm + phần cứng) – Ràng 
buộc (giới hạn).
1.4
Yêu cầu tốt: đúng đắn, nhất quán, rõ ràng, đầy đủ, khả thi, kiểm chứng được, truy vết được. Design Thinking (làm đúng sản 
phẩm) + Agile (làm đúng cách).
1.5
Ba thách thức: giao tiếp với các bên liên quan · yêu cầu thay đổi liên tục (scope creep → MoSCoW) · xung đột yêu cầu 
(Featuritis, Flexibilitis, Performitis).
47

## Slide 48
C Â U  H Ỏ I  Ô N  T Ậ P  C H Ư Ơ N G  1
Câu 1 – 3
1 Phân tích Yêu cầu phần mềm (SRA) là gì?
Phân tích tầm quan trọng chiến lược của việc “thấu hiểu” yêu cầu trong việc quyết định thành bại của một dự án phần mềm, đặc 
biệt trong bối cảnh hệ thống ngày càng phức tạp (so sánh tư duy CMM và CMMI).
2 Phân loại yêu cầu phần mềm
Trình bày mô hình phân cấp bốn nhóm yêu cầu chính: Nghiệp vụ, Người dùng, Hệ thống và Các Ràng buộc. Cho biết mối quan hệ 
giữa ba nhóm đầu theo mức độ chi tiết và nền tảng.
3 Đặc tính của một yêu cầu tốt?
Liệt kê và giải thích tối thiểu bốn (4) đặc tính quan trọng mà một yêu cầu phần mềm tốt cần đáp ứng: tính đúng đắn và nhất quán,
tính rõ ràng, tính khả thi và kiểm chứng, tính truy vết.
48

## Slide 49
C Â U  H Ỏ I  Ô N  T Ậ P  C H Ư Ơ N G  1
Câu 4 – 6
4 Quy trình phân tích yêu cầu?
Mô tả tóm tắt vai trò và mục tiêu chính của ba bước đầu tiên trong quy trình 7 bước: Khởi đầu (Inception), Khai thác (Elicitation) 
và Xây dựng chi tiết (Elaboration).
5 Thách thức trong phân tích yêu cầu?
Trình bày ba thách thức phổ biến nhất. Giải thích vì sao yêu cầu thay đổi liên tục (Scope Creep) là rủi ro lớn và đề xuất một biện 
pháp đã học trong chương để quản lý rủi ro này hiệu quả.
6 Giải quyết xung đột FR ↔ NFR
Trong giai đoạn phân tích, xung đột giữa Yêu cầu Chức năng và Phi chức năng là phổ biến (ví dụ: tốc độ xử lý cao xung đột với chi 
phí phát triển thấp). Trình bày các bước cơ bản mà Nhà phân tích cần thực hiện để giải quyết và đàm phán những xung đột này.
49

## Slide 50
B À I  T Ậ P  T H Ự C  H À N H
Bài tập 1 — Phân loại và phân biệt yêu cầu
Tình huống: Một công ty muốn phát triển ứng dụng di động cho phép khách hàng đặt lịch cắt tóc và làm đẹp tại các 
cửa hàng của họ.
a Xác định Yêu cầu Nghiệp vụ
Mục tiêu kinh doanh cốt lõi mà ứng dụng cần đạt được là gì? (Ví dụ: tăng doanh thu, giảm thời gian chờ đợi của khách hàng.)
b Phân loại Yêu cầu Hệ thống
Đề xuất 01 Yêu cầu Chức năng và 01 Yêu cầu Phi chức năng (liên quan đến Hiệu năng hoặc Bảo mật) cho ứng dụng này.
c Xác định Yêu cầu Người dùng
Đề xuất 01 yêu cầu viết từ góc độ người dùng cuối (khách hàng), tập trung vào khả năng tương tác với hệ thống — dạng “Người dùng
có thể …”.
Gợi ý: Bám sát Hình 1.3 để không nhầm lẫn giữa bốn nhóm yêu cầu.
50

## Slide 51
B À I  T Ậ P  T H Ự C  H À N H
Bài tập 2 — Phân tích và đàm phán yêu cầu
Hệ thống Quản lý Kho hàng (WMS) — hai yêu cầu từ hai bên liên quan khác nhau:
Yêu cầu A — Quản lý Kho
“Hệ thống phải cho phép nhân viên nhập kho chỉ sử dụng giọng 
nói để xác nhận đơn hàng, nhằm giảm thiểu tiếp xúc vật lý.”
Yêu cầu B — Giám đốc Công nghệ
“Toàn bộ dữ liệu kho phải đồng bộ với hệ thống kế toán trong 
thời gian thực (dưới 100 ms) và mở rộng được để xử lý ít nhất 
5.000 giao dịch mỗi phút.”
1 Phân tích đặc tính (Critique)
Dựa trên các đặc tính của một yêu cầu tốt (mục 1.4), chỉ ra 
các vấn đề về TÍNH KHẢ THI và TÍNH KIỂM CHỨNG của Yêu 
cầu B.
2 Giải quyết xung đột (Negotiation)
Giả sử Yêu cầu A gây chi phí phát triển vượt ngân sách 
40%. Là Nhà phân tích, bạn đàm phán với Quản lý Kho ra 
sao để vừa tiết kiệm chi phí, vừa đạt mục tiêu nghiệp vụ 
cốt lõi (giảm tiếp xúc vật lý)?
51

## Slide 52
HẾT CHƯƠNG 1
Chuẩn bị cho Chương 2:
Thu thập Yêu cầu Phần mềm
Tài liệu tham khảo chính: Pressman (2015) [3] · Sommerville (2015) [10] · Klaus Pohl (2010) [8] · Hull, Jackson & Dick 
(2010) [9] · Buschmann và cộng sự [5] · DSDM Consortium [1][2]
CT241 — Phân tích Yêu cầu Phần mềm
