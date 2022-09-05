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
|Mô tả và phân tách rõ ràng chức năng nhiệm vụ của từng tầng|Mô tả cách truyền dữ liệu qua Internet|
#### TCP/IP
- Tầng 4: Application Cung cấp cho các ứng dụng những trao đổi dữ liệu chuẩn hóa, giao tiếp dữ liệu giữa 2 máy khác nhau thông qua dịch vụ mạng khác nhau. Giao thức: HTTP, HTTPS, 
- Tầng 3: Transport Tương tự tầng Transport của mô hình OSI. Giao thức UDP và TCP
- Tầng 2: Network Xử lý các gói và truyền qua network. Giao thức IP và ICMP 
- Tầng 1: Physical Truyền dữ liệu giữa hai thiết bị trong cùng một mạng. Giao thức Ethernet (mạng LAN) và ARP. 
#### TCP/UDP
|TCP|UDP|
|------|-----|
|Giao thức hướng kết nối (cần thiết lập kết nối (bắt tay 3 bước) trước mới có thể truyền)|Giao thức phi kết nối (đẩy gói tin vào đường truyền)|
|Hỗ trợ cơ chế Full-duplex (truyền và nhận dữ liệu cùng lúc)|Truyền nhanh, hiệu quả với các gói tin yêu cầu thời gian|
|Cung cấp cơ chế báo nhận (gửi yêu cầu → nhận → báo đã nhận → xác thực → truyền)|Truyền không tin cậy, chỉ truyền và không quan tâm lỗi|
|Có cơ chế điều khiển luồng thích hợp (flow control) để tránh nghẽn xảy ra|Truyền liên tục, hỏng thì tiếp tục truyền gói mới|
|Phục hồi dữ liệu bị mất trên đường truyền|Gói tin bị lỗi thì bỏ qua và tiếp tục truyền gói mới|
#### Cấu trúc IPv4, IPv6
- IPv4
  - Địa chỉ IPv4 gồm 32 bits, được chia đều thành 4 octets
  - Địa chỉ IPv4 hiện tại đang k đủ cung cấp nhu cầu sử dụng hiện tại nên để giải quyết vấn đề thiếu hụt thì ta dùng đến các kĩ thuật: NAT, subnetting, IPv6, ...
  - Có 2 loại địa chỉ IPv4 là: Public (dùng cho host trên Internet) và Private (dùng cho host trong LAN) 
  - Broadcast Address là địa chỉ có các bit trong dải bằng 1, đại diện cho tất cả các thiết bị kết nối cùng mạng. Khi một gói tin được gửi đến địa chỉ broadcast, toàn bộ các thiết bị đều nhận được.
  - Default Gateway được sử dụng cho mục đích: Nếu không tồn tại đường gửi đến địa chỉ nào đó trong routing table thì gửi gói tin đó qua gateway. Nhiệm vụ của gateway thường là gửi gói tin đó đến nơi cần đến. 
- IPv6
  - Gồm 128 bits. Gấp 4 lần địa chỉ IPv4
  - Loại bỏ công nghệ NAT. Có khả năng tự động cấu hình không dùng DHCP Server. 
## Switching 
#### VLAN
- Các mạng lớn hiện nay đều triển khai mạng mạng cục bộ ảo (VLANs). Nếu không có VLANs, Switch sẽ coi các port đều ở trong cùng một miền quảng bá. Port của Switch sẽ được chia làm các nhóm trong các VLANs khác nhau (chia đoạn miền quảng bá)
- Switch ban đầu mặc định có 1 VLAN, tuy nhiên có thể tự cấu hình thành nhiều VLAN khác nhau. Điều này sẽ tạo ra nhiều miền quảng bá bằng cách đặt nhiều giao diện vào 1 VLAN.
  - Nhóm các người dùng lại thành 1 cụm mà không cần chia theo vị trí địa lý.
  - Tăng cường bảo mật bằng cách tách riêng dữ liệu thành một VLAN riêng biệt
- Khi một liên kết giữa hai switch hoặc giữa một router và một switch truyền tải lưu lượng của nhiều VLAN thì cổng đó gọi là cổng `trunk`
- Các thành viên trong cùng VLAN ở các switch khác nhau vẫn có thể giao tiếp với nhau. 
![1](/../../../Network-CCNA/blob/main/image/2021-04-01_16-41-45.png)
- Routing giữa các VLAN thì ta dùng InterVLAN - các thiết bị ở các VLAN khác nhau có thể giao tiếp được với nhau. Chỉ áp dụng được trong mô hình có thiết bị ở Layer3.
#### Etherchannel, bonding
- Công nghệ EtherChannel giúp gộp nhiều interface vật lý thành một kênh logic để tăng băng thông trên đường dẫn point-to-point. 
- Cấu hình bonding là từ 2 hoặc nhiều interface kết hợp lại thành 1 interface ảo. Điều này tăng tính dự phòng, cân bằng tải. Khi 1 card mạng vật lý có sự cố thì với cơ chế bonding sẽ tự độg chuyển sang card còn lại để hoạt động.
## Routing
- 2 loại cơ bản: Định tuyến tĩnh, định tuyến động. 
  - Trong định tuyến động gồm giao thức EGP, BGP dùng định tuyến biên. IGP, RIP, OSPF, EIGRP định tuyến nội miề. 
