# SSL

## SSL là gì?

SSL (Secure Sockets Layer) là giao thức mã hóa dữ liệu giữa client và server nhằm:

- Bảo mật dữ liệu truyền tải.
- Chống nghe lén (sniffing).
- Xác thực website/server.
- Đảm bảo tính toàn vẹn dữ liệu.

Hiện nay SSL đã được thay thế bởi TLS (Transport Layer Security), nhưng người ta vẫn thường gọi chung là SSL.

Website dùng SSL sẽ có:

- `https://`
- Biểu tượng ổ khóa trên trình duyệt.

---

## Có bao nhiêu cách xác thực SSL?

### 1. DV SSL (Domain Validation)

Xác thực quyền sở hữu domain.

Ví dụ:

- xác nhận qua email
- DNS record
- HTTP file

Đây là loại phổ biến nhất.

---

### 2. OV SSL (Organization Validation)

Xác thực:

- domain
- thông tin doanh nghiệp/tổ chức

Mức độ tin cậy cao hơn DV.

---

### 3. EV SSL (Extended Validation)

Xác thực chuyên sâu doanh nghiệp:

- giấy phép kinh doanh
- thông tin pháp lý
- tổ chức sở hữu

Độ tin cậy cao nhất.

---

## CSR file dùng để làm gì?

CSR (Certificate Signing Request) là file dùng để:

- gửi yêu cầu cấp SSL đến CA (Certificate Authority)
- chứa:
  - domain
  - organization
  - public key
  - thông tin doanh nghiệp

CA sẽ dùng CSR để tạo SSL Certificate.

---

## Gen CSR file và request SSL bằng OpenSSL

Ví dụ domain:

```bash
tech.training.vietnix.tech
```

### Generate Private Key

```bash
openssl genrsa -out tech.training.vietnix.tech.key 2048
```

---

### Generate CSR

```bash
openssl req -new \
-key tech.training.vietnix.tech.key \
-out tech.training.vietnix.tech.csr
```

Sau đó nhập:

```text
Country Name
State
Locality
Organization
Common Name
Email
```

`Common Name` phải là:

```text
tech.training.vietnix.tech
```

---

### Kiểm tra nội dung CSR

```bash
openssl req -text -noout -verify \
-in tech.training.vietnix.tech.csr
```

---

## PEM file là gì?

PEM (Privacy Enhanced Mail) là định dạng file chứa:

- certificate
- private key
- public key

PEM thường có đuôi:

- `.pem`
- `.crt`
- `.cer`
- `.key`

Nội dung dạng:

```text
-----BEGIN CERTIFICATE-----
...
-----END CERTIFICATE-----
```

---

## Private Key SSL là gì?

Private Key là khóa bí mật dùng để:

- giải mã dữ liệu SSL/TLS
- xác thực certificate

Ví dụ:

```text
-----BEGIN PRIVATE KEY-----
```

Private key phải được bảo mật tuyệt đối.

Nếu lộ private key:

- SSL không còn an toàn
- attacker có thể giả mạo server

---

## PFX file là gì?

PFX (PKCS#12) là file chứa:

- certificate
- private key
- intermediate certificate

Thường dùng trên:

- Windows Server
- IIS
- Microsoft Exchange

Đuôi file:

```text
.pfx
.p12
```

---

## Chuyển từ CRT sang PFX

Ví dụ có:

- `domain.crt`
- `domain.key`

Lệnh:

```bash
openssl pkcs12 -export \
-out domain.pfx \
-inkey domain.key \
-in domain.crt
```

Nếu có CA Bundle:

```bash
openssl pkcs12 -export \
-out domain.pfx \
-inkey domain.key \
-in domain.crt \
-certfile ca-bundle.crt
```

---

# Domain

## Domain là gì?

Domain là tên định danh của website trên Internet.

Ví dụ:

```text
google.com
vietnix.vn
```

Domain giúp người dùng truy cập website dễ dàng thay vì dùng IP.

---

## Các trạng thái của domain

| Trạng thái | Ý nghĩa |
|---|---|
| Active | Domain đang hoạt động |
| Expired | Domain hết hạn |
| Redemption | Giai đoạn chuộc domain |
| Pending Delete | Sắp bị xóa |
| Transfer Lock | Khóa transfer domain |
| Client Hold | Domain bị tạm ngưng |

---

## Subdomain là gì?

Subdomain là domain con của domain chính.

Ví dụ:

| Domain chính | Subdomain |
|---|---|
| vietnix.vn | blog.vietnix.vn |
| vietnix.vn | mail.vietnix.vn |

Subdomain thường dùng để:

- tách service
- blog
- mail
- api
- staging

---

## Virtual Hosts là gì?

Virtual Host là cơ chế cho phép:

- nhiều website chạy trên cùng 1 server/IP.

Ví dụ:

- `site1.com`
- `site2.com`

cùng chạy trên Apache/Nginx.

---

# Mail Server

## MX Record là gì?

MX (Mail Exchange) Record dùng để xác định mail server nhận email cho domain.

Ví dụ:

```dns
example.com.  IN MX 10 mail.example.com.
```

Ý nghĩa:

- mail gửi tới `example.com`
- sẽ được chuyển tới `mail.example.com`

Priority càng nhỏ càng ưu tiên cao.

---

## DKIM là gì?

DKIM (DomainKeys Identified Mail) dùng để:

- ký điện tử email
- xác thực email không bị giả mạo

Hoạt động bằng:

- private key
- public key DNS record

Giúp giảm spam/phishing.

---

## SPF là gì?

SPF (Sender Policy Framework) dùng để:

- xác định server nào được phép gửi mail cho domain.

Ví dụ:

```dns
v=spf1 ip4:1.2.3.4 include:_spf.google.com ~all
```

Giúp chống giả mạo email.

---

## PTR là gì?

PTR (Pointer Record) là reverse DNS.

Dùng để:

- ánh xạ IP → domain

Ví dụ:

```text
1.2.3.4 -> mail.example.com
```

Mail server thường kiểm tra PTR để chống spam.

---

# DNS

## DNS là gì?

DNS (Domain Name System) là hệ thống phân giải:

```text
Domain -> IP
```

Ví dụ:

```text
google.com -> 142.250.x.x
```

DNS giúp người dùng truy cập website bằng tên thay vì IP.

---

## Các loại record DNS

| Record | Chức năng |
|---|---|
| A | Domain → IPv4 |
| AAAA | Domain → IPv6 |
| CNAME | Alias domain |
| MX | Mail server |
| TXT | Text record |
| NS | Name Server |
| PTR | Reverse DNS |
| SRV | Service record |
| SOA | Start of Authority |

---

## Nguyên tắc làm việc của DNS

Quá trình hoạt động:

1. User nhập domain.
2. Browser kiểm tra cache.
3. Hỏi Recursive DNS Resolver.
4. Resolver hỏi:
   - Root DNS
   - TLD DNS
   - Authoritative DNS
5. Nhận IP.
6. Browser kết nối server.

---

## Cách phân giải địa chỉ DNS

Ví dụ truy cập:

```text
google.com
```

Quy trình:

```text
Client
   ↓
Local DNS Cache
   ↓
Recursive DNS
   ↓
Root DNS
   ↓
.com TLD DNS
   ↓
Authoritative DNS
   ↓
IP Address trả về
```

Sau khi có IP:

```text
Browser -> Web Server
```

Website sẽ được tải lên.
