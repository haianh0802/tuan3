# Cài đặt Mariadb
Tiến hành Update hệ thống

sudo apt -y upgrade

Cài đặt MariaDB

sudo apt install -y software-properties-common mariadb-server mariadb-client

Khởi động dịch vụ MariaDB

systemctl start mariadb
systemctl enable mariadb

Kiểm tra trạng thái của MariaDB

systemctl status mariadb

![image](https://user-images.githubusercontent.com/101684058/160345445-29d081b2-1346-4c91-88c0-5638928d1624.png)


# Cấu hình và thao tác cơ bản với MariaDB
1 Cấu hình ban đầu cho MariaDB

Cho phép cải thiện khả năng bảo mật với lệnh sau :

mysql_secure_installation

![image](https://user-images.githubusercontent.com/101684058/160349690-6bda9a83-3afa-4b48-8d8f-72fca37d8d53.png)

1.Bấm Enter để tiếp tục.
2. Nhập vào y để tạo mật khẩu root mới cho MariaDB. Sau đó hãy nhập vào mật khẩu mà bạn sẽ sử dụng cho user root khi đăng nhập mariaDB
3. Nhập y để xóa user mặc định
4. Nhập vào n vì mình muốn có thể truy cập mariadb từ xa.
5. Nhập y để xóa cơ sở dữ liệu test và xóa truy cập vào nó.
6. Nhập y để tải lại bảng đặc quyền ngay lúc này.


Sau khi cấu hình ban đầu cho MariDB, ta truy cập vào cơ sở dữ liệu bằng user root và mật khẩu vừa tạo và thao tác với cơ sở dữ liệu :

mysql -u root -p

Sau đó nhập vào mật khẩu cho root. Ta sẽ truy cập được vào MariaDB như sau :


![image](https://user-images.githubusercontent.com/101684058/160349518-23517e08-cf2f-4d8c-a156-843153e57631.png)

2 Thao tác cơ bản với MariaDB
Các thao tác cơ bản với cơ sở dữ liệu :
Để xem các bảng cơ sở dữ liệu có sẵn trong MariaDB như sau :

show databases;

![image](https://user-images.githubusercontent.com/101684058/160350244-ecbbb031-a353-488d-9153-c4021fd6e4bc.png)

Để tạo 1 cơ sở dữ liệu mới , thực hiện câu lệnh sau :

create database <Tên cơ sở dữ liệu>;

![image](https://user-images.githubusercontent.com/101684058/160350679-d68e6eaf-a49d-4895-9322-f06d7865e56d.png)


# Cài đặt MySQL trên Ubuntu 20.04
Bước 1 - Cài đặt MySQL
Trên Ubuntu 20.04, bạn có thể cài đặt MySQL bằng cách sử dụng kho lưu trữ gói APT. Tại thời điểm viết bài này, phiên bản MySQL có sẵn trong kho lưu trữ Ubuntu mặc định là phiên bản 8.0.19.

Để cài đặt nó, hãy cập nhật chỉ mục gói trên máy chủ, nếu gần đây bạn chưa làm như vậy:

sudo apt update

Sau đó cài đặt gói mysql-server:

sudo apt install mysql-server
Thao tác này sẽ cài đặt MySQL, nhưng sẽ không nhắc bạn đặt mật khẩu hoặc thực hiện bất kỳ thay đổi cấu hình nào khác.

Bước 2 - Cấu hình MySQL
Đối với các bản cài đặt mới của MySQL, bạn sẽ muốn chạy script bảo mật đi kèm của DBMS. Script này thay đổi một số tùy chọn mặc định kém bảo mật hơn cho những thứ như thông tin đăng nhập root từ xa và người dùng mẫu.

Chạy script bảo mật với sudo:

sudo mysql_secure_installation

![image](https://user-images.githubusercontent.com/101684058/160370235-bd1a86dd-3753-476d-ae0b-95b5ee019800.png)

Nhập mật khẩu mới vào, rồi nhập Y.
Khi script hoàn tất, cài đặt MySQL sẽ được bảo mật. Bây giờ, bạn có thể chuyển sang tạo người dùng cơ sở dữ liệu chuyên dụng với MySQL client.

Bước 3 - Tạo người dùng MySQL chuyên dụng và cấp các đặc quyền

gọi mysql với đặc quyền sudo để có quyền truy cập vào người dùng MySQL root:

sudo mysql

![image](https://user-images.githubusercontent.com/101684058/160371169-54ff1807-5d26-40f1-8b46-600c26156b32.png)

Tạo database 

![image](https://user-images.githubusercontent.com/101684058/160551727-1dce7659-ca18-43ed-a6dc-0b92d6ab21d4.png)

### Các bước cài đặt LAMP trên Ubuntu
Bước 1: Cập nhật gói phần mềm
Trước khi cài đặt  LAMP, bạn nên cập nhật gói phần mềm và kho lưu trữ. Chạy các lệnh sau trên hệ điều hành Ubuntu 20.04:

sudo apt update 

sudo apt upgrade

Bước 2: Cài đặt Apache Web Server
Nhập lệnh sau để cài đặt Apache Web server. Gói apache2-utils sẽ cài đặt một số tiện ích hữu ích như công cụ benchmark Apache HTTP server.

sudo apt install -y apache2 apache2-utils


Sau khi được cài đặt, Apache sẽ tự động được khởi động. Kiểm tra trạng thái của nó với systemctl.

systemctl status apache2

![image](https://user-images.githubusercontent.com/101684058/160526437-ff54fc4f-01e9-4acc-aece-d8f15c9d94f2.png)

Kiểm tra phiên bản Apache:

apache2 -v

![image](https://user-images.githubusercontent.com/101684058/160526801-f87aee7a-6399-4968-a9ce-6d325278662f.png)



![image](https://user-images.githubusercontent.com/101684058/160530570-4e868515-39f8-4796-9628-9e8425ae7b90.png)



# Cài đặt php
Bước 1: Thêm PHP PPA

Chạy lệnh sau để thêm kho lưu trữ PHP ondrej vào hệ thống Ubuntu của bạn.

sudo apt install software-properties-common
sudo add-apt-repository ppa:ondrej/php -y

![image](https://user-images.githubusercontent.com/101684058/160731892-1d740385-dd4a-4acf-a09f-bb84658450c5.png)

Cập nhật apt

![image](https://user-images.githubusercontent.com/101684058/160732086-5f441034-33c3-403b-a608-d49daa43cf82.png)

Cài đặt php

sudo apt install -y php7.3

Bước 3: Xem phiên bản hoạt động hiện tại

![image](https://user-images.githubusercontent.com/101684058/160732529-bb1401a2-4794-4ccf-bbeb-799358716d76.png)

Bước 4: Cài đăth php Modul







