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
- check port

  <img width="939" height="237" alt="image" src="https://github.com/user-attachments/assets/7c0c3346-45ef-49a9-bbfd-df066b02ae50" />
  ## step 2 — Cấu hình Apache để sử dụng mod_fastcgi

  
