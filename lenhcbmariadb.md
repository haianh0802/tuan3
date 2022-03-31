# Kết nối tới MariaDB
1. Để kết nối tới MariaDB, chúng ta sử dụng mysql client tool

`mysql -u root -p`

![image](https://user-images.githubusercontent.com/101684058/160968392-c4b0acd2-c342-4fd0-8de0-83d9a27fc478.png)


2. Để đổi mật khẩu tài khoản root sử dụng lệnh sql sau:

`MariaDB [(none)]> SET PASSWORD FOR 'root'@'localhost' = PASSWORD('MatKhau');`

3. Tạo Database
Để tạo database ta sử dụng câu lệnh:
` CREATE DATABASE test;`

![image](https://user-images.githubusercontent.com/101684058/160969014-d29b755f-8d80-40f9-907d-74cfcaf61c18.png)

4. Tạo User Password
Tạo User và password cho user bạn nhập vào dòng lệnh:

`CREATE USER 'database'@'localhost' IDENTIFIED BY 'my-password'; `

![image](https://user-images.githubusercontent.com/101684058/160969362-d840cf88-92a5-4770-9f97-ab5ad4292ff3.png)

5. Gán quyền User Database

Khi đã tạo database và user xong bạn sẽ cần gán quyền để thực thi các truy vấn. Để gán bạn sử dụng cú pháp sau.
GRANT ALL PRIVILEGES ON test.* TO 'test'@'localhost';

![image](https://user-images.githubusercontent.com/101684058/160969740-8cb828fc-70fd-4f74-bf84-6930807dcbbc.png)
