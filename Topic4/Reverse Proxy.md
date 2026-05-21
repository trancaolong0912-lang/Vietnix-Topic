## MÔ HÌNH Nginx (Reverse Proxy) + Apache + PHP 8.1 + MySQL + phpMyAdmin.
# 1.lợi ích việc Nginx đứng trước apache.
- Nginx xuất sắc trong việc xử lý static content (ảnh, CSS, JS, file tĩnh), concurrency cao, và làm load balancer / reverse proxy rất hiệu quả, tiêu tốn ít RAM/CPU.

- Apache mạnh về dynamic content (PHP), hỗ trợ .htaccess tốt (rất quan trọng với WordPress), module phong phú.

- Kết hợp: Nginx nhận request từ user → phục vụ static files nhanh → proxy dynamic/PHP request sang Apache (thường listen port khác như 8080). Giúp tăng performance, bảo mật (Apache không expose trực tiếp), và dễ scale

  ## 2. thao tác xây dựng 2 website- sử dụng vhosst
  ## Step 1 — Configuring Apache and PHP-FPM

- Ở bước này, chúng ta sẽ thay đổi số cổng của Apache thành 8080 và cấu hình nó để hoạt động với PHP-FPM bằng cách sử dụng mô-đun mod_fastcgi. Đổi tên tệp cấu hình ports.conf của Apache:
  
<img width="1108" height="308" alt="image" src="https://github.com/user-attachments/assets/51b77014-4c31-4d34-b07e-5f7e17db8d93" />

- disable virtual host default do k còn xài port 80.

<img width="523" height="142" alt="image" src="https://github.com/user-attachments/assets/84761073-d6a1-4109-aa8e-8aaf542016e5" />

- tạo virtual host file mới, dùng site default đang có
  
<img width="1124" height="49" alt="image" src="https://github.com/user-attachments/assets/002c8fec-1d7a-42ba-b409-070e440204b5" />

<img width="1016" height="656" alt="image" src="https://github.com/user-attachments/assets/906b091a-0a85-4f44-bff7-0b834a173b90" />
  
- imporrt source code

<img width="1535" height="178" alt="image" src="https://github.com/user-attachments/assets/0d266633-c9ee-4a50-b369-98bddfbf1d74" />

- vhost cho wordpress
  
<img width="1422" height="456" alt="image" src="https://github.com/user-attachments/assets/2d7a5130-f694-40e6-9a8e-9594c08a7854" />

 - vhost cho lavarel
   
<img width="1472" height="608" alt="image" src="https://github.com/user-attachments/assets/932df1e0-88d9-44b5-a103-1de4a7c258de" />

- check port

  <img width="939" height="237" alt="image" src="https://github.com/user-attachments/assets/7c0c3346-45ef-49a9-bbfd-df066b02ae50" />
  ## step 2 — Cấu hình NGINX
  - TẠO DEFAULT VHOST ĐỂ CHUYỂN HƯỚNG CÁC REQUESST KO HỢP LỆ
 
<img width="1094" height="737" alt="image" src="https://github.com/user-attachments/assets/8f427127-c828-46a8-895a-c51775a18cda" />
  - tạo vhost cho lavarel nginx

<img width="1235" height="752" alt="image" src="https://github.com/user-attachments/assets/6b4876ea-2ed1-4aa5-8c44-ebb898725b9e" />

  - tạo vhost wordpress nginx

  <img width="1336" height="870" alt="image" src="https://github.com/user-attachments/assets/c7e22be4-ee50-4d9f-8882-388323d221fe" />

  ## cấu hình ssl
  
  - do Trong database WordPress còn lưu:

siteurl = https://linhlt.id.vn
home    = https://linhlt.id.vn
  nên khi vào wp.caolong.vietnix.tech sẽ tự redirect sang linhlt.id.nv

- fix bằng cách vào databse để đổi sag domain khác

<img width="897" height="338" alt="image" src="https://github.com/user-attachments/assets/0a2a2768-3776-49e1-9657-51d4dcb0ab9f" />
- hoặc dùng wp-cli để migrate toàn bộ

<img width="1058" height="468" alt="image" src="https://github.com/user-attachments/assets/da600f7a-04ed-4ff0-914f-2b1880edeb0c" />

## KẾT QUẢ DÙNG VHOST
<img width="1767" height="1000" alt="image" src="https://github.com/user-attachments/assets/bf2ea17d-bb41-4bab-80bb-5d36bd908c52" />

<img width="1849" height="1019" alt="image" src="https://github.com/user-attachments/assets/d089f317-40d2-4a13-bcac-f14b028a94f6" />

- check reverse proxy
  
  <img width="1857" height="130" alt="image" src="https://github.com/user-attachments/assets/193bca56-d5b7-4052-8a27-d21fa42600a5" />


- Bất kỳ domain nào khác khi trỏ về IP VPS hoặc truy cập qua IP phải cần qua 1
default vhost.

<img width="719" height="405" alt="image" src="https://github.com/user-attachments/assets/c57f80d1-af47-4e8d-b1a0-9de31b62fda6" />

- cho site chạy 2 giao thức http và https

  
<img width="1165" height="309" alt="image" src="https://github.com/user-attachments/assets/9d6dd63f-a311-4297-a277-791e56e0688a" />

- check và kết quả đề trả về 200 khi truy cập http
  
<img width="653" height="266" alt="image" src="https://github.com/user-attachments/assets/205be7c6-4555-4ce1-85b1-c7e679bd11ab" />


<img width="987" height="303" alt="image" src="https://github.com/user-attachments/assets/36a203d7-eb08-4539-8086-fec7f90584ed" />

