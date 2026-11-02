# 5. Yêu cầu đầu ra
1. Phần I. Báo cáo phân tích(I/O)
- Input: 

||Nội dung bài học|Danh sách video|
|-|-|-|
Content|840x600|840x600|
Padding|15px|15px|
Border|2px solid red|2px solid red|
Margin|margin-left 28px; margin-right -20px|margin-right -28px; margin-left 20px|

- Output: tính toán sai lệch, padding lớn khiến kích thước hộp mặc định là content-box, khung chiếm không gian, margin âm bị lệch tọa độ kéo khung đè lên nhau
2. Phần II. Thiết kế giải pháp
- Sửa đổi: 
    - .video-sidebar { flex: 0 0 320px; margin: 0; }\
      .lesson-content { flex: 1; margin: 0; }