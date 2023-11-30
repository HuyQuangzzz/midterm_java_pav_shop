# midterm_java_pav_shop
# PAV_SHOP
## Giới thiệu

Cửa hàng Java PAV giữa kỳ là một ứng dụng dựa trên Java được thiết kế để quản lý một cửa hàng gian hàng ảo. Dự án này nhằm mục đích cung cấp một nền tảng đơn giản nhưng hiệu quả để xử lý hàng tồn kho sản phẩm, hoạt động bán hàng và tương tác với khách hàng. Nó được phát triển như một phần của dự án giữa kỳ nhằm chứng minh ứng dụng thực tế của các kỹ năng lập trình Java.
Dự án PAV Shop bao gồm một số tính năng chính:

-Quản lý sản phẩm: Cho phép thêm, xóa, sửa đổi chi tiết sản phẩm.
-Theo dõi hàng tồn kho: Theo dõi mức tồn kho và đưa ra cảnh báo về lượng hàng tồn kho thấp.

-Xử lý đơn hàng: Tạo điều kiện thuận lợi cho việc xử lý đơn đặt hàng của khách hàng, bao gồm tạo, sửa đổi và theo dõi đơn hàng.
Giao diện người dùng:

-Giao diện thân thiện với người dùng cho cả khách hàng và quản trị viên.

-Tích hợp cơ sở dữ liệu: Sử dụng cơ sở dữ liệu để lưu trữ và quản lý dữ liệu một cách hiệu quả.
Báo cáo: Tạo báo cáo về doanh số bán hàng, hàng tồn kho và hoạt động của khách hàng.

## Cấu trúc source code
![Screenshot 2023-11-30 194501](https://github.com/HuyQuangzzz/midterm_java_pav_shop/assets/147068105/356769ea-38e8-4e00-b01d-29ded616adb5)


## ERD
![Screenshot 2023-11-30 113848](https://github.com/HuyQuangzzz/midterm_java_pav_shop/assets/147068105/a217d008-a0f6-4630-a799-e2c2d9c9412b)




## Yêu cầu hệ thống

- Java JDK 11 trở lên
- IntelliJ IDEA
- Visual Studio Code
- Docker hoặc XAMPP
## Cài đặt và chạy dự án:
**1. Thiết Lập Cơ Sở Dữ Liệu**
- Sử dụng Docker hoặc XAMPP để tạo một MySQL server.
- Tạo cơ sở dữ liệu pav_shop bằng cách chạy script pav_shop.sql.
**2. Chạy Backend**
Clone the Repository: git clone https://github.com/HuyQuangzzz/midterm_java_pav_shop.git
- Cấu hình kết nối cơ sở dữ liệu trong file application.yml, mật khẩu để kết nối hiện tại là "abc123".
- Mở thư mục cara bằng IntelliJ IDEA và chạy file PavShopApplication.java.
- tài khoản user:   tk:user  pass: 123456
- tài khoản admin:  tk:admin123 pass: 123123

## Một số hình ảnh của PAV_SHOP

-Trang chủ pav_shop
![Screenshot 2023-11-30 195955](https://github.com/HuyQuangzzz/midterm_java_pav_shop/assets/147068105/ad39e1f6-13e6-4124-bb8d-e661733e30b2)

-Trang thanh toán 
![Screenshot 2023-11-30 200941](https://github.com/HuyQuangzzz/midterm_java_pav_shop/assets/147068105/a63839c2-1ba5-4d41-aa41-969662e5b403)
![Screenshot 2023-11-30 200954](https://github.com/HuyQuangzzz/midterm_java_pav_shop/assets/147068105/8f793763-45aa-486a-bddc-ade0286950bf)

-Trang sản phẩm 
![Screenshot 2023-11-30 201203](https://github.com/HuyQuangzzz/midterm_java_pav_shop/assets/147068105/c029743e-1e57-4dda-8779-4f16b6372adb)

-Trang quản lí thể loại
![Screenshot 2023-11-30 201342](https://github.com/HuyQuangzzz/midterm_java_pav_shop/assets/147068105/c6e8594e-b17b-4fab-9cdf-71690e792284)

-Trang quản lí sản phẩm 
![Screenshot 2023-11-30 201425](https://github.com/HuyQuangzzz/midterm_java_pav_shop/assets/147068105/1aa84a56-0e14-4848-b9ca-20348790824c)

-Trang quản lí nhãn hiệu 
![Screenshot 2023-11-30 201401](https://github.com/HuyQuangzzz/midterm_java_pav_shop/assets/147068105/c45f284a-332b-4553-ad87-6fadb6b09a73)

-Trang quản lí đơn hàng 
![Screenshot 2023-11-30 201456](https://github.com/HuyQuangzzz/midterm_java_pav_shop/assets/147068105/d54671a3-6307-4296-9795-f81ee0c26406)

-Trang quản lí khách hàng
![Screenshot 2023-11-30 201515](https://github.com/HuyQuangzzz/midterm_java_pav_shop/assets/147068105/b9d7e8e5-214b-461f-b6e2-5ace447e83b2)


## API Reference

#### Admin
- add  product

Endpoint: /admin/products/add

Method: POST

Data Params:

    name [string]
    description [string]
    price [float]
    stock [integer]

Success Response:
```json
{
    "name": "Coffee Mug",
    "description": "A large coffee mug.",
    "price": 12.99,
    "stock": 100
}
```
```json
{
    "productId": 201,
    "message": "Product added successfully."
}
```
- update  product

Endpoint: /admin/products/add

Method: POST

Data Params:

    name [string, optional]
    description [string, optional]
    price [float, optional]
    stock [integer, optional]

Success Response:
```json
{
  "name": "Large Coffee Mug",
  "description": "An extra-large coffee mug.",
  "price": 14.99,
  "stock": 150
}
```
```json
{
  "message": "Product updated successfully."
}
```
- delete  product

Endpoint: /admin/products/delete/{productId}

Method: DELETE

URL Params:

    productId [integer]



```json
{
  "message": "Product deleted successfully."
}

```
URL Params: 'productId=123'

- Login

Endpoint:/users/login

Method: POST

Data Params:

    username [string]
    password [string]
    email [string]

Success Response:
```json
{
  "username": "existinguser",
  "password": "password123"
}
```
```json
{
  "accessToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...",
  "userId": 101
}
```
- Signup

Endpoint:/users/signup

Method: POST

Data Params:

    username [string]
    password [string]
    email [string]

Success Response:
```json
{
    
  
  "username": "newuser",
  "password": "password123",
  "email": "newuser@example.com"
}
```
```json
{
  "userId": 101,
  "message": "User registered successfully."
}

```
-  Place an Order

Endpoint:/orders/place

Method:POST

Data Params:

    userId [integer]
    items [array of { productId, quantity }]

Payload
```json
{
  "userId": 101,
  "items": [
    {
      "productId": 123,
      "quantity": 2
    },
    {
      "productId": 124,
      "quantity": 1
    }
  ]
}
```
Success Response:
```json
{
  "orderId": 301,
  "message": "Order placed successfully."
}

```
-  Place an Order

Endpoint:/orders/place

Method:POST

Data Params:

    userId [integer]
    items [array of { productId, quantity }]

Payload
```json
{
  "userId": 101,
  "items": [
    {
      "productId": 123,
      "quantity": 2
    },
    {
      "productId": 124,
      "quantity": 1
    }
  ]
}
```
Success Response:
```json
{
  "orderId": 301,
  "message": "Order placed successfully."
}

```
- View order detail

Endpoint:/orders/{orderId}

Method:GET

Data Params:

    orderId [integer]


Success Response:
```json
{
  "order": {
    "orderId": 301,
    "items": [
      {
        "productId": 401,
        "quantity": 2
      }
      // ... other items
    ],
    "totalPrice": 59.98,
    "status": "Processing"
  }
}

```
- View List Users

Endpoint:/admin/users

Method:GET

Data Params:

    orderId [integer]


Success Response:
```json
{
  "users": [
    {
      "userId": 501,
      "username": "johndoe",
      "email": "john@example.com"
    },
    // ... other users
  ]
}

```
- Update User Information

Endpoint:/admin/users/update/{userId}

Method:PUT
URL Params:
    userId [integer]
Data Params:

    username [string, optional]
    email [string, optional]

No payload required for GET request

Success Response:
```json
{
  "users": [
    {
      "userId": 501,
      "username": "johndoe",
      "email": "john@example.com"
    },
    // ... other users
  ]
}

```
- Delete User 

Endpoint: /admin/users/delete/{userId}

Method: DELETE
URL Params:
    userId [integer]




Success Response:
```json
{
  "message": "User deleted successfully."
}


```
