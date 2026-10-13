# Bước 1. Tìm lỗi

| Mã | Kết quả và lý do |
|---|---|
| **US1** | **Đạt:** Vai trò rõ ràng, một việc cụ thể và có thể kiểm thử bằng cách chọn loại món rồi xem kết quả. |
| **US2** | **Testable:** “Đẹp và dễ dùng” chưa có thông số đo lường cụ thể để kiểm thử. |
| **US3** | **Valuable:** Mục tiêu chỉ là lựa chọn công nghệ và lợi ích cho lập trình viên, chưa thể hiện rõ giá trị đối với người dùng hoặc sản phẩm. |
| **US4** | **Small:** Chứa quá nhiều chức năng như xem báo cáo, lọc dữ liệu, xuất Excel và tự động gửi email nên khó ước lượng. |

# Bước 2. Sửa lỗi

## a) Viết lại US2

Là một khách hàng, tôi muốn giao diện đặt món hiển thị rõ tên món, giá tiền và nút đặt hàng, để tôi có thể hoàn tất đặt món trong tối đa 2 phút.

## b) Tách US4

**Epic:** Quản lý và theo dõi doanh thu

&emsp;&emsp; **Feature:** Báo cáo doanh thu

&emsp;&emsp;&emsp;- **UC4.1:** Là một admin, tôi muốn xem doanh thu theo ngày, tuần, tháng và theo nhà hàng hoặc khu vực, để theo dõi tình hình kinh doanh.

&emsp;&emsp;&emsp;- **UC4.2:** Là một admin, tôi muốn xuất báo cáo doanh thu ra Excel và gửi qua email cho ban giám đốc, để chia sẻ kết quả kinh doanh.

# Bước 3. Xếp lại backlog

## a) Xếp thứ tự ưu tiên

| Ưu tiên | User Story |
|:---:|---|
| **1** | UC1 - Lọc nhà hàng theo món |
| **2** | UC2 - Giao diện đặt món đễ dùng |
| **3** | UC4.1 Xem báo cáo doanh thu |
| **4** | UC4.2 - Xuất và gửi báo cáo |

## b) DEEP

- Detailed appropriately: Story đứng đầu cần được làm rõ vừa đủ, gồm mục tiêu, tiêu chí chấp nhận, quy tắc lọc và các trường hợp cần xử lý.
- Estimated: Nhóm phát triển ước lượng độ lớn hoặc công sức thực hiện.
- Emergent: Backlog có thể được cập nhật khi có thông tin hoặc yêu cầu mới.
- Prioritized: Các mục được sắp xếp theo giá trị, mức độ cấp thiết và sự phụ thuộc.

## c) Refinement

- Làm rõ yêu cầu và các tiêu chí chấp nhận.
- Thảo luận các trường hợp ngoại lệ.
- Chia nhỏ thêm nếu story vẫn quá lớn.
- Ước lượng công sức và kiểm tra nhóm có đủ khả năng hoàn thành trong Sprint hay không.
- Sắp xếp lại thứ tự ưu tiên.