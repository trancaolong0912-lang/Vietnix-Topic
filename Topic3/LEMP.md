<img width="658" height="296" alt="image" src="https://github.com/user-attachments/assets/0bbcf76d-c987-4fbf-9a95-8d5e4f869044" /># XÂY DỰNG MÔ HÌNH LEMP
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

- check domain

<img width="658" height="296" alt="image" src="https://github.com/user-attachments/assets/9752495d-8cbf-4e71-a718-8b03c783f8e5" />

- kiểm tra PHP với nginx

<img width="1067" height="128" alt="image" src="https://github.com/user-attachments/assets/d313aae2-31bc-4ffd-9a2d-2cdc37d8e98f" />
<img width="1627" height="1016" alt="image" src="https://github.com/user-attachments/assets/b92919cc-14b0-4d5b-9b5f-8336188cf649" />

- kiểm tra mysql kết nối tới php

  <img width="1066" height="242" alt="image" src="https://github.com/user-attachments/assets/7c480c76-e79c-4ee6-8b89-27f1f6f4574e" />

- truy cập thử với account longtc

  <img width="748" height="270" alt="image" src="https://github.com/user-attachments/assets/b907835c-3791-49a6-a6c9-cc0e37d7e1f5" />
  
- check truy cập vào database

  <img width="340" height="320" alt="image" src="https://github.com/user-attachments/assets/867ed382-7d66-4754-9e39-7df58555f483" />
- tạo bảng

  <img width="946" height="79" alt="image" src="https://github.com/user-attachments/assets/36791cd0-93f3-4c80-9a50-814fddfc48fd" />

- thêm nội dung
  
<img width="818" height="68" alt="image" src="https://github.com/user-attachments/assets/3bcfb8cd-1f85-41cd-ab97-6d21f2f2b207" />

<img width="436" height="251" alt="image" src="https://github.com/user-attachments/assets/c8abe9a8-c38a-4129-9955-78af44f58b1e" />

-
<img width="936" height="478" alt="image" src="https://github.com/user-attachments/assets/97549929-3cb6-4555-8e53-cd5639ec4aa4" />

  

## cài php-admin

<img width="877" height="419" alt="image" src="https://github.com/user-attachments/assets/54232e67-cf9c-47d9-8d68-771b8580d4ec" />

## Tạo symlink cho nginx

<img width="1102" height="108" alt="image" src="https://github.com/user-attachments/assets/5ee48e63-5587-4102-ab53-c3ba55c82efc" />

## truy cập vào phpmyadmin

<img width="1269" height="570" alt="image" src="https://github.com/user-attachments/assets/a6e42122-700a-4a80-978a-ad50fa785463" />
<img width="1276" height="426" alt="image" src="https://github.com/user-attachments/assets/fd64fa20-e594-4ffd-ab93-8139e5d8a558" />

<img width="1851" height="894" alt="image" src="https://github.com/user-attachments/assets/363aca94-9786-4fe0-a0ac-df36e04790de" />

