# TC01 - Customer Account Test Case

## 1. Business Process

BP01 - Quản lý tài khoản khách hàng

## 2. Requirement Coverage

### FR

-   FR01: Đăng ký tài khoản khách hàng
-   FR02: Đăng nhập khách hàng
-   FR03: Cập nhật thông tin cá nhân

### UC

-   UC01: Đăng ký/Quản lý tài khoản khách hàng

### Business Rule

-   Người dùng phải được xác thực trước khi sử dụng chức năng yêu cầu
    tài khoản.

## 3. Test Scenario

### TS01 - Đăng ký tài khoản khách hàng

  -----------------------------------------------------------------------
  Test Case ID            Input                   Expected Output
  ----------------------- ----------------------- -----------------------
  TC01_01                 fullName=Nguyen Van A,  API 201 Created, tạo
                          email=a@gmail.com,      Customer thành công
                          password=Password@123   

  TC01_02                 email đã tồn tại        API 409 Conflict, thông
                                                  báo tài khoản đã tồn
                                                  tại

  TC01_03                 email=null              API 400 Bad Request,
                                                  yêu cầu nhập email

  TC01_04                 password rỗng           API 400 Bad Request
  -----------------------------------------------------------------------

### TS02 - Đăng nhập khách hàng

  Test Case ID   Input                       Expected Output
  -------------- --------------------------- ------------------------
  TC01_05        email đúng, password đúng   API 200, trả JWT token
  TC01_06        email đúng, password sai    API 401 Unauthorized
  TC01_07        customer không tồn tại      API 401 Unauthorized

### TS03 - Cập nhật thông tin cá nhân

  -----------------------------------------------------------------------
  Test Case ID            Input                   Expected Output
  ----------------------- ----------------------- -----------------------
  TC01_08                 cập nhật phone, email   API 200, thông tin được
                          hợp lệ                  cập nhật

  TC01_09                 email sai định dạng     API 400 Bad Request
  -----------------------------------------------------------------------
