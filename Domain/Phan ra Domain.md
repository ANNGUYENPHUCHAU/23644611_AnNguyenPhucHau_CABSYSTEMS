| **Bounded Context** | **Use Case liên quan** | **Năng lực nghiệp vụ** | **Khái niệm chính** |
|---|---|---|---|
| **Identity & Access** | UC01, UC06; hỗ trợ UC10–UC13 | Xác thực người dùng, đăng nhập và kiểm soát quyền truy cập theo loại người dùng. | Account, Credential, Authentication, Role, Access Token |
| **Customer Profile** | UC01, UC10 | Quản lý thông tin hồ sơ khách hàng; cho phép khách hàng cập nhật hồ sơ và nhân viên vận hành quản lý thông tin khách hàng theo quyền. | Customer, CustomerProfile |
| **Driver Profile** | UC06, UC11 | Quản lý hồ sơ tài xế; cho phép tài xế cập nhật thông tin và nhân viên vận hành quản lý thông tin tài xế. | Driver, DriverProfile |
| **Vehicle Management** | UC06, UC11 | Quản lý thông tin phương tiện gắn với tài xế. | Vehicle, VehicleType, LicensePlate, DriverID |
| **Driver Availability** | UC06, UC07, UC12 | Quản lý trạng thái hoạt động của tài xế và xác định tài xế có sẵn sàng nhận chuyến hay không. | DriverAvailability, READY, BUSY, OFFLINE |
| **Booking** | UC02 | Tiếp nhận yêu cầu đặt xe gồm điểm đón, điểm đến và loại xe; tạo yêu cầu chuyến trước khi điều phối tài xế. | Booking, PickupLocation, Destination, VehicleType |
| **Dispatch & Matching** | UC02, UC07 | Tìm tài xế phù hợp, gửi yêu cầu nhận chuyến, xử lý tài xế nhận, từ chối hoặc không phản hồi và tiếp tục tìm tài xế khác. | Dispatch, DriverCandidate, TripRequest, Assignment, Acceptance |
| **Trip Lifecycle** | UC08, UC12 | Quản lý vòng đời thực hiện chuyến và các trạng thái: đã đến điểm đón, đã đón khách, đang di chuyển, hoàn thành. | Trip, TripStatus, Driver, Customer |
| **Driver Location** | UC09, UC03 | Tiếp nhận và lưu vị trí tài xế để hỗ trợ tìm tài xế và xác định thời gian dự kiến đến. | DriverLocation, Latitude, Longitude, RecordedAt |
| **Trip Tracking** | UC03, UC12 | Cung cấp trạng thái hiện tại của chuyến, tài xế được phân công và thời gian dự kiến tài xế đến. | TripTracking, TripStatus, AssignedDriver, ETA |
| **Fare Calculation** | UC14 | Xác định số tiền phải trả sau khi chuyến xe hoàn thành dựa trên loại dịch vụ và thông tin chuyến đi. | Fare, Trip, ServiceType, Amount |
| **Payment** | UC14 | Xử lý thanh toán tiền mặt hoặc điện tử; tiếp nhận kết quả từ nhà cung cấp thanh toán và hỗ trợ xử lý lại khi thanh toán điện tử thất bại. | Payment, PaymentMethod, PaymentStatus, PaymentProvider |
| **Transaction** | UC13, UC14 | Ghi nhận kết quả giao dịch thanh toán và cung cấp dữ liệu để nhân viên vận hành tra cứu lịch sử giao dịch. | Transaction, TransactionStatus, TransactionTime, Payment |
| **Notification** | UC02, UC07, UC08, UC14 | Gửi thông báo khi yêu cầu đặt xe được tiếp nhận, tài xế nhận chuyến, tài xế đến điểm đón, chuyến hoàn thành và thanh toán có kết quả. | Notification, Recipient, Event, NotificationStatus |
| **Trip History** | UC04 | Cung cấp lịch sử các chuyến đã thực hiện và số tiền phải trả cho khách hàng. | TripHistory, Trip, Fare, Customer |
| **Rating** | UC05 | Cho phép khách hàng đánh giá tài xế sau khi chuyến xe hoàn thành và lưu kết quả đánh giá. | Rating, RatingValue, Comment, Customer, Driver, Trip |
| **Operations Monitoring** | UC12 | Cho phép nhân viên vận hành xem các chuyến đang diễn ra, trạng thái chuyến, trạng thái tài xế và hỗ trợ theo dõi trường hợp chuyến gặp lỗi. | OperationsStaff, Trip, TripStatus, DriverStatus |
