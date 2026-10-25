# 5.1. Chuẩn hóa ước lượng

## Phân loại

- CF03 - Cần thảo luận lại: Các phiếu chênh lệch do chưa rõ quy tắc chọn điểm nhận ngoài trường.
- CF04 - Cần thảo luận lại: Phạm vi xử lý và cập nhật trạng thái chưa được làm rõ; phụ thuộc CF02 và CF03.
- CF06 - Thiếu dữ liệu: Chưa có SLA cổng QR, chưa rõ xử lý timeout, callback chậm hoặc thất bại.
- CF08 - Thiếu dữ liệu: Chưa có AC về điều kiện, số tiền và trạng thái hoàn tiền.

## Làm rõ phiếu cao/thấp

- CF03: Người chấm 3 SP có thể đang giả định chỉ chọn điểm nhận trong trường; người chấm 8 SP có thể tính thêm quy tắc ngoài trường và xử lý lỗi. Cần thống nhất phạm vi trước khi estimate lại.
- CF04: Phiếu 5 SP có thể giả định luồng nhận đơn đơn giản, phiếu 13 SP có thể tính thêm nhiều trạng thái, xử lý lỗi và phối hợp với quán. Cần làm rõ trạng thái đơn, quyền cập nhật và điều kiện chuyển trạng thái.
- CF06: Phiếu 5 SP có thể chỉ tính luồng thanh toán thành công, phiếu 13 SP có thể bao gồm timeout, callback chậm, giao dịch thất bại và chống thanh toán trùng. Cần làm rõ SLA và hợp đồng tích hợp QR.
- CF08: Mức 13 SP mới là tạm chốt, chưa đủ cơ sở xác nhận vì thiếu AC. Cần làm rõ điều kiện quán hủy, số tiền hoàn, trạng thái đơn và cách xử lý hoàn tiền thất bại.

## Đề xuất refine

- CF03 - Bổ sung AC cho điểm nhận trong/ngoài trường, dữ liệu bắt buộc và thông báo lỗi; sau đó Planning Poker lại.
- CF04 - Làm rõ luồng nhận đơn và các trạng thái giao; cân nhắc tách phần nhận đơn khỏi phần cập nhật giao nếu phạm vi quá lớn.
- CF06 - Làm rõ SLA, timeout, callback và trạng thái giao dịch; cân nhắc tách luồng thanh toán cơ bản khỏi xử lý đối soát hoặc ngoại lệ phức tạp.
- CF08 - Bổ sung AC trước khi estimate lại; cân nhắc tách yêu cầu hoàn tiền thông thường khỏi xử lý hoàn tiền thất bại nếu cần.

# 5.2. Sprint Goal và phạm vi

| PBI | Quyết định |
|---|---|
| **CF01 - Xem thực đơn/tình trạng món** | Chọn - 3 SP |
| **CF02 - Tạo đơn/mã xác nhận** | Chọn - 5 SP |
| **CF03 - Chọn điểm nhận** | Chưa chọn |
| **CF04 - Nhận đơn/cập nhật giao hàng** | Chưa chọn |
| **CF05 - Xem trạng thái giao hàng** | Chưa chọn |
| **CF06 - Thanh toán QR** | Chưa chọn |
| **CF07 - Hóa đơn điện tử** | Chưa chọn |
| **CF08 - Hoàn tiền khi quán hủy** | Loại khỏi Sprint |
| **CF09 - Đánh giá người giao** | Loại khỏi Sprint |

# 5.3. Task Breakdown và Capacity

## Tính Capacity từng người/toàn đội

| Thành viên | Giờ làm việc | Giờ gián đoạn | Capacity |
|:---:|:---:|:---:|:---:|
| Lan – Frontend | 10 × 6 = 60h | 6h | 54h |
| Minh – Backend | 8 × 6 = 48h | 0h | 48h |
| Ngọc – QA/BA | 10 × 5 = 50h | 5h | 45h |
| Phúc – Integration | 9 × 6 = 54h | 8h | 46h |
| **Toàn đội** | **212h** | **19h** | **193h** |

## Tính lại khi Minh nghỉ thêm 2 ngày

| Thành viên | Capacity |
|---|:---:|
| Lan | 54h |
| Minh | 36h |
| Ngọc | 45h |
| Phúc | 46h |
| **Toàn đội** | **181h** |

**Tác động:** Capacity toàn đội giảm 12 giờ (khoảng 6,2%). Nhóm cần xem lại phân công Backend, phối hợp với Phúc để giảm rủi ro tích hợp và cân nhắc thu hẹp phạm vi nếu cần. Không được kết luận Velocity giảm đúng 6,2% vì SP không quy đổi trực tiếp thành giờ.

## Phân rã PBI

### CF01

| Task | Động từ và đầu ra | Phụ thuộc/phối hợp |
|:---:|---|---|
| 1 | Thiết kế giao diện danh sách món ăn - bản giao diện thực đơn | Lan thực hiện |
| 2 | Xây dựng API lấy thực đơn và tình trạng món - API hoạt động | Minh thực hiện |
| 3 | Tích hợp API vào giao diện - màn hình hiển thị dữ liệu thực | T2; Lan phối hợp Minh |
| 4 | Kiểm thử hiển thị món còn/hết hàng - kết quả kiểm thử | T1, T2, T3; Ngọc kiểm thử |

### CF02

| Task | Động từ và đầu ra | Phụ thuộc/phối hợp |
|:---:|---|---|
| 1 | Thiết kế biểu mẫu tạo đơn - giao diện nhập thông tin | CF01; Lan thực hiện |
| 2 | Xây dựng API tạo đơn - API lưu đơn và trả mã xác nhận | CF01; Minh thực hiện |
| 3 | Tích hợp giao diện với API - luồng tạo đơn hoạt động | T1, T2; Lan phối hợp Minh |
| 4 | Kiểm thử tạo đơn hợp lệ và dữ liệu thiếu - kết quả kiểm thử | T3; Ngọc thực hiện |
| 5 | Kiểm thử tích hợp và sửa lỗi - luồng tạo đơn đạt DoD | T4; Phúc phối hợp Minh, Ngọc |

### CF06

| Task | Động từ và đầu ra | Phụ thuộc/phối hợp |
|:---:|---|---|
| 1 | Làm rõ SLA, timeout và callback - tài liệu yêu cầu thanh toán | Ngọc phối hợp PO và nhà cung cấp |
| 2 | Thiết kế luồng thanh toán - sơ đồ luồng và trạng thái giao dịch | T1; Minh phối hợp Phúc |
| 3 | Xác định trường hợp kiểm thử thành công/thất bại - bộ test case | T1, T2; Ngọc thực hiện |
| 4 | Đánh giá khả năng tích hợp - kết quả đánh giá kỹ thuật | T1; Phúc phối hợp Minh |

# 5.5. Burndown và thích nghi

## Burndown Chart

## Điều tra

| Tín hiệu | Giả thuyết | Dữ liệu cần kiểm tra |
|---|---|---|
| Ngày 1: còn 21 SP, không giảm | Nhóm chưa hoàn thành PBI nào theo DoD hoặc đang xử lý công việc chưa tạo ra PBI Done. | Trạng thái task, PR, kết quả kiểm thử và tiêu chí DoD. |
| Ngày 4: tăng từ 18 lên 23 SP | Có thêm phạm vi, ước lượng thay đổi hoặc PBI chưa hoàn thành được đánh giá lại. | Lịch sử Sprint Backlog, thay đổi SP, PBI được thêm và lý do thay đổi. |
| Ngày 5: giảm từ 23 xuống 18 SP | Một PBI đã hoàn thành hoặc nhóm điều chỉnh lại phạm vi/ước lượng. | PBI chuyển Done, kết quả kiểm thử và lịch sử chỉnh sửa backlog. |
| Ngày 9–10: giữ ở mức 5 SP | PBI còn lại bị chặn, chưa kiểm thử xong hoặc không đáp ứng DoD. | Task chưa hoàn thành, lỗi còn mở, phụ thuộc và phản hồi của QA. |

## Đề xuất trao đổi/cập nhật kế hoạch

- Daily Scrum: Nhóm kiểm tra tiến độ, công việc bị chặn và kế hoạch trong 24 giờ tiếp theo; ưu tiên xử lý PBI đang gần hoàn thành nhưng còn thiếu kiểm thử.
- Trao đổi với Product Owner: Làm rõ phạm vi, yêu cầu và thứ tự ưu tiên; không tự ý đưa PBI mới vào Sprint.
- Khi phát sinh thêm phạm vi: Đánh giá ảnh hưởng đến Sprint Goal, Capacity và các PBI đã cam kết. Chỉ điều chỉnh phạm vi khi nhóm và PO thống nhất, đồng thời bảo vệ Sprint Goal.
- Cuối Sprint: Kiểm tra từng PBI theo DoD. PBI chưa hoàn thành phải được ghi nhận là chưa Done và đưa lại Product Backlog để PO xem xét ưu tiên.

# 5.6. Ngoại lệ và thay đổi

| Tình huống | Cách xử lý | Tác động và cách công khai |
|---|---|---|
| QR lỗi sau khi tạo đơn | Giữ đơn ở trạng thái chờ thanh toán; kiểm tra trạng thái giao dịch, xử lý timeout/callback và tránh thanh toán trùng. | **Sprint Goal:** Có thể chưa đạt luồng đặt món–thanh toán hoàn chỉnh. DoD: Chưa Done nếu lỗi ảnh hưởng AC hoặc còn lỗi nghiêm trọng. **Velocity:** Không tính SP nếu PBI chưa Done. **Burndown:** Giữ SP còn lại cho đến khi hoàn thành. Báo PO và trình bày lỗi cùng phương án xử lý tại Sprint Review. |
| Thiếu SĐT/điểm nhận ngoài trường | Trao đổi với PO để xác định dữ liệu bắt buộc, quy tắc kiểm tra và thông báo lỗi; cập nhật AC trước khi triển khai. | **Sprint Goal:** Có thể bị ảnh hưởng do luồng nhận món chưa hoàn chỉnh. DoD: Chưa đạt nếu thiếu yêu cầu cần thiết. **Velocity:** Không tính SP cho PBI chưa Done. **Burndown:** Phản ánh công việc còn lại thực tế. Công khai yêu cầu chưa rõ và quyết định của PO. |
| PO thêm PBI khuyến mãi 5 SP giữa Sprint | Đánh giá giá trị, rủi ro và Capacity; trao đổi với Developers về ảnh hưởng đến Sprint Goal. Nếu cần thêm, thống nhất điều chỉnh phạm vi với PO, không tự động cộng việc. | **Sprint Goal:** Có nguy cơ phân tán nguồn lực. DoD: PBI mới vẫn phải đáp ứng đầy đủ DoD. **Velocity:** Chỉ tính SP khi PBI hoàn thành. **Burndown:** Ghi nhận thay đổi phạm vi tại thời điểm xảy ra, không sửa dữ liệu cũ. Công khai lý do thêm PBI và công việc nào bị ảnh hưởng. |
| PBI mới hoàn thành 80% nhưng chưa kiểm thử | Tiếp tục kiểm thử, sửa lỗi và xác nhận toàn bộ AC/DoD; nếu chưa kịp hoàn thành, đưa PBI về Product Backlog để PO xem xét ưu tiên lại. | **Sprint Goal:** Chưa thể coi là đạt nếu PBI này cần thiết để hoàn thành mục tiêu. DoD: Chưa đạt. **Velocity:** Không tính SP, dù đã hoàn thành 80%. **Burndown:** Giữ nguyên SP còn lại cho đến khi PBI thực sự Done. Công khai trạng thái, lỗi còn tồn tại và kế hoạch tiếp theo tại Sprint Review. |