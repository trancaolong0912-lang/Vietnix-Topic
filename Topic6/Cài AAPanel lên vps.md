---
title: Cài AAPanel lên vps

---

# Cài AAPanel lên vps 
## 1. Lý thuyết - aaPanel là gì?
aaPanel (trước đây là phiên bản quốc tế của BaoTa Panel - BT.cn) là một giao diện web (GUI) giúp quản lý máy chủ Linux một cách dễ dàng mà không cần dùng nhiều lệnh dòng lệnh (Command Line).
Nó được thiết kế để đơn giản hóa việc quản trị VPS/Server, đặc biệt phù hợp với:

* Người mới bắt đầu
* Developer
* Freelancer
* Doanh nghiệp nhỏ muốn host nhiều website

 Tính năng chính của aaPanel:

* One-click install môi trường web: LNMP (Nginx + MySQL/MariaDB + PHP), LAMP (Apache), OpenLiteSpeed...
* Quản lý Website (thêm domain, SSL miễn phí Let's Encrypt, rewrite rule...)
* Quản lý Database (MySQL, MariaDB)
* Quản lý FTP accounts
* Quản lý File (File Manager mạnh)
* Backup & Restore
* Giám sát tài nguyên server (CPU, RAM, Disk, Bandwidth)
* Firewall, Security (Fail2ban, WAF...)
* Crontab (lập lịch)
* Hỗ trợ nhiều phiên bản PHP cùng lúc
* WordPress Toolkit (Pro)
* Và hơn 100 tính năng khác

## Ưu điểm:

Hoàn toàn miễn phí (có bản Pro trả phí với tính năng nâng cao)
Nhẹ, ổn định, giao diện đẹp và hiện đại
Cài đặt nhanh (khoảng 2-5 phút)
Cộng đồng lớn, cập nhật thường xuyên

## Nhược điểm:

Có một số tính năng nâng cao (multi-user hosting chuyên nghiệp) chỉ có ở bản Pro
Server gốc phải sạch (chưa cài Apache/Nginx/PHP trước đó)

## 2. Hướng dẫn cài aaPanel trên VPS

- cài aaPanel qua dòng lệnh sau
![image](https://hackmd.io/_uploads/r1OXB4ZgGl.png)

- sau khi tải xong dc cấp url, username, password

![image](https://hackmd.io/_uploads/SkX9rVZlGe.png)

- chọn mô hình cho hosting

![image](https://hackmd.io/_uploads/rJQsDEblGe.png)

+ Multi-WebServer: Là mô hình chạy nhiều loại web server cùng lúc (Nginx Apache + OpenLiteSpeed). Mô hình này linh hoạt nhưng tốn tài nguyên server hơn, phức tạp và dễ gặp vấn đề nếu không cấu hình tốt.

+ Single WebServer (khuyến nghị chọn): Đây là mô hình chỉ sử dụng một web server chính (thường là Nginx).

## ở đây chúng ta sẽ sử dụng model single

![image](https://hackmd.io/_uploads/rJSX5NZlMe.png)
![image](https://hackmd.io/_uploads/Sy6BqV-gzx.png)

## tạo website

![image](https://hackmd.io/_uploads/By9oc4bgfx.png)
![image](https://hackmd.io/_uploads/rJytoVWefl.png)


## upload source code và giải nén

![image](https://hackmd.io/_uploads/HkPn64bgMg.png)

## import database

![image](https://hackmd.io/_uploads/BJl-gBWlzx.png)

## sửa lại thông tin database của wp

![image](https://hackmd.io/_uploads/SkXASBZxfl.png)

## sửa lại thông tin database của laravel

![image](https://hackmd.io/_uploads/rJT-IBWefl.png)

## 3. deploy lavarel

- cài các gói phụ thuộc

![image](https://hackmd.io/_uploads/SkZ85B-xGe.png)

- set APP-KEY

![image](https://hackmd.io/_uploads/ryPtTHWlfl.png)

- set quyền cho laravel ghi file

![image](https://hackmd.io/_uploads/Hy_6pB-gfe.png)
![image](https://hackmd.io/_uploads/rkSoRSWefl.png)

- cài ssl cho website

![image](https://hackmd.io/_uploads/HkMG18WgMe.png)


![image](https://hackmd.io/_uploads/BJBj0u-lzl.png)


## 4. deploy wordpress

- add domain
![image](https://hackmd.io/_uploads/B1XiLYWgGx.png)

- up source code

![image](https://hackmd.io/_uploads/H102IYZxfe.png)

- import database

![image](https://hackmd.io/_uploads/r1B0LKZgMl.png)




![image](https://hackmd.io/_uploads/H15lcYZlzl.png)























## fix lỗi redirect sang site cũ khi migrate site

![image](https://hackmd.io/_uploads/Sk0DVK-ezl.png)

## SỬ DỤNG WordPress – All-in-One WP Migration and Backup Plugin

Dùng để:

* backup website
* migrate WordPress
* chuyển hosting/VPS
* restore full site

# cách back up

- trong trang admin đi tới 
![image](https://hackmd.io/_uploads/ByGN5YZeMl.png)


![image](https://hackmd.io/_uploads/Bk-r3tWgzx.png)


![image](https://hackmd.io/_uploads/HJ_BatWeMe.png)

- export website muốn back up

![image](https://hackmd.io/_uploads/r1oqTtWxfl.png)

- imporrt website muốn restore

![image](https://hackmd.io/_uploads/SyLDRF-lfe.png)

## CÀI ĐẶT CÁC PLUGIN
1. Rank Math SEO
- Mục đích

SEO plugin.

Chức năng:

* SEO title/meta
* sitemap XML
* schema
* redirect
* index Google
* Dùng khi

Website cần:

* SEO
* tối ưu Google
* blog
* bán hàng

## CÁC BƯỚC CÀI

B1: tải file zip của plugin lên

![image](https://hackmd.io/_uploads/BJ7WecWlfe.png)

B2: Active plugin

![image](https://hackmd.io/_uploads/B1O8e9bgGl.png)
![image](https://hackmd.io/_uploads/S1Mul5Wlfx.png)
---
![image](https://hackmd.io/_uploads/Skhue9WxGl.png)

![image](https://hackmd.io/_uploads/HJJim5-lGg.png)
## mytheme shop

![image](https://hackmd.io/_uploads/r1sIEc-xze.png)

- kích hoạt 

![image](https://hackmd.io/_uploads/Hyk-Hc-lMe.png)

- theme mới 

![image](https://hackmd.io/_uploads/B1_6r9Wlfl.png)


## plugin elememtor
- Elementor là plugin kéo-thả để thiết kế giao diện WordPress mà không cần code.

## Elementor thường dùng để làm:

* Trang chủ đẹp
* Landing page
* Banner
* Form
* Header/footer
* Popup
* Shop WooCommerce
* Responsive mobile


![image](https://hackmd.io/_uploads/r1mZ89-gzg.png)

![image](https://hackmd.io/_uploads/HyypacWeze.png)

## Divi Theme

![image](https://hackmd.io/_uploads/B1gP0c-lfe.png)
![image](https://hackmd.io/_uploads/rJUsyj-xGg.png)
