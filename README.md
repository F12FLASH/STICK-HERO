# h5game

Đối với trò chơi io loại h5, khách hàng sử dụng phiên bản ts của trình tạo cocos. Máy chủ sử dụng khuôn khổ phân tán diễn viên golang và có thể được triển khai theo cách có thể mở rộng.
[địa chỉ demo demo] (http://magicsea.top:82/web-mobile/)

## Sự phụ thuộc của khách hàng

-cocos Creator 2.4.0

## Các sự cố đã biết của khách hàng:

-Sau khi nâng cấp công cụ, một số hộp nhập liệu được hiển thị không chính xác theo mặc định, và cần được xóa và định vị lại

-Sự thay đổi của công tắc làm cho hình đại diện không được hiển thị

## Phụ thuộc mã nguồn máy chủ

``
Gói quản lý Go mod đã được sử dụng.
golang phiên bản 1.13.
Các bước để kéo các phụ thuộc:
1. Nhập thư mục máy chủ / src / Server
2. Thực thi go mod gọn gàng
``

## Hoạt động của máy chủ

-Cài đặt redis cơ sở dữ liệu

-Nhập thư mục máy chủ và thực thi build.bat để biên dịch

-Configuration server / bin / config.json là địa chỉ cơ sở dữ liệu và địa chỉ cấu hình của cụm máy chủ
  
  ``
  "redis": {
        "addr": "127.0.0.1:6379",//redis address
        "password": "1111", // redis password, không điền nếu chưa đặt mật khẩu
        "poolize": 10,
        "dbs": [0,1,2,3,4]
    },
  "proto": "json", // Phương pháp đóng gói giao thức tham số thông báo, hỗ trợ protobuf, json
  ``

- khởi động
  
  ``
  các cửa sổ:
  Phương pháp 1: Chạy trực tiếp bin / server.exe
  Phương pháp 2: Thực thi StartSingleServer.bat (chế độ xử lý đơn)
  Phương pháp 3: Thực thi StartMultiServer.bat (chế độ đa quy trình)
      
  linux:
  Thực thi ./run.sh start
  ``
  
  ## LÀM:

- [x] Đăng nhập, trò chuyện, sửa đổi thông tin cá nhân, trận chiến cơ bản

- [x] quyền truy cập hành vi

- [x] tcp, giao thức websocket tương thích. pb, json là tùy chọn.

- [] Điện thoại di động giảm việc gửi gói tin, ứng dụng khách suôn sẻ

## QQ 群 ： 285728047