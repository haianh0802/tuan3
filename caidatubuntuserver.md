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





