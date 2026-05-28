
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

