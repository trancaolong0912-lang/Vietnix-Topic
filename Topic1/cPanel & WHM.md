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
# II. cPanel Features

# 1. Email

Các tính năng quản lý email theo tên miền riêng.

| Tính năng | Công dụng | Ví dụ thực tế |
|---|---|---|
| Email Accounts | Tạo và quản lý email domain | Tạo `support@company.com` |
| Forwarders | Chuyển tiếp email sang địa chỉ khác | Email gửi tới `support@company.com` sẽ chuyển sang Gmail cá nhân |
| Email Routing | Cấu hình đường đi email | Chuyển mail sang Google Workspace |
| Autoresponders | Tự động phản hồi email | Tự động gửi: “Chúng tôi đã nhận được yêu cầu của bạn” |
| Default Address | Email mặc định nhận thư lỗi | Nhận email gửi sai địa chỉ |
| Mailing Lists | Tạo danh sách gửi mail hàng loạt | Gửi thông báo tới toàn bộ nhân viên |
| Track Delivery | Kiểm tra trạng thái gửi email | Kiểm tra mail có bị lỗi hay không |
| Email Filters | Lọc email | Tự động đưa mail spam vào thùng rác |
| Email Deliverability | Kiểm tra cấu hình gửi mail | Kiểm tra SPF/DKIM |
| Address Importer | Import danh sách email | Upload danh sách email nhân viên |
| Spam Filters | Chống spam email | Chặn email quảng cáo rác |
| BoxTrapper | Chống spam nâng cao | Yêu cầu người gửi xác minh |
| Email Disk Usage | Kiểm tra dung lượng email | Kiểm tra mailbox nào chiếm nhiều dung lượng |
| ASSP Antispam | Hệ thống chống spam | Phân tích và lọc mail độc hại |

---

# 2. File

Các tính năng quản lý file và dữ liệu website.

| Tính năng | Công dụng | Ví dụ thực tế |
|---|---|---|
| File Manager | Quản lý file trực tiếp | Upload source code WordPress |
| Images | Quản lý và tối ưu hình ảnh | Resize ảnh website |
| Directory Privacy | Đặt mật khẩu thư mục | Khóa thư mục admin |
| Disk Usage | Kiểm tra dung lượng | Xem thư mục nào chiếm nhiều GB |
| Web Disk | Quản lý file như ổ đĩa mạng | Kết nối hosting như ổ cứng máy tính |
| FTP Accounts | Quản lý tài khoản FTP | Cấp FTP cho developer |
| Backup Wizard | Sao lưu dữ liệu | Backup website trước khi update |
| Git Version Control | Quản lý source code Git | Deploy website từ GitHub |
| JetBackup 5 | Backup nâng cao | Restore website chỉ với vài click |

---

# 3. Database

Các công cụ quản lý cơ sở dữ liệu.

| Tính năng | Công dụng | Ví dụ thực tế |
|---|---|---|
| phpMyAdmin | Quản lý database trên web | Sửa dữ liệu user WordPress |
| MySQL Databases | Tạo database MySQL | Tạo DB cho website mới |
| MySQL Database Wizard | Tạo database tự động | Tự động tạo DB + user |
| Remote MySQL | Cho phép kết nối DB từ xa | Kết nối database bằng Navicat |

---

# 4. Domain

Các tính năng quản lý domain và DNS.

| Tính năng | Công dụng | Ví dụ thực tế |
|---|---|---|
| WP Toolkit | Quản lý WordPress | Update plugin WordPress |
| Site Publisher | Tạo website cơ bản nhanh | Tạo landing page đơn giản |
| Domain | Quản lý domain | Add thêm domain vào hosting |
| Redirects | Chuyển hướng domain | Chuyển `abc.com` sang `xyz.com` |
| Zone Editor | Quản lý DNS Record | Thêm record TXT xác minh Google |
| Dynamic DNS | DNS động | Camera IP dùng IP động |
| IP Manager | Quản lý IP | Gán IP riêng cho website |

---

# 5. Metrics

Các công cụ theo dõi hiệu năng và traffic.

| Tính năng | Công dụng | Ví dụ thực tế |
|---|---|---|
| Visitors | Theo dõi lượt truy cập | Xem IP truy cập website |
| Errors | Kiểm tra lỗi website | Xem lỗi `500 Internal Server Error` |
| Bandwidth | Theo dõi băng thông | Kiểm tra traffic tháng |
| Raw Access | Xem log truy cập | Phân tích request user |
| Resource Usage | Kiểm tra CPU/RAM sử dụng | Phát hiện website quá tải |

---

# 6. Security

Các tính năng bảo mật hosting và server.

| Tính năng | Công dụng | Ví dụ thực tế |
|---|---|---|
| SSH Access | Truy cập server bằng SSH | Dùng terminal quản trị Linux |
| IP Blocker | Chặn IP | Block IP spam |
| SSL/TLS | Quản lý SSL | Cài HTTPS cho website |
| Manage API Tokens | Quản lý API Token | Kết nối ứng dụng ngoài |
| Hotlink & Leech Protection | Chống hotlink và leech | Chặn website khác lấy ảnh |
| SSL/TLS Status | Kiểm tra trạng thái SSL | Kiểm tra SSL hết hạn |
| Two-Factor Authentication | Xác thực 2 lớp | Login bằng OTP |
| Imunify360 | Hệ thống bảo mật nâng cao | Quét malware website |

---

# 7. Software

Các công cụ cài đặt và quản lý phần mềm.

| Tính năng | Công dụng | Ví dụ thực tế |
|---|---|---|
| WordPress Manager by Softaculous | Quản lý WordPress | Login admin WordPress nhanh |
| Setup Node.js App | Chạy ứng dụng Node.js | Deploy API ExpressJS |
| MultiPHP Manager | Quản lý phiên bản PHP | Website A dùng PHP 8.2 |
| MultiPHP INI Editor | Chỉnh cấu hình PHP | Tăng `upload_max_filesize` |
| Select PHP Version | Chọn phiên bản PHP | Chuyển PHP 7.4 → 8.2 |

---

# 8. Advanced

Các tính năng nâng cao cho server và website.

| Tính năng | Công dụng | Ví dụ thực tế |
|---|---|---|
| LiteSpeed Web Cache Manager | Quản lý cache LiteSpeed | Tăng tốc WordPress |
| Terminal | Dùng command line | Chạy lệnh Linux |
| Cron Jobs | Tạo tác vụ tự động | Backup database mỗi ngày |
| Indexes | Quản lý index thư mục | Chặn xem danh sách file |
| Track DNS | Kiểm tra DNS | Kiểm tra domain đã trỏ đúng chưa |
| Error Pages | Tùy chỉnh trang lỗi | Tạo trang `404 Not Found` riêng |
| Apache Handlers | Quản lý Apache | Xử lý file PHP |
| MIME Types | Quản lý định dạng file | Thêm MIME cho `.webp` |

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
