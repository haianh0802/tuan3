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

6. Show Database
Để hiển thị tất cả database bạn sử dụng lệnh show databases. Với lệnh này bạn sẽ thấy tất cả các database hiện có.

`show databases;`

![image](https://user-images.githubusercontent.com/101684058/160969984-3839ac5b-9157-4c2d-8d7e-a59f23cff17f.png)

7. Truy cập vào Database
Để truy cập vào một database nào đó. Bạn sử dụng use ten-database để truy cập vào

` use test;`

8. Tạo Table cho Database

![image](https://user-images.githubusercontent.com/101684058/160970527-91b86f06-9793-47cf-a221-04f3018475ff.png)


9. Show Table Database

`show tables;`

![image](https://user-images.githubusercontent.com/101684058/160970696-41333eec-eb78-4552-8346-8c66a03e38fc.png)

10. Kiểm tra các trường trong bảng

`desc user;`

![image](https://user-images.githubusercontent.com/101684058/160970849-495f4fe2-76de-443f-af40-a5a7fe54c716.png)


11. Chèn dữ liệu vào trong bảng

![image](https://user-images.githubusercontent.com/101684058/160971486-fed4ab1d-2304-49cc-bed1-815e321ec666.png)

![image](https://user-images.githubusercontent.com/101684058/160971616-2519d890-7171-4055-aa01-304bb2ca3f56.png)

12. Lệnh thêm mới cột trong bảng
Cú pháp chung để thêm mới cột như sau:

`ALTER TABLE table_name ADD column_name column_definition;`

![image](https://user-images.githubusercontent.com/101684058/160972268-770ebfc9-3a12-4935-aeef-c158deeba0c5.png)

13.  Lệnh đổi tên cột trong bảng
Sau đây là cú pháp chung để đổi tên cột như sau:
`ALTER TABLE table_name CHANGE COLUMN old_column new_column VARCHAR(25)`

![image](https://user-images.githubusercontent.com/101684058/160973062-c9f6825e-bf68-4e53-ad1c-10d451e55cf8.png)

14. Lệnh xóa cột trong MariaDB
Cú pháp chung để xóa cột như sau:
`ALTER TABLE table_name DROP COLUMN column_name;`

![image](https://user-images.githubusercontent.com/101684058/160973199-798991b2-bc4b-4255-8b90-eb2d303c2df0.png)

15. Lệnh thay đổi cột kiểu dữ liệu cột trong bảng
Cú pháp chung để thay đổi kiểu dữ liệu cột như sau:

`ALTER TABLE table_name MODIFY column_name VARCHAR(50);`

![image](https://user-images.githubusercontent.com/101684058/160973424-01e2921b-69eb-46bb-9e1a-47895d8de6fa.png)



