# CT241_Chuong2_ThuThapYeuCauPhanMem
**Tổng số slide:** 74

## Slide 1
TRƯỜNG CÔNG NGHỆ THÔNG TIN & TRUYỀN THÔNG  •  CT241
PHÂN TÍCH YÊU CẦU PHẦN MỀM
Chương 2
Thu thập Yêu cầu
Phần mềm
Requirements Elicitation — Techniques, Tools & Process

## Slide 2
C H Ư Ơ N G  2
Chương này nói về điều gì?
Chương này trình bày chi tiết về giai đoạn Khai thác và Thu thập Yêu cầu (Elicitation) — bước quan trọng đầu tiên để khám 
phá và hiểu rõ nhu cầu thực sự của các bên liên quan: xác định đúng các bên liên quan (Stakeholders), giới thiệu và hướng dẫn
áp dụng các kỹ thuật khai thác chuyên nghiệp (Phỏng vấn, JAD, Khảo sát, Quan sát, Phân tích tài liệu…), đồng thời phân tích 
ưu – nhược điểm của từng kỹ thuật.
? Ai là người chúng ta phải lắng nghe?
Xác định lớp người dùng, người tiên phong sản phẩm và 
người ra quyết định về yêu cầu.
! Khai thác ≠ chỉ hỏi khách hàng muốn gì
Khách hàng thường không biết chính xác họ cần gì — phải 
đào sâu tới nhu cầu gốc rễ.
→ 10 kỹ thuật thu thập yêu cầu
Không kỹ thuật nào luôn tốt nhất — hầu hết dự án kết hợp 
nhiều kỹ thuật.
✓ Tầm nhìn & phạm vi là điểm khởi đầu
Mọi yêu cầu người dùng đều phải nằm trong ranh giới đã 
thống nhất từ đầu.
2

## Slide 3
L E A R N I N G  O U T C O M E S
Mục tiêu của chương
Sau khi hoàn thành chương này, người học có khả năng:
1 Xác định và phân tích được vai trò, quyền hạn của tất cả các bên liên quan (Stakeholders) trong dự án.
2 Nắm vững và áp dụng thành thạo các kỹ thuật khai thác yêu cầu chủ yếu: Phỏng vấn, Workshop (JAD/Kano) và Quan sát.
3 Sử dụng các kỹ thuật làm rõ yêu cầu như Tạo mẫu (Prototyping) và Kịch bản / Câu chuyện người dùng (User Story).
4 Lựa chọn và kết hợp các kỹ thuật khai thác hiệu quả tuỳ theo loại dự án và đặc điểm của các bên liên quan.
5 Quản lý và giải quyết các vấn đề thường gặp khi khai thác: xung đột ý kiến, yêu cầu mập mờ, yêu cầu còn thiếu.
3

## Slide 4
A G E N D A
Nội dung chương 2
2.1 Thiết lập tầm nhìn sản phẩm và phạm vi dự án
2.2 Tìm kiếm tiếng nói của khách hàng
2.3 Lắng nghe tiếng nói của khách hàng
2.4 Các kỹ thuật thu thập yêu cầu (10 kỹ thuật)
2.5 Lựa chọn kỹ thuật phù hợp
2.6 Công cụ thu thập yêu cầu
2.7 Quy trình thu thập yêu cầu (6 bước)
2.8 Những trở ngại phổ biến
2.9 Biểu mẫu thu thập yêu cầu người dùng
Câu hỏi ôn tập & 12 bài tập thực hành cuối chương
4

## Slide 5
2.1
Thiết lập tầm nhìn sản phẩm
và phạm vi dự án
Tầm nhìn hướng mọi bên liên quan theo một hướng chung; phạm vi vạch ranh giới giữa 
những gì được phép và không được phép trong dự án hiện tại.

## Slide 6
2 . 1  M Ở  Đ Ầ U
Thu thập yêu cầu — giai đoạn quyết định
Thu thập yêu cầu là một QUÁ TRÌNH KHÁM PHÁ: nghiên cứu và ghi chép các yêu cầu chính xác của dự án từ đầu đến 
cuối. Thành công của dự án thường phụ thuộc vào tính chính xác và đầy đủ của các yêu cầu được thu thập.
① Là lĩnh vực khó nhất của kỹ nghệ phần mềm
Vì nó quyết định và xác định NHỮNG GÌ cần được phát triển; phần lớn thời gian bị chiếm dụng bởi các vấn đề đa dạng khi các bên 
liên quan tương tác.
② Là hoạt động lấy CON NGƯỜI làm trung tâm
Do sự tham gia của nhiều người khác nhau, luôn có khả năng xảy ra lỗi của con người trong quá trình chuyển nhu cầu thành yêu cầu.
③ Không diễn ra một cách tự nhiên
Phụ thuộc chặt chẽ vào bối cảnh thực hiện, đặc điểm dự án, tổ chức, môi trường, kinh nghiệm nhà phân tích và kỹ thuật được sử
dụng.
Nền tảng lý thuyết: Karl E. Wiegers (2003), Software Requirements [6] · James Robertson và cộng sự (2024), Mastering the Requirements 
Process [4]. 6

## Slide 7
2 . 1 . 1
Tầm nhìn sản phẩm ≠ Phạm vi dự án
TẦM NHÌN (Vision)
• Áp dụng cho TOÀN BỘ sản phẩm
• Mô tả sản phẩm là gì và tương lai sẽ trở thành gì
• Hướng tất cả các bên liên quan theo một hướng 
chung
• Thay đổi tương đối CHẬM, khi định vị chiến lược hoặc 
mục tiêu nghiệp vụ thay đổi
PHẠM VI (Scope)
• Liên quan đến MỘT dự án hoặc lần lặp cụ thể
• Xác định phần nào của tầm nhìn được giải quyết lúc 
này
• Vạch ranh giới giữa được phép và không được phép
• LINH HOẠT hơn: điều chỉnh theo lịch trình, ngân sách, 
nguồn lực, chất lượng
Mục tiêu của người lập kế hoạch: quản lý phạm vi của một dự án cụ thể như một TẬP HỢP CON được xác định rõ của tầm nhìn chiến
lược tổng thể. Phát biểu phạm vi có thể xuất hiện trong SRS thay vì một tài liệu riêng.
7

## Slide 8
H Ì N H  2 . 1
Tầm nhìn bao gồm phạm vi cho mỗi bản phát hành
Ví dụ minh hoạ
Một cơ quan chính phủ thực hiện dự án hệ thống thông tin quy mô lớn kéo dài 5 năm. Mục tiêu nghiệp vụ và tầm nhìn được xác 
định ngay từ đầu và sẽ KHÔNG thay đổi đáng kể. Cơ quan lên kế hoạch khoảng 15 bản phát hành riêng lẻ — mỗi bản là một dự án 
riêng với mô tả phạm vi riêng, phải phù hợp với tầm nhìn tổng thể và liên kết với các tuyên bố phạm vi khác để không nội dung nào 
bị bỏ sót.
8

## Slide 9
2 . 1 . 1
Yêu cầu nghiệp vụ đến từ nhiều nguồn — và xung đột
Ví dụ: một chức năng chứa phần mềm nhúng, được khách hàng của cửa hàng bán lẻ sử dụng.
Nhà phát triển
Tạo doanh thu bằng cách cho thuê / bán 
chức năng cho nhà bán lẻ
Bán hàng tiêu dùng qua chức năng
Thu hút khách hàng đến với thương hiệu
Cung cấp đa dạng sản phẩm
Muốn hướng đi mới, công nghệ cao và thú 
vị
Nhà bán lẻ
Tối đa hoá doanh thu từ không gian mặt 
bằng hiện có
Thu hút thêm khách hàng đến cửa hàng
Tăng doanh số và biên lợi nhuận nếu thay 
thế thao tác thủ công
Muốn một hệ thống chìa khoá trao tay đơn 
giản
Khách hàng
Thực hiện được việc mình cần một cách 
nhanh chóng
Không phải học cách dùng phức tạp
Được phục vụ tốt hơn so với cách làm cũ
Ưa chuộng sự tiện lợi và nhiều tính năng
NHÀ TÀI TRỢ DỰ ÁN phải giải quyết những xung đột này TRƯỚC KHI nhà phân tích trình bày chi tiết yêu cầu hệ thống — không 
trông đợi nhóm phần mềm tự tìm cách. Càng nhiều nhóm có lợi ích cạnh tranh tham gia, nguy cơ vượt phạm vi càng tăng.
9

## Slide 10
2 . 1 . 1
Yêu cầu nghiệp vụ quyết định độ rộng và độ sâu
ĐỘ RỘNG (breadth)
Tập hợp các tác vụ nghiệp vụ (tình huống) mà ứng dụng cho 
phép. Nếu yêu cầu nghiệp vụ giúp xác định một tình huống 
nằm NGOÀI phạm vi, ta đang ra quyết định về độ rộng.
ĐỘ SÂU (depth)
Mức độ triển khai của từng tình huống — từ triển khai đơn 
giản đến tự động hoá hoàn toàn với nhiều công cụ hỗ trợ 
khả năng sử dụng.
→ Ảnh hưởng đến THỨ TỰ ƯU TIÊN triển khai
Mục tiêu “tạo doanh thu tối đa” ⇒ ưu tiên sớm các tính năng giúp bán được nhiều sản phẩm. Tính năng hào nhoáng chỉ hấp dẫn số ít 
khách hàng ham công nghệ thì không nên ưu tiên cao.
→ Ảnh hưởng đến CÁCH THỨC triển khai yêu cầu
Hệ thống giám sát hoá chất muốn giảm mua chai mới ⇒ phỏng vấn và quan sát để hiểu vì sao tái sử dụng chưa diễn ra ⇒ sinh ra 
chức năng theo dõi hoá chất theo từng phòng thí nghiệm.
10

## Slide 11
B Ả N G  2 . 1
Mẫu tài liệu về tầm nhìn và phạm vi
1
Các yêu cầu nghiệp vụ
Bối cảnh · Cơ hội nghiệp vụ · Mục tiêu nghiệp vụ và tiêu chí thành công · Nhu cầu của khách hàng hoặc thị trường · Rủi ro nghiệp
vụ
2
Tầm nhìn của giải pháp
Tuyên bố tầm nhìn · Các đặc điểm chính · Giả định và phụ thuộc
3
Phạm vi và hạn chế
Phạm vi của bản phát hành đầu tiên · Phạm vi của các bản phát hành tiếp theo · Hạn chế và loại trừ
4
Bối cảnh nghiệp vụ
Hồ sơ các bên liên quan · Ưu tiên dự án · Môi trường hoạt động
Chủ sở hữu tài liệu: nhà tài trợ điều hành / cơ quan cấp vốn. Nhà phân tích yêu cầu làm việc cùng chủ sở hữu để soạn thảo. Hãy điều chỉnh 
mẫu cho phù hợp với dự án của mình. 11

## Slide 12
2 . 1 . 2 . 1
Phần 1 — Các yêu cầu nghiệp vụ
1
Bối cảnh
Tóm tắt cơ sở lý luận và bối cảnh; mô tả lịch sử hoặc tình huống dẫn đến quyết định xây dựng sản phẩm này.
2
Cơ hội nghiệp vụ
Cơ hội thị trường / vấn đề kinh doanh đang giải quyết; đánh giá so sánh với sản phẩm hiện có; lợi thế của sản phẩm đề xuất.
3
Mục tiêu nghiệp vụ & tiêu chí thành công
Lợi ích nghiệp vụ quan trọng, ĐỊNH LƯỢNG và ĐO LƯỜNG ĐƯỢC; cách các bên liên quan xác định và đo lường thành công.
4
Nhu cầu của khách hàng / thị trường
Nhu cầu chưa được đáp ứng bởi hệ thống hiện tại; ví dụ về cách khách hàng sẽ sử dụng sản phẩm (chưa đi vào thiết kế).
5
Rủi ro nghiệp vụ
Cạnh tranh, thời gian, sự chấp nhận của người dùng, vấn đề triển khai; ước tính tổn thất, khả năng xảy ra và hành động giảm thiểu.
12

## Slide 13
2 . 1 . 2 . 2
Tầm nhìn giải pháp — mẫu từ khoá tuyên bố tầm nhìn
1 Đối với [khách hàng mục tiêu]
2 Ai [tuyên bố về nhu cầu hoặc cơ hội]
3 [Tên sản phẩm]
4 Là [một danh mục sản phẩm]
5 Đó [lợi ích chính, lý do thuyết phục để dùng]
6 Không giống như [phương án cạnh tranh / hệ thống hiện tại]
7 Sản phẩm của chúng tôi [khác biệt chính và lợi thế]
Tuyên bố tầm nhìn cần:
• Ngắn gọn, tóm tắt mục đích và ý định DÀI HẠN của 
sản phẩm
• Phản ánh quan điểm cân bằng, đáp ứng nhu cầu 
nhiều bên liên quan
• Có thể hơi lý tưởng nhưng phải dựa trên thực tế 
thị trường, kiến trúc doanh nghiệp và hạn chế 
nguồn lực
Phần này KHÔNG bao gồm yêu cầu chức năng chi tiết 
hoặc thông tin lập kế hoạch dự án.
13

## Slide 14
V Í  D Ụ  M I N H  H O Ạ
Tuyên bố tầm nhìn: Hệ thống theo dõi hoá chất
“Đối với các nhà khoa học cần yêu cầu các thùng chứa hoá chất, hệ thống theo dõi hoá chất là một hệ thống thông tin 
cung cấp một điểm truy cập duy nhất đến kho hoá chất và các nhà cung cấp. Hệ thống sẽ lưu trữ vị trí của mọi thùng 
chứa hoá chất trong đơn vị, lượng vật liệu còn lại, toàn bộ lịch sử vị trí và việc sử dụng của từng thùng chứa. Hệ thống sẽ 
giúp đơn vị tiết kiệm 25% chi phí hoá chất trong năm đầu tiên… Không giống như các quy trình đặt hàng thủ công hiện 
tại, sản phẩm của chúng tôi sẽ tạo ra tất cả báo cáo cần thiết để tuân thủ các quy định của chính quyền.”
◆ Khách hàng mục tiêu + nhu cầu“Nhà khoa học cần yêu cầu các 
thùng chứa hoá chất”
◆ Lợi ích ĐO LƯỜNG ĐƯỢC
“Tiết kiệm 25% chi phí hoá chất 
trong năm đầu tiên”
◆ Khác biệt so với hiện tại
“Không giống như quy trình đặt 
hàng thủ công hiện tại…”
14

## Slide 15
2 . 1 . 2 . 2
Đặc điểm chính · Giả định và phụ thuộc
Các đặc điểm chính
• Đặt tên hoặc đánh số từng tính năng chính một cách 
độc đáo và nhất quán
• Nhấn mạnh những gì phân biệt sản phẩm mới với sản 
phẩm trước / cạnh tranh
• Gắn nhãn riêng cho phép TRUY XUẤT NGUỒN GỐC tới 
yêu cầu người dùng và yêu cầu chức năng
Giả định và phụ thuộc
• Ghi lại mọi giả định các bên đưa ra khi hình thành dự 
án
• Giả định của một bên thường KHÔNG được các bên 
khác chia sẻ
• Ghi lại phụ thuộc vào yếu tố bên ngoài: tiêu chuẩn 
ngành, quy định, dự án khác, nhà cung cấp bên thứ ba
Ví dụ giả định — hệ thống theo dõi hoá chất
Nhà tài trợ điều hành cho rằng hệ thống mới sẽ THAY THẾ hệ thống kiểm kê kho hoá chất hiện có, và sẽ TƯƠNG TÁC với hệ thống 
mua sắm. Nếu không ghi lại và xem xét, những giả định như vậy sẽ gây nhầm lẫn và rắc rối về sau.
15

## Slide 16
2 . 1 . 2 . 3
Phạm vi và hạn chế — nêu rõ cả những gì KHÔNG làm
Giống như một nhà hoá học viết phần “Phạm vi và hạn chế” khi công bố phản ứng mới, dự án phần mềm phải nêu rõ cả những gì hệ 
thống CÓ và những gì hệ thống KHÔNG cần có.
1 Phạm vi của bản phát hành đầu tiên
Tóm tắt các tính năng chính của bản 1.0. Tránh nhồi mọi tính năng mà khách hàng “một ngày nào đó” có thể muốn. Tập trung vào tính 
năng giá trị cao nhất, chi phí chấp nhận được nhất, cho cộng đồng rộng nhất, sớm nhất.
2 Phạm vi của các bản phát hành tiếp theo
Chỉ ra tính năng nào được hoãn lại và thời điểm mong muốn. Càng nhìn xa, tuyên bố phạm vi càng mơ hồ — chu kỳ phát hành ngắn giúp 
học hỏi thường xuyên từ phản hồi khách hàng.
3 Hạn chế và loại trừ
Liệt kê những khả năng mà bên liên quan CÓ THỂ DỰ ĐOÁN nhưng chưa được lên kế hoạch đưa vào. Đây là cách quản lý vượt phạm vi
và kỳ vọng của khách hàng.
Yêu cầu ngoài phạm vi phải bị TỪ CHỐI — trừ khi quá giá trị đến mức cần mở rộng phạm vi kèm thay đổi ngân sách, tiến độ, nhân 
sự. Hãy lưu hồ sơ yêu cầu bị từ chối và lý do, vì chúng có thể quay trở lại.
16

## Slide 17
2 . 1 . 2 . 4
Bối cảnh nghiệp vụ — Hồ sơ các bên liên quan
Bên liên quan = cá nhân, nhóm hoặc tổ chức TÍCH CỰC THAM GIA vào dự án, BỊ ẢNH HƯỞNG bởi kết quả, hoặc CÓ KHẢ 
NĂNG TÁC ĐỘNG đến kết quả của dự án.
Giá trị / lợi ích chính bên liên quan nhận được
• Nâng cao năng suất
• Giảm thiểu việc làm lại
• Tiết kiệm chi phí
• Quy trình nghiệp vụ được tinh gọn
• Tự động hoá các tác vụ thủ công trước đây
• Khả năng thực hiện các tác vụ hoàn toàn mới
• Tuân thủ các tiêu chuẩn hoặc quy định liên quan
• Cải thiện khả năng sử dụng so với sản phẩm hiện tại
Mỗi hồ sơ còn ghi
• Thái độ của họ đối với sản phẩm
• Các tính năng và đặc điểm chính đáng 
quan tâm
• Bất kỳ hạn chế nào đã biết cần được 
điều chỉnh
Tập trung vào loại khách hàng, phân khúc thị 
trường mục tiêu và các nhóm người dùng.
17

## Slide 18
2 . 1 . 2 . 4
Ưu tiên dự án — 5 khía cạnh và 3 vai trò
Năm khía cạnh của một dự án phần mềm: tính năng (phạm vi) · chất lượng · tiến độ · chi phí · nhân sự. Mỗi khía cạnh rơi vào MỘT 
trong ba loại sau:
Ràng buộc
Constraint
Yếu tố hạn chế mà người quản lý dự án 
BẮT BUỘC phải vận hành trong phạm vi 
đó.
Động lực
Driver
Mục tiêu thành công đáng kể, với sự linh 
hoạt HẠN CHẾ để điều chỉnh.
Bậc tự do
Degree of freedom
Yếu tố mà người quản lý dự án CÓ QUYỀN 
TỰ DO điều chỉnh, cân bằng với các khía 
cạnh khác.
Tình huống: tiếp thị đột nhiên yêu cầu phát hành sớm hơn một tháng. Chúng ta phản ứng thế nào?
• Trì hoãn một số yêu cầu cho lần phát hành sau?
• Rút ngắn chu kỳ kiểm tra hệ thống đã lên kế hoạch?
• Trả lương làm thêm giờ hay thuê nhà thầu để đẩy nhanh phát triển?
• Chuyển nguồn lực từ các dự án khác sang hỗ trợ?
18

## Slide 19
2 . 1 . 2 . 4
Môi trường hoạt động — những câu hỏi cần đặt
Thông tin này ảnh hưởng đáng kể đến việc xác định KIẾN TRÚC hệ thống — bước thiết kế đầu tiên và thường là quan trọng nhất.
? Người dùng phân bố rộng rãi về mặt địa lý hay ở gần nhau? Họ ở bao nhiêu múi giờ?
? Khi nào người dùng ở các địa điểm khác nhau cần truy cập hệ thống?
? Dữ liệu được tạo và sử dụng ở đâu? Các địa điểm này cách nhau bao xa?
? Dữ liệu từ nhiều địa điểm có cần được kết hợp không?
? Có quy định cụ thể về thời gian phản hồi tối đa khi truy cập dữ liệu lưu trữ từ xa không?
? Người dùng có thể chịu được gián đoạn dịch vụ, hay truy cập liên tục là rất quan trọng?
? Cần có các biện pháp kiểm soát bảo mật truy cập và yêu cầu bảo vệ dữ liệu nào?
Hệ thống phục vụ người dùng phân tán cần truy cập 24/7 đòi hỏi kiến trúc khác hẳn hệ thống chỉ dùng tại chỗ trong giờ hành chính.
19

## Slide 20
2.2
Tìm kiếm tiếng nói
của khách hàng
Xác định các nhóm người dùng, nguồn gốc yêu cầu, người đại diện cho từng nhóm và người 
có quyền ra quyết định về yêu cầu.

## Slide 21
H Ì N H  2 . 3
Khi không có kỹ thuật yêu cầu rõ ràng…
Khoảng cách kỳ vọng (expectation gap): sự không phù hợp giữa sản phẩm khách hàng MONG ĐỢI nhận được và sản phẩm nhà 
phát triển THỰC SỰ xây dựng. Sự tham gia của khách hàng là cách duy nhất để tránh khoảng cách này.
21

## Slide 22
2 . 2
Bốn bước để tìm ra tiếng nói của khách hàng
1 Xác định các nhóm người dùng khác nhau cho sản phẩm
2 Xác định nguồn gốc yêu cầu của người dùng
3 Lựa chọn và làm việc với các cá nhân đại diện cho từng nhóm người dùng và nhóm bên liên quan khác
4 Thống nhất về việc AI là người ra quyết định về yêu cầu cho dự án
Cảnh báo quan trọng
Chỉ hỏi vài khách hàng xem họ muốn gì rồi bắt đầu viết mã là CHƯA ĐỦ. Nếu nhà phát triển xây dựng chính xác những gì khách hàng 
yêu cầu ban đầu, họ có thể sẽ phải xây dựng lại — vì khách hàng thường KHÔNG BIẾT họ thực sự cần gì. “Mong muốn” không đồng 
nghĩa với chức năng họ CẦN để thực hiện nhiệm vụ.
22

## Slide 23
2 . 2 . 1
Tám nguồn yêu cầu phần mềm điển hình
1
Phỏng vấn & thảo luận với người dùng tiềm năng
Cách rõ ràng nhất để tìm hiểu nhu cầu: hỏi họ.
 2
Tài liệu sản phẩm hiện tại / cạnh tranh
Tiêu chuẩn đơn vị, quy định, luật lệ; bài đánh giá so sánh đã công bố.
3
Đặc tả yêu cầu hệ thống
Yêu cầu hệ thống cấp cao được phân bổ cho từng hệ thống con phần 
mềm.
4
Báo cáo sự cố & yêu cầu cải tiến
Bộ phận hỗ trợ nắm rõ vấn đề người dùng gặp với hệ thống hiện tại.
5
Khảo sát tiếp thị & bảng câu hỏi
Thu thập lượng lớn dữ liệu; luôn thử nghiệm beta khảo sát trước khi 
phát.
6
Quan sát người dùng làm việc
Nghiên cứu “một ngày làm việc”: xác thực thông tin từ phỏng vấn 
trước đó.
7
Phân tích kịch bản các tác vụ người dùng
Xác định tác vụ ⇒ rút ra yêu cầu chức năng cho phép thực hiện tác vụ 
đó.
8
Sự kiện và phản hồi
Liệt kê sự kiện bên ngoài hệ thống phải phản ứng — hiệu quả với hệ 
thống thời gian thực.
23

## Slide 24
2 . 2 . 2
Lớp người dùng — phân biệt theo cách TƯƠNG TÁC
Người dùng khác nhau ở 5 khía cạnh
• Tần suất sử dụng sản phẩm
• Kinh nghiệm lĩnh vực ứng dụng & chuyên môn máy tính
• Các tính năng họ sử dụng
• Các tác vụ họ thực hiện để hỗ trợ quy trình nghiệp vụ
• Quyền truy cập / cấp độ bảo mật (thông thường, khách, 
quản trị)
Sai lầm thường gặp
Phân nhóm theo vị trí địa lý, loại đơn vị hay chức danh — thay 
vì theo CÁCH HỌ TƯƠNG TÁC với hệ thống.
Ví dụ: ngân hàng thương mại lớn / nhỏ / quỹ tín dụng là các 
PHÂN KHÚC THỊ TRƯỜNG, không phải lớp người dùng. Tên 
hợp lý hơn: “người tiếp nhận đơn xin vay” — vai trò này có 
thể do nhân viên tín dụng, phó chủ tịch, giao dịch viên… đảm 
nhiệm.
Lớp người dùng không nhất thiết phải là con người
Các ứng dụng hoặc thành phần phần cứng khác mà hệ thống tương tác cũng là lớp người dùng. Hệ thống phun nhiên liệu là một lớp
người dùng của phần mềm nhúng trong bộ điều khiển động cơ ô tô — nó không tự nói được, nên nhà phân tích phải lấy yêu cầu từ 
kỹ sư đã thiết kế hệ thống phun.
24

## Slide 25
H Ì N H  2 . 4
Phân cấp bên liên quan – khách hàng – người dùng
Bên liên quan
Tập lớn nhất: mọi cá nhân, nhóm, tổ chức tham gia 
hoặc bị ảnh hưởng.
Khách hàng
Tập con: người mua sắm, người quản lý và người 
dùng.
Người dùng
Tập con: những người thực sự sử dụng sản phẩm.
Lớp người dùng
Tập con nhỏ nhất: nhóm người dùng có cách tương 
tác tương tự.
Lớp người dùng chỉ đại diện cho một nhóm nhỏ những người cần cung cấp thông tin đầu vào 
về yêu cầu.
25

## Slide 26
2 . 2 . 2
Ưu tiên lớp người dùng & kỹ thuật “Mở rộng rồi thu hẹp”
Được ưu tiên
Favored
Nhóm mà việc chấp nhận và sử dụng hệ 
thống sẽ quyết định hệ thống có đạt được 
mục tiêu nghiệp vụ hay không. Được đối 
xử ưu tiên khi giải quyết xung đột.
Không được ưu tiên
Disfavored
Nhóm KHÔNG được phép sử dụng sản 
phẩm vì lý do pháp lý, bảo mật hoặc an 
toàn.
Bị bỏ qua / ngang nhau
Ignored / equal
Nhóm ta không xây dựng sản phẩm riêng 
để phù hợp; các lớp còn lại có tầm quan 
trọng gần như ngang nhau.
Kỹ thuật “Mở rộng rồi thu hẹp” (Expand then contract)
Bắt đầu bằng cách xem xét CÀNG NHIỀU lớp người dùng càng tốt — đừng lo nếu có hàng chục lớp. Sau đó tìm các nhóm có nhu cầu 
tương tự để kết hợp hoặc xử lý như một lớp chính với một số lớp con. Bỏ sót một lớp người dùng sẽ gây bất lợi rất lớn về sau.
Ví dụ: một công ty có 65 khách hàng doanh nghiệp từng coi mỗi công ty là một người dùng riêng biệt. Việc gom lại thành SÁU lớp người dùng 
đã đơn giản hoá đáng kể thách thức về yêu cầu cho các bản phát hành sau.
26

## Slide 27
B Ả N G  2 . 2
Lớp người dùng — hệ thống theo dõi hoá chất
Các nhà hoá học
(được ưu tiên)
~1.000 người tại 6 toà nhà; dùng hệ thống nhiều lần mỗi ngày để yêu cầu hoá chất và theo dõi thùng chứa 
ra vào phòng thí nghiệm; cần tìm kiếm danh mục theo cấu trúc hoá học.
Người mua ~5 người ở bộ phận mua hàng; xử lý yêu cầu hoá chất, đặt và theo dõi đơn hàng với nhà cung cấp; biết rất ít 
về hoá học, cần công cụ truy vấn đơn giản; ~20 lần/ngày.
Nhân viên kho hoá chất 6 kỹ thuật viên + 1 giám sát; quản lý hơn 500.000 thùng chứa; là người duy nhất dùng tính năng báo cáo tồn 
kho; khối lượng giao dịch lớn nên chức năng phải tự động và hiệu quả.
Nhân viên sở y tế
(ưu tiên)
Chỉ tạo báo cáo hàng quý theo quy định liên bang và tiểu bang; yêu cầu thay đổi báo cáo nhiều lần mỗi năm 
khi quy định thay đổi — ưu tiên hàng đầu, quan trọng về thời gian.
Ghi lại lớp người dùng, đặc điểm, trách nhiệm, vị trí và quy mô trong SRS — giúp ưu tiên yêu cầu thay đổi và đánh giá tác động sau này.
27

## Slide 28
H Ì N H  2 . 5
Các đường giao tiếp giữa người dùng và nhà phát triển
Phát hiện nghiên cứu
Các dự án THÀNH CÔNG CAO sử dụng nhiều loại 
liên kết giao tiếp và nhiều liên kết TRỰC TIẾP hơn 
giữa nhà phát triển và khách hàng, so với các dự 
án kém thành công.
Rủi ro của trung gian
Hãy nhận thức rủi ro khi dùng nhân viên tiếp thị, 
quản lý sản phẩm hay chuyên gia lĩnh vực làm đại 
diện cho tiếng nói THỰC SỰ của khách hàng.
Giao tiếp trực tiếp nhất diễn ra khi nhà phát triển tự mình giao tiếp với người dùng phù hợp 
— nghĩa là nhà phát triển cũng đang thực hiện vai trò của nhà phân tích.
28

## Slide 29
2 . 2 . 3
Người tiên phong sản phẩm (Product Champion)
Là giao diện chính giữa các thành viên của MỘT lớp người dùng và nhà phân tích yêu cầu của dự án. Họ thu thập yêu 
cầu từ các thành viên khác trong lớp mình đại diện và điều chỉnh các điểm không nhất quán.
✓ Lý tưởng là NGƯỜI DÙNG THỰC TẾ
Không phải người đại diện như nhà tài trợ, khách hàng 
mua sắm, nhân viên tiếp thị hay nhà phát triển giả vờ làm 
người dùng.
✓ Có tầm nhìn rõ ràng và nhiệt tình
Vì họ thấy được lợi ích hệ thống mang lại cho họ và đồng 
nghiệp.
✓ Giao tiếp hiệu quả, được đồng nghiệp tôn trọng
Hiểu biết sâu về lĩnh vực ứng dụng và môi trường vận 
hành của hệ thống.
! Được săn đón cho các nhiệm vụ khác
Phải xây dựng cơ sở thuyết phục về lý do cá nhân đó quan 
trọng với thành công của dự án.
Nhiều người tiên phong: hệ thống theo dõi hoá chất có 4 lớp người dùng chính ⇒ chọn 4 người tiên phong (hoá học, người mua, sở y tế, kho 
hoá chất), mỗi người dành vài giờ mỗi tuần; 3 nhà phân tích làm việc cùng họ và 1 người tổng hợp vào một SRS duy nhất.
29

## Slide 30
B Ả N G  2 . 3
Các hoạt động của người tiên phong sản phẩm
Lập kế hoạch
Tinh chỉnh phạm vi và hạn chế · Xác định giao diện với hệ thống khác · Đánh giá tác động đến hoạt động kinh doanh · 
Xác định lộ trình chuyển đổi từ ứng dụng hiện tại
Yêu cầu
Thu thập yêu cầu từ người dùng khác · Phát triển kịch bản và trường hợp sử dụng · Giải quyết xung đột · Xác định ưu 
tiên triển khai · Chỉ định yêu cầu chất lượng và hiệu năng · Đánh giá nguyên mẫu giao diện
Xác thực
Kiểm tra tài liệu yêu cầu · Xác định tiêu chí chấp nhận của người dùng · Phát triển trường hợp kiểm thử từ tình huống 
sử dụng · Cung cấp bộ dữ liệu kiểm thử · Thực hiện thử nghiệm
Trợ giúp người dùng
Viết một phần hướng dẫn sử dụng và văn bản trợ giúp · Chuẩn bị tài liệu đào tạo · Trình bày sản phẩm cho đồng nghiệp
Quản lý thay đổi
Đánh giá và ưu tiên sửa lỗi · Đánh giá và ưu tiên yêu cầu cải tiến · Đánh giá tác động của yêu cầu đề xuất · Tham gia ra 
quyết định thay đổi
Không phải người tiên phong nào cũng làm tất cả — dùng bảng này làm điểm khởi đầu để thương lượng trách nhiệm của từng người.
30

## Slide 31
2 . 2 . 3
Người tiên phong sản phẩm — những vấn đề cần tránh
Mô hình này CHỈ hiệu quả khi người tiên phong hiểu rõ và cam kết trách nhiệm, có THẨM QUYỀN ra quyết định ở cấp độ yêu cầu 
người dùng, và có ĐỦ THỜI GIAN.
✗
Nhà quản lý PHỦ QUYẾT quyết định của người tiên phong đã được uỷ quyền hợp lệ — dẫn đến người dùng không hài lòng, giao hàng trễ và 
người tiên phong thất vọng vì cảm thấy không được tin tưởng.
✗
Người tiên phong QUÊN rằng mình đang đại diện cho khách hàng khác và chỉ đưa ra yêu cầu của riêng mình.
✗
Người tiên phong THIẾU HÌNH DUNG rõ ràng về hệ thống mới nên giao phó quyết định quan trọng cho nhà phân tích — chấp nhận mọi ý 
kiến của nhà phân tích thì cũng không giúp ích gì.
✗
Người dùng cấp cao ĐỀ CỬ một người ít kinh nghiệm hơn vì không có thời gian, nhưng vẫn muốn ảnh hưởng mạnh đến hướng đi dự án.
✗
Người dùng TỰ NHẬN mình là đại diện cho một nhóm mà thực ra họ không thuộc về.
31

## Slide 32
2 . 2 . 4
Ai là người ra quyết định về yêu cầu?
Nếu không rõ ai chịu trách nhiệm, hoặc người được uỷ quyền thoái thác, quyết định sẽ MẶC ĐỊNH thuộc về NHÀ PHÁT TRIỂN —
một lựa chọn không tốt, vì họ thường không có đủ kiến thức, kinh nghiệm và tầm nhìn để ra quyết định nghiệp vụ tốt nhất.
Năm tình huống xung đột và cách xử lý được đề xuất
Người dùng cá nhân không đồng ý về yêu cầu →  Người tiên phong sản phẩm quyết định — họ được trao quyền giải quyết xung đột từ những người mình đại diện.
Các nhóm người dùng có nhu cầu không tương thích →  Ưu tiên nhóm được ưa chuộng nhất hoặc phân khúc thị trường có tác động lớn nhất đến thành công nghiệp vụ.
Mỗi khách hàng nghiệp vụ muốn thiết kế riêng cho mình →  Dùng mục tiêu nghiệp vụ của dự án để xác định khách hàng nào ảnh hưởng mạnh nhất đến thành bại.
Quản lý người dùng xung đột với người dùng thực tế →  Quản lý không phải thành viên của nhóm người dùng nên TUÂN THEO người đại diện của nhóm đó.
Nhà phát triển vs khách hàng về sản phẩm nên xây →  Thông thường KHÁCH HÀNG là người đưa ra quyết định.
Nên ra quyết định ở cấp bậc CÀNG THẤP càng tốt, bởi những người gần gũi và hiểu rõ vấn đề. Ưu tiên ra quyết định có THAM VẤN hơn là chờ 
ĐỒNG THUẬN tuyệt đối. 32

## Slide 33
2.3
Lắng nghe tiếng nói
của khách hàng
Khai thác (elicitation) là trọng tâm của kỹ nghệ yêu cầu: khám phá các tác vụ người dùng cần 
hoàn thành và kỳ vọng của họ về chất lượng.

## Slide 34
2 . 3
Lập kế hoạch cho hoạt động khai thác yêu cầu
Sản phẩm của phát triển yêu cầu là SỰ HIỂU BIẾT CHUNG giữa các bên về nhu cầu đang được giải quyết. Người tham gia 
khai thác nên TRÁNH thiết kế hệ thống cho đến khi hiểu rõ vấn đề.
1 Mục tiêu khai thác Xác thực dữ liệu thị trường, khám phá các tình huống, hay phát triển bộ yêu cầu chức năng chi tiết?
2 Chiến lược và quy trình thu thập Kết hợp khảo sát, hội thảo, thăm khách hàng, phỏng vấn cá nhân — có thể khác nhau cho từng nhóm bên liên quan.
3 Sản phẩm của nỗ lực thu thập Danh sách tình huống, SRS chi tiết, phân tích kết quả khảo sát, hoặc thông số thuộc tính chất lượng.
4 Ước tính lịch trình và nguồn lực Xác định người tham gia phía phát triển và phía khách hàng, cùng ước tính nỗ lực và thời gian.
5 Rủi ro khai thác Yếu tố cản trở việc hoàn thành hoạt động khai thác; ước tính mức nghiêm trọng và cách giảm thiểu.
34

## Slide 35
2 . 3 . 1
Thu thập yêu cầu — nghệ thuật đặt câu hỏi
① Dùng từ vựng của MIỀN ỨNG DỤNG
Không buộc khách hàng phải hiểu thuật ngữ máy tính; ghi 
lại thuật ngữ quan trọng trong một bảng thuật ngữ chung.
② Hỏi “TẠI SAO” nhiều lần
Đưa cuộc thảo luận từ một giải pháp được trình bày sang 
sự hiểu biết sâu sắc về vấn đề cần giải quyết.
③ Đặt câu hỏi MỞ và thăm dò ngoại lệ
“Còn điều gì khác có thể…”, “Điều gì xảy ra khi…”, “Bạn có 
bao giờ cần phải…”, “Bạn lấy… ở đâu?”, “Có ai từng…”.
④ Đóng vai người học việc
Tưởng tượng bạn đang học công việc của người dùng —
người dùng sẽ dẫn dắt và mô tả điều họ coi là quan trọng.
Câu hỏi vàng khi thay hệ thống cũ
“Ba điều gì khiến bạn khó chịu nhất về hệ thống hiện tại?”
Sau mỗi cuộc phỏng vấn
Ghi lại các mục đã thảo luận và yêu cầu người được phỏng vấn 
XEM LẠI và CHỈNH SỬA.
35

## Slide 36
2 . 3 . 2
Hội thảo thu thập yêu cầu — vai trò và quy tắc
Ba vai trò trong hội thảo
• Người điều phối (facilitator): lên kế hoạch, chọn người 
tham gia, dẫn dắt tới kết quả
• Người ghi chép (scribe): ghi lại các điểm được nêu trong 
suốt cuộc thảo luận
• Người tham gia: người tiên phong sản phẩm, đại diện 
người dùng, chuyên gia, nhà phân tích, nhà phát triển
Quy tắc cơ bản cần thống nhất
• Bắt đầu và kết thúc cuộc họp đúng giờ
• Trở về sau giờ nghỉ đúng giờ
• Chỉ một cuộc trò chuyện tại một thời điểm
• Mong đợi mọi người đóng góp
• Tập trung phê bình vào VẤN ĐỀ, không phải vào CÁ 
NHÂN
Điều phối là gì?
“Điều phối là NGHỆ THUẬT dẫn dắt mọi người thông qua các quy trình hướng tới những mục tiêu đã thống nhất, theo cách khuyến 
khích sự tham gia, tinh thần làm chủ và năng suất từ tất cả những người liên quan.”
Khi nhóm mới áp dụng phương pháp này, hãy để một người điều phối BÊN NGOÀI dẫn dắt các buổi đầu tiên — nhờ vậy nhà phân 
tích có thể tập trung hoàn toàn vào nội dung thảo luận.
36

## Slide 37
2 . 3 . 2
Bốn nguyên tắc điều hành hội thảo hiệu quả
1 Duy trì phạm vi
Dùng tài liệu tầm nhìn & phạm vi để xác nhận yêu cầu đề xuất có nằm trong phạm vi hiện tại. Người dùng dễ liệt kê bố cục chính xác của 
báo cáo hay hộp thoại TRƯỚC KHI nhóm thống nhất về nhiệm vụ người dùng — ghi lại chi tiết đó sẽ đặt ra hạn chế không cần thiết cho 
thiết kế sau này.
2 Thảo luận theo khung thời gian
Phân bổ thời gian cố định cho mỗi chủ đề (ví dụ 30 phút mỗi tình huống). Timebox giúp tránh dành quá nhiều thời gian cho chủ đề đầu 
tiên và bỏ bê các chủ đề đã lên kế hoạch.
3 Duy trì quy mô nhóm nhỏ
Hội thảo với hơn 5–6 người tham gia tích cực dễ sa lầy vào thảo luận riêng lẻ và cãi vã. Cân nhắc tổ chức nhiều buổi song song cho các 
nhóm người dùng khác nhau.
4 Giữ cho mọi người tham gia
Người điều phối phải đọc ngôn ngữ cơ thể, hiểu vì sao ai đó ngừng đóng góp và đưa họ trở lại — cá nhân đó có thể có quan điểm sâu 
sắc, đóng góp quan trọng.
37

## Slide 38
H Ì N H  2 . 6
Phân loại tiếng nói của khách hàng — 9 nhóm
1 Yêu cầu nghiệp vụ
2 Tình huống hoặc ngữ cảnh
3 Quy tắc nghiệp vụ
4 Yêu cầu chức năng
5 Thuộc tính chất lượng
6 Yêu cầu giao diện bên ngoài
7 Ràng buộc
8 Định nghĩa dữ liệu
9 Ý tưởng giải pháp
Đừng mong đợi khách hàng trình bày một danh sách ngắn gọn, đầy đủ và được 
sắp xếp hợp lý. Nhà phân tích phải PHÂN LOẠI vô số thông tin nghe được để ghi 
chép và sử dụng đúng cách.
38

## Slide 39
2 . 3 . 3
Cụm từ cần lắng nghe (1/2)
Yêu cầu nghiệp vụ
Mô tả lợi ích tài chính, thị trường hoặc 
nghiệp vụ mà tổ chức mong đạt được.
“Tăng thị phần lên X%.” · “Tiết kiệm Y đô la mỗi năm cho điện bị lãng phí.” · “Tiết kiệm Z đô la chi phí bảo 
trì hệ thống W cũ.”
Tình huống / kịch bản
Tuyên bố chung về mục tiêu người dùng 
hoặc nhiệm vụ nghiệp vụ cần thực hiện.
“Tôi cần in nhãn gửi thư cho một kiện hàng.” · “Tôi cần quản lý hàng loạt mẫu hoá chất chờ phân tích.” · 
“Tôi cần hiệu chuẩn bộ điều khiển bơm.”
Quy tắc nghiệp vụ
Chỉ một số lớp người dùng được thực hiện 
hoạt động trong điều kiện cụ thể. KHÔNG 
phải yêu cầu chức năng.
“Phải tuân thủ <luật / chính sách>.” · “Phải tuân thủ <tiêu chuẩn>.” · “Nếu <điều kiện đúng> thì <điều gì 
đó xảy ra>.” · “Phải được tính theo <công thức>.”
Yêu cầu chức năng
Hành vi quan sát được mà hệ thống thể hiện, 
và hành động hệ thống cho phép người dùng 
thực hiện.
“Nếu áp suất vượt quá 40, đèn cảnh báo sẽ bật sáng.” · “Người dùng phải có khả năng sắp xếp danh 
sách dự án.” · “Hệ thống sẽ gửi email khi ai đó gửi ý tưởng mới.”
39

## Slide 40
2 . 3 . 3
Cụm từ cần lắng nghe (2/2)
Thuộc tính chất lượng
Hệ thống thực hiện hành vi TỐT NHƯ THẾ NÀO.
Các từ mô tả: nhanh, dễ dàng, trực quan, thân thiện, mạnh mẽ, đáng tin cậy, an toàn, hiệu quả → phải làm rõ 
và viết thành mục tiêu KIỂM CHỨNG ĐƯỢC.
Yêu cầu giao diện bên ngoài
Kết nối giữa hệ thống của ta và phần còn lại.
“Phải đọc tín hiệu từ <thiết bị>.” · “Phải gửi tin nhắn đến <hệ thống khác>.” · “Phải đọc/ghi tệp ở <định 
dạng>.” · “Phải tuân thủ <tiêu chuẩn UI>.”
Ràng buộc
Hạn chế hợp lệ các tuỳ chọn của nhà phát triển.
Ghi lại LÝ DO đằng sau mỗi ràng buộc. Ràng buộc không cần thiết cản trở giải pháp tốt nhất; ràng buộc chỉ 
định công nghệ cụ thể có nguy cơ lỗi thời.
Định nghĩa dữ liệu
Định dạng, kiểu, giá trị được phép hoặc mặc 
định của một mục dữ liệu.
“Mã ZIP gồm năm chữ số, theo sau là dấu gạch ngang tuỳ chọn và bốn chữ số mặc định 0000.” → thu thập 
vào TỪ ĐIỂN DỮ LIỆU.
Ý tưởng giải pháp
Phần lớn những gì người dùng nêu ra thuộc 
nhóm này.
Người mô tả một cách CỤ THỂ để tương tác với hệ thống là đang đề xuất giải pháp. Nhà phân tích phải đào 
sâu để nắm YÊU CẦU THỰC SỰ (mật khẩu chỉ là một giải pháp cho yêu cầu bảo mật).
40

## Slide 41
2 . 3 . 3  – 2 . 3 . 4
Ngoài 9 nhóm & một số lưu ý khi thu thập
Thông tin không thuộc 9 nhóm
• Yêu cầu không liên quan đến phát triển phần mềm (ví 
dụ: đào tạo người dùng)
• Ràng buộc của DỰ ÁN: chi phí, lịch trình
• Một giả định
• Một yêu cầu về dữ liệu
• Thông tin bổ sung mang tính lịch sử, bối cảnh hoặc mô tả
Cân bằng số lượng đại diện
Quá ít đại diện, hoặc chỉ nghe khách hàng “có quan điểm nhất”, 
dẫn đến bỏ sót yêu cầu quan trọng hoặc đưa vào yêu cầu không 
đại diện cho đa số.
Cân bằng tốt nhất: một vài người tiên phong CÓ THẨM QUYỀN, 
mỗi người được hỗ trợ bởi một số đại diện khác từ cùng lớp 
người dùng.
Phạm vi quá lớn hay quá nhỏ?
Quá lớn → thu thập nhiều yêu cầu hơn mức cần thiết, quá trình 
kéo dài. Quá nhỏ → khách hàng nêu nhu cầu rõ ràng quan trọng 
nhưng nằm ngoài phạm vi. Thu thập yêu cầu có thể dẫn tới THAY 
ĐỔI tầm nhìn hoặc phạm vi.
“Cái gì” vs “Thế nào” — vùng xám
Khai thác nên tập trung vào “cái gì”, nhưng giữa phân tích và 
thiết kế là một VÙNG XÁM, không phải ranh giới rõ. Mô hình, bản 
phác thảo màn hình và nguyên mẫu chỉ là GỢI Ý KHÁI NIỆM để 
giao tiếp, không phải ràng buộc thiết kế cuối cùng.
41

## Slide 42
2 . 3 . 5
Tìm kiếm các yêu cầu còn thiếu
Thiếu yêu cầu là loại KHIẾM KHUYẾT PHỔ BIẾN NHẤT — và rất khó phát hiện khi đánh giá, vì chúng VÔ HÌNH.
1 Phân tích yêu cầu cấp cao thành đủ chi tiết
Yêu cầu mơ hồ để lại nhiều cách hiểu sẽ tạo khoảng cách 
giữa điều người yêu cầu nghĩ và điều nhà phát triển xây. 
Tránh các từ: hỗ trợ, cho phép, xử lý, quản lý.
2 Bảo đảm mọi lớp người dùng có đầu vào
Và bảo đảm mỗi tình huống có ít nhất một tác nhân được 
xác định.
3 Theo dõi truy vết xuống yêu cầu chức năng
Truy vết yêu cầu hệ thống, tình huống, danh sách phản hồi 
sự kiện và quy tắc nghiệp vụ xuống các yêu cầu chức năng 
chi tiết.
4 Biểu diễn yêu cầu theo NHIỀU CÁCH
Khó đọc một khối văn bản và nhận ra điều bất ổn. Trên mô 
hình trực quan, một mũi tên bị thiếu chính là một yêu cầu 
bị thiếu — dễ phát hiện hơn nhiều.
Một cách nghiêm ngặt để tìm yêu cầu còn thiếu: tạo MA TRẬN CRUD(L) — Create · Read · Update · Delete · List.
42

## Slide 43
H Ì N H  2 . 7
Ma trận CRUDL cho hệ thống theo dõi hoá chất
Cách đọc: cột “Người yêu cầu” không có ô nào chứa chữ D — ba cách diễn giải có thể
① Việc xoá người yêu cầu KHÔNG phải chức năng mong đợi của hệ thống · ② Chúng ta đang THIẾU một tình huống để xoá người yêu 
cầu · ③ Tình huống “Chỉnh sửa người yêu cầu” mô tả CHƯA CHÍNH XÁC — lẽ ra cho phép xoá nhưng chức năng đó đang bị thiếu.
43

## Slide 44
2.4
Các kỹ thuật
thu thập yêu cầu
Mười kỹ thuật chủ yếu: Phỏng vấn · Nhóm tập trung · Tạo mẫu · Bảng câu hỏi · Phân tích giao 
diện · JAD · Động não · Phân tích tài liệu · Hội thảo · Quan sát.

## Slide 45
2 . 4 . 1  – 2 . 4 . 2
Phỏng vấn & Nhóm tập trung
1. Phỏng vấn
Interview
Bản chất
Trò chuyện có cấu trúc, bán cấu trúc hoặc phi cấu trúc; nhà phân 
tích đặt câu hỏi có mục tiêu để bên liên quan nêu rõ kỳ vọng, thách 
thức và hành vi mong muốn của hệ thống.
Điểm mạnh
Linh hoạt và có cơ hội đặt câu hỏi TIẾP THEO; đặc biệt hữu ích để 
khám phá KIẾN THỨC NGẦM mà bên liên quan không nghĩ tới việc 
ghi lại.
Hạn chế
Tốn thời gian; chất lượng phụ thuộc nhiều vào kỹ năng giao tiếp của 
cả hai phía.
2. Nhóm tập trung
Focus group
Bản chất
Tập hợp một nhóm nhỏ bên liên quan (thường 6–12 người) trong 
một cuộc thảo luận có hướng dẫn do người điều phối dẫn dắt.
Điểm mạnh
Sự cộng hưởng nhóm: khi nghe người khác bày tỏ, người dùng suy 
ngẫm sâu hơn và đóng góp thêm; cho phép quan sát ĐỒNG THUẬN 
và BẤT ĐỒNG giữa các phân khúc.
Hạn chế
Khó lên lịch; dễ bị ảnh hưởng bởi áp lực nhóm và người tham gia có 
ảnh hưởng.
45

## Slide 46
2 . 4 . 1
Năm lưu ý khi tiến hành phỏng vấn
1 Bắt đầu bằng những câu hỏi CHUNG Cho phép bên liên quan mô tả điều họ cần bằng chính ngôn từ của họ, đồng thời cho ta cái nhìn về mục tiêu và kỳ vọng.
2 Tránh câu hỏi trả lời được bằng một từ Câu trả lời “Có” hoặc “Không” không cung cấp dữ liệu liên quan — ta cần thông tin cụ thể.
3 NHẮC LẠI những gì ta nghe “Điều này quan trọng với bạn vì nó giúp đơn vị bạn an toàn hơn?” — khẳng định lại mong muốn, giảm khả năng hiểu lầm.
4 Đặt nhiều câu hỏi TIẾP THEO Đây là cách thu thập đầy đủ các chi tiết cụ thể ẩn sau một phát biểu chung.
5 Luôn LẮNG NGHE cẩn thận Kỹ năng lắng nghe tốt và thiết lập mối quan hệ với bên liên quan là chìa khoá để thực sự hiểu nhu cầu của họ.
Lắng nghe tích cực: chú ý cả giọng điệu, sự ngập ngừng và tín hiệu phi ngôn ngữ, không chỉ nội dung lời nói.
46

## Slide 47
2 . 4 . 3  – 2 . 4 . 4
Tạo mẫu & Bảng câu hỏi
3. Tạo mẫu
Prototyping
Bản chất
Tạo một phiên bản ban đầu, đơn giản hoá của phần mềm — bản mô 
phỏng giấy (độ trung thực thấp) hoặc mô hình tương tác (độ trung 
thực cao) — để người dùng hình dung và tương tác.
Điểm mạnh
Hiện thực hoá ý tưởng trừu tượng; phát hiện YÊU CẦU TIỀM ẨN mà 
người dùng không nhớ ra; phơi bày sự không nhất quán giữa các 
nhóm người dùng ngay từ đầu.
Hạn chế
Người dùng dễ nhầm nguyên mẫu là hệ thống cuối; rủi ro “mất kiểm 
soát nguyên mẫu” nếu không quản lý phạm vi.
4. Bảng câu hỏi
Questionnaire / Survey
Bản chất
Thu thập thông tin từ nhiều người trả lời cùng lúc qua các biểu mẫu 
viết có cấu trúc; kết hợp câu hỏi đóng (trắc nghiệm, thang đánh giá) 
và câu hỏi mở.
Điểm mạnh
Hiệu quả chi phí, có khả năng mở rộng; phù hợp khi thời gian, 
khoảng cách địa lý hoặc nguồn lực cản trở thảo luận trực tiếp; dễ 
phân tích khi thu điện tử.
Hạn chế
Không có cơ hội làm rõ hay theo dõi; người trả lời có thể hiểu khác 
nhau; tỷ lệ phản hồi có thể thấp.
47

## Slide 48
2 . 4 . 4
Nội dung một bảng câu hỏi thu thập yêu cầu
Tổng quan dự án Mục đích của dự án? · Mục tiêu và mục đích? · Kết quả mong đợi / sản phẩm đầu ra? · Định nghĩa thành công? · Đầu mối liên hệ chính? · Đối tượng mục tiêu?
Tiến độ & ngân sách Tiến độ dự kiến bao lâu? · Có mốc thời gian cụ thể nào? · Ngân sách được phân bổ? · Có hạn chế nào về nguồn lực?
Yêu cầu chức năng Những chức năng cụ thể nào được yêu cầu? · Tính năng nào là quan trọng? · Các yêu cầu kiểm thử là gì?
Yêu cầu phi chức năng Kỳ vọng về hiệu năng (tốc độ, khả năng mở rộng)? · Yêu cầu bảo mật hoặc tuân thủ? · Kỳ vọng về khả năng sử dụng và trải nghiệm người dùng?
Chi tiết kỹ thuật Nền tảng công nghệ nào cần hỗ trợ? · Yêu cầu tích hợp với hệ thống khác? · Hệ thống xử lý những loại dữ liệu nào?
Thông tin bổ sung & tài liệu Yêu cầu pháp lý / quy định? · Rủi ro tiềm ẩn và cách giảm thiểu? · Tiêu chuẩn đảm bảo chất lượng? · Tải lên tài liệu quan trọng.
Luôn THỬ NGHIỆM bảng câu hỏi với một mẫu nhỏ trước khi phân phối rộng rãi — để phát hiện câu hỏi mơ hồ, thiếu chủ đề hoặc vấn đề
định dạng. 48

## Slide 49
2 . 4 . 5  – 2 . 4 . 6
Phân tích giao diện & Phát triển ứng dụng chung (JAD)
5. Phân tích giao diện
Interface analysis
Bản chất
Xác định, kiểm tra và định nghĩa các tương tác giữa hệ thống và 
thực thể bên ngoài: người dùng, hệ thống khác, thiết bị phần cứng, 
CSDL, dịch vụ bên thứ ba.
Điểm mạnh
Giảm mơ hồ về RANH GIỚI hệ thống; ngăn bỏ sót yêu cầu tích hợp 
— vốn là một trong những vấn đề tốn kém nhất trong phát triển 
phần mềm.
Hạn chế
Đòi hỏi hợp tác chặt chẽ với chuyên gia kỹ thuật và quyền truy cập 
tài liệu API, hướng dẫn thiết bị.
6. JAD
Joint Application Development
Bản chất
Hội thảo có cấu trúc, được điều phối, tập hợp người dùng, quản lý, 
nhà phát triển và nhà phân tích để thảo luận, làm rõ và đàm phán 
yêu cầu theo THỜI GIAN THỰC.
Điểm mạnh
TÍCH HỢP THÔNG TIN NGAY LẬP TỨC — mâu thuẫn giữa hai người 
dùng lộ ra tức thì cùng nguồn gốc của nó; tăng sự đồng thuận và 
tinh thần làm chủ của người dùng.
Hạn chế
Khó lên lịch; đòi hỏi kỹ năng điều phối cao và chuẩn bị kỹ; là kỹ thuật 
khó nhất trong các kỹ thuật đã học.
49

## Slide 50
2 . 4 . 7  – 2 . 4 . 8
Tư duy sáng tạo & Phân tích tài liệu
7. Tư duy sáng tạo
Brainstorming
Bản chất
Nhóm nhỏ bên liên quan cùng khám phá phần mềm NÊN làm gì. 
Nguyên tắc cốt lõi: KHÔNG PHÊ BÌNH — ưu tiên SỐ LƯỢNG ý tưởng, 
sau đó mới nhóm, loại trùng và đánh giá tính khả thi.
Điểm mạnh
Kích thích sáng tạo, thúc đẩy tham gia, bộc lộ quan điểm đa dạng; 
đặc biệt hữu ích ở giai đoạn đầu hoặc khi dự án hướng tới đổi mới.
Hạn chế
Cá tính nổi trội có thể lấn át; thường chỉ tạo ra ý tưởng CẤP CAO, 
cần kỹ thuật tiếp theo để chuyển thành yêu cầu chi tiết.
8. Phân tích tài liệu
Document analysis
Bản chất
Xem xét có hệ thống các tài liệu hiện có để hiểu quy trình hiện tại, 
hành vi hệ thống, quy tắc nghiệp vụ và kỳ vọng của các bên liên 
quan.
Điểm mạnh
Cung cấp thông tin KHÁCH QUAN và KIỂM CHỨNG ĐƯỢC — bằng 
chứng thực tế về cách tổ chức hoạt động; làm rõ yêu cầu bắt buộc 
như tuân thủ quy định.
Hạn chế
Tài liệu có thể lỗi thời, thiếu hoặc không khớp thực tiễn; nhân viên 
thường có giải pháp thay thế không chính thức, không được ghi lại.
50

## Slide 51
2 . 4 . 8
Những tài liệu có thể phân tích
“Đây là một công việc nhàm chán và vất vả, nhưng lại là một hướng đi khác để thu thập yêu cầu.”
Kế hoạch kinh doanh
 Tài liệu tiếp thị
 Thoả thuận
 Yêu cầu đề xuất
Luồng quy trình hiện tại
 Mô hình dữ liệu logic
 Quy tắc nghiệp vụ
 Kho lưu trữ
Tài liệu phần mềm ứng dụng
 Tài liệu quy trình / giao diện 
nghiệp vụ
 Tình huống
 Tài liệu yêu cầu khác
Nhật ký sự cố / vấn đề
 Chính sách
 Quy trình
 Tài liệu quy định (luật, quy 
tắc…)
Ví dụ: khi xây hệ thống thông tin sinh viên mới cho một trường đại học, nhà phân tích xem xét quy định học thuật, biểu mẫu đăng ký, chính 
sách chấm điểm và hướng dẫn sử dụng hệ thống cũ.
51

## Slide 52
2 . 4 . 9  – 2 . 4 . 1 0
Hội thảo & Quan sát
9. Hội thảo
Workshop
Bản chất
Tập hợp nhiều bên liên quan trong môi trường hợp tác để TẠO, 
TINH CHỈNH và XÁC THỰC yêu cầu theo thời gian thực, qua các hoạt 
động có hướng dẫn: động não, nhập vai, lập bản đồ quy trình, bài 
tập ưu tiên.
Điểm mạnh
Đẩy nhanh RA QUYẾT ĐỊNH — tranh luận, đàm phán và đạt đồng 
thuận trong cùng một buổi; người tham gia có cảm giác sở hữu nên 
giảm phản kháng khi triển khai.
Hạn chế
Khó lên lịch; tiếng nói chủ đạo dễ lấn át; tạo ra khối lượng thông tin 
lớn cần ghi chép và phân tích theo dõi cẩn thận.
10. Quan sát
Observation
Bản chất
Quan sát người dùng thực hiện tác vụ hằng ngày trong MÔI 
TRƯỜNG LÀM VIỆC TỰ NHIÊN. Hai hình thức: chủ động (tham gia, 
đặt câu hỏi) và thụ động (quan sát im lặng, không can thiệp).
Điểm mạnh
Ghi lại HÀNH VI THỰC TẾ chứ không phải điều người dùng nhớ ra; 
phát hiện điểm kém hiệu quả, tắc nghẽn, giải pháp tạm thời và hoạt 
động không được ghi chép.
Hạn chế
Tốn thời gian, cần giám sát kéo dài; người dùng có thể thay đổi 
hành vi khi biết bị quan sát; một số tác vụ bị hạn chế vì bảo mật 
hoặc an toàn.
52

## Slide 53
2.5
Lựa chọn
kỹ thuật phù hợp
Không kỹ thuật nào luôn tốt hơn kỹ thuật khác — hầu hết dự án đều sử dụng kết hợp nhiều 
kỹ thuật theo sáu tiêu chí so sánh.

## Slide 54
H Ì N H  2 . 8
Bảng so sánh các kỹ thuật thu thập yêu cầu
Về kinh nghiệm cần có: phân tích tài liệu và quan sát đòi hỏi ít đào tạo nhất, trong khi các buổi JAD là khó khăn nhất.
54

## Slide 55
2 . 5
Sáu tiêu chí lựa chọn kỹ thuật
1 Loại thông tin
Phù hợp với giai đoạn nào: hiểu hệ trạng, xác định cải tiến hay phát triển hệ thống tương lai. Phỏng vấn và JAD 
dùng được cả ba; phân tích tài liệu và quan sát hữu ích nhất cho hệ trạng.
2 Độ sâu thông tin
Mức độ phong phú, chi tiết và khả năng hiểu được LÝ DO đằng sau. Phỏng vấn và JAD rất cao; bảng câu hỏi ở mức 
trung bình.
3 Độ rộng thông tin
Phạm vi và số nguồn thông tin thu được. Bảng câu hỏi và phân tích tài liệu rất cao; phỏng vấn và quan sát phải 
xem xét từng nguồn nên tốn thời gian.
4 Tích hợp thông tin
Kết hợp thông tin mâu thuẫn từ nhiều nguồn. JAD vượt trội vì thông tin được tích hợp NGAY KHI thu thập — đây 
là lợi ích quan trọng nhất của JAD.
5 Sự tham gia của người dùng
Bảng câu hỏi, phân tích tài liệu và quan sát đặt gánh nặng ít nhất; JAD đòi hỏi nỗ lực lớn nhất từ người dùng.
6 Chi phí
Bảng câu hỏi, phân tích tài liệu và quan sát chi phí thấp; phỏng vấn và JAD chi phí vừa phải. JAD tốn kém ban đầu 
nhưng tiết kiệm hơn về lâu dài nhờ giảm thời gian tích hợp.
55

## Slide 56
2 . 5
Kết hợp các kỹ thuật trong thực tế
1
Phỏng vấn quản lý cấp cao Hiểu rõ hơn về dự án và các vấn đề tổng thể; thấy được thay đổi lớn hay nhỏ đang được 
dự đoán.
2
Phân tích tài liệu & chính sách Hiểu rõ hơn về hệ thống hiện trạng.
3
Phỏng vấn tiếp theo Thu thập phần thông tin còn thiếu cho bức tranh tổng thể.
4
Các phiên JAD Xác định cải tiến: người dùng và bên liên quan chính cùng đi đến hiểu biết chung về khả 
năng của hệ thống tương lai.
5
Bảng câu hỏi diện rộng Gửi tới nhóm người dùng rộng hơn để xem ý kiến của người tham gia JAD có được chia sẻ 
rộng rãi hay không.
6
JAD với người dùng mọi cấp Phát triển khái niệm cho hệ thống tương lai, bảo đảm nhu cầu chính được hiểu rõ.
Trình tự trên chỉ là một lộ trình điển hình — hãy điều chỉnh theo quy mô, phương pháp luận và con người của từng dự án.
56

## Slide 57
2.6
Công cụ
thu thập yêu cầu
Phương pháp “hộp công cụ”: mỗi dự án, mỗi phương pháp luận và mỗi nhóm người khác 
nhau thì công cụ yêu cầu cũng không nên giống nhau.

## Slide 58
H Ì N H  2 . 9
Lược đồ ngữ cảnh (Context diagram)
Vai trò
• Xác định RANH GIỚI của hệ thống và 
môi trường xung quanh
• Hệ thống được vẽ ở giữa sơ đồ
• Xác định khách hàng, hệ thống bên 
trong/bên ngoài, người dùng cuối, 
nhà cung cấp dịch vụ bên thứ ba
• Giúp người dùng cuối thống nhất cái 
gì TRONG và cái gì NGOÀI phạm vi
Bằng cách xây dựng mô hình trực quan của giải pháp phần mềm, chúng ta hiểu rõ hơn về các 
tương tác và tác nhân chính trong hệ thống.
58

## Slide 59
H Ì N H  2 . 1 0  – 2 . 1 1
Phân rã chức năng & Lược đồ chức năng
Phân rã chức năng
Góc nhìn TỪ TRÊN XUỐNG về quy trình nghiệp vụ và các chức năng 
chính; tương tự sơ đồ tổ chức nên người dùng cuối dễ liên hệ. Kết 
quả thường làm cơ sở cho danh sách use case ban đầu.
Lược đồ chức năng (Use case)
Mô tả tương tác giữa hệ thống và người dùng. Mỗi vai trò người 
dùng là một “tác nhân” (actor); mỗi tương tác có thể chia nhỏ thành 
các bước gồm “đường chính” và các đường thay thế.
59

## Slide 60
2 . 6 . 3
Ví dụ phân rã một tình huống: Nộp đơn xin thẻ tín dụng
Tình huống Nộp đơn.
Tác nhân Khách hàng.
Mô tả Mô tả quy trình nộp đơn xin thẻ tín dụng.
Hoàn tất thành công ① Người dùng nhập thông tin đơn xin, bao gồm mã số an sinh xã hội  ·  ② Hệ thống xác thực dữ liệu nhập 
vào có lỗi không  ·  ③ Hệ thống nộp đơn.
Phương án thay thế Hệ thống từ chối đơn xin, trích dẫn lỗi nhập biểu mẫu về mã số an sinh xã hội.
Điều kiện tiên quyết Người dùng đã được chuyển hướng đến đơn xin tín dụng từ chiến dịch email hoặc trang web.
Điều kiện hậu quyết Người dùng nhận được thông báo thành công.
Giả định Không có.
Chi tiết đặc tả use case sẽ được trình bày trong Chương 3.
60

## Slide 61
2 . 6 . 4  – 2 . 6 . 6
Lược đồ trình tự · Câu chuyện người dùng · Sơ đồ tư duy
Lược đồ trình tự
Thể hiện tương tác giữa các đối tượng THEO THỜI GIAN. Trong 
giai đoạn thu thập, dùng để minh hoạ một use case cụ thể — ví 
dụ trình tự thông điệp giữa “Người dùng”, “Giao diện đăng nhập” 
và “Cơ sở dữ liệu”. Nhờ đó phát hiện sớm các bước tương tác 
còn thiếu.
Câu chuyện người dùng
Công cụ hữu ích để nhanh chóng xác định các chức năng chính. Vì 
được viết trên thẻ ghi chú (vật lý hoặc ảo), một câu chuyện quá 
phức tạp có thể được CHIA NHỎ thành các câu chuyện nhỏ hơn 
và được hỗ trợ bằng một trong các sơ đồ nêu trên.
Hình 2.12. Sơ đồ tư duy (Mind map)
Nên dùng ở GIAI ĐOẠN ĐẦU của hội thảo, khi ý tưởng còn 
rời rạc và chưa có cấu trúc. Nó giúp sắp xếp cuộc trò 
chuyện bằng cách liên kết bình luận, yêu cầu và ý tưởng 
vào các nhánh tư duy chính — tránh lạc đề. Sau khi hoàn 
thiện, sơ đồ có thể chuyển thành danh sách yêu cầu đã ưu 
tiên, hoặc làm đầu vào cho sơ đồ phân rã chức năng.
61

## Slide 62
2 . 6 . 7  – 2 . 6 . 1 3
Bảy nhóm công cụ phần mềm hỗ trợ thu thập yêu cầu
Công cụ cộng tác Jira · Trello · Asana Phân công nhiệm vụ, theo dõi tiến độ, diễn đàn thảo luận. Ví dụ: bảng Trello với cột “Yêu cầu mới – Đang làm rõ – Đã xác nhận”.
Quản lý tài liệu Confluence · SharePoint Kho lưu trữ tập trung, kiểm soát phiên bản. Mỗi tài liệu yêu cầu gắn nhãn phiên bản, liên kết trang thảo luận.
Khảo sát & biểu mẫu Google Forms · Typeform · 
SurveyMonkey
Thu thập dữ liệu có cấu trúc từ lượng lớn đối tượng khi phỏng vấn từng người 
không khả thi.
Công cụ tạo mẫu Sketch · Balsamiq · Figma Dựng nhanh bản mẫu giao diện gửi cho bên liên quan phản hồi TRƯỚC KHI viết mã — giảm chi phí sửa đổi về sau.
Kiểm soát phiên bản Git · SVN Đặc tả lưu dạng Markdown trong kho Git: mỗi chỉnh sửa ghi nhận người thực hiện và lý do; khôi phục được yêu cầu cũ.
Quản lý yêu cầu IBM DOORS · Jama Connect Mỗi yêu cầu có mã định danh duy nhất, liên kết với thiết kế và kiểm thử; ma trận truy xuất được tạo TỰ ĐỘNG.
Cộng tác trực quan DrawIO · Miro · Lucidchart Nhiều thành viên cùng chỉnh sửa lược đồ ngữ cảnh hay sơ đồ luồng theo thời gian thực trong hội thảo trực tuyến.
Phương pháp “hộp công cụ”: dùng nhiều công cụ và kỹ thuật khác nhau, thay vì ép mọi dự án dùng chung một công cụ yêu cầu.
62

## Slide 63
2.7 – 2.9
Quy trình · Trở ngại
· Biểu mẫu
Sáu bước của quy trình thu thập yêu cầu, bảy trở ngại phổ biến cần vượt qua, và các mẫu tài 
liệu chuẩn hoá đầu ra.

## Slide 64
2 . 7
Quy trình thu thập yêu cầu — 6 bước
1
Phân công vai trò và xác định các bên liên quan Phân công trách nhiệm thu thập và phân tích cho quản lý dự án, chuyên viên phân tích 
nghiệp vụ…; xác định khách hàng, người dùng cuối, nhà tài trợ và các bên quan tâm khác.
2
Gặp gỡ các bên liên quan và đặt câu hỏi Phỏng vấn, thảo luận nhóm tập trung, khảo sát… Đặt CÂU HỎI MỞ để khuyến khích họ chia 
sẻ suy nghĩ và ý tưởng.
3
Thu thập thông tin để bắt đầu dự án Phân tích quy trình hiện có, nghiên cứu thông lệ tốt nhất trong ngành, xem xét tài liệu liên 
quan.
4
Liệt kê các giả định và mục tiêu yêu cầu Thời lượng dự án, người tham gia, ngân sách và các rủi ro liên quan — giúp mọi thành viên 
cùng đi đúng hướng.
5
Nhận phê duyệt Trình bày phát hiện cho các bên liên quan, xin ý kiến đóng góp và sự chấp thuận TRƯỚC KHI 
triển khai.
6
Giám sát tiến độ Kiểm tra thường xuyên với các bên liên quan, báo cáo tiến độ; thực hiện điều chỉnh cần thiết 
trong suốt dự án.
64

## Slide 65
V Í  D Ụ  M I N H  H O Ạ
Áp dụng 6 bước: Hệ thống đặt sách của hiệu sách trường
Sinh viên đặt sách trực tuyến và nhận sách tại ký túc xá hoặc nhà ở ngoài trường.
1 Vai trò & bên liên quan Chỉ định 1 BA và 1 quản lý dự án. Bên liên quan: sinh viên, nhân viên hiệu sách, phòng công tác sinh viên, ban quản lý ký túc xá, bộ phận CNTT, nhà cung cấp sách.
2 Gặp gỡ & đặt câu hỏi Phỏng vấn 3 nhân viên hiệu sách, khảo sát 300 sinh viên, tổ chức 1 nhóm tập trung 8 sinh viên ở nội trú và ngoại trú.
3 Thu thập thông tin Phân tích quy trình bán sách hiện tại, biểu mẫu đặt hàng giấy, dữ liệu tồn kho học kỳ trước và cách các trường khác triển khai.
4 Giả định & mục tiêu Giả định: hệ thống dùng chung tài khoản sinh viên hiện có. Mục tiêu: giảm 60% thời gian xếp hàng đầu học kỳ; giao trong 24 giờ; ngân sách và 4 tháng triển khai.
5 Nhận phê duyệt Trình bày tài liệu yêu cầu cho ban giám hiệu và trưởng hiệu sách; chốt phạm vi bản 1.0 (đặt và nhận sách), hoãn thanh toán online sang bản 1.1.
6 Giám sát tiến độ Họp kiểm tra 2 tuần/lần với hiệu sách; theo dõi yêu cầu trên Jira; mọi thay đổi phạm vi phải qua phê duyệt của trưởng hiệu sách.
65

## Slide 66
2 . 8
Bảy trở ngại phổ biến khi thu thập yêu cầu
✗ Mục tiêu không rõ ràng Bên liên quan không chắc chắn muốn đạt được gì → khó xác định và ưu tiên yêu cầu; dẫn tới nhầm lẫn và vượt phạm vi.
✗ Yêu cầu mơ hồ Ngôn ngữ mơ hồ hoặc tuyên bố mâu thuẫn tạo hiểu lầm; sản phẩm bàn giao không đáp ứng kỳ vọng, phải làm lại nhiều lần.
✗ Sự tham gia kém của bên liên quan Bên liên quan thiết yếu không tích cực tham gia → bỏ sót yêu cầu quan trọng hoặc quyết định không phù hợp nhu cầu người dùng cuối.
✗ Yêu cầu thay đổi Thay đổi thường xuyên (“scope creep”) gây chậm trễ, tăng chi phí và khó duy trì trọng tâm dự án.
✗ Rào cản giao tiếp Rào cản ngôn ngữ, hiểu sai, kênh trao đổi không đầy đủ; cần thiết lập kênh rõ ràng và thống nhất thuật ngữ dự án.
✗ Quá phụ thuộc vào tài liệu Chỉ dựa vào tài liệu mà thiếu hợp tác tích cực dẫn đến hiểu lầm; cần bổ sung hội thảo và phỏng vấn.
✗ Thiếu sự tham gia của người dùng Người dùng là người hưởng lợi cuối cùng; thiếu đại diện của họ khiến hệ thống không đáp ứng hiệu quả nhu cầu thực tế.
66

## Slide 67
2 . 9
Vì sao dùng biểu mẫu thu thập yêu cầu?
Mẫu thu thập yêu cầu là NỀN TẢNG cho dự án — một tài liệu có cấu trúc thu thập, sắp xếp và ghi chép nhu cầu, kỳ vọng của 
các bên liên quan; tạo CẦU NỐI thông tin giữa người dùng và nhà phát triển.
✓ Bảo đảm sự hài lòng của các bên liên quan và cơ hội cao nhất nhận được chấp thuận từ nhà tài trợ.
✓ Nhóm dự án thống nhất ngay từ ngày đầu tiên: cải thiện giao tiếp, phân công nhiệm vụ và tiến độ chung.
✓ Mọi người hiểu rõ yêu cầu, nhiệm vụ, tài liệu và kết quả mong muốn — quan trọng với dự án cộng tác cao.
✓ Tiết kiệm chi phí nhờ giảm thiểu rủi ro và tạo ra sản phẩm an toàn hơn khi ra mắt.
✓ Lập kế hoạch công việc chính xác dựa trên mô tả / đặc tả yêu cầu → tiết kiệm thời gian, hoàn thành nhanh hơn.
✓ Là phương tiện dễ dàng để nhóm ƯU TIÊN và PHÂN LOẠI yêu cầu cho các nhiệm vụ quan trọng.
✓ Phân biệt rõ “bắt buộc phải có” và “nên có” để theo dõi tiến độ với hướng dẫn đơn giản.
67

## Slide 68
2 . 9 . 1
Mẫu tài liệu yêu cầu nghiệp vụ — 9 thành phần
1 Thông tin chi tiết về dự án
2 Tóm tắt tổng quan — phân tích, phát hiện, phạm vi, động lực nghiệp vụ, quy trình đề xuất/hiện tại, yêu cầu chức năng
3 Mô tả dự án — mục đích, quy trình/giải pháp hiện tại, thách thức và lý do cần thực hiện
4 Phạm vi dự án — mục tiêu, nhiệm vụ, kết quả đầu ra, chi phí, thời hạn, mọi thứ “trong” và “ngoài” phạm vi
5 Quy trình hiện tại — kèm sơ đồ, biểu đồ luồng minh hoạ
6 Quy trình đề xuất — dùng CÙNG công cụ / phong cách minh hoạ với quy trình hiện tại
7 Yêu cầu chức năng — cách quy trình hiện tại giải quyết vấn đề và yêu cầu chức năng cần cho thành công
8 Độ ưu tiên — hệ thống xếp hạng: giá trị, trạng thái, mô tả của từng yêu cầu
9 Yêu cầu phi chức năng — tính năng, hành vi hệ thống, đặc điểm liên quan đến trải nghiệm người dùng
Mẫu tài liệu yêu cầu phần mềm (SRS): mục đích, tài liệu tham khảo, phạm vi, định nghĩa, quy ước, giao diện, đặc tả chức năng, hiệu 
năng, bảo mật… — chi tiết ở Chương 4. 68

## Slide 69
T Ổ N G  K Ế T
Tóm tắt Chương 2
2.1 Tầm nhìn (toàn sản phẩm, thay đổi chậm) ≠ Phạm vi (một dự án/lần lặp, linh hoạt). Tài liệu tầm nhìn & phạm vi gồm 4 phần: yêu cầu nghiệp vụ, tầm nhìn giải pháp, phạm vi & hạn chế, bối cảnh nghiệp vụ.
2.2 Bốn bước tìm tiếng nói khách hàng; 8 nguồn yêu cầu; lớp người dùng phân theo CÁCH TƯƠNG TÁC; người tiên phong sản phẩm và người ra quyết định về yêu cầu.
2.3 Khai thác: lập kế hoạch, nghệ thuật đặt câu hỏi, hội thảo có điều phối, phân loại 9 nhóm đầu vào khách hàng, tìm yêu cầu còn thiếu bằng ma trận CRUDL.
2.4 Mười kỹ thuật: Phỏng vấn · Nhóm tập trung · Tạo mẫu · Bảng câu hỏi · Phân tích giao diện · JAD · Động não · Phân tích tài liệu · Hội thảo · Quan sát.
2.5 Sáu tiêu chí lựa chọn: loại thông tin · độ sâu · độ rộng · tích hợp · sự tham gia của người dùng · chi phí. Thực tế luôn KẾT HỢP nhiều kỹ thuật.
2.6–2.9 Hộp công cụ: lược đồ ngữ cảnh, phân rã chức năng, use case, lược đồ trình tự, user story, sơ đồ tư duy + 7 nhóm phần mềm hỗ trợ. Quy trình 6 bước, 7 trở ngại, biểu mẫu chuẩn.
69

## Slide 70
C Â U  H Ỏ I  Ô N  T Ậ P  C H Ư Ơ N G  2
Câu 1 – 4
1 Tuyên bố tầm nhìn
Yêu cầu một số bên liên quan viết tuyên bố tầm nhìn theo mẫu từ khoá trong chương. Xem chúng giống nhau đến mức nào, khắc phục 
khác biệt và đưa ra một tuyên bố thống nhất.
2 Tài liệu tầm nhìn và phạm vi
Viết tài liệu theo mẫu Bảng 2.1 và yêu cầu các thành viên còn lại xem xét. Điều này có thể cho thấy nhóm chưa có cùng hiểu biết — hãy 
khắc phục ngay thay vì để trôi qua.
3 Lớp người dùng
Xác định các nhóm người dùng cho dự án của bạn. Nhóm nào được ưu tiên? Nhóm nào bị phản đối? Ai sẽ là người tiên phong sản phẩm 
tốt cho mỗi nhóm quan trọng?
4 Người ra quyết định
Xác định ai là người ra quyết định về yêu cầu. Phương pháp hiện tại hiệu quả đến mức nào? Bị lỗi ở đâu? Có đúng người không? Đề 
xuất quy trình để đạt được sự đồng thuận.
70

## Slide 71
C Â U  H Ỏ I  Ô N  T Ậ P  C H Ư Ơ N G  2
Câu 5 – 7
5 Yêu cầu còn thiếu
Hãy nghĩ về những yêu cầu còn thiếu được phát hiện MUỘN trong dự án của bạn. Tại sao chúng bị bỏ qua trong quá trình thu thập? 
Làm thế nào để phát hiện từng yêu cầu này sớm hơn?
6 Phân loại đầu vào của khách hàng
Chọn một phần ý kiến khách hàng đã ghi chép hoặc một phần từ SRS. Phân loại từng mục vào 9 nhóm: yêu cầu nghiệp vụ, tình 
huống/kịch bản, quy tắc nghiệp vụ, yêu cầu chức năng, thuộc tính chất lượng, yêu cầu giao diện bên ngoài, ràng buộc, định nghĩa dữ 
liệu và ý tưởng giải pháp. Nếu phát hiện mục phân loại sai, hãy chuyển chúng về đúng vị trí.
7 Đánh giá phương pháp thu thập
Liệt kê các phương pháp thu thập yêu cầu đang dùng trong dự án hiện tại. Phương pháp nào hiệu quả và vì sao? Phương pháp nào 
không? Xác định kỹ thuật bạn nghĩ sẽ hiệu quả hơn, cách áp dụng lần sau, các rào cản có thể gặp và cách vượt qua.
71

## Slide 72
B À I  T Ậ P  T H Ự C  H À N H
Bài 1 – 6: Ghép kỹ thuật với tình huống dự án
1 Phỏng vấn Hệ thống quản lý quan hệ khách hàng mới BA lên lịch phỏng vấn trực tiếp giám đốc bán hàng, đại diện dịch vụ khách hàng và giám đốc tiếp thị để hiểu nhu cầu và khó khăn với hệ thống hiện tại.
2 Bảng câu hỏi Công cụ đánh giá hiệu suất nhân viên mới BA phát bảng câu hỏi cho tất cả nhân viên về quy trình đánh giá hiện tại, tính năng hữu ích và cải tiến mong muốn.
3 Hội thảo Thiết kế trang web thương mại điện tử mới BA tổ chức hội thảo với tiếp thị, CNTT và dịch vụ khách hàng để cùng xác định yêu cầu, ưu tiên tính năng và xây dựng chân dung người dùng.
4 Nhóm tập trung Ứng dụng di động cho dịch vụ ngân hàng BA tiến hành thảo luận nhóm với các nhóm khách hàng khác nhau (sinh viên, người dùng doanh nghiệp…) về tính năng mong muốn và trải nghiệm.
5 Quan sát Nâng cấp hệ thống quản lý kho BA dành một ngày theo dõi nhân viên kho: công việc hằng ngày, tương tác với hệ thống hiện tại và các quy trình thủ công có thể tự động hoá.
6 Phân tích tài liệu Nâng cấp hệ thống ERP hiện có BA xem xét tài liệu hệ thống, hướng dẫn sử dụng, quy trình và báo cáo dự án trước đó để hiểu chức năng hiện tại và xác định điểm cần cải tiến.
72

## Slide 73
B À I  T Ậ P  T H Ự C  H À N H
Bài 7 – 12
7 Tạo mẫu
Giao diện người dùng mới cho công cụ báo cáo nội bộ: BA làm việc với nhóm UX/UI tạo nguyên mẫu độ trung thực 
thấp, sau đó người dùng cuối xem xét để thu phản hồi và tinh chỉnh yêu cầu.
8 Tư duy sáng tạo
Ra mắt tính năng sản phẩm mới: BA điều phối buổi thảo luận với quản lý sản phẩm, nhà phát triển và nhóm bán hàng 
để đưa ra ý tưởng cho tính năng tiềm năng.
9 Phiên họp JAD
Mô-đun quản lý hàng tồn kho cho chuỗi bán lẻ: BA tổ chức các buổi JAD, bên liên quan nghiệp vụ và chuyên gia CNTT 
hợp tác trong vài ngày để xác định yêu cầu và thống nhất thiết kế.
10 Phân tích công nghệ
Trường đại học tăng mạnh số lượng tuyển sinh và thiếu chỗ cho sinh viên trong các khoá học. Hãy phân tích để xác định 
những cách MỚI giúp sinh viên hoàn thành việc học và tốt nghiệp.
11 Phỏng vấn theo cặp
Tìm một người bạn đồng hành, lập kế hoạch phỏng vấn ngắn gọn, phỏng vấn lẫn nhau về nhiệm vụ trong công việc gần 
nhất. Sau đó xác định loại hình phỏng vấn, phương pháp và các loại câu hỏi đã dùng.
12 Chọn kỹ thuật
Bạn là nhà phân tích phát triển hệ thống cho hiệu sách trường: sinh viên đặt sách trực tuyến, nhận tại ký túc xá hoặc 
nhà ngoài trường. Bạn sẽ dùng những kỹ thuật thu thập nào? Mô tả chi tiết cách áp dụng.
73

## Slide 74
HẾT CHƯƠNG 2
Chuẩn bị cho Chương 3:
Phân tích và Mô hình hoá Yêu cầu
Tài liệu tham khảo chính: Karl E. Wiegers (2003), Software Requirements [6] · James Robertson và cộng sự (2024), 
Mastering the Requirements Process [4] · Pressman (2015) [3] · Sommerville (2015) [10]
CT241 — Phân tích Yêu cầu Phần mềm
