---
layout: post
title:  "Báo Cáo Play(Scala)"
date:   2017-05-06                    # Thời gian tạo bài viết
---
# Giới thiệu về Scala
### Giới thiệu chung
-	Ngôn ngữ Scala (Scalable Language - Ngôn ngữ có khả năng mở rộng) là ngôn ngữ lập trình đa mẫu hình, được thiết kế tích hợp các tính năng của lập trình hướng đối tượng và lập trình hàm.
-	Scala là 1 ngôn ngữ được thiết kế để có khả năng mở rộng tùy theo nhu cầu của người sử dụng. Ngôn ngữ Scala được sử dụng trong nhiều lĩnh vực , qui mô, từ những đoạn script nhỏ cho đến những hệ thống lớn.
-	Scala chạy trên nền máy ảo Java và nó tương thích hoàn toàn với Java. Ngoài ra nó cũng có thể chạy trên .NET, tuy nhiên chưa ổn định.
-	Scala có kiểu biên dịch giống Java nên nó có thể đọc được các thư viện của Java.
-	Scala được xây dựng với các tính năng của lập trình hàm và lập trình hướng đối tượng. Sự kết hợp của lập trình hàm và lập trình hướng đối tượng được thể hiện trong nhiều khia cạnh, 2 kiểu lâp trình này bổ sung sức mạnh cho nhau đặc biệt khi hệ thống được mở rộng. Lập trình hàm có thể xây dựng nhanh chóng và dễ dàng những tính năng từ những phần nhỏ trong khi lập trình hướng đối tượng thích hợp để cấu trúc 1 hệ thống lớn.
### Lịch sử phát triển
Scala bắt đầu được thiết kế từ năm 2001 bởi Martin Odersky, tiếp tục phát triển khi làm việc tại Funnel, một ngôn ngữ lập trình tích hợp các ý tưởng về lập trình hàm và mạng Petri. Scala được cho ra những phiên bản đầu vào cuối năm 2003 /đầu 2004 trên nền Java, và nền.NET vào tháng 6 năm 2004. Phiên bản 2.0 ra mắt tháng 3 năm 2006. 
### Một số đặc điểm của ngôn ngữ Scala
- Ngôn ngữ lập trình hàm bậc cao.
- Tương thích với Java.
- Ưu việt khi xử lý tính toán song song, phân tán và bất đồng bộ.
- Cơ động linh hoạt về cú pháp.
- Sở hữu vòng lặp for mạnh mẽ.
- Được thiết kế để phù hợp với cả lập trình hàm cũng như lập trình hướng đối tượng.
- Hệ thống kiểu dữ liệu phong phú và có khả năng mở rộng (định nghĩa thêm phương thức cho kiểu có sẵn).
### Lập trình hàm
Scala hỗ trợ lập trình hàm. Nó hỗ trợ cú pháp ngắn gọn cho việc định nghĩa các hàm, cho phép hàm lồng nhau. Dùng từ khóa lazy để trì hoãn sử dụng một biến cho đến khi sử dụng nó.
### Lập trình hướng đối tượng
Giống Java, Scala là ngôn ngữ hướng đối tượng. Scala là ngôn ngữ thuần lập trình hướng đối tượng trong cú pháp theo quy tắc tất cả giá trị biến đều là một đối tượng. Kiểu dữ liệu cà hành vi của một đối tượng được mô tả bằng các lớp. Các lớp trừu tượng được mở rộng bằng các lớp con và hạn chế các khó khăn trong đa kế thừa.
### Demo chương trình “HelloWorld”
-	Đây là chương trình “Hello world” viết bằng scala:
> object HelloWorld extends Application {
> println("Hello, world!")
> }

-	Hoặc:
> object HelloWorld {
> def main(args: Array[String]) {
> println("Hello, world!")
> }
> }

-	Chương trình lưu dưới dạng HelloWorld.scala, biên dịch bằng cú pháp:
> scalac HelloWorld.scala

-	Chạy chương trình:
> scala HelloWorld
- [kết quả chạy chương trình HelloWorld](https://github.com/laitrongsang95/laitrongsang95.github.io/blob/master/images/demo5.JPG)
# Play Frameword
### Tổng quan về Play Framework
#### Khái niệm
Play là 1 framework dùng để tạo các ứng dụng web, được viết bằng Scala và Java theo kiến trúc model-view-controller (MVC). Play được tạo ra với mục đích tăng hiệu suất lập trình bằng cách sử dụng các quy ước bằng cầu hình, tải lại mã nóng và hiện thị lỗi trên trình duyệt.
#### Những đặc điểm nổi bật
Play framework dùng để viết web bằng ngôn ngữ java và scala với tiêu chí nhẹ, không trạng thái, thân thiện với nền tảng web có các điểm sau:
-	Dựa trên nền tảng java JVM (Java Virtual Machine): có thể sử dụng đa nền.
-	Thân thiện với người phát triển: Bạn chỉ cần chỉnh sửa text-editor và sau đó nhấn refresh trên trình duyệt web, mọi chỉnh sửa sẽ có hiệu lực.
-	Quy mô đơn giản: bên dưới nền tảng Play sử dụng một mô hình hoàn toàn bất đồng bộ được xây dựng trên Akka. Kết hợp với đặc điểm không trạng thái của web, quy mô của Play trở nên đơn giản.
-	Thích hợp cho cả web và mobile: Play có thể hoạt động tốt trên cả nền tảng web và mobile. 
### Bắt đầu làm việc với Play Framework
#### Những công cụ cần thiết
Để có thể sử dụng được Play Framework cần cài đặt những công cụ sau:
- [JDK-Java SE Development Kit 8](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)
-	[Scala](http://scala-lang.org/download/)
-	[Sbt](http://www.scala-sbt.org/download.html)
-	[Activator](https://www.lightbend.com/activator/download) 
#### Tạo project mới
1. Tạo project Play Framework có 2 cách
- Tạo project dùng sbt: gõ lệnh trên cửa sổ command line 				
> sbt new playframework/play-scala-seed.g8
- [Download các project đã được tạo sẵn trên trang wed](https://playframework.com/download#examples)
2. Sau khi tạo project xong. Trên cửa sổ cmd gõ lệnh “cd myproject” (myproject là tên project vừa được tạo). 
3. Gõ lệnh “sbt run” và truy cập vào địa chỉ “localhost:9000” để xem kết quả.
#### Một số IDE cho Scala và Play Framework
-	[IntelliJ IDEA](https://www.jetbrains.com/idea/download/#section=windows)
-	[Eclipse](http://scala-ide.org/download/sdk.html)
#### Cấu trúc Play Framework
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

- ![hình minh họa cấu trúc](https://github.com/laitrongsang95/laitrongsang95.github.io/blob/master/images/struct.png "Logo Title Text 1")


