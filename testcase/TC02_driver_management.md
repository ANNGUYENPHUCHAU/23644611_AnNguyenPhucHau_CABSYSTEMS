# TC02 - Driver Management Test Case

## Business Process

BP02 - Quản lý tài xế và phương tiện

## Requirement Coverage

FR04, FR05, FR06 UC06 - Quản lý tài khoản và phương tiện tài xế

## Business Rule

BRL01: Chỉ tài xế sẵn sàng mới được xem xét nhận chuyến.

## Test Scenario

### TS01 - Quản lý hồ sơ tài xế

  Test Case ID   Input                             Expected Output
  -------------- --------------------------------- ---------------------
  TC02_01        driverName, phone, email hợp lệ   Cập nhật thành công
  TC02_02        phone=null                        API 400 Bad Request
  TC02_03        email sai format                  API 400 Bad Request

### TS02 - Quản lý phương tiện

  -----------------------------------------------------------------------
  Test Case ID            Input                   Expected Output
  ----------------------- ----------------------- -----------------------
  TC02_04                 vehicleType=CAR,        Lưu phương tiện thành
                          licensePlate hợp lệ     công

  TC02_05                 licensePlate=null       Báo lỗi validation
  -----------------------------------------------------------------------

### TS02 - Cập nhật trạng thái hoạt động

  Test Case ID   Input                  Expected Output
  -------------- ---------------------- --------------------------------
  TC02_06        status=AVAILABLE       Cập nhật trạng thái thành công
  TC02_07        status không tồn tại   API 400 Bad Request
