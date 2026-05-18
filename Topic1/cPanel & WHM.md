# cPanel Interface


---

# 1. Search Bar

Thanh tìm kiếm tính năng trong cPanel.

Do cPanel có rất nhiều chức năng nên người dùng có thể sử dụng ô tìm kiếm để truy cập nhanh công cụ cần dùng.

## Ví dụ

Muốn tìm:

```txt
File Manager
```

chỉ cần nhập:

```txt
file
```

hệ thống sẽ tự động hiển thị tính năng liên quan.

---

# 2. General Information

Khu vực hiển thị thông tin tổng quan của tài khoản hosting và server.

## Bao gồm
- Current User
- Primary Domain
- Home Directory
- Shared IP Address
- Last Login IP
- Server Information

## Công dụng
- Kiểm tra thông tin hosting
- Theo dõi IP server
- Xác định tài khoản đang sử dụng

---

# 3. Statistics

Khu vực thống kê tài nguyên hosting đang sử dụng.

## Bao gồm
- RAM Usage
- CPU Usage
- Processes
- Disk Usage
- Bandwidth
- Email Accounts
- Addon Domains
- Subdomains

## Công dụng
- Theo dõi hiệu năng hosting
- Kiểm tra giới hạn tài nguyên
- Phát hiện website quá tải

---

# 4. Features

Khu vực chứa toàn bộ tính năng quản trị của cPanel.

## Một số tính năng phổ biến

| Tính năng | Công dụng |
|---|---|
| File Manager | Quản lý file website |
| FTP Accounts | Quản lý FTP |
| Email Accounts | Tạo email domain |
| phpMyAdmin | Quản lý database |
| SSL/TLS | Quản lý SSL |
| Backup | Sao lưu dữ liệu |
| Cron Jobs | Tạo tác vụ tự động |
| Domains | Quản lý domain |

---

# Tổng quan hoạt động của cPanel

```txt
Người dùng
     ↓
Đăng nhập cPanel
     ↓
Quản lý:
- Website
- Domain
- Database
- Email
- File
- Backup
     ↓
Server xử lý và vận hành website
```
# II.cPanel Features

# 1. Email

Các tính năng quản lý email theo tên miền riêng.

| Tính năng | Công dụng |
|---|---|
| Email Accounts | Tạo và quản lý email domain |
| Forwarders | Chuyển tiếp email sang địa chỉ khác |
| Email Routing | Cấu hình đường đi email |
| Autoresponders | Tự động phản hồi email |
| Default Address | Email mặc định nhận thư lỗi |
| Mailing Lists | Tạo danh sách gửi mail hàng loạt |
| Track Delivery | Kiểm tra trạng thái gửi email |
| Email Filters | Lọc email |
| Email Deliverability | Kiểm tra cấu hình gửi mail |
| Address Importer | Import danh sách email |
| Spam Filters | Chống spam email |
| BoxTrapper | Chống spam nâng cao |
| Email Disk Usage | Kiểm tra dung lượng email |
| ASSP Antispam | Hệ thống chống spam |

---

# 2. File

Các tính năng quản lý file và dữ liệu website.

| Tính năng | Công dụng |
|---|---|
| File Manager | Quản lý file trực tiếp |
| Images | Quản lý và tối ưu hình ảnh |
| Directory Privacy | Đặt mật khẩu thư mục |
| Disk Usage | Kiểm tra dung lượng |
| Web Disk | Quản lý file như ổ đĩa mạng |
| FTP Accounts | Quản lý tài khoản FTP |
| Backup Wizard | Sao lưu dữ liệu |
| Git Version Control | Quản lý source code Git |
| JetBackup 5 | Backup nâng cao |

---

# 3. Database

Các công cụ quản lý cơ sở dữ liệu.

| Tính năng | Công dụng |
|---|---|
| phpMyAdmin | Quản lý database trên web |
| MySQL Databases | Tạo database MySQL |
| MySQL Database Wizard | Tạo database tự động |
| Remote MySQL | Cho phép kết nối DB từ xa |

---

# 4. Domain

Các tính năng quản lý domain và DNS.

| Tính năng | Công dụng |
|---|---|
| WP Toolkit | Quản lý WordPress |
| Site Publisher | Tạo website cơ bản nhanh |
| Domain | Quản lý domain |
| Redirects | Chuyển hướng domain |
| Zone Editor | Quản lý DNS Record |
| Dynamic DNS | DNS động |
| IP Manager | Quản lý IP |

---

# 5. Metrics

Các công cụ theo dõi hiệu năng và traffic.

| Tính năng | Công dụng |
|---|---|
| Visitors | Theo dõi lượt truy cập |
| Errors | Kiểm tra lỗi website |
| Bandwidth | Theo dõi băng thông |
| Raw Access | Xem log truy cập |
| Resource Usage | Kiểm tra CPU/RAM sử dụng |

---

# 6. Security

Các tính năng bảo mật hosting và server.

| Tính năng | Công dụng |
|---|---|
| SSH Access | Truy cập server bằng SSH |
| IP Blocker | Chặn IP |
| SSL/TLS | Quản lý SSL |
| Manage API Tokens | Quản lý API Token |
| Hotlink & Leech Protection | Chống hotlink và leech |
| SSL/TLS Status | Kiểm tra trạng thái SSL |
| Two-Factor Authentication | Xác thực 2 lớp |
| Imunify360 | Hệ thống bảo mật nâng cao |

---

# 7. Software

Các công cụ cài đặt và quản lý phần mềm.

| Tính năng | Công dụng |
|---|---|
| WordPress Manager by Softaculous | Quản lý WordPress |
| Setup Node.js App | Chạy ứng dụng Node.js |
| MultiPHP Manager | Quản lý phiên bản PHP |
| MultiPHP INI Editor | Chỉnh cấu hình PHP |
| Select PHP Version | Chọn phiên bản PHP |

---

# 8. Advanced

Các tính năng nâng cao cho server và website.

| Tính năng | Công dụng |
|---|---|
| LiteSpeed Web Cache Manager | Quản lý cache LiteSpeed |
| Terminal | Dùng command line |
| Cron Jobs | Tạo tác vụ tự động |
| Indexes | Quản lý index thư mục |
| Track DNS | Kiểm tra DNS |
| Error Pages | Tùy chỉnh trang lỗi |
| Apache Handlers | Quản lý Apache |
| MIME Types | Quản lý định dạng file |

# III. WHM

WHM (Web Host Manager) là công cụ quản trị server dành cho:
- Admin
- Reseller Hosting
- Quản trị viên hệ thống

WHM cho phép quản lý:
- Hosting account
- Tài nguyên server
- Domain
- Security
- Process hệ thống

---

# 1. Terminal

Cho phép truy cập command line trực tiếp trên server thông qua trình duyệt.

## Công dụng
- Chạy lệnh Linux
- Quản trị server
- Kiểm tra hệ thống
- Cài đặt phần mềm

---

# 2. Change Default Domain

Tính năng thay đổi domain mặc định của hosting account.

## Công dụng
- Đổi domain chính cho user hosting
- Chuyển website sang domain mới

---

# 3. Transfer Account

Công cụ chuyển dữ liệu hosting giữa các server WHM/cPanel.

## Công dụng
- Migration website
- Chuyển hosting sang server mới
- Sao chép account cPanel

---

# 4. Kiểm tra nghẽn Process / CPU

WHM hỗ trợ kiểm tra:
- CPU Usage
- RAM Usage
- Process hệ thống

## Công dụng
- Phát hiện website quá tải
- Kiểm tra user dùng quá nhiều tài nguyên
- Tối ưu hiệu năng server

---

# 5. PHP X-Ray

Công cụ phân tích hiệu năng PHP và WordPress.

## Công dụng
- Kiểm tra plugin WordPress gây chậm
- Phân tích request PHP
- Tìm bottleneck hệ thống
- Debug website chậm

---

# 6. Kĩ năng quản trị khác trong WHM

## 6.1 Imunify360

Hệ thống bảo mật nâng cao cho server.

### Công dụng
- Quét virus
- Chặn malware
- Chống brute force
- Bảo vệ website

---

## 6.2 Check Subdomain thuộc user nào

Kiểm tra subdomain thuộc tài khoản hosting nào.

### Công dụng
- Quản lý hosting
- Kiểm tra ownership domain

---

## 6.3 Check domlogs

Kiểm tra log truy cập domain.

### Công dụng
- Theo dõi traffic
- Debug lỗi website
- Phân tích request

---

## 6.4 Check process đang chạy của user

Kiểm tra process của từng hosting account.

### Công dụng
- Phát hiện process lỗi
- Kiểm tra user dùng CPU cao
- Debug website chậm

---

## 6.5 Reload User Hosting

Khởi động lại dịch vụ hosting của user.

### Công dụng
- Reload cấu hình
- Reset session hosting
- Khắc phục lỗi tạm thời

---

## 6.6 Check website WordPress chậm bằng PHP X-Ray

Sử dụng PHP X-Ray để phân tích website WordPress.

### Có thể kiểm tra:
- Plugin chậm
- Query database chậm
- Theme lỗi
- Request PHP tiêu tốn tài nguyên

---

# Mối quan hệ giữa WHM và cPanel

```txt
WHM
 ↓
Quản lý Server
 ↓
Tạo Account cPanel
 ↓
Người dùng quản lý Website
```
