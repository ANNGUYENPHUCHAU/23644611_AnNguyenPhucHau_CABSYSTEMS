# TC06 - Notification History Rating Test Case

## Business Process

BP06 - Thông báo BP07 - Lịch sử và đánh giá

## Requirement Coverage

FR23, FR24, FR25

## UC

UC04, UC05

## Business Rule

Chỉ đánh giá sau khi chuyến xe hoàn thành.

## Test Scenario

### TS01 - Gửi thông báo

  Test Case ID   Input                     Expected Output
  -------------- ------------------------- --------------------------
  TC06_01        trip accepted event       Customer nhận thông báo
  TC06_02        payment completed event   Gửi thông báo thanh toán

### TS02 - Đánh giá tài xế

  Test Case ID   Input                      Expected Output
  -------------- -------------------------- ---------------------
  TC06_03        rating=5, trip completed   Lưu đánh giá
  TC06_04        rating=0                   API 400 Bad Request
  TC06_05        trip chưa hoàn thành       Từ chối đánh giá
