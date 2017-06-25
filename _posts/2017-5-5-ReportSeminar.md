---
layout: post
title: Báo cáo đồ án
date:   2017-06-25                    # Thời gian tạo bài viết
---

### I. Giới thiệu thông tin nhóm
* Sinh viên 1
  * MSSV: 1312432
  * Họ Tên: Phạm Hữu Phong
  * Email: 1312432@student.hcmus.edu.vn
  * Số ĐT: 0965191514
* Sinh viên 2
  * MSSV: 1312479
  * Họ Tên: Lại Trọng Sang
  * Email: 1312479@student.hcmus.edu.vn
  * Số ĐT: 0962525036

### II. Tài liệu tham khảo
-	Chạy chương trình:
> scala HelloWorld
- [Kết quả chạy chương trình HelloWorld](https://github.com/laitrongsang95/laitrongsang95.github.io/blob/master/images/demo5.JPG)
## Play Frameword
### I. Tổng quan về Play Framework
#### 1. Khái niệm
Play là 1 framework dùng để tạo các ứng dụng web, được viết bằng Scala và Java theo kiến trúc model-view-controller (MVC). Play được tạo ra với mục đích tăng hiệu suất lập trình bằng cách sử dụng các quy ước bằng cầu hình, tải lại mã nóng và hiện thị lỗi trên trình duyệt.
#### 2. Những đặc điểm nổi bật
Play framework dùng để viết web bằng ngôn ngữ java và scala với tiêu chí nhẹ, không trạng thái, thân thiện với nền tảng web có các điểm sau:
-	Dựa trên nền tảng java JVM (Java Virtual Machine): có thể sử dụng đa nền.
-	Thân thiện với người phát triển: Bạn chỉ cần chỉnh sửa text-editor và sau đó nhấn refresh trên trình duyệt web, mọi chỉnh sửa sẽ có hiệu lực.
-	Quy mô đơn giản: bên dưới nền tảng Play sử dụng một mô hình hoàn toàn bất đồng bộ được xây dựng trên Akka. Kết hợp với đặc điểm không trạng thái của web, quy mô của Play trở nên đơn giản.
-	Thích hợp cho cả web và mobile: Play có thể hoạt động tốt trên cả nền tảng web và mobile. 
### II. Bắt đầu làm việc với Play Framework
#### 1. Những công cụ cần thiết
Để có thể sử dụng được Play Framework cần cài đặt những công cụ sau:
- [JDK-Java SE Development Kit 8](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)
-	[Scala](http://scala-lang.org/download/)
-	[Sbt](http://www.scala-sbt.org/download.html)
-	[Activator](https://www.lightbend.com/activator/download) 
#### 2. Tạo project mới
1. Tạo project Play Framework có 2 cách
- Tạo project dùng sbt: gõ lệnh trên cửa sổ command line 				
> sbt new playframework/play-scala-seed.g8
- [Download các project đã được tạo sẵn trên trang wed](https://playframework.com/download#examples)
2. Sau khi tạo project xong. Trên cửa sổ cmd gõ lệnh “cd myproject” (myproject là tên project vừa được tạo). 
3. Gõ lệnh “sbt run” và truy cập vào địa chỉ “localhost:9000” để xem kết quả.
#### 3. Một số IDE cho Scala và Play Framework
-	[IntelliJ IDEA](https://www.jetbrains.com/idea/download/#section=windows)
-	[Eclipse](http://scala-ide.org/download/sdk.html)
#### 4. Cấu trúc Play Framework
**Những phần quan trọng:** 
- /buid.sbt
Là file định nghĩa các plugin muốn dùng trong project.
- /conf/application.conf 
Là nơi bạn define toàn bộ conf ứng với plugin trong buid.sbt như kết nối database, akka…
- /conf/routes
Là nơi bạn define toàn bộ URL và match với action của hệ thống.
- /app 
chứa toàn bộ các file về application như: controller, view…
 - /public 
chứa các file như image, javascript, css
##### [Hình ảnh minh họa cấu trúc](https://github.com/laitrongsang95/laitrongsang95.github.io/blob/master/images/struct.png)
#### 5. Kết nối với database(mySql)
Đầu tiên ta cần định nghĩa database connection, có 2 chỗ ta cần sửa:
1.	Define những thư viện bạn cần trong build.sbt
2.	Define các thông số kết nối ở application.conf
- trong /buid.sbt cần khai báo thư viện sau:
 > - libraryDependencies += jdbc  
 > - libraryDependencies += "mysql" % "mysql-connector-java" % "5.1.34"
- trong /conf/application.conf thêm thông tin kết nối:
  > - db.default.driver=com.mysql.jdbc.Driver
  > - db.default.url="jdbc:mysql://localhost/play"
  > - db.default.username=sangus1
  > - db.default.password="12345"

- Thông tin cung cấp ở trên đó là tên của database (play) cùng đường dẫn đến đó, có username và password do mình tự đặt.
- Chúng ta chạy lại project và truy cập vào địa chỉ localhost:9000 ta sẽ thấy nó bắt đầu kết nối với database.
- Vậy là ta đã kết nối được tới mysql database.Bây giờ bạn có thể tự tạo bảng trong cơ sở dữ liệu của bạn hoặc sử dụng evolution trong playframeword để làm việc đó.
## Video demo
- [Demo create project "HelloWorld" by Scala](https://www.youtube.com/watch?v=0BPlSuW6Ji8)
- [Demo connect mySQL DB with play framework](https://youtu.be/8qujfLmDtZI)

## Link tài liệu tham khảo
   
        https://hoaiptvn.blogspot.com/search/label/Play%20Framework
        http://luanvan.net.vn/luan-van/do-an-tim-hieu-ngon-ngu-lap-trinh-scala-xay-dung-website-chia-se-anh-truc-tuyen-66875/
        https://playframework.com/documentation/2.5.x/Home
        https://viblo.asia/tran.thi.thuy.duong/posts/1l0rvmx0GyqA




