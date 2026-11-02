# 5.Yêu cầu
1. Phần A: Thiết lập Profile và Bookmark chuẩn Dev
- Nếu tiếp tục dùng chung **1 Profile** cho cả GitHub cá nhân và GitHub công ty: sẽ gây xung đột, các dữ liệu từ tài khoản cũ sẽ ghi đè lên và dẫn đến văng đăng xuất
> Mô hình 3 Profile
- Profile 1: Dùng cho công việc(Work)
- Profile 2: Dùng cho cá nhân(Personal)
- Profile 3: Dùng để thử nghiệm(Sandbox)
> Cấu trúc Bookmark:
- Thư mục Work: Jira, Confluence
- Thư mục Dev: Github, StackOverflow
- Thư mục API: Swagger, Poster
- Khi cho đồng nghiệp mượn máy thì sẽ cho sử dụng Guest Profile để cô lập hoàn toàn dữ liệu
2. Phần B: Chọn đúng Extension hỗ trợ
- Extention JSON: Nhóm Productivity Suite còn 2 nhóm kia không chuyên xử lý hiển thị json thô.
- Site Access: Cấu hình On click tuân thủ nguyên tắc tối thiểu quyền
3. Phần C: Phân tích luồng HTTP Request
- 4 giai đoạn xử lý: DNS lookup -> TCP/TLS Handshake -> HTTP Request và Respond -> Rendering Pipeline
- So sánh mã trạng thái: 
    - 404 Not Found: Lỗi đường dẫn
    - 505 Internet Server Error: Lỗi sự cố hệ thống máy chủ
- Tab Network để xem mã trạng thái HTTP của trang vì các tab khác không hiển thị HTTP status
4. Phần D: Chuẩn đoán Cache và Cookies
- Lỗi CSS do Browser Cache. Cách khắc phục Ctrl + Shift + R
- Thiếu HTTPONLY: không có dấu tích trong session_id sẽ dễ dàng bị tấn công bởi người khác 
- Xóa session giữ cache vào Tab application -> Cookies -> xóa thủ công cookies session_id
5. Phần E: Debug bằng Inspect Element và Network Tab
- Đổi màu nút: Inspect -> Tab Elements -> background-color ở khung Style
- 4 bước debug: Click request lỗi -> Xem status ở Headers -> Đọc thông báo ở Respond -> Kiểm tra Payload/Headers gửi đi
- 2 Thao tác trên Network: Bật lọc Fetch/XHR -> Tích chọn Disable Cache