<img width="1359" height="704" alt="image" src="https://github.com/user-attachments/assets/ab032527-f2c7-439f-9275-8a189cdea1a8" /><img width="805" height="541" alt="image" src="https://github.com/user-attachments/assets/40ba3e75-e44f-45d6-b423-9de0f59a1cbe" />
# allow port, allow ip trên window fw
## check trạng thái từ máy client

<img width="1105" height="234" alt="image" src="https://github.com/user-attachments/assets/0f180688-450d-435c-b058-2a932c17d0c9" />

port 80 đã bị fw drop

## 1.tiến hành mở port 80 và chỉ định ip 115.78.5.187 được phép remote vào server
## allow port

- B1: VÀO Tools - > window fw with advance secuiry

<img width="1816" height="941" alt="image" src="https://github.com/user-attachments/assets/c4b4029d-d9fe-4758-903b-c344b35581be" />
- B2: Chọn inbounds - > new rules 
<img width="1818" height="948" alt="image" src="https://github.com/user-attachments/assets/193edceb-28b7-4dde-9109-e4daaab61784" />

- B3: Làm theo các bước sau

## THAO TÁC TRÊN UI
<img width="713" height="573" alt="image" src="https://github.com/user-attachments/assets/782461d0-1f1e-4b61-8f98-7edb7d941694" />

<img width="702" height="583" alt="image" src="https://github.com/user-attachments/assets/3bf44025-84de-4f29-8ca3-2fd3eb6308b1" />


<img width="710" height="589" alt="image" src="https://github.com/user-attachments/assets/0b2d5f86-9b20-4ae0-b1db-573b570422db" />

<img width="1133" height="919" alt="image" src="https://github.com/user-attachments/assets/1add4d90-ed09-4d18-9cf5-d32923ff73fa" />

# THAO TÁC TRÊN CLI
<img width="1134" height="124" alt="image" src="https://github.com/user-attachments/assets/13a02a32-d308-4b16-a2e1-9111c6ada1dc" />

## kết quả
<img width="1136" height="198" alt="image" src="https://github.com/user-attachments/assets/742b12a7-b9f8-459d-8228-f1faf2a92e80" />

# allow ip remote

# thao tác UI
- dùng 1 ip khác (ip từ mạng 4g) để remote vào server
<img width="1255" height="426" alt="image" src="https://github.com/user-attachments/assets/f0662f79-0c4f-4d86-990c-3b6c36b2c71a" />

- đã kết nối remote thành công vào server khi dùng ip 171.253.251.124
  
<img width="1447" height="774" alt="image" src="https://github.com/user-attachments/assets/317cc4fb-995e-464d-a336-4edb94e021d8" />

- cấu hình chỉ cho phép 115.78.5.187 dc remote vào
  
<img width="722" height="585" alt="image" src="https://github.com/user-attachments/assets/af4672fd-e2e1-4c17-9c4e-244b8f1006ce" />
<img width="721" height="593" alt="image" src="https://github.com/user-attachments/assets/d02dab62-b01f-4f9d-a9fc-98a4c7771f01" />
<img width="713" height="579" alt="image" src="https://github.com/user-attachments/assets/382b8b5c-98fe-4cb9-8567-f947a4fe4875" />
<img width="706" height="575" alt="image" src="https://github.com/user-attachments/assets/35646525-4f49-4606-9c7d-f506aeaea323" />
<img width="730" height="596" alt="image" src="https://github.com/user-attachments/assets/a430bc8a-df51-4bdb-ba1f-b0ba95c046ec" />
  <img width="707" height="580" alt="image" src="https://github.com/user-attachments/assets/ab3acd2b-e4ee-4859-b552-cbdf4c4dea00" />

# thao tác cli

```
New-NetFirewallRule -DisplayName "Allow RDP from 115.78.5.187" `
  -Direction Inbound `
  -Protocol TCP `
  -LocalPort 3389 `
  -RemoteAddress 115.78.5.187 `
  -Action Allow
```
## kết quả

- dùng ip 171.253.251.124 để vô lại
<img width="1297" height="767" alt="image" src="https://github.com/user-attachments/assets/c0b08e99-5ccb-4aa3-b233-c8e15433562e" />

- quay lại ip 115.78.5.187 để xác nhận đăng nhập xem log
  
<img width="1340" height="739" alt="image" src="https://github.com/user-attachments/assets/8ebf1bb4-7d98-48fd-9765-860e044ad9a6" />

# 2. Thực hiện block port 3389, block ip 171.253.251.124 truy cập RDP trên window fw

# block Port 3389

## trên GUI

<img width="710" height="572" alt="image" src="https://github.com/user-attachments/assets/50640313-a37c-4a43-a55b-909678db41f0" />

---

<img width="719" height="598" alt="image" src="https://github.com/user-attachments/assets/0b262fbf-8eb6-47ef-8b83-d6f620f38717" />

---

<img width="728" height="574" alt="image" src="https://github.com/user-attachments/assets/4be192e3-b6ef-4e87-9d7f-ca306c60ce92" />


---

<img width="739" height="558" alt="image" src="https://github.com/user-attachments/assets/22e1ca36-29f4-4829-9602-ff8d5f6b0344" />

## trên CLI

```
New-NetFirewallRule `
-DisplayName "BLOCK_RDP_3389" `
-Direction Inbound `
-Protocol TCP `
-LocalPort 3389 `
-Action Block

```
# block IP 171.253.251.124 truy cập RDP port 3389

# trên GUI
<img width="721" height="722" alt="image" src="https://github.com/user-attachments/assets/6012fbe4-83f7-4fa9-b26e-90c0ba31f325" />

---

<img width="728" height="573" alt="image" src="https://github.com/user-attachments/assets/13c29ff6-7319-4527-b034-9200bad6e448" />


---


<img width="721" height="588" alt="image" src="https://github.com/user-attachments/assets/015f5c37-b90d-4195-bda3-bbacae2b6139" />


---

<img width="721" height="560" alt="image" src="https://github.com/user-attachments/assets/f1398ac5-090d-4e9a-b3ec-0f2d4f78aeec" />

---

<img width="697" height="580" alt="image" src="https://github.com/user-attachments/assets/1a721e10-f474-450a-90c5-a2d084723a54" />

# trên CLI

```
New-NetFirewallRule `
-DisplayName "BLOCK_IP_192.168.0.19_RDP" `
-Direction Inbound `
-Protocol TCP `
-LocalPort 3389 `
-RemoteAddress 192.168.0.19 `
-Action Block
```

# 3.Thực hiện giới hạn port, giới hạn ip trên window fw chỉ cho phép ip chỉ định truy cập

# Giới hạn port 80 chỉ cho phép 1 IP truy cập, các ip khác sẽ bị chặn

# trện GUI
<img width="722" height="583" alt="image" src="https://github.com/user-attachments/assets/6a681e4e-aa26-49bf-9a29-cc26e9ad23eb" />

---
<img width="723" height="576" alt="image" src="https://github.com/user-attachments/assets/15ccd1d7-e657-4804-a86f-fbabe0e06af5" />

<img width="726" height="609" alt="image" src="https://github.com/user-attachments/assets/7b11734a-ddca-40ab-a949-88d3ea448afc" />

---

<img width="1106" height="561" alt="image" src="https://github.com/user-attachments/assets/3db77ef3-54f6-49cb-8620-b1db10a1f7e3" />

--- 

<img width="725" height="588" alt="image" src="https://github.com/user-attachments/assets/e0626517-5ea1-4fb1-bc59-2cce58e517b0" />

---

- Thêm dải ip dc chỉ định

  <img width="674" height="269" alt="image" src="https://github.com/user-attachments/assets/bb55cfcc-9e94-46e8-b7bc-2fe0a6b9f84f" />

<img width="468" height="602" alt="image" src="https://github.com/user-attachments/assets/c5d6a942-8776-456d-920c-0edcd4c3821f" />

<img width="465" height="567" alt="image" src="https://github.com/user-attachments/assets/761443fe-3851-40a2-bd05-3abc45d6c3cc" />




# Thực hành cài đặt
- Webserver IIS, trên Webserver IIS+ Cài đặt website wordpress mặc định+ Cài đặt SSL

- Bước 1: Mở Server Manager
Manage → Add Roles and Features → Next

<img width="1442" height="943" alt="image" src="https://github.com/user-attachments/assets/470e8567-039f-416b-b7b6-c00552b1d497" />

- Bước 2: Add Roles and Features
Manage → Add Roles and Features → Next

<img width="785" height="545" alt="image" src="https://github.com/user-attachments/assets/8c395297-ee73-491d-acd1-a0cb7f6429f4" />

- Bước 3: Chọn Installation Type
Role-based or feature-based installation → Next

<img width="766" height="553" alt="image" src="https://github.com/user-attachments/assets/44285e21-a10a-4537-acd1-fa85bae59f8c" />

Bước 4: Chọn Server
Select a server from the server pool → chọn server hiện tại → Next


<img width="805" height="541" alt="image" src="https://github.com/user-attachments/assets/a946fd53-e8b7-46cf-ac23-a05d532cd99a" />

Bước 5: Chọn Role và install
<img width="807" height="538" alt="image" src="https://github.com/user-attachments/assets/15ebb204-8076-4db4-88e4-5876b7fc66ee" />

<img width="924" height="614" alt="image" src="https://github.com/user-attachments/assets/500da1de-c9fe-4f8a-b104-95986be79912" />

<img width="685" height="509" alt="image" src="https://github.com/user-attachments/assets/968f9157-738d-4967-9c15-593a197752d6" />

<img width="777" height="589" alt="image" src="https://github.com/user-attachments/assets/2350e517-fad9-4857-b010-04abf491f7ec" />

- hoàn tất cài

<img width="798" height="563" alt="image" src="https://github.com/user-attachments/assets/dd5ed4d2-8183-4bbf-a511-a951fa983093" />

# Phần 2: cài đặt PHP 8.1

```
https://windows.php.net/download/
→ PHP 8.x Non-Thread Safe x64
→ Giải nén vào C:\PHP
```
  <img width="1353" height="901" alt="image" src="https://github.com/user-attachments/assets/0880a0dd-a023-4631-a45c-3e9a8e1cca68" />

-   sửa tên file  ```php.ini-production``` và đổi tên thành ```php.ini``` Cấu hình php.ini
-   
<img width="942" height="392" alt="image" src="https://github.com/user-attachments/assets/5efd66dc-844c-413b-80fd-a94dac7b58bc" />

- edit file php.ini và bỏ dấu ";" các dòng sau
extension=mysqli
extension=gd
extension=mbstring
extension=openssl
extension=curl
<img width="985" height="679" alt="image" src="https://github.com/user-attachments/assets/d48c8ac0-8774-4f7c-b4f1-16e2109081de" />
## Kết nối PHP với IIS 
- thêm PHP vào PATH

  <img width="1816" height="956" alt="image" src="https://github.com/user-attachments/assets/c6f2e062-43a3-4e56-b08c-fae11f8ed839" />

 <img width="791" height="214" alt="image" src="https://github.com/user-attachments/assets/f0d294c7-458c-406b-ab40-cc04b67a82ea" />

# đăng kí PHP vào IIS
-  B1:Mở IIS Manager (Internet Information Services).
  
<img width="1621" height="809" alt="image" src="https://github.com/user-attachments/assets/d05a2aba-f06c-4a21-aa40-6c05226d1f67" />

- B2: ADD MODULE MAPPING

<img width="1611" height="767" alt="image" src="https://github.com/user-attachments/assets/c0520346-6352-4fa2-8cd5-85e39654d19c" />

<img width="1534" height="671" alt="image" src="https://github.com/user-attachments/assets/e7eda1df-9ed7-4680-b219-9979405d85ee" />


  # PHẦN 3: CÀI MYSQL

- B1: MOUNT FILE MSSQL.ISO

<img width="832" height="507" alt="image" src="https://github.com/user-attachments/assets/2cdcfc46-19b5-4a3f-b64e-2c9eb37aa11f" />

- B2: CHẠY  SETUP

<img width="1224" height="420" alt="image" src="https://github.com/user-attachments/assets/06ccf750-547a-43d8-b641-8c8a743d0f04" />

<img width="783" height="594" alt="image" src="https://github.com/user-attachments/assets/f3cfb153-a399-4677-8fc4-2b9867c3a667" />

<img width="625" height="497" alt="image" src="https://github.com/user-attachments/assets/183d1090-99d5-4508-8a2e-5574eb555794" />

<img width="1605" height="778" alt="image" src="https://github.com/user-attachments/assets/c86bd3c6-cd23-4097-bd6f-31915aea1345" />

<img width="1777" height="802" alt="image" src="https://github.com/user-attachments/assets/2286056f-0de9-4391-9720-123a8c87daf6" />

cài thêm mysql
- hoàn tất cài đặt

<img width="830" height="617" alt="image" src="https://github.com/user-attachments/assets/31356e95-d5eb-43c0-a24c-1d40bbcef571" />

- B3: Cài đặt WordPress trên IIS

  <img width="1757" height="878" alt="image" src="https://github.com/user-attachments/assets/931ace26-7a46-44e8-8aae-8c0ac76b9e04" />

- B4: Move tới C:\inetpub\wwwroot\wordpress
  <img width="1204" height="677" alt="image" src="https://github.com/user-attachments/assets/e646d20f-6f9d-429b-a609-efa7425fd8a0" />

- B5: Cấu hình IIS cho WordPress

  <img width="1681" height="955" alt="image" src="https://github.com/user-attachments/assets/8871fe44-5023-44f4-a685-7a9af18158cf" />

- B6: Cài URL Rewrite module

  <img width="899" height="78" alt="image" src="https://github.com/user-attachments/assets/49e381ad-487f-418f-80f8-718684df719e" />

- B7: EDIT wordpress.conf

   <img width="1359" height="704" alt="image" src="https://github.com/user-attachments/assets/bf3e3be7-b5f1-4476-875c-31fc6af605ea" />

<img width="1632" height="843" alt="image" src="https://github.com/user-attachments/assets/005bfc16-c5cf-48cb-b127-b9970e085ed8" />

<img width="1440" height="888" alt="image" src="https://github.com/user-attachments/assets/cb58e5ce-c404-4976-9607-26953bc4fb40" />

<img width="1758" height="974" alt="image" src="https://github.com/user-attachments/assets/197ece8a-c227-4ec4-88be-032856f88ff4" />

cài ssl

<img width="1622" height="927" alt="image" src="https://github.com/user-attachments/assets/4af7cafb-177c-4c13-93bc-ebff48dfa64e" />

<img width="1665" height="806" alt="image" src="https://github.com/user-attachments/assets/c5233b96-62c4-40ee-8765-1a9e711bbf6b" />


<img width="1621" height="901" alt="image" src="https://github.com/user-attachments/assets/3698bbc4-fd4f-4fdb-ad5c-c25ce74bda05" />

<img width="701" height="397" alt="image" src="https://github.com/user-attachments/assets/eddf5d95-55af-45ae-8060-8e6e5ca57470" />


<img width="686" height="236" alt="image" src="https://github.com/user-attachments/assets/30b6a192-dda2-4940-afca-9975a75c4204" />

<img width="1819" height="933" alt="image" src="https://github.com/user-attachments/assets/b427ac93-233f-4831-a923-40cd8cc1af52" />
