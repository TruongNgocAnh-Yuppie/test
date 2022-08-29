## Mô hình OSI, TCP/IP
#### OSI
- Tầng 7: Application Xác định giao diện giữa người sử dụng và môi trường OSI. Hỗ trợ ứng dụng và các tiến trình có liên quan đến người sử dụng cuối. Cung cấp nền tảng làm việc ứng dụng đó chạy bên trên. Giao thức điển hình: HTTP, HTTPS, SMTP, FTP, 
- Tầng 6: Presentation Mã hóa dữ liệu theo chuẩn. Giao thức điển hình là: SSL
- Tầng 5: Session Tạo phiên giao tieeso giữa hai thiết bị: thiết lập, duy trì, và đồng bộ. 
- Tầng 4: Transport Chuyển dữ liệu. Chia các gói tin lớn thành các gói nhỏ và đánh số theo thứ tự. Theo dõi và truyền lại gói tin nếu thất bại. Kiểm soát và sửa lỗi, điều khiển lưu lượng dữ liệu, đảm bảo gói tin được truyền đi chính xác, trọn vẹn. Giao thức điển hình: TCP, UDP.
- Tầng 3: Network Cung cấp thuật toán dò đường cho Router, xác định đường truyền vật lý tốt nhất cho dữ liệu. Kiểm tra và sắp xếp các gói tin đúng vị trí như bên gửi. Kiểm tra gói truyền bị thiếu. Chức năng điều khiển tắc nghẽn bằng cách giao tiếp giữa các mạng 
- Tầng 2: Data link Nơi thiết bị chuyển mạch hoạt động. Tạo/gỡ bỏ khung thông tin (Frame). Truyền dữ liệu trong cùng mạng. Kiểm soát lỗi và sửa chữa từ tầng vật lý. 
- Tầng 1: Physical Bao gồm các thiết bị vật lý phần cứng thực hiện truyền tải dữ liệu. Điều chế hoặc biến đổi các loại tín hiệu.
#### Sự khác nhau giữa hai mô hình
|OSI|TCP/IP|
|---------|--------|
|Là mô hình lý thuyết, được sử dụng cho hệ thống máy tính|Là mô hình Server-Client, truyền dữ liệu qua Internet|
#### TCP/IP
- Tầng 4: Application Cung cấp cho các ứng dụng những trao đổi dữ liệu chuẩn hóa, giao tiếp dữ liệu giữa 2 máy khác nhau thông qua dịch vụ mạng khác nhau. Giao thức: HTTP, HTTPS, 
