# 5. Yêu cầu đầu ra
1. Phần I.Phân tích vấn đề
- Sai lệch về DNS: Thực tập sinh nghĩ rằng URL gửi thẳng tới server mà không cần DNS
- Sai lệch về TCP/TLS: Thực tập sinh nghĩ không cần thực hiện bước bắt tay TCP/TLS vì HTTPS tự động mở không điều kiện là hoàn toàn sai
- Sai lệch về mã lỗi HTTP: Thực tập sinh nghĩ rằng hồ sơ bệnh nhân bị xóa nhưng thực chất là lỗi đường dẫn URL
- Sai lệch về việc sửa DOM trên DevTools: Thực tập sinh nghĩ việc gõ sửa chữ "Âm tính - Bình thường" trên thẻ ở Tab Elements là đã lưu thành công vào Database của máy chủ
- Vì mã 500 là do lỗi nội bộ máy chủ, sự cố hệ thống. Tác động tới bệnh nhân khiến bệnh nhân mất niềm tin vào dữ liệu y tế
2. Phần II. Sửa đổi và Hoàn thiện giải pháp
- Bước 1: Trình duyệt kiểm tra tên miền thành địa chỉ IP máy chủ
- Bước 2: Trình duyệt bắt tay thực hiện TCP và thiết lập phiên mã hóa TLS để bảo mật
- Bước 3: Gửi yêu cầu "Get ....". Do lỗi hệ thống nên server sẽ phản hồi chuẩn mã 500
- Bước 4: Trình duyệt sẽ rendering Pipeline từ mã phản hồi và hiển thị giao diện thông báo 
- Tab Elements: chỉ là RAM tạm thời của trình duyệt máy khách, dữ liệu gốc thì nằm bên máy chủ, mọi sửa đổi từ máy khách sẽ không hoạt động trên chính máy chủ