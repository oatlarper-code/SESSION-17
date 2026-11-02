# 4. Yêu cầu đầu ra
1. Phần I. Báo cáo phân tích kiến trúc đa Profile
- Nguyên nhân văng phiên đăng nhập là do sử dụng cùng một profile lưu trữ cùng cookies. Khi đăng nhập tài khoản mới vào profile sẽ bị tài khoản cũ ghi đè hoặc bị máy chủ hủy bảo mật

> Mô hình 3 profile


||Nội dung|Nền|
|:-:|:-:|:-:|
Work|Lưu dữ liệu chính|Xanh
Personal|Việc cá nhân|Đỏ
Sandbox|Thử nghiệm|Cam
2. Phần II. Bookmark và An toàn thông tin
- `01_CarePulse_Clinic`: Tra cứu bệnh nhân
- `02_Pharma_Portal`: Các tri nhánh liên quan đến bộ y tế
- `03_Medical_Tools`: Các loại thuốc 

> Mẹo sử dụng Falvicon-Only

- Chuột phải bookmark -> Edit -> Delete content -> Save

> An ninh và Cloud sync

- Sử dụng Guest Profile vì nó sẽ xóa toàn bộ dữ liệu khi đóng, không cho phép các profile khác truy cập
- Không bật Sync cá nhân vì sẽ mang theo thông tin cá nhân riêng tư, gây rò rỉ dữ liệu