# Phần 1 - Phân tích

## 1. Tính Planning Capacity

| Developer | Capacity cá nhân | Việc cố định | Planning Capacity |
|---|:---:|:---:|:---:|
| Tú | 10 × 6 = 60h | 6h | 54h |
| Vy | 10 × 6 = 60h | 0h | 60h |
| Khoa | 9 × 6 = 54h | 4h | 50h |
| Hà | 8 × 6 = 48h | 0h | 48h |
| **Tổng** | **222h** | **10h** | **212h** |

## 2. Khoảng Velocity dự báo

**Average Velocity** = 18 SP

- Dùng khoảng 15–20 SP để tham khảo khi chọn phạm vi Sprint

# Phần 2 - Thiết kế

**Sprint Goal:** Giúp khách hàng thanh toán chuyến đi bằng ví RikkeiPay ổn định và biết chắc tiền đã được hoàn vào ví khi chuyến đi bị hủy.

**Danh sách PBI chọn:**

- Thanh toán chuyến đi bằng ví RikkeiPay - 8 SP	
- Hoàn tiền vào ví khi chuyến bị hủy - 5 SP
- Xem số dư và lịch sử giao dịch ví - 3 SP

**Danh sách PBI không chọn:**

- Gửi SMS khi tài xế sắp đến - 3 SP (Nhà cung cấp SMS chưa ký hợp đồng nên chưa sẵn sàng triển khai.)
- Giao diện chủ đề Tết - 2 SP (Không trực tiếp phục vụ Sprint Goal về thanh toán và hoàn tiền.)
- Chat với tài xế - 5 (Không trực tiếp giải quyết vấn đề thanh toán và xác nhận hoàn tiền.)

# Phần 3- Phân rã

| Task | Nội dung | Đầu ra kiểm chứng được |
|:---:|---|---|
| 1 | Xây dựng logic xác định chuyến bị hủy và tính số tiền cần hoàn. | Các test case xác nhận đúng số tiền hoàn theo trạng thái chuyến đi. |
| 2 | Xây dựng API hoàn tiền vào ví và cập nhật lịch sử giao dịch. | API trả kết quả hoàn tiền; số dư và lịch sử giao dịch được cập nhật đúng, không hoàn tiền trùng. |
| 3 | Viết Integration Test cho luồng hủy chuyến và hoàn tiền. | Bộ Integration Test chạy thành công, xác nhận số dư tăng đúng và giao dịch hoàn tiền được ghi nhận. |