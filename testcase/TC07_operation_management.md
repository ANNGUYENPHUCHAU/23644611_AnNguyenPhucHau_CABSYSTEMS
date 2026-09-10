# TC07 - Operation Management Test Case

## Business Process

BP08 - Quản lý vận hành

## Requirement Coverage

FR26-FR33

## UC

UC10, UC11, UC12, UC13

## Business Rule

Chức năng quản trị phải được kiểm soát quyền truy cập.

## Test Scenario

### TS01 - Quản lý dữ liệu vận hành

  Test Case ID   Input                              Expected Output
  -------------- ---------------------------------- ------------------------
  TC07_01        Staff có quyền truy cập Customer   Trả danh sách Customer
  TC07_02        Staff không có quyền               API 403 Forbidden

### TS02 - Giám sát chuyến xe

  Test Case ID   Input                   Expected Output
  -------------- ----------------------- ----------------------------
  TC07_03        tripId đang hoạt động   Hiển thị trạng thái chuyến
  TC07_04        transactionId hợp lệ    Trả lịch sử giao dịch
