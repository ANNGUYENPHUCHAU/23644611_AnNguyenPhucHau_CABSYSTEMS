# TC05 - Payment Test Case

## Business Process

BP05 - Tính cước và thanh toán

## Requirement Coverage

FR19, FR20, FR21, FR22

## UC

UC14 - Thanh toán chuyến xe

## Business Rule

-   Không lưu thông tin thanh toán nhạy cảm.
-   Thanh toán lỗi phải cho phép xử lý lại.

## Test Scenario

### TS01 - Tính cước

  Test Case ID   Input                              Expected Output
  -------------- ---------------------------------- ----------------------
  TC05_01        trip completed, trip data hợp lệ   Trả số tiền phải trả

### TS02 - Thanh toán

  -----------------------------------------------------------------------
  Test Case ID            Input                   Expected Output
  ----------------------- ----------------------- -----------------------
  TC05_02                 method=CASH             Ghi nhận thanh toán

  TC05_03                 method=ONLINE,          Payment Success
                          transaction success     

  TC05_04                 method=ONLINE,          Thông báo lỗi và cho
                          transaction failed      retry

  TC05_05                 amount=null             API 400 Bad Request
  -----------------------------------------------------------------------
