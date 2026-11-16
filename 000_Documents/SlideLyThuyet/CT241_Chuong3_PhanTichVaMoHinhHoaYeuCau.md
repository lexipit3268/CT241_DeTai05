# CT241_Chuong3_PhanTichVaMoHinhHoaYeuCau
**Tổng số slide:** 60

## Slide 1
TRƯỜNG CÔNG NGHỆ THÔNG TIN & TRUYỀN THÔNG  •  CT241
PHÂN TÍCH YÊU CẦU PHẦN MỀM
Chương 3
Phân tích và
Mô hình hoá Yêu cầu
Requirements Analysis & Modeling with UML

## Slide 2
C H Ư Ơ N G  3
Chương này nói về điều gì?
Chương này tập trung vào giai đoạn Phân tích và Mô tả chi tiết Yêu cầu (Analysis & Elaboration) — chuyển đổi các yêu cầu 
THÔ được thu thập sang một dạng thức CÓ CẤU TRÚC, rõ ràng và nhất quán, thông qua các kỹ thuật mô hình hoá UML: Use 
Case, Activity, Class, State và Sequence Diagram.
① Mô hình hoá = ngôn ngữ chung
Chuyển yêu cầu bằng văn bản thành hình ảnh trực quan 
mà cả khách hàng và lập trình viên đều hiểu.
② Cấu trúc TĨNH và hành vi ĐỘNG
Class Diagram mô tả cấu trúc; Activity, State, Sequence mô 
tả hành vi theo thời gian.
③ Phát hiện thiếu sót và mâu thuẫn
Một mũi tên bị thiếu trên mô hình chính là một yêu cầu bị 
thiếu — dễ thấy hơn trong văn bản.
④ Cầu nối sang thiết kế và kiểm thử
Use case sinh ra test case; class diagram là cơ sở thiết kế 
CSDL và kiến trúc phần mềm.
2

## Slide 3
L E A R N I N G  O U T C O M E S
Mục tiêu của chương
Sau khi hoàn thành chương này, người học có khả năng:
1 Áp dụng các kỹ thuật để phân tích, sắp xếp và giải quyết xung đột, mâu thuẫn giữa các yêu cầu.
2 Sử dụng Mô hình Use Case để xác định phạm vi hệ thống, mô tả chi tiết chức năng và kịch bản tương tác người dùng.
3 Áp dụng các loại mô hình UML (Class, Activity, State Machine, Sequence) để làm rõ khía cạnh cấu trúc và hành vi.
4 Thực hiện quy trình Thẩm định (Validation) yêu cầu: rà soát, kiểm thử tạo mẫu và kiểm tra giả định.
5 Bảo đảm yêu cầu nhất quán, không dư thừa và kiểm chứng được trước khi chuyển sang giai đoạn đặc tả.
3

## Slide 4
A G E N D A
Nội dung chương 3
3.1 Phân tích và Mô tả chi tiết Yêu cầu
3.2 Sơ đồ Trường hợp Sử dụng (Use Case Diagram)
3.3 Sơ đồ Hoạt động (Activity Diagram)
3.4 Sơ đồ Lớp (Class Diagram)
3.5 Sơ đồ Trạng thái (State Diagram) & Sơ đồ Tuần tự (Sequence Diagram)
3.6 Phân tích yêu cầu phi chức năng
Câu hỏi ôn tập (4 câu) & 2 bài tập thực hành cuối chương
4

## Slide 5
3.1
Phân tích và
Mô tả chi tiết Yêu cầu
Chuyển đổi yêu cầu thô thành dạng thức có cấu trúc, rõ ràng, nhất quán — nền tảng để đưa 
yêu cầu vào khuôn khổ thiết kế vững chắc.

## Slide 6
3 . 1
Vai trò của giai đoạn phân tích
Giai đoạn phân tích đóng vai trò quan trọng trong việc bảo đảm TÍNH NHẤT QUÁN và KHẢ THI của yêu cầu: phân tích 
độ khả thi, giải quyết xung đột giữa các yêu cầu, và dùng kỹ thuật mô hình hoá để trực quan hoá, làm rõ yêu cầu.
Bốn mô hình UML được dùng trong chương này
◆ Use Case Diagram
Xác định PHẠM VI hệ thống, các tác nhân và chức năng hệ 
thống cung cấp cho họ.
◆ Activity Diagram
Mô tả LUỒNG công việc, luồng điều khiển và xử lý song 
song trong một quy trình.
◆ Class Diagram
Mô tả cấu trúc TĨNH: các thực thể, thuộc tính và mối quan 
hệ giữa chúng.
◆ State & Sequence Diagram
Mô tả hành vi ĐỘNG: trạng thái đối tượng và trình tự trao 
đổi thông điệp theo thời gian.
Nền tảng lý thuyết: Klaus Pohl (2010) [8] · Hull, Jackson & Dick (2010) [9] · Sommerville (2015) [10] · Pressman (2015) [3].
6

## Slide 7
3.2
Sơ đồ Trường hợp
Sử dụng (Use Case)
Kỹ thuật xác định yêu cầu chức năng: người dùng muốn làm gì với hệ thống và hệ thống phản 
hồi ra sao.

## Slide 8
3 . 2 . 1
Vai trò của các mô hình kịch bản (Scenario)
Scenario (kịch bản) là mô tả cụ thể một TÌNH HUỐNG SỬ DỤNG hệ thống, thể hiện chuỗi các bước tương tác giữa 
người dùng và phần mềm để đạt được một mục tiêu.
① Kết nối ngôn ngữ người dùng với mô hình kỹ thuật
Là cầu nối giữa cách khách hàng diễn đạt và cách kỹ sư mô hình hoá.
② Mô tả cụ thể BỐI CẢNH sử dụng của yêu cầu
Làm rõ yêu cầu chức năng được dùng trong thực tế như thế nào.
③ Giúp phát hiện yêu cầu còn thiếu hoặc bất hợp lý
Khi diễn lại từng bước, chỗ hổng trong quy trình lộ ra rõ ràng.
④ Là cơ sở để xây dựng Use Case · Test Case · Tài liệu hướng dẫn
Một kịch bản tốt sinh ra đồng thời use case, ca kiểm thử và hướng dẫn sử dụng.
Scenario giúp làm rõ yêu cầu chức năng và cách hệ thống được sử dụng trong thực tế.
8

## Slide 9
3 . 2 . 1  V Í  D Ụ
Kịch bản “Sinh viên mượn sách” — Quản lý thư viện
1 Sinh viên truy cập hệ thống và đăng nhập.
2 Sinh viên tìm kiếm tên sách cần mượn.
3 Hệ thống hiển thị thông tin sách và tình trạng còn / hết.
4 Nếu sách còn, sinh viên gửi yêu cầu mượn.
5 Thủ thư xác nhận yêu cầu mượn và cập nhật tình trạng sách.

## Slide 10
3 . 2 . 2
Khái niệm Use Case
Use case mô tả một yêu cầu mà hệ thống cần cung cấp cho người dùng cuối để đạt một mục tiêu cụ thể. Nó chỉ mô tả 
NHỮNG GÌ hệ thống phải làm, chứ không mô tả hệ thống làm NHƯ THẾ NÀO.
Use case trả lời câu hỏi: “Người dùng muốn làm gì với hệ thống và hệ thống phản hồi ra sao?”
Ba đặc điểm của use case
Tập trung vào HÀNH VI hệ thống
Không mô tả giao diện hay cấu trúc dữ 
liệu.
Lấy NGƯỜI DÙNG làm trung tâm
Mỗi use case phục vụ đúng một mục tiêu 
của người dùng.
Dễ GIAO TIẾP
Dễ hiểu với cả nhà phát triển phần mềm 
lẫn khách hàng.
10

## Slide 11
B Ả N G  3 . 1
Các thành phần của Use Case Diagram
Actor
 Người dùng hoặc hệ thống bên ngoài tương tác với hệ thống. Mỗi actor đại diện cho một VAI TRÒ, 
không phải một cá nhân cụ thể.
Use Case
 Chức năng mà hệ thống cung cấp. Được đặt tên bằng một cụm động từ mô tả mục tiêu của người 
dùng (ví dụ: “Mượn sách”).
System Boundary
 Ranh giới của hệ thống đang mô tả. Mọi use case nằm BÊN TRONG ranh giới; actor luôn nằm BÊN 
NGOÀI.
Lưu ý khi đặt tên: use case là một MỤC TIÊU của người dùng, không phải một bước thao tác giao diện. “Đăng nhập” là use case; 
“Nhấn nút OK” thì không.
11

## Slide 12
H Ì N H  3 . 1
Sơ đồ trường hợp sử dụng cho yêu cầu Quản lý sách
Ranh giới hệ thống bao lấy các use case; actor đứng ngoài và nối với use case bằng quan hệ Association.
12

## Slide 13
B Ả N G  3 . 2
Các mối quan hệ trong Use Case Diagram
Association
 Actor — Use case.  Thực hiện: tác nhân tham gia vào trường hợp sử dụng.
Include
 Use case — Use case.  Bao gồm (BẮT BUỘC): use case này luôn gọi use case kia.
Extend
 Use case — Use case.  Bao gồm (TUỲ CHỌN): chỉ mở rộng khi thoả một điều kiện.
Generalization (Tổng quát / phân loại)
Áp dụng cho cả Use case — Use case và Actor — Actor. Ví dụ: “Độc giả” là actor tổng quát, “Sinh viên” và “Giảng viên” là hai actor chuyên 
biệt kế thừa từ nó.
13

## Slide 14
H Ì N H  3 . 2
Ví dụ về các mối quan hệ của sơ đồ use case
Include vẽ bằng mũi tên nét đứt có nhãn «include»; Extend cũng nét đứt nhưng nhãn «extend» và hướng ngược lại — từ use case mở rộng về 
use case gốc.
14

## Slide 15
3 . 2 . 5
Đặc tả use case chi tiết — 12 nội dung
Dùng để mô tả rõ trình tự tương tác, điều kiện và ràng buộc của một use case.
1 Mã Use case Use case ID — mã phân biệt duy nhất
 2 Tên Use case Use case Name — nội dung chính
3 Mô tả Description — chi tiết nội dung
 4 Tác nhân Actor — người dùng / hệ thống bên ngoài
5 Độ ưu tiên Priority — Cao, Trung bình, Thấp
 6 Ràng buộc Trigger — các ràng buộc liên quan
7 Điều kiện tiên quyết Pre-Condition
 8 Điều kiện kết thúc Post-Condition
9 Luồng xử lý chính Basic Flow
 10 Luồng xử lý ngoại lệ Exception Flow
11 Quy tắc nghiệp vụ Business Rules
 12 Yêu cầu phi chức năng Non-Functional Requirement
15

## Slide 16
B Ả N G  3 . 3
Đặc tả use case “Đăng nhập” (1/2)
Tên Use Case Đăng nhập tài khoản.
Mô tả Cho phép người dùng đăng nhập vào hệ thống với vai trò thành viên của hệ thống.
Tác nhân Quản lý, Thủ thư, Độc giả.
Độ ưu tiên Cao.
Ràng buộc Tài khoản có 3–15 ký tự. Mật khẩu 8–20 ký tự, gồm chữ thường và chữ hoa, ít nhất 1 ký tự số và 1 ký tự đặc biệt.
Điều kiện tiên quyết Tài khoản đã được hệ thống QLTV cung cấp · Người dùng chưa đăng nhập · Thiết bị đã kết nối Internet.
Điều kiện kết thúc Người dùng đăng nhập thành công và sử dụng được các chức năng tương ứng vai trò của mình.
16

## Slide 17
B Ả N G  3 . 3
Đặc tả use case “Đăng nhập” (2/2)
Luồng xử lý chính (Basic Flow)
• Người dùng truy cập vào hệ thống QLTV
• Người dùng nhấp vào nút “Đăng nhập” trên trang chủ
• Hệ thống mở form đăng nhập
• Người dùng nhập tài khoản và mật khẩu
• Hệ thống kiểm tra; nếu đúng, mở form chức năng và cấp quyền theo vai trò của người dùng
Luồng xử lý ngoại lệ (Exception Flow)
Nếu tài khoản và mật khẩu không hợp lệ, hệ thống thông báo lỗi và hiển thị lại form đăng nhập.
Quy tắc nghiệp vụ (Business Rules)
Nhập sai thông tin đăng nhập 5 lần liên tiếp sẽ bị khoá tài khoản 1 giờ và gửi mail thông báo về địa chỉ đã đăng ký.
Yêu cầu phi chức năng (NFR)
Thời gian chứng thực không quá 3 giây · Mật khẩu nhập vào phải hiển thị thay bằng dấu “*” hoặc “.” · Mật khẩu phải được mã hoá trước khi gửi 
về server chứng thực.
17

## Slide 18
3.3
Sơ đồ Hoạt động
(Activity Diagram)
Trực quan hoá luồng công việc, luồng điều khiển và các tiến trình song song trong một quy 
trình nghiệp vụ.

## Slide 19
3 . 3 . 1
Khái niệm và mục đích của Sơ đồ Hoạt động
Sơ đồ hoạt động mô tả LUỒNG THỰC HIỆN của các hoạt động trong hệ thống — cung cấp bức tranh rõ ràng cho mọi 
luồng công việc từ đơn giản đến phức tạp. Mỗi sơ đồ bắt đầu từ MỘT điểm ban đầu và kết thúc tại MỘT điểm cuối 
cùng.
Bốn mục đích chính
① Mô tả luồng công việc (workflow)
Biểu diễn cách thức một quy trình nghiệp vụ vận hành.
② Mô tả luồng điều khiển và luồng dữ liệu
Control flow và object flow trong hệ thống.
③ Mô tả trình tự các hành động
Thứ tự các hành động diễn ra trong hệ thống.
④ Mô hình hoá các quy trình SONG SONG
Thể hiện sự đồng bộ hoặc bất đồng bộ giữa các tiến trình 
diễn ra đồng thời.
19

## Slide 20
3 . 3 . 1
Sáu chức năng của Sơ đồ Hoạt động
1
Mô hình hoá quy trình nghiệp vụ Từ tổng thể đến chi tiết: luồng công việc, quy trình xử lý, quy tắc nghiệp vụ — hỗ trợ phân tích, 
tối ưu hoá và tự động hoá.
2
Minh hoạ luồng điều khiển Thể hiện luồng điều khiển giữa các hoạt động và cách chuyển từ hoạt động này sang hoạt động 
khác theo điều kiện hoặc sự kiện.
3
Mô tả luồng xử lý của một Use case Chi tiết hoá cách một use case được thực hiện; phân tích cách hệ thống phản hồi hành động 
người dùng hoặc sự kiện bên ngoài.
4
Mô tả quy trình xử lý song song Hỗ trợ thiết kế hệ thống đa luồng (multi-threading) hiệu quả, hiển thị rõ các luồng tác vụ song 
song.
5
Hỗ trợ thiết kế hệ thống phần mềm Giúp hiểu logic hệ thống và cách các phần tương tác TRƯỚC KHI bắt tay vào thiết kế.
6
Làm rõ logic phức tạp Đơn giản hoá các quy trình ra quyết định phức tạp với nhiều nhánh rẽ và kết quả khác nhau.
20

## Slide 21
3 . 3 . 1
Vai trò của Sơ đồ Hoạt động trong dự án
◆ Hỗ trợ nhà phân tích hệ thống
Hiểu rõ luồng hoạt động nghiệp vụ, xác định các điểm TẮC NGHẼN và các bước không hiệu quả trong quy trình.
◆ Tối ưu hoá quy trình kinh doanh
Phát hiện và loại bỏ các bước không cần thiết; hỗ trợ chuẩn hoá và cải thiện năng suất thông qua tự động hoá.
◆ Hỗ trợ giao tiếp giữa các bên liên quan
Mô hình trực quan giúp quản lý, lập trình viên và khách hàng hiểu cách hệ thống hoạt động → giảm sai sót khi triển khai.
◆ Cải thiện khả năng bảo trì và mở rộng
Nhóm phát triển dễ hiểu và cập nhật hệ thống khi có thay đổi; mở rộng mà không ảnh hưởng các phần hiện có.
◆ Hỗ trợ giai đoạn kiểm thử
Kỹ sư kiểm thử xác định các ca kiểm thử dựa trên luồng hoạt động, bảo đảm mọi kịch bản có thể xảy ra đều được kiểm tra. 21

## Slide 22
B Ả N G  3 . 4
Thành phần trong Sơ đồ Hoạt động (1/2)
Initial (Bắt đầu)
 Bắt đầu quy trình xử lý. Chỉ MỘT nút bắt đầu cho mỗi sơ đồ, trừ khi mô tả các hoạt động lồng nhau.
Activity Final (Kết thúc)
 Kết thúc toàn bộ quy trình xử lý.
Flow Final (Kết thúc nhánh)
 Kết thúc MỘT nhánh xử lý, các nhánh khác vẫn tiếp tục.
Action (Hoạt động)
 Là bước xử lý (hoạt động) đơn lẻ trong quy trình.
Control Flow
 Thể hiện thứ tự thực hiện. Một action có thể có NHIỀU luồng đi vào, nhưng chỉ MỘT luồng đi ra.
Object Node (Đối tượng)
 Thể hiện dữ liệu được tạo ra, sử dụng hoặc truyền giữa các action.
22

## Slide 23
B Ả N G  3 . 4
Thành phần trong Sơ đồ Hoạt động (2/2)
Decision (Rẽ nhánh)
 Xác định nhánh xử lý theo điều kiện. Có ít nhất 2 mũi tên đi ra, mỗi mũi tên có NHÃN là điều kiện. 
Chỉ MỘT nhánh được chọn tại một thời điểm.
Merge
 Dùng khi các hoạt động riêng lẻ (KHÔNG đồng thời) hợp nhất về một hoạt động khác.
Fork (Song song)
 Hỗ trợ các hoạt động ĐỒNG THỜI: một mũi tên đi vào, nhiều mũi tên đi ra. Cả hai nhánh đều phải 
được thực thi.
Join (Hội tụ)
 Các hoạt động đồng thời hội tụ về một hoạt động: nhiều mũi tên đi vào, một mũi tên đi ra.
Swimlane (Làn)
 Còn gọi là Activity Partition. Chia sơ đồ thành các vùng thể hiện trách nhiệm của role, actor hoặc tiểu 
hệ thống; vẽ dọc hoặc ngang.
23

## Slide 24
3 . 3 . 3
Luồng điều khiển và Swimlanes
Luồng điều khiển
Mô tả trình tự các bước, điều kiện thực thi, xử lý song song và 
sự kết thúc của hoạt động. Gồm 2 loại:
• Luồng CHÍNH: các bước quan trọng trong quy trình
• Luồng PHỤ: xử lý ngoại lệ, lỗi hoặc trường hợp đặc biệt
Swimlanes
Giúp xác định “AI thực hiện action nào” — phân tách trách 
nhiệm giữa các actor và xác định điểm giao tiếp giữa người và 
hệ thống.
Lưu ý khi sử dụng:
• Không nên tạo quá nhiều swimlanes
• Action phải đặt bên trong ĐÚNG swimlane thể hiện chủ 
thể thực hiện
Ví dụ — quy trình “Nhập sách”
Hai swimlane: THỦ THƯ (người dùng thực hiện quy trình) và HỆ THỐNG phần mềm quản lý thư viện. Hoạt động bắt đầu nằm ở làn 
Thủ thư (chọn chức năng “Nhập sách”); hoạt động kết thúc nằm ở làn Hệ thống, vì sau khi hệ thống thực hiện hoạt động cuối cùng 
thì quy trình kết thúc.
24

## Slide 25
H Ì N H  3 . 3
Năm bước vẽ Sơ đồ Hoạt động
1 Xác định Swimlane Hệ thống là một swimlane thực hiện các xử lý chính; mỗi actor cũng là một swimlane.
2 Xác định Initial và Final Đặt điểm bắt đầu và kết thúc vào đúng swimlane tương ứng.
3 Xác định các Action trung gian Liệt kê các bước cần thực hiện để đi từ điểm bắt đầu đến điểm kết thúc.
25

## Slide 26
3 . 3 . 4
Bước 4 – 5 và ví dụ quy trình “Nhập sách”
4 Xác định các điều kiện và ràng buộc
Xác định các yếu tố quyết định khi nào chuyển từ hoạt động này sang hoạt động khác. Ví dụ: hoạt động “Lưu thông tin sách vào 
CSDL” chỉ được thực hiện khi “các thông tin đó là hợp lệ”.
5 Hoàn chỉnh sơ đồ với ký hiệu thích hợp
Biểu diễn trực quan các trạng thái, hoạt động và điều kiện bằng các ký hiệu phù hợp. Sơ đồ đóng vai trò như một BẢN ĐỒ TRỰC 
QUAN về quy trình xử lý.
Trạng thái đầu – cuối của quy trình “Nhập sách”
Trạng thái ban đầu: “Chưa tồn tại sách trong cơ sở dữ liệu” → Trạng thái kết thúc: “Sách đã được lưu trong CSDL”.
Các action lần lượt: Nhập thông tin sách → Kiểm tra thông tin nhập vào có hợp lệ hay không → Lưu thông tin sách vào CSDL → …
26

## Slide 27
H Ì N H  3 . 4
Sơ đồ hoạt động cho yêu cầu Thêm sách
Chú ý hai swimlane (Thủ thư · Hệ thống), nút Decision kiểm tra tính hợp lệ và nhánh quay lui khi dữ liệu sai.
27

## Slide 28
3.4
Sơ đồ Lớp
(Class Diagram)
Mô tả cấu trúc TĨNH của hệ thống: các lớp, thuộc tính, phương thức và mối quan hệ giữa 
chúng.

## Slide 29
3 . 4
Vai trò của Sơ đồ Lớp
Class Diagram thể hiện trực quan CẤU TRÚC của hệ thống bằng cách hiển thị các lớp, thuộc tính, phương thức và mối 
quan hệ giữa chúng. Nó mô tả cấu trúc TĨNH — xác định các thực thể chính, các đối tượng nghiệp vụ và mối quan hệ 
giữa chúng.
① Cơ sở để thiết kế cơ sở dữ liệuCác lớp và thuộc tính trở thành 
bảng và cột trong CSDL.
② Cơ sở để thiết kế kiến trúc phần mềmXác định các thành phần và cách 
chúng liên kết với nhau.
③ Sinh mã tự động
Nhiều công cụ sinh mã nguồn 
trực tiếp từ sơ đồ lớp.
Các trường hợp sử dụng sơ đồ lớp
• Xác định mô hình miền (domain model)
• Thiết kế tầng nghiệp vụ
• Mô hình hoá thông tin khi xây dựng hệ thống quản lý, hệ thống thông tin, ứng dụng hướng đối tượng
29

## Slide 30
3 . 4 . 1
Lớp (Class), Thuộc tính và Hoạt động
Lớp đại diện cho một nhóm các đối tượng có thuộc tính và hành vi tương tự nhau. Ký hiệu là hình chữ nhật chia làm ba phần.
Hình 3.5. Ký hiệu lớp
 Hình 3.6. Ký hiệu lớp Sách
Tên lớp
Tên đại diện cho nhóm đối tượng.
Thuộc tính (Attribute)
Mô tả TRẠNG THÁI của các đối tượng. Xác 
định bằng tên, kiểu dữ liệu và các ràng buộc.
Hoạt động (Operation)
Xác định HÀNH VI của các đối tượng. Gồm 
tên, danh sách tham số và kiểu dữ liệu trả 
về.
30

## Slide 31
3 . 4 . 1  V Í  D Ụ
Thuộc tính lớp “Độc giả” và ba cách biểu diễn lớp
Thuộc tính lớp “Độc giả”
• Mã số: chuỗi văn bản có 8 ký tự
• Họ tên: chuỗi văn bản từ 3–50 ký tự
• Năm sinh: số nguyên 4 chữ số, lớn hơn 1900
Mỗi thuộc tính được xác định bởi
• Tên thuộc tính
• Kiểu dữ liệu
• Các ràng buộc (điều kiện) của nó
Ba cách biểu diễn một lớp
1 1 thành phần
Chỉ tên lớp
2 2 thành phần
Tên lớp + danh sách thuộc tính
3 3 thành phần
Tên lớp + thuộc tính + danh sách hoạt 
động
31

## Slide 32
B Ả N G  3 . 5
Các mối quan hệ trong Sơ đồ Lớp
Association (Kết hợp)
 Liên kết thông thường — mối quan hệ cơ bản nhất, thể hiện sự tương tác giữa các lớp.
Aggregation (Tập hợp)
 Thành phần YẾU — lớp thành phần có thể tồn tại độc lập với lớp chính.
Composition (Thành phần)
 Thành phần MẠNH — xoá lớp chính thì lớp thành phần cũng bị xoá theo.
Generalization (Tổng quát)
 Tổng quát, phân loại, kế thừa — lớp con kế thừa thuộc tính và hành vi của lớp cha.
Dependency (Phụ thuộc)
 Liên kết YẾU, có hướng — lớp này cần lớp kia trong hoạt động của nó; có thể chỉ tạm 
thời.
Bốn loại quan hệ cơ bản theo giáo trình: Association · Composition · Aggregation · Inheritance (Generalization).
32

## Slide 33
3 . 4 . 2
Association — quan hệ kết hợp
Association là mối quan hệ CƠ BẢN NHẤT, thể hiện sự tương tác giữa các lớp: các thể hiện của một lớp được kết nối 
với các thể hiện của một lớp khác.
Hình 3.7. Quan hệ Association
Trên mỗi đầu của đường kết hợp cần ghi rõ SỐ LƯỢNG (multiplicity) — bao nhiêu đối tượng của lớp này tham gia vào quan hệ 
với lớp kia.
33

## Slide 34
3 . 4 . 2
Aggregation & Composition — quan hệ thành phần
Aggregation — thành phần YẾU
Lớp thành phần CÓ THỂ tồn tại độc lập với lớp chính. Xoá lớp 
chính, lớp thành phần vẫn tồn tại.
Ví dụ: một số quyển sách có video đính kèm (sách học tiếng Anh). 
Video tồn tại và hoạt động độc lập với quyển sách.
Composition — thành phần MẠNH
Lớp thành phần KHÔNG THỂ tồn tại độc lập. Xoá lớp chính, lớp 
thành phần bị xoá theo.
Ví dụ: một phiếu mượn gồm nhiều chi tiết phiếu mượn (tối đa 5 
quyển, trả ở các ngày khác nhau). Chi tiết phiếu mượn không tồn 
tại độc lập với phiếu mượn.
Hình 3.8. Quan hệ Aggregation
 Hình 3.9. Quan hệ Composition
Ký hiệu: hình thoi RỖNG ở phía lớp chính = Aggregation · hình thoi ĐẶC = Composition.
34

## Slide 35
3 . 4 . 2
Generalization & Dependency
Generalization (Tổng quát)
Còn gọi là chuyên biệt hoá, phân loại hay kế thừa. Ví dụ: độc giả 
thư viện có hai loại — sinh viên và giáo viên. Thông tin, chính sách 
và quy định mượn trả của họ khác nhau.
Dependency (Phụ thuộc)
Quan hệ có HƯỚNG, lỏng lẻo hơn liên kết hay kế thừa: nếu lớp A 
phụ thuộc lớp B thì thay đổi ở B có thể ảnh hưởng A. Có thể chỉ 
tồn tại tạm thời tại một thời điểm hay điều kiện nào đó.
Hình 3.10. Quan hệ Generalization
 Hình 3.11. Quan hệ Dependency
Ví dụ Dependency: khi độc giả trả sách trễ sẽ bị lập phiếu phạt. Lớp PhiếuPhạt sử dụng lớp TínhTiềnPhạt để tính số tiền → PhiếuPhạt 
PHỤ THUỘC vào TínhTiềnPhạt.
35

## Slide 36
3 . 4 . 2
Multiplicity — số lượng của quan hệ
Multiplicity là số lượng các đối tượng tham gia vào mối quan hệ. Mọi quan hệ đều cần được xác định multiplicity.
Bảng 3.6. Các giá trị phổ biến
1 chính xác 1
0..1 0 hoặc 1
0..* 0 hoặc nhiều
1..* ít nhất 1
n..m từ n đến m
Hình 3.12. Số lượng của quan hệ
Đọc quan hệ Sách — LoạiSách
Một quyển sách thuộc 1 loại sách  ·  Một loại sách có thể KHÔNG có quyển sách nào hoặc có NHIỀU quyển sách (0..*).
36

## Slide 37
H Ì N H  3 . 1 3
Ví dụ về số lượng của quan hệ
Sách — Video (Aggregation)
 Phiếu mượn — Chi tiết (Composition)
Vì sao phải luôn ghi multiplicity?
• Xác định rõ ràng ràng buộc nghiệp vụ: “một phiếu mượn tối đa 5 quyển sách” chính là 1..5
• Là cơ sở trực tiếp để thiết kế khoá ngoại và bảng trung gian trong cơ sở dữ liệu
• Giúp phát hiện mâu thuẫn: nếu hai sơ đồ ghi số lượng khác nhau cho cùng một quan hệ thì có yêu cầu chưa thống nhất
37

## Slide 38
3.5
Sơ đồ Trạng thái &
Sơ đồ Tuần tự
Hai mô hình hành vi: State Diagram mô tả vòng đời trạng thái của đối tượng; Sequence 
Diagram mô tả trình tự trao đổi thông điệp theo thời gian.

## Slide 39
3 . 5 . 1
Vai trò của các mô hình hành vi
Mô hình hành vi mô tả hành vi ĐỘNG của hệ thống: cách hệ thống phản ứng lại các sự kiện, tương tác với tác nhân, và 
trạng thái thay đổi theo thời gian.
Trả lời các câu hỏi: “Khi người dùng thực hiện hành động A thì hệ thống làm gì tiếp theo?” · “Dữ liệu thay đổi như thế nào 
theo chuỗi sự kiện?”
① Làm rõ các luồng hoạt động ĐỘNG trong hệ thống
Bổ sung khía cạnh “động” cho các mô hình tĩnh như Class Diagram.
② Biểu diễn rõ ràng trạng thái và hành vi phức tạp
Những phần mà mô tả bằng văn bản dễ gây hiểu nhầm hoặc bỏ sót.
③ Hỗ trợ nhiều công việc trong dự án
Kiểm tra tính đầy đủ của yêu cầu · phát hiện mâu thuẫn và thiếu sót · giao tiếp với khách hàng · chuẩn bị cho thiết kế và kiểm định.

## Slide 40
3 . 5 . 2
Tác động của Sự kiện (Event) đến phần mềm
Sự kiện là một TÍN HIỆU, HÀNH ĐỘNG hoặc ĐIỀU KIỆN làm thay đổi hành vi của hệ thống — đến từ tác nhân, hệ thống bên 
ngoài, bộ hẹn giờ hoặc điều kiện nội bộ thay đổi.
Bảng 3.7. Bốn loại sự kiện phổ biến
Signal Event Thông điệp đến Nhân viên thư viện gửi yêu cầu “Gia hạn mượn sách”
Call Event Lời gọi hàm / phương thức Người dùng nhấn “Mượn sách”
Time Event Sự kiện thời gian Hệ thống gửi email đến hạn trả sách · Sau 5s · Đến 24:00
Change Event Điều kiện trở thành đúng Khi số lượng sách = 0
Nguồn sự kiện: actor (nhấn nút, gửi yêu cầu) · hệ thống bên ngoài (thông điệp, API call) · timer (timeout, đến hạn) · điều kiện nội bộ (dữ liệu 
thoả điều kiện). 40

## Slide 41
3 . 5 . 3
State Diagram — khái niệm và mục đích
State Diagram mô tả quá trình BIẾN ĐỔI TRẠNG THÁI của các đối tượng trong hệ thống suốt vòng đời của chúng. Dùng 
khi muốn làm rõ các trạng thái và sự thay đổi trạng thái của một đối tượng.
Mục đích mô hình hoá
• Khía cạnh “động” của hệ thống
• Sự tương tác bên trong hệ thống
• Phản ứng của các phần tử khi có sự kiện
• Vòng đời của các phần tử
• Sự thay đổi trạng thái của các phần tử
Ba thành phần chính
• State (trạng thái) và SubState
• Transition (chuyển trạng thái)
• Condition (điều kiện)
Ví dụ vòng đời một quyển sách
Quyển sách đang ở trạng thái “Sẵn dùng”. Khi độc giả “Mượn sách”, nó chuyển sang “Bận”. Khi độc giả “Trả sách”, nó quay về “Sẵn 
dùng”.
41

## Slide 42
B Ả N G  3 . 8
Các thành phần trong Sơ đồ Trạng thái
Initial State
 Trạng thái BẮT ĐẦU — trạng thái được sinh ra của đối tượng. Hình tròn nhỏ tô màu. Mỗi sơ đồ chỉ có 
MỘT.
Final State
 Trạng thái KẾT THÚC — trạng thái bị huỷ của đối tượng. Hình tròn nhỏ tô màu có đường viền nét đôi. 
Mỗi sơ đồ chỉ có MỘT.
State (Simple State)
 Trạng thái của đối tượng (ngoài sinh ra và bị huỷ). Hình chữ nhật bo tròn bốn góc, tên đặt bên trong. 
Có thể có NHIỀU.
Composite State
 Trạng thái HỢP THÀNH — chứa nhiều trạng thái con (Nested State); bên trong có thể chứa cả một sơ 
đồ trạng thái.
Transition
 Chuyển trạng thái — mũi tên có NHÃN. Hướng mũi tên xác định hướng thay đổi; nhãn là sự kiện, 
thao tác hay xử lý gây ra thay đổi đó.
42

## Slide 43
H Ì N H  3 . 1 4
Sơ đồ trạng thái của đối tượng Sách
Transition mô tả trình tự thay đổi giữa các trạng thái của đối tượng — chính là sự liên quan giữa các trạng thái của đối tượng đó.
43

## Slide 44
3 . 5 . 3
Composite State — trạng thái hợp thành
Khái niệm
Composite State là một trạng thái CHỨA NHIỀU trạng thái con 
(Nested State). Bên trong nó có thể chứa cả một sơ đồ trạng 
thái, thể hiện sự biến đổi của các trạng thái con.
Ví dụ — quyển sách
• “Đang vận hành” = quyển sách đang được đưa vào hoạt 
động của thư viện
• Nếu không ai mượn → trạng thái con “Sẵn dùng”
• Nếu đang được mượn → trạng thái con “Bận”
• Vậy “Đang vận hành” là trạng thái HỢP THÀNH của hai 
trạng thái con trên
Hình 3.15. Composite State
44

## Slide 45
3 . 5 . 4
Sequence Diagram — khái niệm
Sequence Diagram biểu diễn khía cạnh “động” của hệ thống THEO THỜI GIAN — mô tả chi tiết sự tương tác giữa các 
đối tượng (actor, hệ thống con, lớp…) theo trình tự thời gian. Còn được gọi là sơ đồ sự kiện (event diagrams) hay kịch 
bản sự kiện (event scenarios).
Trả lời hai câu hỏi
• Trong hệ thống, các đối tượng tương tác như thế 
nào?
• Thứ tự của các tương tác đó theo thời gian?
Giá trị trong phân tích
Tập trung vào THÔNG ĐIỆP (message) được gửi và nhận → 
giúp phát hiện hệ thống thiếu đối tượng, thiếu phương thức, 
hoặc có luồng xử lý phức tạp / bất thường.
Vị trí trong quy trình
Có thể dùng Sequence Diagram để xác định trình tự các xử lý diễn ra BÊN TRONG một use case hoặc một sự kiện. Đây là bước 
CHUẨN BỊ cho giai đoạn thiết kế hướng đối tượng.
45

## Slide 46
B Ả N G  3 . 9
Thành phần chính trong Sơ đồ Tuần tự (1/2)
Lifeline (đường đời)
 Thời gian tồn tại của actor / đối tượng trong một chức năng hoặc sự kiện. Có thể là actor bên 
ngoài hoặc object bên trong hệ thống.
Message (thông điệp)
 Thông điệp giao tiếp ĐỒNG BỘ giữa 2 lifeline khác nhau — bên gửi chờ phản hồi trước khi tiếp tục.
Async Message
 Thông điệp giao tiếp BẤT ĐỒNG BỘ giữa các lifeline khác nhau — bên gửi tiếp tục ngay, không 
chờ.
Self Message
 Thông điệp giao tiếp NỘI BỘ trong 1 lifeline — đối tượng gọi chính phương thức của mình.
Thời điểm sinh ra và mất đi của Lifeline tương ứng với vị trí bắt đầu và kết thúc của nó trong sơ đồ.
46

## Slide 47
B Ả N G  3 . 9
Thành phần chính trong Sơ đồ Tuần tự (2/2)
Reply Message
 Thông điệp chứa KẾT QUẢ PHẢN HỒI trả về cho bên gửi. Thường vẽ bằng mũi tên nét đứt.
Activation (kích hoạt)
 Khoảng thời gian gửi message hoặc chờ đợi phản hồi của message trên Lifeline. Các activation có 
thể LỒNG NHAU trong trường hợp đệ quy.
Fragment (Khối)
 Chứa một nhóm các message; mô tả rẽ nhánh, vòng lặp và một số cấu trúc lập trình khác.
Lifeline có thể được đặt trên trục toạ độ NGANG hoặc DỌC — hai cách biểu diễn tương đương nhau về ý nghĩa.
47

## Slide 48
H Ì N H  3 . 1 6  – 3 . 1 7
Biểu diễn Lifeline và Activation lồng nhau
Lifeline — biểu diễn ngang
 Lifeline — biểu diễn dọc
 Hình 3.17. Activation lồng nhau
Activation lồng nhau xuất hiện khi một đối tượng gọi lại chính mình (đệ quy) hoặc khi một lời gọi mới bắt đầu trong khi lời gọi trước 
chưa kết thúc.
48

## Slide 49
B Ả N G  3 . 1 0
Các loại Fragment trong Sơ đồ Tuần tự
alt Alternative multiple fragments Rẽ nhánh if … else — chọn một trong nhiều nhánh theo điều kiện.
opt Optional Điều kiện thực thi: if — khối chỉ chạy khi điều kiện đúng.
par Parallel Thực thi SONG SONG — các khối bên trong chạy đồng thời.
loop Loop Vòng lặp — khối được lặp lại theo số lần hoặc điều kiện.
sd Sequence diagram Tạo khung cho toàn bộ sơ đồ tuần tự.
49

## Slide 50
3.6
Phân tích yêu cầu
phi chức năng
Đặc tả các thuộc tính chất lượng theo nguyên tắc SMART và đo lường chúng bằng các metrics 
định lượng.

## Slide 51
3 . 6 . 1
Đặc tả yêu cầu phi chức năng — vai trò
NFR không mô tả hệ thống LÀM GÌ, mà mô tả hệ thống HOẠT ĐỘNG TỐT NHƯ THẾ NÀO — tác động trực tiếp vào trải 
nghiệm người dùng, hiệu năng, khả năng mở rộng và bảo trì.
◆ Xác định tiêu chuẩn đánh giá chất lượng hệ thống
 ◆ Ảnh hưởng đến kiến trúc NHIỀU HƠN yêu cầu chức năng
◆ Hỗ trợ quyết định công nghệ, phần cứng, bảo mật
 ◆ Tác động đến chi phí, thời gian phát triển và vận hành
Chín loại yêu cầu phi chức năng phổ biến
Hiệu năng
Performance
Khả năng mở rộng
Scalability
Tính khả dụng
Availability
Độ tin cậy
Reliability
Bảo mật
Security
Tính dễ sử dụng
Usability
Tính bảo trì
Maintainability
Tính tương thích
Compatibility
Tính an toàn
Safety
51

## Slide 52
3 . 6 . 1
Nguyên tắc SMART và ví dụ đặc tả tốt / kém
S
Specific
Cụ thể
M
Measurable
Đo được
A
Achievable
Khả thi
R
Relevant
Phù hợp
T
Time-bound
Có khung thời gian
Bảng 3.11. Đánh giá chất lượng đặc tả yêu cầu — hệ thống quản lý thư viện
Loại yêu cầu Đặc tả TỐT Đặc tả KÉM
Hiệu suất Hệ thống tra cứu sách phải trả kết quả trong ≤ 2 giây với 1.000 truy vấn đồng thời. Tra cứu phải nhanh.
Bảo mật Mật khẩu phải được hash bằng bcrypt với cost ≥ 10. Hệ thống phải an toàn.
Sẵn dùng Hệ thống phục vụ mượn/trả online phải đạt 99,5% uptime mỗi tháng. Hệ thống luôn sẵn sàng.
Ví dụ NFR tốt: “Hệ thống quản lý thư viện phải xử lý 1.000 yêu cầu tra cứu/giây trong giờ cao điểm.” 52

## Slide 53
3 . 6 . 2
Metrics và đo lường (1/2)
Metrics là các chỉ số ĐỊNH LƯỢNG dùng để đo mức độ thoả mãn của yêu cầu phi chức năng — kiểm chứng chất lượng, đo hiệu 
năng khi test và vận hành, kiểm soát và tối ưu hệ thống.
1. Hiệu suất (Performance)
Response time Thời gian phản hồi tìm kiếm sách ≤ 1,5 giây với 95% yêu cầu
Throughput Xử lý tối thiểu 500 yêu cầu tra cứu/giây trong giờ cao điểm
Latency Trả kết quả ≤ 2 giây với tập dữ liệu dưới 100.000 bản ghi
CPU / Memory usage CPU server ≤ 70% khi có tối đa 500 người dùng đồng thời
Concurrency Hỗ trợ ≥ 200 giao dịch mượn/trả đồng thời không xung đột dữ liệu
2. Sẵn dùng (Availability)
Uptime Uptime tối thiểu 99,5%/tháng, gián đoạn ≤ 20 phút trong giờ làm việc
MTBF Mean Time Between Failures ≥ 1.000 giờ vận hành liên tục
MTTR Mean Time To Repair ≤ 45 phút (lỗi trung bình), ≤ 2 giờ (lỗi nghiêm trọng)
53

## Slide 54
3 . 6 . 2
Metrics và đo lường (2/3) — Tin cậy & Bảo mật
3. Độ tin cậy (Reliability)
Error rate Tỷ lệ lỗi trong tra cứu tài liệu ≤ 0,1% trên tổng số yêu cầu tìm kiếm mỗi ngày
System recovery time Thời gian phục hồi dịch vụ sau sự cố ≤ 5 phút
4. Bảo mật (Security)
Prevent attacks Chống SQL Injection, XSS, Brute-force — khoá tài khoản sau tối đa 5 lần đăng nhập sai liên tiếp; kiểm tra input ở tất cả các form
Access control Phân quyền Thủ thư / Sinh viên / Giảng viên / Quản trị viên; sinh viên không thể xoá hồ sơ sách
Encryption Mật khẩu hash bằng SHA-256 trở lên; dữ liệu truyền qua mạng dùng HTTPS với TLS 1.3
Authentication Tài khoản sinh viên phải đăng nhập qua SSO của trường
54

## Slide 55
3 . 6 . 2
Metrics và đo lường (3/3) — Sử dụng, Bảo trì, Mở rộng
5. Khả năng sử dụng (Usability)
Time to learn Người dùng mới hoàn thành thao tác cơ bản (tìm sách, đặt mượn) trong 15 phút đầu
Task success rate Người dùng hoàn thành thao tác mượn sách online trong ≤ 3 bước
Number of user errors Dưới 3 lỗi thao tác mỗi người dùng trong 30 phút sử dụng
6. Bảo trì (Maintainability)  ·  7. Khả năng mở rộng (Scalability)
Error handling Lỗi nghiêm trọng khắc phục trong 24 giờ; lỗi giao diện mức nhẹ sửa trong 7 ngày
System update Cập nhật phần mềm không gây gián đoạn dịch vụ quá 2 phút, không tắt toàn hệ thống
Cyclomatic complexity Mỗi hàm ở backend không vượt quá 12
Users / Resources Tăng người dùng 100% → hiệu năng giảm ≤ 20%; tăng RAM/CPU → throughput tăng tương ứng
55

## Slide 56
3 . 6 . 2
Phương pháp và công cụ đo lường NFR
Hiệu năng Benchmarking (đánh giá chuẩn) · Load Testing (kiểm tra tải) · Profiling (lập hồ sơ)
Độ tin cậy Log Analysis (phân tích log) · Monitoring (quan sát) · Fault Injection (tiêm lỗi)
Bảo mật Penetration Testing · Security Scan · Access Control · Encryption Validation
Bảng 3.13. Một số công cụ đo lường tiêu biểu
JMeter · LoadRunner Kiểm thử hiệu năng, tải và stress test Throughput, Latency, Response Time, Concurrency, Error Rate
Grafana · Prometheus Quan sát và trực quan hoá dữ liệu hệ thống theo thời gian 
thực
CPU / Memory usage, Disk & Network I/O, Uptime, Request per 
second
New Relic · Dynatrace · Nagios Giám sát hiệu năng ứng dụng và hạ tầng, cảnh báo lỗi Response Time, Throughput, Availability, MTBF, MTTR, Error 
Rate
SonarQube Phân tích chất lượng mã nguồn Cyclomatic Complexity, Code Smells, Security Vulnerabilities
OWASP ZAP · Burp Suite Kiểm thử bảo mật tự động và chuyên nghiệp XSS, SQL Injection, Access Control flaws, Encryption flaws
56

## Slide 57
T Ổ N G  K Ế T
Tóm tắt Chương 3
3.1 Phân tích chuyển yêu cầu THÔ thành dạng có cấu trúc, rõ ràng, nhất quán — thông qua phân tích khả thi, giải quyết xung đột và mô hình hoá.
3.2 Use Case Diagram: Actor · Use Case · System Boundary; quan hệ Association, Include (bắt buộc), Extend (tuỳ chọn), Generalization. Đặc tả use case gồm 12 nội dung.
3.3 Activity Diagram: Initial, Final, Action, Control Flow, Decision, Merge, Fork, Join, Swimlane, Object Node. Vẽ theo 5 bước, bắt đầu từ xác định swimlane.
3.4 Class Diagram mô tả cấu trúc TĨNH: lớp (tên – thuộc tính – hoạt động) và 5 quan hệ: Association, Aggregation, Composition, Generalization, Dependency + multiplicity.
3.5 Mô hình hành vi: State Diagram (State, Composite State, Transition) và Sequence Diagram (Lifeline, Message, Activation, Fragment: alt/opt/par/loop/sd).
3.6 NFR phải đạt SMART; đo bằng metrics định lượng theo 7 nhóm và các công cụ JMeter, Grafana, SonarQube, OWASP ZAP…
57

## Slide 58
C Â U  H Ỏ I  Ô N  T Ậ P  C H Ư Ơ N G  3
Câu 1 – 4
1 Vai trò của Use Case Diagram
Sơ đồ Use Case đóng vai trò gì trong việc chuyển các yêu cầu thô (textual requirements) thành một mô hình hệ thống có cấu trúc? Phân tích sự 
khác biệt về thông tin mà sơ đồ này cung cấp so với việc chỉ dùng danh sách yêu cầu chức năng.
2 Activity Diagram vs Sequence Diagram
Với một quy trình nghiệp vụ phức tạp (ví dụ: đặt hàng trực tuyến): khi nào nên ưu tiên Activity Diagram? Khi nào nên ưu tiên Sequence 
Diagram? Nêu sự khác biệt CỐT LÕI về góc nhìn mà hai loại sơ đồ mang lại.
3 Thẩm định yêu cầu (Validation)
Validation xác nhận “chúng ta đang xây dựng ĐÚNG sản phẩm”. Giải thích vì sao bước này không thể thay thế bằng Verification (kiểm tra tính 
đúng đắn kỹ thuật của tài liệu). Nêu tối thiểu 2 kỹ thuật thẩm định và cách chúng phát hiện lỗi thiếu sót.
4 Đánh giá tính khả thi (Feasibility)
Liệt kê ba khía cạnh chính của tính khả thi mà nhà phân tích cần xem xét (Kỹ thuật, Kinh tế, Pháp lý). Cho ví dụ một yêu cầu bị đánh giá là 
KHÔNG khả thi về mặt kỹ thuật trong bối cảnh phát triển phần mềm hiện nay.
58

## Slide 59
B À I  T Ậ P  T H Ự C  H À N H
Bài 1 – 2
1 Phân tích và mô hình hoá Use case
Mục tiêu: xác định actor và use case · vẽ sơ đồ use case · viết đặc tả use case chi tiết.
• a. Viết mô tả chi tiết yêu cầu phần mềm cho hệ thống quản lý thư viện của một trường đại học: quản lý mượn/trả sách 
(mượn, trả, gia hạn, xử lý vi phạm) và quản lý việc nộp, truy xuất niên luận – luận văn của sinh viên
• b. Vẽ sơ đồ trường hợp sử dụng cho hệ thống ở câu a
• c. Viết đặc tả chi tiết cho 5 use case chính trong hệ thống (theo mẫu 12 nội dung ở mục 3.2.5)
2 Xây dựng các lược đồ phân tích
Mục tiêu: vẽ Activity Diagram · Sequence Diagram · Class Diagram.
• a. Vẽ sơ đồ lớp cho hệ thống Quản lý thư viện, bảo đảm dữ liệu cho TẤT CẢ use case trong sơ đồ use case ở Bài 1
• b. Vẽ sơ đồ hoạt động và sơ đồ tuần tự cho ba yêu cầu: Mượn sách · Trả sách · Gia hạn thời gian mượn sách
59

## Slide 60
HẾT CHƯƠNG 3
Chuẩn bị cho Chương 4:
Đặc tả và Quản lý Yêu cầu
Tài liệu tham khảo chính: Klaus Pohl (2010) [8] · Hull, Jackson & Dick (2010) [9] · Sommerville (2015) [10] · Pressman 
(2015) [3]
CT241 — Phân tích Yêu cầu Phần mềm
