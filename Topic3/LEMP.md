<img width="809" height="390" alt="image" src="https://github.com/user-attachments/assets/42526581-c58e-4b35-b7da-9227a5e0e702" /># XÂY DỰNG MÔ HÌNH LEMP
* mô hình LEMP gồm linux,nginx, mysql, PHP

## 1 CÀI ĐẶT NGINX

<img width="1687" height="305" alt="image" src="https://github.com/user-attachments/assets/c0b37140-b361-4d66-b3ba-278b71f196fe" />

## 1.2 CÀI ĐẶT PHP 8.1

## cài các gói phụ thuộc

<img width="1618" height="821" alt="image" src="https://github.com/user-attachments/assets/d2ddc944-2e29-47a3-9e8f-3140f2e4f374" />

## thêm kho PHP của Ondřej để apt tải package PHP từ đó

<img width="1162" height="540" alt="image" src="https://github.com/user-attachments/assets/101b2628-d757-47e1-8384-684e80e31764" />

## cài php8.1

<img width="1182" height="758" alt="image" src="https://github.com/user-attachments/assets/fbc51f9f-6b6c-4562-9052-0f01873550fe" />

## cài các package của PHP 8.1

<img width="1851" height="502" alt="image" src="https://github.com/user-attachments/assets/1b1c4310-c7ad-44ca-b9a9-9845d7d4b837" />

## check trạng thái của PHP-FPM

<img width="1180" height="418" alt="image" src="https://github.com/user-attachments/assets/f41631ce-a94c-4f82-b96b-b41f2f58b68c" />

## 1.3 CÀI MYSQL

<img width="1178" height="489" alt="image" src="https://github.com/user-attachments/assets/72d84d0e-bd50-4d08-8a64-27dfe4e72315" />

## check trạng thái dịch vụ

<img width="941" height="291" alt="image" src="https://github.com/user-attachments/assets/2054da96-a9b7-4662-aa26-fe04119b2dc9" />

## Cấu hình Nginx để sử dụng bộ xử lý PHP

-tạo thư mục root web cho domain

<img width="413" height="23" alt="image" src="https://github.com/user-attachments/assets/c65e0b58-969b-43d3-9bdb-845b566bd9b9" />

-Gán quyền sở hữu thư mục bằng cách sử dụng biến môi trường $USER, biến này sẽ tham chiếu đến người dùng hệ thống hiện tại:

<img width="660" height="20" alt="image" src="https://github.com/user-attachments/assets/eec38468-23ed-41fe-855e-3c8c32327954" />

-Mở một tệp cấu hình mới trong thư mục sites-available của Nginx bằng trình soạn thảo dòng 

<img width="590" height="402" alt="image" src="https://github.com/user-attachments/assets/86f1e90f-15f0-4a4e-8bb3-e6b6919a5323" />

<img width="814" height="414" alt="image" src="https://github.com/user-attachments/assets/ebddb38b-3b29-4945-9e0d-674296514688" />

-Kích hoạt cấu hình bằng cách liên kết đến tệp cấu hình từ thư mục sites-enabled của Nginx:

<img width="974" height="17" alt="image" src="https://github.com/user-attachments/assets/e27fccfa-22ea-47f0-a37a-d83e960c2d3e" />

-Tiếp theo, hãy gỡ bỏ liên kết đến tệp cấu hình mặc định khỏi thư mục /sites-enabled/

<img width="772" height="14" alt="image" src="https://github.com/user-attachments/assets/8bccb6ec-1de1-43f5-9d39-393b317942d5" />

-check domain

<img width="658" height="296" alt="image" src="https://github.com/user-attachments/assets/9752495d-8cbf-4e71-a718-8b03c783f8e5" />

-kiểm tra PHP với nginx

<img width="1067" height="128" alt="image" src="https://github.com/user-attachments/assets/d313aae2-31bc-4ffd-9a2d-2cdc37d8e98f" />
<img width="1627" height="1016" alt="image" src="https://github.com/user-attachments/assets/b92919cc-14b0-4d5b-9b5f-8336188cf649" />

-kiểm tra mysql kết nối tới php

  <img width="1066" height="242" alt="image" src="https://github.com/user-attachments/assets/7c480c76-e79c-4ee6-8b89-27f1f6f4574e" />

  -truy cập thử với account longtc

  <img width="748" height="270" alt="image" src="https://github.com/user-attachments/assets/b907835c-3791-49a6-a6c9-cc0e37d7e1f5" />
  
  -check truy cập vào database

  <img width="340" height="320" alt="image" src="https://github.com/user-attachments/assets/867ed382-7d66-4754-9e39-7df58555f483" />
  -tạo bảng

  <img width="946" height="79" alt="image" src="https://github.com/user-attachments/assets/36791cd0-93f3-4c80-9a50-814fddfc48fd" />

-thêm nội dung
  
<img width="818" height="68" alt="image" src="https://github.com/user-attachments/assets/3bcfb8cd-1f85-41cd-ab97-6d21f2f2b207" />

<img width="436" height="251" alt="image" src="https://github.com/user-attachments/assets/c8abe9a8-c38a-4129-9955-78af44f58b1e" />

-viết chươn trình PHP lấy dử liệu trên database Mysql
<img width="936" height="478" alt="image" src="https://github.com/user-attachments/assets/97549929-3cb6-4555-8e53-cd5639ec4aa4" />

<img width="679" height="300" alt="image" src="https://github.com/user-attachments/assets/343b3669-2171-47be-a39f-1e2eedecc569" />

  

## 1.5 cài php-admin

<img width="877" height="419" alt="image" src="https://github.com/user-attachments/assets/54232e67-cf9c-47d9-8d68-771b8580d4ec" />

## Tạo symlink cho nginx

<img width="1102" height="108" alt="image" src="https://github.com/user-attachments/assets/5ee48e63-5587-4102-ab53-c3ba55c82efc" />

## truy cập vào phpmyadmin

<img width="1269" height="570" alt="image" src="https://github.com/user-attachments/assets/a6e42122-700a-4a80-978a-ad50fa785463" />
<img width="1276" height="426" alt="image" src="https://github.com/user-attachments/assets/fd64fa20-e594-4ffd-ab93-8139e5d8a558" />

<img width="1851" height="894" alt="image" src="https://github.com/user-attachments/assets/363aca94-9786-4fe0-a0ac-df36e04790de" />
## 2. cài wordpress và lavarel

-tạo thư mục cho domain wordpress và lavarel

<img width="649" height="46" alt="image" src="https://github.com/user-attachments/assets/c168ad03-17ec-44b9-9b84-053f030207ca" />

-gán quyền cho webserver sử dung thư mục

<img width="585" height="60" alt="image" src="https://github.com/user-attachments/assets/730c33f5-1838-42c0-a10a-41aa2bde9fdf" />

-tạo database, user cho wordpress và lavarel

<img width="782" height="437" alt="image" src="https://github.com/user-attachments/assets/a7040867-5178-4a00-9f62-c8d7b1bf5cab" />

- 2.1 cài wordpress

<img width="1720" height="111" alt="image" src="https://github.com/user-attachments/assets/4ec6ff4b-8e75-4db8-9a45-1b422b47e980" />

-chỉnh config 

<img width="1067" height="661" alt="image" src="https://github.com/user-attachments/assets/2981e38b-2989-4b9b-b39e-d90862486d34" />

- 2.2 cài lavarel
  
<img width="1420" height="263" alt="image" src="https://github.com/user-attachments/assets/990c330b-98be-4365-9e06-ea7c12d89f13" />

<img width="973" height="352" alt="image" src="https://github.com/user-attachments/assets/20a7ecde-1ae2-40df-9eb6-e3eec826ddc2" />

## cấu hình Nginx cho 2 domain

-wordpress

<img width="1262" height="444" alt="image" src="https://github.com/user-attachments/assets/1d149f7d-c35e-4d7a-81b3-35d95ec98ac9" />

-lavarel

<img width="1302" height="367" alt="image" src="https://github.com/user-attachments/assets/31cc8789-05f2-49fe-81cd-755266df644a" />

-kích hoạt site để nginx truy câp

<img width="1213" height="68" alt="image" src="https://github.com/user-attachments/assets/0debbcbc-4368-41f2-a2c3-f2236d565a6f" />

-wordpress interface

<img width="1271" height="999" alt="image" src="https://github.com/user-attachments/assets/a9d93c78-1791-4f74-9b2c-19f4dadce170" />

-Lavarel interface

<img width="1529" height="896" alt="image" src="https://github.com/user-attachments/assets/9e165160-3109-48c6-a5ae-334514fd6fa5" />

## 3. CÀI SSL

-Cài certbot

CÀI CHO wp.caolong.vietnix.tech
<img width="993" height="531" alt="image" src="https://github.com/user-attachments/assets/2ac6283d-9631-4c2f-bdac-3f28973e5791" />

<img width="948" height="751" alt="image" src="https://github.com/user-attachments/assets/95154b35-a282-4d6b-b829-4dc43635bb64" />

<img width="366" height="277" alt="image" src="https://github.com/user-attachments/assets/44feedc9-eb87-4085-9114-a5f6c7e78976" />


CÀI CHO laravel.caolong.vietnix.tech

<img width="1123" height="407" alt="image" src="https://github.com/user-attachments/assets/1c7d2433-296a-4bec-8455-4610faa58d9a" />

<img width="511" height="296" alt="image" src="https://github.com/user-attachments/assets/694fb0c1-0ae7-4fd8-b74d-9b2ae3355def" />

## 4. thiết lập remote cho mysql

-cấu hình cho mysql 

<img width="425" height="73" alt="image" src="https://github.com/user-attachments/assets/3dc307ae-6095-44c1-9dbe-84e61fe7e4ac" />

- tạo user remote 

<img width="822" height="340" alt="image" src="https://github.com/user-attachments/assets/3dc02837-4a3b-4406-9776-51253a3be53b" />

-cấu hình firewall bảo mật

<img width="693" height="42" alt="image" src="https://github.com/user-attachments/assets/7b9e9792-bbc2-4ebd-b8b5-a6f493a85e83" />

-dùng thiết bị khác để kết nối vào user remote_user

<img width="917" height="329" alt="image" src="https://github.com/user-attachments/assets/fe684893-afaa-47b3-9683-957627fe039c" />
