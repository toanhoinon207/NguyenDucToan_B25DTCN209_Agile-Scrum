# Phần 1 - Điền bảng

| # | Hạng mục | Nhãn MoSCoW | Vì sao chọn nhãn này |
|:---:|---|---|---|
| **1** | Sửa lỗi hiển thị sai cước sau khuyến mãi (đang thu sai tiền khách) | **Must** | Thiếu hạng mục này thì bản mới có thể tiếp tục thu sai tiền khách, không đảm bảo tính chính xác của hệ thống. |
| **2** | Áp mã khuyến mãi khi đặt xe | **Must** | Đây là chức năng cốt lõi của chương trình khuyến mãi. Thiếu chức năng này thì không đạt mục tiêu chính của bản phát hành. |
| **3** | Thanh toán bằng ví RikkeiPay (khách vẫn trả được tiền mặt) | **Should** | Rất cần thêm phương thức thanh toán, nhưng khách vẫn có thể trả tiền mặt nên chưa bắt buộc phải có trong bản này. |
| **4** | Hẹn giờ đặt xe trước (không cần cho chương trình khuyến mãi; đội chưa bàn xong cách làm) | **Won't** | Không cần cho chương trình khuyến mãi và cách làm chưa được thống nhất. Đội quyết định không thực hiện trong bản này và cần thông báo cho bên đề xuất. |
| **5** | Chat với tài xế (khách vẫn gọi điện được) | **Could** | Khách vẫn có thể gọi điện cho tài xế nên thiếu chức năng chat không ảnh hưởng nhiều. Dù Chăm sóc khách hàng muốn là Must, chức năng này không bắt buộc để phát hành bản mới. |
| **6** | Giao diện trang trí cho chương trình khuyến mãi | **Could** | Giao diện đẹp giúp tăng tính hấp dẫn nhưng không quyết định việc phát hành bản mới. Dù Marketing muốn là Must, chức năng trang trí không quan trọng bằng việc áp dụng khuyến mãi và tính cước chính xác. |

# Phần 2 - Khi tình hình thay đổi

## (a) Đội bị chậm 2 ngày và phải bỏ bớt việc

- Đội nên bỏ các hạng mục Could trước, #5 (Chat với tài xế) và #6 (Giao diện trang trí), sau đó cân nhắc #3 (Thanh toán bằng ví RikkeiPay) nếu vẫn thiếu thời gian. Cần giữ #1 (Sửa lỗi hiển thị sai cước) và #2 (Áp mã khuyến mãi) đến cùng vì đây là các chức năng cốt lõi để đảm bảo thu đúng tiền và thực hiện chương trình khuyến mãi.

## (b) Tài xế không nhận tiền mặt nữa

- Nhãn của #3 đổi từ Should thành Must. Khi không còn thanh toán tiền mặt, ví RikkeiPay trở thành phương thức thanh toán cần thiết để khách trả tiền và bản mới có thể hoạt động theo quy định mới.