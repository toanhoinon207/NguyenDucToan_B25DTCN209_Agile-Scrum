# Nhiệm vụ 1 - Kiểm tra dữ liệu trước khi ước lượng

| Mã Story | Đủ rõ | Cần làm rõ | Thông tin/câu hỏi còn thiếu |
|---|---|:---:|---|
| LS01 |  | X | Khi đến giờ bắt đầu, hệ thống có cần tự chuyển trạng thái phiên sang trạng thái khác không? |
| LS03 |  | X | Nếu nhiều khách đặt đồng thời khi tồn kho chỉ còn đủ cho một đơn, hệ thống xử lý đơn và cập nhật tồn kho như thế nào? |

# Nhiệm vụ 2 - Phân tích Planning Poker và chốt Story Point

| Mã Story | Mức ưu tiên | Kết quả phiếu | SP cuối cùng | Lý do ngắn |
|---|:---:|---|:---:|---|
| LS01 | 1 | 3 - 3 - 5 - 3 | 2 | Phiếu 5 SP lo ngại xử lý trạng thái theo thời gian. PO xác nhận chỉ cần trạng thái “Sắp diễn ra”, nên LS01 nhỏ hơn LS02 |
| LS02 | 2 | 3 - 3 - 3 - 3 | 3 | Reference Story; các phiếu đã trùng nhau.
| LS03 | 3 | 5 - 8 - 8 - 5 | 8 | Phiếu 8 SP nhấn mạnh rủi ro đặt đồng thời và quy tắc giảm/hoàn tồn. Sau khi làm rõ, LS03 vẫn có độ phức tạp và rủi ro cao hơn LS02 |

# Nhiệm vụ 3 - Phát hiện cách hiểu sai

- Story Point đo lường tương đối độ lớn của User Story, bao gồm công sức, độ phức tạp, rủi ro và mức độ chưa chắc chắn, chứ không phải số giờ cố định.
- Nhóm sử dụng Velocity để dự báo phạm vi Sprint tiếp theo dựa trên năng lực thực tế, không quy đổi Story Point thành giờ.