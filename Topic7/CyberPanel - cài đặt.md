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

