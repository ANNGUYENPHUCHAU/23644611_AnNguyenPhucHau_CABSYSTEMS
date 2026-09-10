# Test Case - CAB System


| Test Case ID | Context | FR | UC | Input | Expected Output |
|---|---|---|---|---|---|
| TC01 | Đăng ký tài khoản khách hàng thành công | FR01 | UC01 | Họ tên, email chưa tồn tại, mật khẩu hợp lệ | Tài khoản được tạo thành công |
| TC02 | Đăng ký tài khoản với email đã tồn tại | FR01 | UC01 | Email đã tồn tại trong hệ thống | Hệ thống báo lỗi email đã được sử dụng |
| TC03 | Đăng nhập khách hàng | FR02 | UC01 | Email và mật khẩu đúng | Khách hàng đăng nhập thành công |
| TC04 | Cập nhật thông tin cá nhân | FR03 | UC01 | Thông tin cá nhân mới | Thông tin được cập nhật thành công |


| TC05 | Cập nhật hồ sơ tài xế | FR04 | UC06 | Thông tin tài xế hợp lệ | Hồ sơ tài xế được cập nhật |
| TC06 | Cập nhật phương tiện | FR05 | UC06 | Biển số xe, loại xe | Thông tin phương tiện được lưu |
| TC07 | Tài xế chuyển trạng thái sẵn sàng | FR06 | UC06 | Status = Available | Hệ thống cập nhật trạng thái tài xế |


| TC08 | Khách hàng tạo chuyến xe | FR07, FR08 | UC02 | Điểm đón, điểm đến, loại xe | Hệ thống tạo yêu cầu đặt xe |
| TC09 | Không nhập điểm đến | FR07 | UC02 | Thiếu Destination | Hệ thống yêu cầu nhập đầy đủ thông tin |


| TC10 | Tìm được tài xế phù hợp | FR09 | UC02 | Có Driver Available | Hệ thống chọn tài xế phù hợp |
| TC11 | Gửi yêu cầu nhận chuyến | FR10 | UC07 | Driver nhận được yêu cầu | Driver nhận thông báo chuyến |
| TC12 | Driver từ chối chuyến | FR11 | UC07 | Driver chọn Reject | Hệ thống tiếp tục tìm tài xế khác |
| TC13 | Không có tài xế phù hợp | FR12 | UC02 | Không có Driver Available | Khách hàng nhận thông báo không tìm được tài xế |


| TC14 | Driver nhận chuyến | FR13 | UC07 | Driver chọn Accept | Chuyến xe được gán cho Driver |
| TC15 | Driver cập nhật trạng thái chuyến | FR15 | UC08 | Đã đến điểm đón, đã đón khách, đang đi, hoàn thành | Trạng thái chuyến được cập nhật |


| TC16 | Customer theo dõi chuyến xe | FR16, FR17 | UC03 | Trip đang hoạt động | Hiển thị trạng thái, tài xế |
| TC17 | Xem ETA tài xế | FR18 | UC03 | Driver có vị trí | Hiển thị thời gian dự kiến đến |


| TC18 | Tính tiền chuyến xe | FR19 | UC14 | Trip hoàn thành | Hệ thống tạo số tiền thanh toán |
| TC19 | Thanh toán tiền mặt | FR20 | UC14 | PaymentMethod = Cash | Thanh toán được ghi nhận |
| TC20 | Thanh toán điện tử thành công | FR21 | UC14 | PaymentMethod = Online | Nhà cung cấp trả kết quả thành công |
| TC21 | Thanh toán điện tử thất bại | FR22 | UC14 | Transaction Failed | Thông báo lỗi và cho phép xử lý lại |


| TC22 | Gửi thông báo trạng thái chuyến | FR23 | UC02/UC07/UC08 | Phát sinh sự kiện chuyến xe | Người dùng nhận thông báo |
| TC23 | Xem lịch sử chuyến xe | FR24 | UC04 | Customer có chuyến đã hoàn thành | Hiển thị lịch sử chuyến |
| TC24 | Đánh giá tài xế | FR25 | UC05 | Rating sau chuyến hoàn thành | Đánh giá được lưu |


| TC25 | Nhân viên quản lý khách hàng | FR26 | UC10 | Staff truy cập quản lý Customer | Thông tin khách hàng hiển thị |
| TC26 | Nhân viên quản lý tài xế | FR27 | UC11 | Staff truy cập Driver | Thông tin tài xế hiển thị |
| TC27 | Nhân viên giám sát chuyến | FR29, FR30 | UC12 | Trip đang hoạt động | Hiển thị trạng thái chuyến |
| TC28 | Tra cứu lịch sử giao dịch | FR33 | UC13 | Transaction ID | Hiển thị thông tin giao dịch |
