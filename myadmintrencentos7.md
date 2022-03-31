# 1. Caì đặt Apache trên Centos 7
Bước 1: Cài đặt Apache
Để cài đặt Apache hãy chạy lệnh sau:
`yum install httpd -y`
Bước 2: Khởi động Apache
`systemctl enable httpd`
`systemctl start httpd`

![image](https://user-images.githubusercontent.com/101684058/161010633-e61f86af-8e7f-49cf-877a-c950fe3d6c8a.png)

Để kiểm tra trạng thái của Apache hãy sử dụng lệnh sau:

`systemctl status httpd`

![image](https://user-images.githubusercontent.com/101684058/161010795-a33c4319-729c-4cd2-8944-84c9214bb2d8.png)

 Cấu hình Firewalld (Nếu có)

`firewall-cmd --permanent --zone=public --add-service=http`
`firewall-cmd --permanent --zone=public --add-service=https`
`firewall-cmd --reload`

![image](https://user-images.githubusercontent.com/101684058/161017613-013eb4c2-b0ed-44c0-8d1c-a910f64d714f.png)

Và trình duyệt sẽ hiển thị giao diện mặc định trang web CentOS 7 Apache:

![image](https://user-images.githubusercontent.com/101684058/161019269-50a66b3b-7afa-4913-853a-9548b179022a.png)


Bước 3: Thiết lập quy trình hoạt động cho Apache
Sau khi cài đặt, bạn cần thiết lập quy trình hoạt động và chạy cho Apache trên CentOS 7. Bạn có thể sử dụng một số lệnh cơ bản sau đây:

Muốn dừng máy chủ web, hãy nhập lệnh sau:

`sudo systemctl stop httpd`
Khởi động lại máy chủ bằng lệnh:

`sudo systemctl start httpd`
Để dừng và bắt đầu lại dịch vụ trên server, hãy nhập:

`sudo systemctl restart httpd`
Nếu bạn chỉ cần thay đổi cấu hình, Apache sẽ có thể tự tải lại và không làm mất kết nối, lệnh đó được dùng như sau:

`sudo systemctl reload httpd`
Apache được cấu hình mặc định có thể tự khởi động khi máy chủ được khởi động. Nếu như không muốn điều này, bạn có thể tắt chức năng đó bằng cách dùng lệnh:

`sudo systemctl disable httpd`
Trong trường hợp đã tắt chức năng tự khởi động nhưng muốn bật lại, hãy dùng lệnh:

`sudo systemctl enable httpd`
Cấu hình mặc định của Apache trên CentOS 7 sẽ cho phép nó lưu trữ cho một trang web duy nhất.

Bước 4: Cấu hình virtual server (Vhost)
Cách tạo folder virtual server
Để tạo folder cho tên miền example.com, hãy sử dụng lệnh:
