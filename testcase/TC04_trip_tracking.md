# TC04 - Trip Tracking Test Case

## Business Process

BP04 - Thực hiện và theo dõi chuyến xe

## Requirement Coverage

FR13, FR14, FR15, FR16, FR17, FR18

## UC

UC03, UC07, UC08

## Test Scenario

### TS01 - Driver cập nhật trạng thái chuyến

  Test Case ID   Input                 Expected Output
  -------------- --------------------- ---------------------
  TC04_01        status=ARRIVED        Cập nhật thành công
  TC04_02        status=PICKED_UP      Cập nhật thành công
  TC04_03        status=COMPLETED      Trip hoàn thành
  TC04_04        status không hợp lệ   API 400 Bad Request

### TS02 - Customer theo dõi chuyến

  Test Case ID   Input                  Expected Output
  -------------- ---------------------- ------------------------------------
  TC04_05        tripId hợp lệ          Trả trạng thái chuyến, driver, ETA
  TC04_06        tripId không tồn tại   API 404 Not Found
