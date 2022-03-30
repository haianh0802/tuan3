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
Sử dụng lệnh sau để tìm kiếm các modules PHP 7 có sẵn trong kho lưu trữ.

sudo apt-cache search php7*

Bước 5 – Chuyển đổi giữa các phiên bản PHP
Bạn có thể sử dụng lệnh update-alternatives để chuyển đổi giữa các phiên bản PHP.

update-alternatives --config php

1.5. Bước 5: Cấu hình PHP Module
Sau khi cài đặt php hãy kích hoạt module Apache php7.4 sau đó khởi động lại máy chủ Web Apache.
![image](https://user-images.githubusercontent.com/101684058/160733551-16acd6ae-a56a-4ffe-ba1a-1a61be8df131.png)

Để kiểm tra các tập lệnh PHP với máy chủ Apache, chúng ta cần tạo một tệp info.php trong thư mục /var/www/html.

Hướng dẫn sử dụng Nano Editor trên Linux
sudo nano /var/www/html/info.php
Dán mã PHP sau vào tệp.

<?php phpinfo(); ?>

Bây giờ trong thanh địa chỉ của trình duyệt, nhập server-ip-address/info.php. Thay thế địa chỉ server-ip-address bằng IP thực tế của bạn. Nếu bạn làm theo hướng dẫn này trên máy tính của mình, hãy nhập 127.0.0.1/info.php hoặc localhost/info.php.

![image](https://user-images.githubusercontent.com/101684058/160735574-df0278e0-a464-431b-8946-a0bea8658382.png)

2. Chạy PHP-FPM với Apache (Tuỳ chọn)
Về cơ bản có hai cách để chạy mã PHP với máy chủ web Apache:

Apache PHP module
PHP-FPM.
Trong các bước trên, modules Apache PHP7.3 được sử dụng để xử lý mã PHP. Tuy nhiên trong một số trường hợp, bạn cần chạy mã PHP bằng PHP-FPM. Để làm điều này hãy làm theo các bước sau.

Vô hiệu hóa mô-đun Apache PHP7.3.

![image](https://user-images.githubusercontent.com/101684058/160738853-268812cb-0d50-4c7d-adf6-56b0f724e32b.png)

Cài đặt PHP-FPM.

sudo apt install php7.3-fpm -y


Kích hoạt mô-đun proxy_fcgi và setenvif.

![image](https://user-images.githubusercontent.com/101684058/160739199-7613a603-e6a2-46ce-a063-16bec5cbbfb8.png)

Kích hoạt tệp cấu hình /etc/apache2/conf-available/php7.3-fpm.conf.
![image](https://user-images.githubusercontent.com/101684058/160739327-ade210ba-b35d-4b51-a492-0faa5532d384.png)

Khởi động lại Apache để các thay đổi có hiệu lực.

![image](https://user-images.githubusercontent.com/101684058/160739813-570e1f37-3d87-4833-998c-592aeb46c758.png)

Bây giờ truy cập lại trang info.php trong trình duyệt của mình, bạn sẽ thấy API máy chủ được thay đổi từ Apache 2.0 Handler thành FPM / FastCGI, có nghĩa là máy chủ web Apache sẽ chuyển các yêu cầu PHP sang PHP-FPM.

![image](https://user-images.githubusercontent.com/101684058/160739786-f3dbcae8-d441-417d-a24d-450a66e49689.png)

# cài đặt phpMyAdmin
phpMyAdmin có sẵn trong kho phần mềm Ubuntu 20.04. vì vậy chúng ta có thể dễ dàng cài đặt nó bằng lệnh bên dưới.

![image](https://user-images.githubusercontent.com/101684058/160740943-fadb4d98-8b9b-4904-8676-312af5d763e3.png)
![image](https://user-images.githubusercontent.com/101684058/160741070-3de6a49e-e403-4ae5-8030-d84b1c921089.png)

Lệnh trên sẽ cài đặt tất cả các thành phần cần thiết bao gồm các phần mở rộng PHP7. Trong quá trình cài đặt, nó sẽ nhắc bạn chọn một máy chủ web để cấu hình
![image](https://user-images.githubusercontent.com/101684058/160741252-4ec76ecf-b93c-42d8-a3ee-ac8f11e96c4a.png)

Trong màn hình tiếp theo, chọn Yes để định cấu hình cơ sở dữ liệu cho phpMyAdmin với dbconfig-common.
![image](https://user-images.githubusercontent.com/101684058/160741431-a764ae9c-3135-40b0-8fc9-5d92539c2860.png)

Đặt mật khẩu cho người dùng

![image](https://user-images.githubusercontent.com/101684058/160741557-d2a171aa-a830-4226-9782-773169c1127a.png)

Xác nhận mật khẩu 1 lần nữa
![image](https://user-images.githubusercontent.com/101684058/160741706-43eacbd5-f30c-439f-a0df-bc080385eb9f.png)



![image](https://user-images.githubusercontent.com/101684058/160742553-67c105ec-68e0-41ba-8db4-bbd7b22a4843.png)

![image](https://user-images.githubusercontent.com/101684058/160742679-79ff0f10-5b10-4c8a-8b70-b8b04151c6ca.png)

![image](https://user-images.githubusercontent.com/101684058/160742799-d6b8bdf8-0f9b-4400-8bf5-7a4b071dd6aa.png)





