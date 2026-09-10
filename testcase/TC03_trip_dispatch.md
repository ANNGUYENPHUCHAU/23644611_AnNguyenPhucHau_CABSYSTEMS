# TC03 - Trip Dispatch Test Case

## Business Process

BP03 - Đặt chuyến và tìm tài xế

## Requirement Coverage

FR07, FR08, FR09, FR10, FR11, FR12

## UC

UC02 - Đặt chuyến xe UC07 - Nhận/Từ chối chuyến xe

## Business Rule

-   BRL01: Chỉ tài xế sẵn sàng mới được xem xét nhận chuyến.
-   BRL02: Tài xế phải phù hợp yêu cầu chuyến.
-   BRL03: Tài xế từ chối thì tiếp tục tìm tài xế khác.
-   BRL04: Tài xế không phản hồi thì tiếp tục tìm tài xế khác.
-   BRL05: Không tìm được tài xế phải thông báo khách hàng.

## Test Scenario

### TS01 - Tạo yêu cầu đặt chuyến

  -----------------------------------------------------------------------
  Test Case ID            Input                   Expected Output
  ----------------------- ----------------------- -----------------------
  TC03_01                 customerId,             API 201, tạo Trip
                          pickupLocation,         
                          destination,            
                          vehicleType hợp lệ      

  TC03_02                 pickupLocation=null     API 400

  TC03_03                 vehicleType không tồn   API 400
                          tại                     
  -----------------------------------------------------------------------

### TS02 - Tìm tài xế

  Test Case ID   Input                    Expected Output
  -------------- ------------------------ ---------------------
  TC03_04        driverStatus=AVAILABLE   Chọn Driver phù hợp
  TC03_05        driverStatus=BUSY        Không chọn Driver

### TS03 - Xử lý từ chối/timeout

  Test Case ID   Input                    Expected Output
  -------------- ------------------------ ---------------------------------
  TC03_06        driverAction=REJECT      Tìm Driver khác
  TC03_07        driverResponse=TIMEOUT   Tìm Driver khác
  TC03_08        availableDriver=0        Thông báo không tìm được tài xế
