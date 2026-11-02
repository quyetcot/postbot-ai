# PostBot AI — Quy trình phát triển và vận hành sản phẩm
## Product Delivery Playbook — v1.0

| Thuộc tính | Giá trị |
| --- | --- |
| Ngày | 02/11/2026 |
| Trạng thái | Đề xuất làm thỏa thuận làm việc chung; chưa ghi nhận hai bên phê duyệt |
| Đối tượng | Hai thành viên cùng tham gia nghiệp vụ, kỹ thuật và vận hành |
| Tài liệu liên quan | PostBot AI — Tài liệu định hướng và yêu cầu sản phẩm, Draft v1.2 |
| Mục tiêu | Học và thực hành đầy đủ từ xác định nhu cầu đến phát hành, vận hành và cải tiến |

## 1. Cách sử dụng

Đây là quy trình đề xuất phù hợp nhóm hai người, tham khảo cách phân giai đoạn của GOV.UK Service Manual. Không có một quy trình duy nhất dùng cho mọi doanh nghiệp; tài liệu này không tuyên bố đạt chứng nhận hay tuân thủ một tiêu chuẩn doanh nghiệp cụ thể.

Mỗi giai đoạn có người phụ trách, đầu ra và điều kiện đi tiếp. Có thể quay lại bước trước khi có bằng chứng mới; không cần hoàn tất mọi tài liệu cho toàn bộ sản phẩm rồi mới thử nghiệm. Viết đủ để người khác hiểu, thực hiện và kiểm tra được.

Hai bạn đọc mục 2–5 trước, thống nhất bằng một ghi nhận chung, rồi thực hiện kế hoạch tại mục 15. Hai thành viên phân công và luân phiên theo từng việc; không phân vai cố định theo chuyên môn. Tra mục 16 khi gặp thuật ngữ chưa quen.

## 2. Phân biệt các loại tài liệu

| Loại | Trả lời câu hỏi | Cách dùng cho PostBot |
| --- | --- | --- |
| Product Brief | Vì sao làm, cho ai, giá trị gì? | Phần định hướng của Draft v1.2 |
| PRD — Product Requirements Document | Sản phẩm cần làm gì, giới hạn gì, đo và nghiệm thu ra sao? | Phần yêu cầu của v1.2; cần chi tiết thêm từng tính năng trước triển khai |
| Feature Specification | Một tính năng xử lý từng tình huống thế nào? | Ví dụ: duyệt phiên bản; kiểm tra lại nguồn sau MVP |
| Technical Design | Dữ liệu, API, hàng đợi, quyền và lỗi được triển khai thế nào? | Viết sau khi yêu cầu đủ rõ; kiến trúc khái niệm trong v1.2 chưa thay thế tài liệu này |
| Backlog | Những việc nào cần làm, ưu tiên nào? | Danh sách issue có người phụ trách và điều kiện hoàn thành |
| Test Plan / UAT | Kiểm tra bằng gì, ai xác nhận đạt? | Bộ ca kiểm thử và biên bản nghiệm thu của người được phân công |
| Runbook | Khi chạy thật hoặc gặp sự cố thì làm gì? | Dừng lịch, mất quyền, chưa rõ kết quả, sửa sai, khôi phục |
| Release Notes | Phiên bản phần mềm này thay đổi gì? | Ghi cho từng lần phát hành phần mềm |

Giữ v1.2 làm tài liệu tổng hợp hiện tại, chưa cần tách thành nhiều bản trùng nhau. Khi tách, chỉ rõ tài liệu nào là nguồn quyết định cho từng nội dung. Phiên bản tài liệu 1.2 không đồng nghĩa sản phẩm đã có bản phần mềm 1.2 hoặc mọi yêu cầu đã được phê duyệt.

## 3. Cùng làm kỹ thuật và nghiệp vụ, phân công theo công việc

Hai thành viên cùng có thể tìm hiểu nhu cầu, viết yêu cầu, thiết kế, lập trình, kiểm thử và vận hành. Không gắn cố định một người với business và một người với kỹ thuật. Vai trò thay đổi theo tính năng, quỹ giờ và năng lực thực tế; cả hai đều có cơ hội thực hành end-to-end.

| Vai trò trong một công việc | Trách nhiệm | Cách chọn |
| --- | --- | --- |
| Người phụ trách chính | Theo dõi việc từ yêu cầu đến kết quả, cập nhật tiến độ và nêu chỗ bị chặn | Chọn một trong hai người cho từng issue; có thể luân phiên |
| Người phối hợp | Cùng tìm hiểu, thiết kế hoặc triển khai phần đã thống nhất | Người còn lại; chia rõ phần làm khi cùng sửa code |
| Người kiểm tra/xác nhận | Đối chiếu với yêu cầu, thử luồng và ghi kết quả; review code khi đủ khả năng | Ưu tiên người không trực tiếp thực hiện phần được kiểm tra |
| Hai người cùng quyết định | Phạm vi MVP, ngân sách, chính sách quan trọng, phát hành và thay đổi lớn | Ghi quyết định và phiên bản; không mặc định im lặng là đồng ý |

Mỗi issue ghi tên người phụ trách và người kiểm tra. Có thể làm cặp nhưng vẫn cần một đầu mối theo dõi. Vai trò vận hành trong PRD là trách nhiệm và quyền trên hệ thống, không đồng nghĩa chức danh cố định của hai thành viên.

Cùng thảo luận yêu cầu trước khi code; người thực hiện demo, người còn lại thử và phản biện. UAT có thể do một trong hai người đóng vai người vận hành, hoặc mời người dùng thực tế tham gia. Review nghiệp vụ và review code là hai việc khác nhau; chỉ ghi code đã được review độc lập khi người còn lại thực sự kiểm tra code và đủ khả năng đánh giá. Nếu cả hai cùng viết phần đó hoặc tự nghiệm thu, ghi rõ giới hạn kiểm tra độc lập.

Nếu chưa thống nhất yêu cầu hoặc quyết định phát hành, ghi phần còn vướng và bằng chứng cần bổ sung; chưa triển khai phần phụ thuộc hoặc chưa phát hành. Người trực xử lý sự cố có thể dừng tác vụ mới theo runbook đã thống nhất rồi báo người còn lại; không phải chờ họp để ngăn lỗi tiếp diễn.

Ví dụ luân phiên: tính năng duyệt phiên bản do thành viên A phụ trách, B kiểm tra; tính năng đặt lịch do B phụ trách, A kiểm tra. Đây là minh họa, không phải phân công đã chốt.

Chốt thêm trước vận hành: ai sở hữu repo, trang Facebook, tài khoản dịch vụ, dữ liệu, quyền truy cập; ai trả chi phí; ai tiếp quản khi một người ngừng tham gia. Ghi thành thỏa thuận riêng nếu cần.

## 4. Vòng đời và điều kiện chuyển giai đoạn

| Giai đoạn | Việc cần làm | Đầu ra tối thiểu | Điều kiện đi tiếp | Người chính |
| --- | --- | --- | --- | --- |
| 1. Khám phá nhu cầu | Xem quy trình làm bài hiện tại, phỏng vấn người vận hành, đo công thủ công | Brief, ví dụ bài thật, vấn đề ưu tiên và số đo ban đầu | Có người dùng cụ thể, vấn đề đáng giải quyết và cách đo | Một người điều phối, người còn lại phối hợp |
| 2. Kiểm chứng khả thi | Thử quyền xuất bản trên đúng trang; thử AI trên bài mẫu, đánh giá tổng công sửa | Biên bản thử nghiệm, giới hạn, chi phí sơ bộ, quyết định tiếp tục/dừng | Cổng đăng khả thi hoặc thống nhất phương án thủ công; giá trị đủ để thử tiếp | Người phụ trách công việc |
| 3. Chốt MVP | Chọn luồng cốt lõi và ngoài phạm vi; chốt tiêu chí thành công, ngân sách, rủi ro | PRD đã review, danh sách MVP và tồn đọng sau MVP | Hai bên xác nhận đúng phiên bản, ghi phần chưa chốt | Cả hai |
| 4. Thiết kế và thử luồng | Prototype nhập nguồn → tạo nháp → sửa → duyệt; thiết kế dữ liệu/quyền/lỗi | Prototype, đặc tả luồng, thiết kế kỹ thuật vừa đủ | Người thử thực hiện được tác vụ; rủi ro kỹ thuật chính có hướng xử lý | Người phụ trách thiết kế; người còn lại thử |
| 5. Lập kế hoạch và xây từng phần | Chia nhỏ thành lát cắt dùng được, ước lượng theo quỹ giờ, triển khai và kiểm thử | Issue, code, PR, bản thử và bằng chứng kiểm tra | Mỗi việc đạt Definition of Done ở mục 7 | Người phụ trách công việc |
| 6. Kiểm tra tích hợp và UAT | Kiểm tra xuyên suốt từ nhập nguồn tới đối soát và sửa sai; người được phân công dùng ca thật | Báo cáo test, danh sách lỗi, biên bản UAT | Không còn lỗi chặn phát hành; hạn chế còn lại có người chấp nhận | Cả hai |
| 7. Phát hành thử có kiểm soát | Kiểm tra môi trường thật, sao lưu, rollback, đào tạo, giới hạn người/trang | Checklist phát hành, runbook, release notes | Cả hai Go; có người trực và dừng được tác vụ mới | Cả hai |
| 8. Vận hành và học | Đo công, lỗi, chi phí, phản hồi; xử lý sự cố; quyết định cải tiến | Dashboard/báo cáo nhỏ, nhật ký sự cố, backlog cập nhật | Tiếp tục, điều chỉnh hoặc dừng dựa trên dữ liệu | Cả hai |
| 9. Bàn giao hoặc kết thúc | Xuất dữ liệu cần giữ, xử lý lịch đang chờ, thu hồi quyền, dừng chi phí | Biên bản bàn giao/kết thúc và tài liệu cập nhật | Không để lịch vô chủ, thông tin xác thực hoặc dịch vụ trả phí bị quên | Cả hai |

Kiểm chứng khả thi có thể làm song song prototype nhỏ sau khi hiểu vấn đề. Khi thay đổi lớn xuất hiện, quay lại xác định nhu cầu và phạm vi; không coi các giai đoạn là đường một chiều.

## 5. Phạm vi MVP đề xuất cho PostBot

Một Fanpage, nguồn do người quản trị chọn, AI tạo nháp, người dùng sửa và duyệt đúng phiên bản, đăng ngay/đặt lịch, lưu kết quả, dừng lịch và xử lý sai sót. Tin rủi ro cao vẫn ngoài luồng MVP.

Source Revalidation & Publication Blocking là **sau MVP**. MVP vẫn cần kiểm tra căn cứ và thời hạn theo quy trình đã chốt; chưa bắt buộc xây cơ chế tự lấy lại nguồn sau 48 giờ. Ghi feature này vào backlog sau MVP để không làm lệch phạm vi đang xây.

Trước khi chốt thời gian, hai bên phải thống nhất: quỹ giờ mỗi tuần, nguồn lực backend/vận hành, ngân sách, trang thử, dữ liệu mẫu và hạn chế tích hợp. Cả hai có thể cùng làm giao diện và backend theo khả năng; các phần quyền, hàng đợi và vận hành cần được kiểm chứng, có người phụ trách và kiểm tra cụ thể.

## 6. Cách quản lý công việc hằng tuần

Dùng một bảng công việc duy nhất: **Backlog → Ready → In Progress → Review/Test → UAT → Done**. Blocked là nhãn có nguyên nhân, người gỡ và ngày kiểm tra lại. Không ghi Done chỉ vì code xong.

Đề xuất mỗi người chỉ xử lý một việc chính tại một thời điểm. Chọn một chu kỳ ngắn phù hợp quỹ giờ, ví dụ một tuần; đây là nhịp làm việc đề xuất, không tuyên bố áp dụng đầy đủ Scrum.

| Nhịp | Nội dung | Kết quả |
| --- | --- | --- |
| Đầu chu kỳ, khoảng 20–30 phút | Chọn mục tiêu và việc đủ rõ; kiểm tra phụ thuộc và quỹ giờ | Danh sách cam kết nhỏ, người phụ trách |
| Khi làm việc, cập nhật ngắn | Đã làm, tiếp theo, đang mắc gì | Bảng việc phản ánh thực tế |
| Cuối chu kỳ, demo khoảng 30 phút | Người còn lại tự thử; phản hồi gắn với issue và tiêu chí | Đạt/chưa đạt, thay đổi được ghi nhận |
| Sau demo, khoảng 10–15 phút | Điều gì gây chậm hoặc làm lại? | Chọn một cải tiến cho chu kỳ sau |

Nếu không có bản mới để demo, báo rõ nguyên nhân và điều chỉnh kế hoạch. Đo tiến độ bằng luồng đã kiểm chứng, không bằng số dòng code hay số trang tài liệu.

## 7. Điều kiện bắt đầu và hoàn thành một việc

### Definition of Ready — đủ rõ để bắt đầu

- Có người dùng, nhu cầu và giá trị cụ thể.
- Có phần trong/ngoài phạm vi, ví dụ đầu vào và kết quả mong đợi.
- Có tiêu chí nghiệm thu cả thành công và lỗi quan trọng.
- Có người quyết định nghiệp vụ; phụ thuộc, quyền và dữ liệu đã sẵn sàng hoặc có kế hoạch.
- Ước lượng đủ nhỏ để hoàn thành và demo trong một chu kỳ; việc lớn được tách.

### Definition of Done — hoàn thành trong phạm vi đã thống nhất

- Triển khai đúng tiêu chí nghiệm thu và tự review thay đổi.
- Kiểm tra phù hợp đã chạy, lưu kết quả; lỗi còn lại có đánh giá và người chấp nhận.
- Kiểm tra quyền, phiên bản, dữ liệu nhạy cảm và tình huống lỗi liên quan.
- Tài liệu/hướng dẫn và cấu hình cần thiết được cập nhật.
- Demo bản thử; người được phân công nghiệm thu nếu việc thay đổi hành vi nghiệp vụ.
- Code được merge theo quy tắc dự án, bản thử xác định được phiên bản.

Done trên môi trường thử khác với đã phát hành thật. Ghi nhãn hoặc trường release riêng để không nhầm.

## 8. Mẫu issue tính năng và ví dụ

```text
Mã / Tiêu đề:
Người dùng / Vấn đề / Giá trị:
Trong phạm vi / Ngoài phạm vi:
Luồng chính:
Các tình huống lỗi:
Tiêu chí nghiệm thu:
Phụ thuộc / Rủi ro:
Người thực hiện / Người nghiệm thu:
Ước lượng / Kết quả kiểm tra / Phiên bản thử:
```

**Ví dụ PB-001 — Duyệt đúng phiên bản:** Là người duyệt, tôi muốn xem bản nháp cùng căn cứ để chỉ cho phép đăng nội dung mình đã kiểm tra.

| Mã | Tình huống | Kết quả cần đạt |
| --- | --- | --- |
| AC-01 | Người có quyền duyệt bản A | Lưu bản A, người duyệt và thời điểm |
| AC-02 | Bản A đã duyệt được sửa thành B | B chưa có quyền đăng; yêu cầu duyệt lại |
| AC-03 | Người không có quyền gửi yêu cầu duyệt | Từ chối trên máy chủ, không chỉ ẩn nút giao diện |
| AC-04 | Tác vụ cũ cố gửi A sau khi A bị vô hiệu | Chặn trước khi gửi, lưu lý do |

Liên kết truy vết: **mục PRD → issue → PR/commit → ca test → kết quả UAT → release**. Một issue có thể ghi các liên kết này, không bắt buộc thêm bảng riêng.

## 9. Quy trình code và kiểm tra kỹ thuật

1. Chọn issue Ready; tạo nhánh ngắn theo mã issue.
2. Triển khai lát cắt từ giao diện đến dữ liệu/quyền liên quan, tránh làm toàn bộ frontend rồi mới phát hiện backend không hỗ trợ.
3. Chạy kiểm tra phù hợp: định dạng/lint/typecheck nếu dự án có; unit cho logic quan trọng, integration cho dữ liệu và tác vụ, end-to-end cho luồng cốt lõi. Không cần viết test hình thức cho mọi thay đổi nhỏ.
4. Mở PR với vấn đề, thay đổi hành vi, cách kiểm tra và hạn chế. Tự review nếu chưa có reviewer kỹ thuật độc lập, ghi rõ điều đó.
5. Triển khai môi trường thử, liên kết bản thử và kết quả vào issue; đưa người còn lại hoặc người dùng thực tế UAT.
6. Merge khi đủ điều kiện; phát hành riêng theo mục 12.

CI là kiểm tra tự động khi thay đổi code; CD là tự động hóa đưa bản đã kiểm tra đến môi trường đích. Đề xuất bắt đầu CI đơn giản và triển khai có kiểm soát; không cần tự động xuất bản mọi thay đổi lên môi trường thật.

Tách môi trường phát triển, môi trường thử và môi trường thật theo nhu cầu; ít nhất phải tách thông tin xác thực và dữ liệu tác vụ thật. Không đặt token Facebook trong frontend hoặc repo. Kiểm tra sao lưu/khôi phục, quyền truy cập và phụ thuộc phần mềm trước phát hành.

## 10. Kiểm thử AI và nghiệm thu người dùng (UAT)

AI cần bộ ví dụ có đầu ra mong đợi, không chỉ thử vài prompt thành công. Tạo bộ mẫu gồm nguồn thiếu, sai năm, mâu thuẫn, tên địa phương, thông tin bị AI thêm, nguồn chứa lệnh độc hại và bản sửa sau duyệt. Giữ nguồn/cấu hình/model và kết quả để so sánh khi thay prompt hoặc model.

Mỗi lần thay thành phần AI, chạy lại những ca liên quan và đánh giá lỗi dữ kiện, công sửa, chi phí. Không dùng chính lời tự đánh giá của AI làm bằng chứng duy nhất rằng nội dung đúng.

UAT nghĩa là người được phân công hoặc người dùng thực tế kiểm tra sản phẩm có phục vụ công việc thật hay không. Hai thành viên có thể luân phiên thực hiện; ưu tiên người còn lại kiểm tra phần một người đã xây. Hướng dẫn thử bằng dữ liệu an toàn, tập trung vào kết quả công việc thay vì chỉ xác nhận code chạy.

```text
Mã UAT / Tính năng / Phiên bản bản thử:
Người thử / Ngày:
Điều kiện và dữ liệu đầu vào:
Các bước:
Kết quả mong đợi / Thực tế:
Đạt / Chưa đạt / Chưa thể thử:
Ảnh hoặc bằng chứng / Issue lỗi:
Người xác nhận / Hạn chế được chấp nhận:
```

Với MVP, chạy ít nhất các luồng cốt lõi đã chốt: nhập nguồn → tạo nháp → sửa → duyệt → đặt lịch → đăng → đối soát; đồng thời kiểm tra mất quyền, timeout, trùng tác vụ, hết hạn, dừng khẩn cấp và sửa sai. Phần kiểm tra lại nguồn tự động có bộ UAT riêng khi được đưa vào một bản sau MVP.

## 11. Phân biệt lỗi và yêu cầu mới

- **Lỗi:** hành vi thực tế khác yêu cầu đã chốt. Ví dụ bản B chưa được duyệt vẫn đăng được.
- **Yêu cầu mới:** thay đổi hoặc thêm hành vi. Ví dụ hỗ trợ nhiều Fanpage khi MVP chỉ có một trang.
- **Cần làm rõ:** yêu cầu cũ chưa đủ cụ thể; hai bên xác nhận cách hiểu trước khi kết luận.

Đề xuất mức lỗi: chặn phát hành khi đăng sai trang/phiên bản, lộ quyền, đăng trùng chưa kiểm soát hoặc luồng cốt lõi không chạy; lỗi quan trọng cần quyết định rõ có phương án tạm và người chịu trách nhiệm; lỗi trình bày nhỏ có thể lên lịch sau. Hai bên chốt mức độ theo hậu quả thực tế, không chỉ theo tên nhãn.

Mọi góp ý được ghi thành issue, đánh giá giá trị, tác động phạm vi, thời gian, chi phí và kiểm thử. Chọn: sửa ngay, đưa vào chu kỳ sau, sau MVP hoặc không làm. Không tự coi comment là yêu cầu đã được nhận vào lịch.

```text
Mã thay đổi / Người đề xuất / Lý do:
Yêu cầu hiện tại → Thay đổi mong muốn:
Ảnh hưởng người dùng / Kỹ thuật / Thời gian / Chi phí:
Phương án / Quyết định / Người quyết định / Ngày:
Tài liệu và issue liên quan:
```

Ví dụ quyết định: Source Revalidation được ghi vào v1.2 để định hướng sau MVP; việc thêm vào tài liệu không tự biến nó thành việc phải xây ngay.

## 12. Phát hành và bàn giao

### Checklist Go/No-Go

- [ ] Đúng phạm vi release, có bản code/phiên bản xác định và UAT được ghi nhận.
- [ ] Không còn lỗi chặn phát hành; các hạn chế còn lại có người chấp nhận.
- [ ] Quyền Facebook và thao tác thực tế đã được thử trong phạm vi cần dùng.
- [ ] Dữ liệu/cấu hình đã chuẩn bị; token không bị lộ, có cách thu hồi.
- [ ] Có bản sao lưu phù hợp và đã thử cách khôi phục.
- [ ] Có hướng dẫn triển khai, kiểm tra nhanh sau triển khai và rollback.
- [ ] Có người theo dõi, đầu mối phản ánh, giờ hỗ trợ và nút dừng lịch.
- [ ] Hai bên ghi Go hoặc No-Go cùng lý do, không để trống được hiểu là đồng ý.

Rollback phần mềm là quay về bản chạy trước; không tự thu hồi bài đã đăng. Nếu có migration dữ liệu, ghi rõ tính tương thích và cách phục hồi; không hứa luôn đảo ngược được bằng cách đổi code. Không khôi phục tác vụ cũ thành lịch đăng mới khi rollback hoặc phục hồi dữ liệu.

Bắt đầu pilot với phạm vi nhỏ đã chốt, theo dõi rồi mới mở rộng. Sau triển khai, thử nhanh đăng nhập/quyền, luồng duyệt, hàng đợi và kết quả xuất bản trong điều kiện được phép. Nếu lỗi nghiêm trọng: dừng tác vụ mới, xác định phạm vi, đối soát trước khi thử lại.

Bàn giao tối thiểu: cách dùng, quyền truy cập, thông tin chủ sở hữu dịch vụ, runbook, cách báo lỗi, lịch hỗ trợ, chi phí và bản phát hành. Không gửi token trong tài liệu bàn giao thông thường.

## 13. Vận hành, đo lường và sự cố

Trước pilot, chốt số liệu gốc và mục tiêu thử nghiệm: thời gian làm bài thủ công, công sửa nháp, tỷ lệ lỗi, chi phí trên bài hoàn tất, phản hồi hữu ích. Ngưỡng cụ thể để hai bên xác nhận theo dữ liệu; không tự mặc định đạt 10.000 follower là sản phẩm thành công.

Báo cáo ngắn theo chu kỳ: đã đăng bao nhiêu, bị giữ/hủy bao nhiêu và vì sao, lỗi/đính chính, tổng công người, chi phí, phản hồi và quyết định tiếp theo. Bao gồm nháp bị loại để không làm đẹp số liệu.

Khi sự cố: ghi nhận → dừng phạm vi ảnh hưởng → đối soát và xác định nguyên nhân → xử lý kỹ thuật/biên tập → xác nhận khôi phục → ghi biện pháp tránh tái diễn. Giao một người điều phối; không đồng thời tự đăng lại từ nhiều người. Bài đã lan truyền có thể cần đính chính công khai, không chỉ rollback.

Khi một thử nghiệm không giảm tổng công hoặc vượt ngân sách, thu hẹp, thay cách làm hoặc dừng; ghi bài học thay vì mở thêm tính năng để che vấn đề.

## 14. Bộ tài liệu và nhật ký quyết định tối thiểu

Đề xuất lưu cùng repo tài liệu, quản lý issue trong một công cụ hai người đều dùng được. Không cần mua công cụ trước khi thử quy trình.

| Tài liệu | Khi cần | Người duy trì |
| --- | --- | --- |
| PRD tổng hợp và lịch sử thay đổi | Ngay từ lúc chốt phạm vi | Một người cập nhật, người còn lại review |
| Backlog/issue có tiêu chí nghiệm thu | Trước bắt đầu việc | Cả hai |
| Thiết kế kỹ thuật và quyết định quan trọng | Trước việc rủi ro hoặc thay kiến trúc | Người phụ trách công việc |
| Test/UAT và bằng chứng | Trong khi làm và trước release | Cả hai, phân công người kiểm tra cụ thể |
| Runbook và release notes | Trước chạy thật, cập nhật khi đổi | Người phụ trách cập nhật, cả hai biết cách dùng |
| Nhật ký quyết định và rủi ro | Khi có quyết định/giả định ảnh hưởng kế hoạch | Cả hai |

Mẫu quyết định: mã, vấn đề, lựa chọn, bằng chứng, quyết định, lý do, người xác nhận, ngày và điều kiện xem lại. Ghi trạng thái tài liệu: Draft → In Review → Approved cho phạm vi cụ thể → Superseded. Không tự ghi Approved chỉ vì đã đẩy lên Git.

Khi một thành viên góp ý trên chat, đưa kết luận trở lại issue/tài liệu, gắn phiên bản; không để quy tắc chính thức chỉ nằm trong hội thoại.

## 15. Kế hoạch bắt đầu cho hai bạn

Đây là thứ tự công việc, không phải cam kết ngày hoàn thành.

1. Cùng đọc v1.2, đánh dấu nội dung MVP và sau MVP; thống nhất cách giao người phụ trách và người kiểm tra theo từng việc, cùng quyết định phạm vi và phát hành.
2. Chọn người vận hành thật, thu một nhóm bài điển hình và đo quy trình thủ công hiện tại; chốt mục tiêu pilot và ngân sách.
3. Xác nhận đúng Fanpage, quyền sở hữu, quyền truy cập và thử tích hợp trước khi xây sâu.
4. Người được phân công thử prototype tạo/sửa/duyệt trên bài mẫu; ghi chỗ khó dùng hoặc thiếu căn cứ.
5. Chốt phạm vi MVP theo phiên bản, lập backlog ưu tiên và tiêu chí nghiệm thu. Ước lượng theo quỹ giờ thực tế, ghi khoảng và điều kiện phụ thuộc.
6. Xây lát cắt đầu tiên: một nguồn → một nháp → sửa → duyệt đúng phiên bản → xuất bản thử có đối soát. Sau đó bổ sung lịch, dừng, khôi phục và các lỗi quan trọng.
7. Chạy UAT, hoàn tất checklist phát hành và pilot có người phụ trách.
8. Đánh giá kết quả; quyết định có đầu tư Source Revalidation hoặc tính năng tiếp theo dựa trên nhu cầu và dữ liệu.

### Thực hành end-to-end cho cả hai

Với mỗi tính năng, cả hai cùng tham gia và luân phiên người phụ trách để thực hành đủ: hỏi nhu cầu → viết yêu cầu → thiết kế UI/dữ liệu/API → triển khai → kiểm tra → demo → nhận phản hồi → phát hành → đo và xử lý lỗi. Ghi quyết định và bài học để có hồ sơ dự án end-to-end, thay vì chỉ danh sách công nghệ đã dùng.

### Buổi thống nhất đầu tiên

Trong một buổi làm việc, cần chốt: người dùng chính, bài toán ưu tiên, MVP/ngoài MVP, cách phân công và kiểm tra chéo, quỹ giờ, ngân sách, trang thử, nơi quản lý issue, cách UAT và người cho phép phát hành. Những mục chưa chốt ghi người chịu trách nhiệm và thời điểm cần trả lời.

## 16. Giải thích thuật ngữ cho cả hai thành viên

Đọc mục này như trang tra cứu. Mỗi thuật ngữ có nghĩa ngắn và ví dụ; không cần biết tiếng Anh hoặc có kinh nghiệm công ty để sử dụng quy trình. Các thuật ngữ về AI, nguồn tin và Facebook được giải thích thêm tại mục 20.6 của PRD v1.2.

| Thuật ngữ | Nghĩa dễ hiểu | Ví dụ áp dụng |
| --- | --- | --- |
| Product / Sản phẩm | Giải pháp phục vụ một nhu cầu của người dùng | PostBot giúp làm và quản lý bài đăng |
| Business / Nghiệp vụ | Công việc thực tế và các quy tắc cần tuân theo | Bài nào cần duyệt, ai chịu trách nhiệm nguồn |
| End-to-end | Xuyên suốt từ nhu cầu tới chạy thật và cải tiến | Hai người cùng tham gia toàn bộ vòng đời |
| Discovery | Tìm hiểu vấn đề, người dùng và ràng buộc trước khi đầu tư xây | Xem người quản trị đang tốn công ở đâu |
| Alpha / Beta / Live | Thử ý tưởng / xây và thử với người dùng / vận hành thật theo cách chia của nguồn tham khảo | Là các giai đoạn, không phải số phiên bản bắt buộc của PostBot |
| Agile | Làm từng phần nhỏ, lấy phản hồi và điều chỉnh thường xuyên | Demo mỗi chu kỳ thay vì chờ xong toàn bộ |
| Scrum | Một khung làm việc có vai trò, sự kiện và quy tắc riêng | Quy trình hiện tại không tuyên bố áp dụng đầy đủ Scrum |
| MVP | Bản nhỏ nhất đủ thử giá trị cốt lõi với người dùng thật | Một Fanpage và luồng duyệt/đăng |
| Prototype | Bản thử ý tưởng hoặc cách dùng, có thể chưa xử lý thật | Màn hình duyệt mô phỏng |
| Pilot | Đợt chạy thật giới hạn để học và kiểm soát rủi ro | Dùng thử với nhóm bài và thời gian đã chốt |
| Product Brief / PRD | Bản định hướng / tài liệu yêu cầu sản phẩm | Vì sao làm / phải có hành vi nào và nghiệm thu thế nào |
| Feature specification | Mô tả chi tiết một tính năng | Các bước và lỗi khi đặt lịch |
| Technical design | Thiết kế cách hệ thống đáp ứng yêu cầu | Dữ liệu, API, quyền và hàng đợi |
| Scope / Out of scope | Trong phạm vi / ngoài phạm vi đã đồng ý | Nhiều trang chưa thuộc MVP |
| Backlog / Roadmap | Danh sách việc có ưu tiên / hướng phát triển theo giai đoạn | Kiểm tra lại nguồn nằm sau MVP; chưa có nghĩa đã hẹn ngày làm |
| Issue / Task / Feature | Mục ghi công việc hoặc lỗi / việc cần làm / khả năng sản phẩm cung cấp | Issue mô tả việc thêm nút dừng lịch |
| User story | Câu mô tả ai cần gì và để làm gì | Là người duyệt, tôi cần xem nguồn để kiểm tra bài |
| Acceptance criteria / AC | Điều kiện cụ thể để biết một yêu cầu đạt | Sửa nội dung sau duyệt phải yêu cầu duyệt lại |
| Definition of Ready | Bộ điều kiện để việc đủ rõ và sẵn sàng bắt đầu | Có đầu vào, tiêu chí và người quyết định |
| Definition of Done | Bộ điều kiện để coi việc hoàn thành trong phạm vi thống nhất | Đã kiểm tra, cập nhật tài liệu và nghiệm thu liên quan |
| Ready / In Progress / Review / Done | Sẵn sàng / đang làm / đang kiểm tra / hoàn thành | Các cột trên bảng công việc |
| Blocked / Dependency | Bị vướng / việc hoặc điều kiện phải có trước | Chưa thử được vì thiếu quyền Fanpage |
| Demo / Feedback | Trình diễn kết quả / phản hồi | Người thực hiện demo, người còn lại thử và góp ý |
| Review / Reviewer | Xem xét và phản biện / người thực hiện việc đó | Có thể review nghiệp vụ, thiết kế hoặc code |
| UAT | Người dùng hoặc người đóng vai vận hành thử và nghiệm thu nhu cầu thực tế | Luân phiên thử tạo, duyệt, đặt lịch và kiểm tra kết quả |
| Test case | Một tình huống kiểm tra có đầu vào và kết quả mong đợi | Mất quyền thì giữ bài, không tiếp tục gửi |
| Unit / Integration / E2E test | Kiểm tra phần nhỏ / các phần phối hợp / luồng xuyên suốt | Kiểm tra hàm thời hạn / hàng đợi với dữ liệu / nhập nguồn tới đăng |
| Lint / Typecheck | Kiểm tra quy tắc code / cách dùng kiểu dữ liệu | Bắt một số lỗi sớm; không chứng minh nghiệp vụ đúng |
| Regression test | Kiểm tra lại để phát hiện phần đang chạy bị hỏng sau thay đổi | Sửa prompt vẫn phải giữ đúng ngày giờ nguồn |
| Bug / Defect | Lỗi khác với yêu cầu đã chốt | Đăng bản chưa duyệt |
| Change request | Đề nghị thay đổi cần đánh giá tác động | Thêm nhiều Fanpage, có thể tăng thời gian và chi phí |
| Git / Repository / Repo | Công cụ theo dõi thay đổi / kho code và lịch sử | Lưu code và tài liệu, biết ai sửa gì |
| Branch / Commit | Nhánh làm việc / mốc lưu thay đổi | Làm một issue trên nhánh rồi ghi commit |
| PR — Pull Request / Merge | Đề nghị xem và nhập thay đổi / gộp thay đổi vào nhánh đích | Review code trước khi gộp |
| Frontend / UI / Backend | Giao diện và xử lý phía người dùng / phần hiển thị tương tác / xử lý máy chủ | Màn hình duyệt / các nút và ô / xác thực quyền và lưu duyệt |
| API / Token | Cổng trao đổi giữa phần mềm / thông tin bí mật chứng minh quyền | Gọi Facebook bằng quyền hợp lệ; không đưa token vào repo |
| AI / Model / Prompt | Hệ thống tạo/phân tích / mô hình cụ thể / chỉ dẫn và dữ liệu gửi cho AI | Tạo bản nháp theo nguồn; vẫn cần kiểm tra |
| CI / CD | Tự động tích hợp và kiểm tra thay đổi / tự động hóa quá trình đưa bản tới môi trường đích | Chạy kiểm tra khi cập nhật code; phát hành thật vẫn theo điều kiện đã chốt |
| Development / Staging / Production | Môi trường làm / thử / sử dụng thật | Không để thử nghiệm vô tình đăng lên trang thật |
| Build / Deploy / Release | Chuẩn bị bản chạy / đưa bản lên môi trường / cung cấp phiên bản cho người sử dụng | Có thể đã deploy bản thử nhưng chưa release cho người dùng |
| Migration | Thay đổi cấu trúc hoặc chuyển dữ liệu có kiểm soát | Thêm trường lịch đăng cần tương thích dữ liệu cũ |
| Rollback / Backup / Restore | Quay phần mềm về bản trước / sao lưu / khôi phục | Rollback không tự thu hồi bài đã đăng |
| Runbook | Hướng dẫn thao tác khi vận hành hoặc gặp lỗi | Cách dừng lịch và đối soát bài chưa rõ kết quả |
| Release notes | Ghi chú phiên bản phần mềm | Tính năng mới, lỗi đã sửa và hạn chế còn lại |
| Go / No-Go | Quyết định được / chưa được tiếp tục phát hành | Cả hai ghi quyết định và lý do |
| Dashboard / Metrics / KPI | Màn hình theo dõi / số đo / số đo được chọn theo mục tiêu | Theo dõi thời gian làm bài và lỗi, không chỉ follower |
| Baseline | Số đo ban đầu dùng làm mốc so sánh | Thời gian làm một bài trước khi dùng bot |
| Incident / Root cause | Sự cố ảnh hưởng vận hành / nguyên nhân gây sự cố | Sai bản vì phê duyệt không gắn phiên bản |
| Draft / In Review / Approved / Superseded | Bản thảo / đang xem xét / đã duyệt trong phạm vi cụ thể / được thay thế | Đẩy file lên Git chưa tự biến thành Approved |
| Traceability / Truy vết | Liên kết yêu cầu, phần triển khai và bằng chứng | Từ mục PRD tới issue, PR, test và release |

## 17. Nguồn tham khảo và giới hạn

- GOV.UK Service Manual, Agile delivery: https://www.gov.uk/service-manual/agile-delivery — tham khảo cách chia vòng đời và quản lý việc lặp lại.
- Discovery: https://www.gov.uk/service-manual/agile-delivery/how-the-discovery-phase-works — tham khảo nguyên tắc hiểu nhu cầu và ràng buộc trước khi đầu tư xây.
- Live: https://www.gov.uk/service-manual/agile-delivery/how-the-live-phase-works — tham khảo việc tiếp tục đo lường và cải tiến khi vận hành.

Các bảng phân vai, checklist, nhịp làm việc và biểu mẫu ở đây là đề xuất riêng cho nhóm PostBot, không phải trích nguyên văn hoặc quy định bắt buộc từ nguồn tham khảo. Cần điều chỉnh theo nhân sự, mức rủi ro và kết quả thử nghiệm.

## 18. Nhật ký phiên bản

| Phiên bản | Ngày | Thay đổi |
| --- | --- | --- |
| v1.0 | 02/11/2026 | Tạo quy trình làm việc end-to-end cho nhóm hai người, vai trò, giai đoạn, yêu cầu, kiểm thử, UAT, phát hành, vận hành và biểu mẫu |

| v1.0 — cập nhật cách làm việc và thuật ngữ | 02/11/2026 | Mở rộng mục 16; thay cách chia cố định business/kỹ thuật bằng phân công theo công việc, luân phiên và kiểm tra chéo; đồng bộ các giai đoạn, UAT và người duy trì tài liệu |
