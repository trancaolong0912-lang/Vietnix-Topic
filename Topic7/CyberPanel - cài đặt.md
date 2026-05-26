# Chuẩn bị môi trường cài đặt CyberPanel

- B1: SSH vào VPS
  

<img width="1121" height="526" alt="image" src="https://github.com/user-attachments/assets/518c20c3-e0c8-47bd-ad7d-749b14e4ac75" />


- Bước 2: Cài đặt CyberPanel
  
UPDATE & UPGRADE UBUNTU

<img width="890" height="420" alt="image" src="https://github.com/user-attachments/assets/78b36d7b-88c5-416a-9fcb-c3a15522b4f0" />


- Sau đó nhập lệnh dưới đây vào terminal để bắt đầu cài đặt CyberPanel:
  
<img width="1238" height="53" alt="image" src="https://github.com/user-attachments/assets/96aa2955-3494-4b04-aa53-9c9136ff9947" />

- Tiếp đó,chọn 1 nếu muốn cài đặt CyberPanel với OpenLiteSpeed (miễn phí):
  

<img width="634" height="363" alt="image" src="https://github.com/user-attachments/assets/4839bf02-e183-4f44-a641-24350d677a29" />

- Sau đó nhập Y để cài đặt CyberPanel với đầy đủ các dịch vụ như PowerDNS, Postfix và Pure-FTPd.
  

<img width="1135" height="173" alt="image" src="https://github.com/user-attachments/assets/fc1e0390-0a33-42e5-9b24-93aac04cf67f" />

- Hệ thống sẽ hỏi có muốn cài đặt Remote MySQL không,nhập Y để chấp nhận cài đăt. và nhập ip host để remote
  

<img width="1423" height="347" alt="image" src="https://github.com/user-attachments/assets/21821540-72bf-4435-9c60-bc0642ffe0cd" />

- cài đặt password cho admin, ko nhập thì pass mặc định là 1234567
  

  <img width="1276" height="180" alt="image" src="https://github.com/user-attachments/assets/fd3f5cde-4987-4865-a960-1c7aa57c701b" />


- cài đặt memcached và redis

<img width="753" height="266" alt="image" src="https://github.com/user-attachments/assets/6a5562ac-f706-4681-be9b-255eac64cf4a" />

- cài watchdog để theo dõi các dịch vụ , nếu dịch vụ bị lõi thì chức năng này sẽ tự restart lại dịch vụ

  <img width="1200" height="162" alt="image" src="https://github.com/user-attachments/assets/4b0f52ea-2fa8-4d4c-906a-b6d13cd0353b" />

- cài đặt thành công

<img width="1054" height="922" alt="image" src="https://github.com/user-attachments/assets/08d22188-05d4-4490-9f45-62a05c68ee84" />

- giao diện cyberpanel

  <img width="1838" height="996" alt="image" src="https://github.com/user-attachments/assets/61fb6511-48a6-4699-ba51-e56319fa52c8" />

- tạo website.

<img width="1475" height="965" alt="image" src="https://github.com/user-attachments/assets/26399856-d055-43c6-92a4-7445592293c9" />

 - upload source code

<img width="1845" height="950" alt="image" src="https://github.com/user-attachments/assets/6c8010bb-19a9-4293-9f30-f962b1fae3ca" />

- phân quyền thư mục
- tạo database

<img width="1012" height="62" alt="image" src="https://github.com/user-attachments/assets/bb2110e9-846e-41af-a6b8-2d7df729aa47" />
<img width="1077" height="46" alt="image" src="https://github.com/user-attachments/assets/a696d4fe-192c-4bea-846e-0f59335324bc" />


- tạo database và import

<img width="1504" height="838" alt="image" src="https://github.com/user-attachments/assets/10481ae4-fd81-4c23-a130-d5c39dafce29" />

<img width="1857" height="981" alt="image" src="https://github.com/user-attachments/assets/26b4b623-8af0-4f7e-a925-d6b7f36d7c8b" />

- sửa thông tin login database

laravel:

<img width="501" height="181" alt="image" src="https://github.com/user-attachments/assets/2103d3ac-af0f-4035-8637-37cc1cdd9163" />

wordpress:

<img width="965" height="509" alt="image" src="https://github.com/user-attachments/assets/560553c2-2f05-436b-842d-063840a1904b" />

## 2. Tạo ứng dụng chạy ở port 5000

- B1: Cài python và flask
apt install python3 python3-pip -y

pip3 install flask
- B2: tạo chương trình bất kì
<img width="1193" height="446" alt="image" src="https://github.com/user-attachments/assets/73085398-b858-4869-b54d-b7835a400bc7" />
- B3: Mở port trong firewall của cyberpanel

<img width="1351" height="229" alt="image" src="https://github.com/user-attachments/assets/af83d5d7-bc7c-4796-9157-31228091f585" />

## KẾT QUẢ 


<img width="1356" height="823" alt="image" src="https://github.com/user-attachments/assets/cbd247c0-fb0f-478d-9488-e5e9be7ee0f1" />

##  3. Cấu hình ProxyPass trong OpenLiteSpeed để khi người dùng truy cập vào domain/api, kết quả sẽ được chuyển tiếp (proxy) từ ứng dụng chạy ở port 5000.

- B1: TẠO USER
<img width="915" height="328" alt="image" src="https://github.com/user-attachments/assets/6cb43d15-e385-47de-8e41-e9d19156cdcd" />

- B2: ĐĂNG NHẬP VÀO OpenLiteSpeed

  <img width="1829" height="972" alt="image" src="https://github.com/user-attachments/assets/92a712f0-490a-430e-9068-ddac792f26e7" />


- Bước 3: Tạo proxy (External App)

<img width="1829" height="581" alt="image" src="https://github.com/user-attachments/assets/eca86f0e-071d-47fa-9f6c-2096f18f52cf" />

- Bước 4: Tại mục Type, bạn chọn Web Server và nhấn dấu mũi tên để chuyển sang bước tiếp theo.

<img width="1529" height="642" alt="image" src="https://github.com/user-attachments/assets/7c9282fa-5f00-4e71-98b5-3f04e39c9a50" />

Cuối cùng, điền đầy đủ các thông tin cần thiết cho proxy và nhấn Save:

- Name: Tên gọi cho proxy.
- Address: Địa chỉ IP của ứng dụng backend.
- Max Connections: Số lượng kết nối tối đa.
- Initial Request Timeout (sec): Thời gian chờ yêu cầu ban đầu (ví dụ: 60 giây).
- Retry Timeout (secs): Thời gian chờ thử lại (thường là 0 giây).
- Response Buffering: Chọn No.

<img width="1815" height="1002" alt="image" src="https://github.com/user-attachments/assets/27ba1e18-c491-4e3b-90dc-c22ea4169f7f" />

- Bước 5: Cấu hình Proxy vào website

Sau khi đã tạo proxy, bạn cần cấu hình website trên CyberPanel để chuyển hướng các yêu cầu đến proxy này. Bạn quay lại trang quản lý của CyberPanel và chọn Websites, sau đó chọn List Websites. Nhấn vào nút Manage tại website mà bạn muốn cấu hình proxy.

Sau đó bạn kéo xuống mục Configuration, chọn vHost Conf và thêm hai dòng sau vào cuối hàm rewrite có tham số enable là 1 (thường là trong file .htaccess ảo của vHost):

<img width="1520" height="738" alt="image" src="https://github.com/user-attachments/assets/8acd1a4e-3f28-4459-b0c5-f157e0fb4b23" />

<img width="1495" height="438" alt="image" src="https://github.com/user-attachments/assets/af1dec9a-4159-4a78-9600-8c079e9f574d" />

<img width="1302" height="725" alt="image" src="https://github.com/user-attachments/assets/2661fb9d-c5ab-4031-a998-9988c8fd24fe" />

<img width="1685" height="961" alt="image" src="https://github.com/user-attachments/assets/e623a602-7c62-45f9-a89a-2c738bd8d630" />


## KẾT QUẢ

## LARAVEL:

<img width="1206" height="638" alt="image" src="https://github.com/user-attachments/assets/1112fa30-75e4-4087-ad5d-051e0266dfc8" />

## WORDPRESS

<img width="1531" height="700" alt="image" src="https://github.com/user-attachments/assets/5ca8eafe-ac02-4c14-b116-97e2d3dc1221" />

