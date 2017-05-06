---
layout: post
title:  "Báo Cáo Play(Scala)"
date:   2017-05-06                    # Thời gian tạo bài viết
permalink: jekyll/tao-blog-jekyll/    # Liên kết của bài viết, xem phần đầu của bài viết
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
![demo1](https://github.com/laitrongsang95/laitrongsang95.github.io/blob/master/images/demo1.JPG) (<img />)

-	Hoặc:
![demo2](demo.gif)

-	Chương trình lưu dưới dạng HelloWorld.scala, biên dịch bằng cú pháp:
![Video Walkthrough](demo.gif)

-	Chạy chương trình:
![Video Walkthrough](demo.gif)
