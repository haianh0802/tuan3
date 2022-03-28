# Cơ sở dữ liệu là gì?
Cơ sở dữ liệu là từ được sử dụng phổ biến trong các lĩnh vực thuộc công nghệ thông tin, dữ liệu, thiết lập và phần mềm… .Database là cơ sở dữ liệu, là một bộ sưu tập được tổ chức hiển thị bản và thường access from the system computer or current under the format file in the database management. Cơ sở dữ liệu có thể được lưu trữ trên thiết bị có bộ nhớ chức năng như: thẻ nhớ, đĩa cứng, CD…
# Đặc điểm của database
Đặc điểm của database (cơ sở dữ liệu) chính là có thể truy xuất thông tin, dữ liệu theo nhiều cách khác nhau, thông tin từ cơ sở dữ liệu được đảm bảo nhất và toàn vẹn dữ liệu, không hề có sự trùng lặp thông tin, nếu có thì tỷ lệ rất thấp. Một cơ sở dữ liệu database có thể có nhiều người sử dụng cùng một lúc.

![image](https://user-images.githubusercontent.com/101684058/160313778-b85f0b71-3cd6-4eaa-b7b2-ee487bf2ddb6.png)

Như vậy từ đặc điểm của cơ sở dữ liệu database ta có thể thấy nó có nhiều ưu điểm và hạn chế nhất định:

Về mặt ưu điểm của cơ sở dữ liệu database đó chính là nhờ vào việc thông tin lưu trữ không bị trùng lặp giúp đảm bảo tính thông nhất cũng như toàn vẹn của dữ liệu. Nhờ việc không bị trùng lặp giúp giảm thời gian xử lý dữ liệu, cũng như tránh khỏi những sai sót trong quá trình kiểm tra cơ sở dữ liệu database. Ngoài ra, nhờ vào việc có thể truy xuất từ các cách khác nhau nên nhiều người có thể sử dụng cơ sở dữ liệu cùng một lúc mà không phải qua các khâu rườm rà phức tạp. Từ đó tạo điều kiện thuận lợi cho việc  sử dụng, quản lý, truy cập dữ liệu,… Bên cạnh đó cơ sở dữ liệu database cũng có thể được lưu trữ dưới nhiều dạng khác nhau như ổ cứng, usb hay đĩa CD.

Tuy vậy, cơ sở dữ liệu database cũng có những hạn chế nhất định,vì nhiều người chung quyền sử dụng, khai thác cơ sở dữ liệu, nên chủ quyền của người người sử dụng khác nhau có thể bị xâm phạm, ngoài ra vấn đề bảo mật cũng thực sự đáng quan tâm khi mà ai cũng có thể xâm nhập vào cơ sở dữ liệu database, từ đó dẫn đến nguy cơ bị tấn công, đánh cắp dữ liệu. Điều này thường gặp nhiều nhất ở các công ty cung cấp hosting dùng chung, sau khi lập trình web, thiết kế website xong thì người ta thường hay đặt website của mình lên các hosting này vì giá thành rẻ, nhưng đó lại là điểm yếu, chỉ cần một cơ sở dữ liệu database của một website bị tấn công sẽ làm liên lụy đến những trang khác. Đó còn là chưa kể đến những ảnh hưởng từ việc thiết bị lưu trữ cơ sở dữ liệu bị hư hỏng, làm mất toàn bộ dữ liệu của người dùng. Do đó khi sử dụng cơ sở dữ liệu database thì việc bạn cần làm đó là phải backup dữ liệu một cách thường xuyên, đừng trông chờ vào các nhà cung cấp như công ty hositng. Đây cũng là lời khuyên của những chuyên gia lập trình database.


# Vai trò của Cơ sở dữ liệu
Cơ sở dữ liệu có vô số trò chơi cùng quan trọng khi làm việc với dữ liệu hệ thống. Chúng tôi giúp người dùng thành công trong việc kết nối các dữ liệu. Người dùng có thể truy cập nhanh chóng cơ sở dữ liệu và dễ dàng hơn. Cơ sở dữ liệu chính là nguồn cơ sở để người dùng có thể truy xuất ra những thông tin cần thiết.

 Đặc biệt của cơ sở dữ liệu chính là truy xuất ra các thông tin, dữ liệu bằng nhiều phương thức khác nhau. Truy xuất nội dung an toàn dữ liệu an toàn ở mức cao. Đồng thời, nguồn thông tin khi xuất ra hoàn toàn không bị trùng lặp, nếu có thì suất xác định cũng rất thấp. Một cơ sở dữ liệu cơ sở cho phép nhiều người dùng truy cập đồng thời trong cùng một khoảng thời gian.
 # Có những loại Database nào?
### Phân loại Database theo mục đích sử dụng
- Database dạng file: Đây là dữ liệu được lưu trữ dưới dạng các file. Loại Database dạng file hay được sử dụng nhất đó *.mdb Foxpro, ngoài ra còn có *.dbf, ascii,…

- Database quan hệ: Chúng là các dữ liệu khác nhau được lưu trữ trong các bảng dữ liệu nhưng giữa chúng lại có mối liên hệ với nhau. Vì vậy, chúng mới có tên gọi là “database quan hệ”. Một số hệ quản trị hỗ trợ database quan hệ hiện rất được ưa chuộng bao gồm: MySQL, MS SQL server, Oracle,…

- Database hướng đối tượng: Điểm giống nhau giữa database hướng đối tượng và database quan hệ chính là chúng đều được lưu trữ trong bảng dữ liệu. Còn điểm khác biệt các bảng của database hướng đối tượng có thêm các tính năng hướng đối tượng, ví dụ như lưu trữ thêm 1 số hành vi để thể hiện rõ hơn hành vi của đối tượng. Nhắc đến tên các hệ quản trị hỗ trợ database hướng đối tượng, người ta sẽ nhớ ngay đến những cái tên nổi bật như: MS SQL server, Postgres SQL, Oracle,…

- Database bán cấu trúc: Loại database này được lưu với định dạng XML, nó có thông tin mô tả dữ liệu và đối tượng được trình bày trong các thẻ tag. Database bán cấu trúc có ưu điểm vượt trội đó là lưu trữ được nhiều loại data khác nhau, chính vì vậy nó đang dần khẳng định được vị trí và giá trị sử dụng của mình.
### Phân loại Database theo hệ điều hành
- Database dùng hệ điều hành Windows, ví dụ như: SQL Server – MSSQL,...

- Database dùng hệ điều hành Linux, ví dụ như: MySQL, Mariadb,...

# Những câu lệnh sql cơ bản
### 1. Trên cơ sở dữ liệu


