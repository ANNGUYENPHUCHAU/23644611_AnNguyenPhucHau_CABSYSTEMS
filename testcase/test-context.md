# Test Context - CAB System

## TCX01 - Quản lý tài khoản khách hàng

### Mục tiêu
Kiểm tra chức năng đăng ký, đăng nhập và cập nhật thông tin cá nhân của khách hàng.

### Actor
Customer

### Functional Requirement liên quan
- FR01: Đăng ký tài khoản khách hàng
- FR02: Đăng nhập khách hàng
- FR03: Cập nhật thông tin cá nhân

### Use Case liên quan
UC01 - Đăng ký/Quản lý tài khoản khách hàng

### Điều kiện kiểm thử
- Người dùng chưa có tài khoản khi đăng ký.
- Người dùng đã có tài khoản khi đăng nhập hoặc cập nhật thông tin.


---

# TCX02 - Quản lý tài xế và phương tiện

### Mục tiêu
Kiểm tra việc quản lý hồ sơ tài xế, phương tiện và trạng thái hoạt động.

### Actor
Driver

### Functional Requirement liên quan
- FR04: Quản lý hồ sơ tài xế
- FR05: Quản lý phương tiện
- FR06: Cập nhật trạng thái hoạt động

### Use Case liên quan
UC06 - Quản lý tài khoản và phương tiện tài xế

### Điều kiện kiểm thử
- Tài xế đã có tài khoản.
- Thông tin phương tiện hợp lệ.


---

# TCX03 - Tạo yêu cầu đặt chuyến xe

### Mục tiêu
Kiểm tra khách hàng có thể tạo yêu cầu đặt xe.

### Actor
Customer

### Functional Requirement liên quan
- FR07: Nhập thông tin chuyến xe
- FR08: Gửi yêu cầu đặt xe

### Use Case liên quan
UC02 - Đặt chuyến xe

### Điều kiện kiểm thử
- Customer đã đăng nhập.
- Có thông tin điểm đón, điểm đến, loại xe.


---

# TCX04 - Tìm và phân công tài xế

### Mục tiêu
Kiểm tra hệ thống tìm tài xế phù hợp và xử lý trường hợp tài xế không nhận chuyến.

### Actor
System / Driver

### Functional Requirement liên quan
- FR09: Tìm tài xế phù hợp
- FR10: Gửi yêu cầu nhận chuyến
- FR11: Xử lý tài xế không nhận chuyến
- FR12: Thông báo không tìm được tài xế

### Use Case liên quan
- UC02 - Đặt chuyến xe
- UC07 - Nhận/Từ chối chuyến xe

### Điều kiện kiểm thử
- Có hoặc không có tài xế ở trạng thái sẵn sàng.


---

# TCX05 - Thực hiện và theo dõi chuyến xe

### Mục tiêu
Kiểm tra quá trình tài xế nhận chuyến và cập nhật trạng thái chuyến.

### Actor
Driver / Customer

### Functional Requirement liên quan
- FR13: Chấp nhận chuyến
- FR14: Từ chối chuyến
- FR15: Cập nhật trạng thái chuyến
- FR16: Theo dõi trạng thái chuyến
- FR17: Xem thông tin tài xế
- FR18: Xem thời gian dự kiến đến

### Use Case liên quan
- UC03 - Theo dõi chuyến xe
- UC07 - Nhận/Từ chối chuyến xe
- UC08 - Cập nhật trạng thái chuyến xe


---

# TCX06 - Tính cước và thanh toán

### Mục tiêu
Kiểm tra hệ thống tính tiền và xử lý thanh toán.

### Actor
Customer

### Functional Requirement liên quan
- FR19: Tính số tiền phải trả
- FR20: Thanh toán tiền mặt
- FR21: Thanh toán điện tử
- FR22: Xử lý thanh toán thất bại

### Use Case liên quan
UC14 - Thanh toán chuyến xe

### Điều kiện kiểm thử
- Chuyến xe đã hoàn thành.
- Hệ thống đã xác định số tiền cần thanh toán.


---

# TCX07 - Thông báo và đánh giá

### Mục tiêu
Kiểm tra gửi thông báo và đánh giá tài xế sau chuyến.

### Actor
Customer / Driver

### Functional Requirement liên quan
- FR23: Gửi thông báo
- FR24: Xem lịch sử chuyến xe
- FR25: Đánh giá tài xế

### Use Case liên quan
- UC04 - Xem lịch sử chuyến xe
- UC05 - Đánh giá tài xế


---

# TCX08 - Quản lý vận hành

### Mục tiêu
Kiểm tra chức năng quản trị của nhân viên vận hành.

### Actor
Operations Staff

### Functional Requirement liên quan
- FR26 → FR33

### Use Case liên quan
- UC10
- UC11
- UC12
- UC13

### Điều kiện kiểm thử
- Nhân viên có quyền truy cập hệ thống.
