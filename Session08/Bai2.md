# Nhiệm vụ 1 - Phân tích Velocity và Capacity

## 1.1. Velocity

| Sprint | SP hoàn thành (Done) | Ghi chú |
|---|---|---|
| Sprint -3 | 15 | Đủ thành viên |
| Sprint -2 | 16 | Đủ thành viên |
| Sprint -1 | 17 | Đủ thành viên |
| Velocity tham khảo | 16 SP | Tính trung bình 3 Sprint - Dùng để dự báo khối lượng PBI có thể chọn cho Sprint tiếp theo. |

## 1.2. Capacity

| Thành viên | Ngày Sprint | Ngày nghỉ | Ngày làm | Giờ/ngày | Capacity |
|---|:---:|:---:|:---:|:---:|:---:|
| Dev A | 10 | 0 | 10 | 5 | 50h |
| Dev B | 10 | 0 | 10 | 5 | 50h |
| Dev C | 10 | 2 | 8 | 5 | 40h |
| Dev D | 10 | 0 | 10 | 5 | 50h |
| **Tổng** |  |  |  |  | **190h** |

**Nhận xét:** Capacity của Sprint này là 190 giờ, thấp hơn mức bình thường 200 giờ là 10 giờ. Nhóm sử dụng Average Velocity 16 SP kết hợp với Capacity thực tế để dự báo phạm vi Sprint phù hợp.

# Nhiệm vụ 2 - Viết lại Sprint Goal

- **Sprint Goal:** Giúp người sử dụng xe máy điện tìm trạm sạc phù hợp, xem khung giờ còn trống và đặt trước vị trí sạc để giảm nguy cơ đến trạm nhưng không còn chỗ.

# Nhiệm vụ 3 - Lập Sprint Backlog

| Mã Story | Ưu tiên | SP | Lựa chọn | Lý do |
|---|:---:|:---:|---|---|
| CS01 | 1 | 3 SP | Chọn | Giúp người dùng tìm trạm sạc phù hợp. |
| CS02 | 2 | 3 SP | Chọn | Giúp người dùng biết thời gian có thể đặt chỗ. |
| CS03 | 3 | 5 SP | Chọn | Là chức năng cốt lõi để đạt Sprint Goal. |
| CS04 | 4 | 5 SP | Chưa chọn | Quy tắc hủy sát giờ bắt đầu chưa được làm rõ. |

**Tổng SP đã chọn:** 11 SP

### Task Breakdown cho CS03

| STT | Task | Đầu ra | Ước lượng (giờ) |
|:---:|---|---|:---:|
| 1 | Xây dựng luồng đặt chỗ; kiểm tra trạm sạc, thời gian, phương tiện và tình trạng chỗ trống; ngăn đặt trùng vị trí trong cùng khung giờ. | Yêu cầu đặt chỗ hợp lệ và không bị trùng lịch. | 12 |
| 2 | Lưu thông tin đặt chỗ hợp lệ và tạo mã xác nhận. | Đặt chỗ được lưu thành công và có mã xác nhận. | 8 |

# Nhiệm vụ 4 - Phân tích Burndown Chart

- Đường thực tế giữ nguyên ở mức 11 SP từ ngày 0 đến ngày 2, trong khi đường lý tưởng giảm còn 8.8 SP vào ngày 2, cho thấy chưa có PBI nào được hoàn thành trong giai đoạn đầu. Đến ngày 7, đường thực tế còn 8 SP so với dường lý tưởng 3.3 SP, cho thấy tiến độ đang quá chậm và Sprint Goal có nguy cơ không đạt.
- Nhóm nên phối hợp xử lý các công việc còn vướng mắc của CS03, ưu tiên hoàn thành và kiểm thử để đưa PBI về trạng thái Done. Scrum Master hỗ trợ loại bỏ trở ngại, còn Developers điều chỉnh cách phối hợp và giảm công việc đang làm dở.