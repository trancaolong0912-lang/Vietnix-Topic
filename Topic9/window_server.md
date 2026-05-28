
## allow port, allow ip trên window fw
# check trạng thái từ máy client

<img width="1105" height="234" alt="image" src="https://github.com/user-attachments/assets/0f180688-450d-435c-b058-2a932c17d0c9" />

port 80 đã bị fw drop

# 1.tiến hành mở port 80 và chỉ định ip 115.78.5.187 được phép remote vào server
# allow port

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




