## At  command
- Là câu lệnh chạy các chương trình theo sắp đặt của người quản trị. 
- Gói (package) cần cài đặt là `at`
- Cần xác định thời gian chạy câu lệnh và sử dụng theo cú pháp `at + thời gian`
- Sau khi thêm các câu lệnh thì nhấn tổ hợp phím `Ctrl+D` để lưu.
## Cron command
- Để thực hiện lặp lại các câu lệnh có chu kỳ. 
## Rotating Log Files
- Lữu trữ các file log hiện tại, xóa các file log cũ. Việc này khiến ta luôn sẵn file log hiện tại để nghiên cứu và các file log được dọn dẹp tránh tình trạng đầy bộ nhớ.
- file config `/etc/logrotate.conf`
## Tar command
- Nén và giải nén file. -c là nén -x là giải nén.
- Dùng khi cần chuyển file và thư mục lớn từ server này sang server khác.
- Tạo backup: Nghiên cứu sau.
## Build DNS Server
- https://www.youtube.com/watch?v=Wp7tQxLHM1k
## Build DHCP Server
- https://www.youtube.com/watch?v=UEqoAbr-ASw
- DHCP cấp địa chỉ IP, Subnet Mask, Default Gateway. Giao tiếp qua hai cổng port 67 và 68. Port 67 nghe thông tin từ client và port 68 để reply thông tin. 
- Ưu điểm: cấu hình IP động cho các máy client theo sắp xếp của người quản trị. Có range sẵn. Linh hoạt trong việc cấp IP. 
- Nguyên lý hoạt động: Clent gửi bản tin Discorvery đến DHCP Server. DHCP Server gửi lại bản tin Offer. Client nhận được offer sẽ gửi bản tin Request đến DHCP Server. Cuối cùng DHCP sẽ gửi bản tin ACK
