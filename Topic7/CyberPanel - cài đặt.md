<img width="1200" height="162" alt="image" src="https://github.com/user-attachments/assets/5dc6aaaa-3e9e-46cb-8aea-5f117db6a324" /><img width="1135" height="173" alt="image" src="https://github.com/user-attachments/assets/0260cda3-058f-4bf2-aa30-90aec4b19a81" />## Chuẩn bị môi trường cài đặt CyberPanel

- B1: SSH vào VPS
  

<img width="1121" height="526" alt="image" src="https://github.com/user-attachments/assets/518c20c3-e0c8-47bd-ad7d-749b14e4ac75" />


- Bước 2: Cài đặt CyberPanel
  
  
<img width="890" height="420" alt="image" src="https://github.com/user-attachments/assets/78b36d7b-88c5-416a-9fcb-c3a15522b4f0" />


- Sau đó nhập lệnh dưới đây vào terminal để bắt đầu cài đặt CyberPanel:
  

<img width="1284" height="545" alt="image" src="https://github.com/user-attachments/assets/168cd4f0-3b3c-4efc-8e12-23655ed091c6" />


<img width="597" height="566" alt="image" src="https://github.com/user-attachments/assets/989aa8ec-dad1-41c9-a52e-3a0d2cc9eef7" />

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


