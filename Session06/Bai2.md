# 1. Product Backlog

| Ưu tiên | Hạng mục | MoSCoW | Lý do và phụ thuộc |
|:---:|---|---|---|
| 1 | Đăng nhập/đăng ký tài khoản độc giả | **Must** | Cần xác định danh tính độc giả để quản lý hoạt động mượn sách. |
| 2 | Thủ thư quản lý kho sách (thêm/sửa/xóa sách) | **Must** | Cần dữ liệu sách chính xác và trạng thái sẵn có để độc giả tìm kiếm, mượn sách. |
| 3 | Tìm kiếm sách theo tên/tác giả | **Must** | Chức năng thiết yếu giúp độc giả tìm được sách trước khi đặt mượn. |
| 4 | Mượn sách online (có giới hạn số sách mượn cùng lúc) | **Must** | Giúp kiểm soát số lượng sách độc giả |
| 5 | Xem lịch sử mượn sách của bản thân | **Should** | Giúp độc giả theo dõi các lần mượn, có thể tạm tra cứu qua thủ thư nếu chưa triển khai. |
| 6 | Thông báo email khi sắp đến hạn trả sách | **Should** | Hạn chế việc trả sách muộn, giai đoạn đầu có thể nhắc thủ công. |
| 7 | Gia hạn mượn sách online | **Should** | Tăng sự thuận tiện nhưng độc giả vẫn có thể liên hệ thủ thư để xin gia hạn. |
| 8 | Đặt trước sách khi hết (kèm thông báo khi sách có sẵn) | **Could** | Cải thiện trải nghiệm khi sách hết, phụ thuộc vào quản lý trạng thái sách và cơ chế đặt mượn, có thể bổ sung sau. |
| 9 | Đánh giá & bình luận sách sau khi đọc | **Could** | Tăng tương tác và cung cấp thông tin tham khảo nhưng không cần cho luồng mượn sách cốt lõi. |
| 10 | Chat trực tiếp với thủ thư | **Could** | Tăng khả năng hỗ trợ nhưng độc giả vẫn có thể hỏi trực tiếp hoặc liên hệ qua kênh hiện có. |
| 11 | Tích hợp đăng nhập bằng Google/Facebook | **Won't** | Đăng nhập thông thường vẫn đáp ứng nhu cầu xác thực, tích hợp mạng xã hội chưa cần cho Release 1. |
| 12 | Gợi ý sách theo sở thích cá nhân (recommendation) | **Won't** | Không cần thiết để hoàn thành luồng mượn sách cơ bản và có thể phát triển sau khi có dữ liệu sử dụng. |

# 2. Tự phản biện

- Người khác có thể xếp đặt trước sách (#5) vào Should vì tính năng này giúp độc giả không phải kiểm tra sách nhiều lần nhưng em xếp Could vì MVP vẫn đáp ứng nhu cầu mượn sách khi sách có sẵn. 
- Chat với thủ thư (#11) cũng có thể là Should nếu thư viện cần hỗ trợ độc giả trực tuyến thường xuyên, nhưng có thể hoãn khi vẫn có kênh liên hệ khác.
- Đăng nhập Google/Facebook (#12) có thể là Could nếu thư viện muốn giảm thao tác đăng ký, nhưng chưa thiết yếu khi đã có đăng nhập thông thường.
- Việc phân loại cần dựa trên mục tiêu Release 1, nguồn lực và phương án thay thế, không dựa vào ý kiến chủ quan của bên đề xuất.