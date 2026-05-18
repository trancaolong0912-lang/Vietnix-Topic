# DirectAdmin Features

Nguồn:
- https://www.directadmin.com/features_list.php

---

# DirectAdmin là gì?

DirectAdmin là web hosting control panel dùng để quản lý:
- Hosting
- Website
- Domain
- Email
- Database
- DNS
- Server

thông qua giao diện web trực quan mà không cần thao tác quá nhiều bằng command line Linux.

---

# Các tính năng chính của DirectAdmin

| Nhóm tính năng | Chức năng |
|---|---|
| User / Reseller / Admin Level | Phân quyền quản trị nhiều cấp |
| File Manager | Quản lý file website |
| FTP Management | Quản lý FTP |
| DNS Management | Quản lý DNS Record |
| Email Administration | Quản lý email domain |
| MySQL Databases | Quản lý database |
| Site Backup | Backup & Restore dữ liệu |
| SSL Management | Cài SSL cho website |
| PHP Selector | Chọn phiên bản PHP |
| Statistics | Theo dõi traffic và tài nguyên |
| Cron Jobs | Tạo tác vụ tự động |
| Security Tools | Bảo mật server |
| Plugin System | Hỗ trợ plugin mở rộng |
| Ticket Support System | Hệ thống hỗ trợ ticket |
| Automatic Recovery | Tự động restart service lỗi |
| Live Updates | Cập nhật hệ thống tự động |

---

# 1. User / Reseller / Admin Level

DirectAdmin hỗ trợ 3 cấp quản trị:

| Cấp quyền | Vai trò |
|---|---|
| Admin | Quản lý toàn bộ server |
| Reseller | Quản lý khách hàng hosting |
| User | Quản lý website cá nhân |

---

# 2. File Manager

Cho phép:
- Upload source code
- Chỉnh sửa file
- Giải nén file
- Phân quyền thư mục

## Ví dụ

```txt
public_html/index.php
```

---

# 3. FTP Management

Quản lý tài khoản FTP để upload dữ liệu website từ máy tính lên server.

## Ví dụ
- Tạo FTP cho developer
- Giới hạn thư mục upload

---

# 4. DNS Management

Quản lý:
- A Record
- MX Record
- TXT Record
- CNAME

## Ví dụ

```txt
example.com → 192.168.1.10
```

---

# 5. Email Administration

Quản lý email domain riêng.

## Ví dụ

```txt
support@example.com
admin@example.com
```

## Bao gồm
- POP3 / IMAP
- Forwarder
- Autoresponder
- Spam Filter

---

# 6. MySQL Databases

Quản lý database website.

## Bao gồm
- Tạo database
- Import / Export dữ liệu
- phpMyAdmin

## Ví dụ

WordPress lưu:
- User
- Bài viết
- Comment

trong MySQL.

---

# 7. Site Backup

Cho phép:
- Backup website
- Backup database
- Restore dữ liệu

## Ví dụ

Khôi phục website sau khi update plugin bị lỗi.

---

# 8. SSL Management

Hỗ trợ cài đặt SSL cho website.

## Ví dụ

```txt
http://example.com
↓
https://example.com
```

## Công dụng
- Kích hoạt HTTPS
- Mã hóa dữ liệu
- Tăng bảo mật website

---

# 9. PHP Selector

Cho phép chọn nhiều phiên bản PHP khác nhau.

## Ví dụ
- Website A dùng PHP 7.4
- Website B dùng PHP 8.2

---

# 10. Statistics & Monitor

Theo dõi:
- CPU Usage
- RAM Usage
- Traffic
- Error Logs
- Bandwidth

## Ví dụ

Kiểm tra lỗi:

```txt
500 Internal Server Error
```

---

# 11. Security Tools

Bao gồm:
- Spam Filter
- SSL
- IP Blocking
- Two-Factor Authentication

## Công dụng
- Chống spam
- Bảo vệ website
- Ngăn truy cập trái phép

---

# 12. Plugin System

Cho phép cài thêm:
- Redis
- LiteSpeed
- Docker
- CloudLinux
- NodeJS

---

# 13. Automatic Recovery

DirectAdmin có khả năng:
- Tự restart service khi lỗi
- Giảm downtime server

## Ví dụ

Nếu Apache bị crash → hệ thống tự restart.

---

# 14. Ưu điểm của DirectAdmin

| Ưu điểm | Mô tả |
|---|---|
| Nhẹ | Ít tốn RAM/CPU |
| Nhanh | Tối ưu hiệu năng |
| Giá rẻ | License thấp hơn cPanel |
| Ổn định | Ít crash |
| Dễ backup | Có sẵn backup tools |

---

# 15. Nhược điểm của DirectAdmin

| Nhược điểm | Mô tả |
|---|---|
| Ít phổ biến hơn cPanel | Ít tutorial hơn |
| Giao diện đơn giản | Không đẹp bằng cPanel |
| Cần kỹ thuật hơn | Phù hợp người biết Linux |
