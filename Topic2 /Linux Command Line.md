**Linux Command Line**
## PING && HPING3

## PING
<img width="1430" height="231" alt="image" src="https://github.com/user-attachments/assets/3130d1d2-e100-41f0-8ed2-8595b04e003f" />

## HPING3

<img width="1335" height="504" alt="image" src="https://github.com/user-attachments/assets/23b1b543-4220-4f4f-96ae-d20ee4d32907" />

## SSH
## - ssh bằng password
<img width="1322" height="753" alt="image" src="https://github.com/user-attachments/assets/41707247-f2c9-4a6c-9fdc-9748c92de330" />

## - ssh bằng key

<img width="1392" height="421" alt="image" src="https://github.com/user-attachments/assets/e98b474a-9575-4d26-b070-44e347551538" />

<img width="1330" height="602" alt="image" src="https://github.com/user-attachments/assets/dcfbd07d-a846-4cfc-8888-533ced98165b" />

## - ssh bằng port custom


<img width="1271" height="944" alt="image" src="https://github.com/user-attachments/assets/a7250e08-2bc8-47e2-bfbc-15f15c243ca8" />

<img width="910" height="445" alt="image" src="https://github.com/user-attachments/assets/3dc4c9f9-c954-4b3b-a44f-f6b185293a05" />

## SCP Command
## - copy 1 file
<img width="1413" height="79" alt="image" src="https://github.com/user-attachments/assets/9a72e654-94cf-4b06-b8a9-f2e0f82b31ed" />

## - copy 1 folder 

<img width="1090" height="92" alt="image" src="https://github.com/user-attachments/assets/ba7edca1-ab52-4f2b-83d6-d19b169a58c1" />

##  Rsync Command:
## -1 file
<img width="1492" height="174" alt="image" src="https://github.com/user-attachments/assets/8df886e7-58da-477c-aaeb-fd3dd4097235" />

## -1 folder
<img width="1500" height="263" alt="image" src="https://github.com/user-attachments/assets/f20e08d2-a6a2-4086-b6c6-4c4a2adfd1ac" />
## -rsync incremental'

<img width="1633" height="137" alt="image" src="https://github.com/user-attachments/assets/0a8f59ac-da70-426b-a364-1ed062a20e30" />

## Cat Command:

<img width="1842" height="382" alt="image" src="https://github.com/user-attachments/assets/bd5f2bdd-14f0-4603-917b-1e16bf1c6f2c" />

## Echo Command:

<img width="1174" height="140" alt="image" src="https://github.com/user-attachments/assets/099e1bb7-0443-4f82-8ee4-53da50f9729c" />

# Tail/Head Command

## Sự khác biệt giữa `tail` và `head`

| Lệnh | Chức năng | Ví dụ |
|---|---|---|
| `head` | Xem các dòng đầu tiên của file | `head notes.txt` |
| `tail` | Xem các dòng cuối cùng của file | `tail notes.txt` |

---
# Sự khác biệt giữa `tail` và `tailf`

| Tiêu chí | `tail` | `tailf` |
|---|---|---|
| Chức năng | Xem các dòng cuối của file | Theo dõi file realtime |
| Hoạt động | Hiển thị xong rồi thoát | Chạy liên tục để cập nhật nội dung mới |
| Realtime | ❌ Không | ✅ Có |
| Thường dùng cho | Xem nhanh log/file | Theo dõi log server |
| Ví dụ | `tail server.log` | `tailf server.log` |
| Phiên bản hiện đại | `tail` | Thường được thay bằng `tail -f` |

---

## Sed Command:


<img width="1204" height="161" alt="image" src="https://github.com/user-attachments/assets/efaf1074-a28c-4fab-8a08-afe36f9f0acd" />

## Traceroute/Tracert Command:


<img width="1138" height="220" alt="image" src="https://github.com/user-attachments/assets/f08ac9e2-b823-4e5c-9c24-3987c8d54637" />
Lệnh `traceroute vietnix.vn` được dùng để kiểm tra đường đi của các packet từ máy tính của bạn tới server `vietnix.vn`. Kết quả hiển thị cho thấy packet đã đi qua nhiều router trung gian trước khi tới đích cuối cùng là `14.225.253.240`.

Trong kết quả, mỗi dòng đại diện cho một `hop` — tức là một router hoặc thiết bị mạng mà packet phải đi qua. Con số ở đầu dòng (`1`, `2`, `3`...) là thứ tự của hop.

Các địa chỉ như `192.168.0.1`, `10.x.x.x` hay `27.x.x.x` là IP của các router trung gian. Trong đó:

- `192.168.x.x` là router nội bộ trong mạng LAN/WiFi của bạn.
- `10.x.x.x` là IP private trong hệ thống mạng của ISP.
- `static.vnpt.vn` là các router thuộc hạ tầng mạng của VNPT.

Các giá trị `ms` là thời gian phản hồi (latency), tính bằng milliseconds. Đây là thời gian packet đi tới router và phản hồi trở lại. Giá trị càng thấp thì kết nối càng nhanh và ổn định.

Dấu `* * *` xuất hiện ở một số hop có nghĩa là router hoặc firewall tại đó không phản hồi packet traceroute. Điều này khá phổ biến và không nhất thiết là lỗi mạng.

Dòng cuối cùng:


11  14.225.253.240

cho thấy packet đã tới được server Vietnix thành công. Tổng cộng packet đi qua khoảng 11 hop với độ trễ trung bình khoảng 80 ms, cho thấy kết nối mạng của bạn tới server hoạt động bình thường.
##  Netstat Command:
##     + Hiển thị các socket đang listen.

<img width="939" height="902" alt="image" src="https://github.com/user-attachments/assets/12d4aaf7-3754-4f88-a128-fccf6f9a3066" />

##     + Không resolve hostname.

<img width="844" height="527" alt="image" src="https://github.com/user-attachments/assets/0de3b9d2-446c-4e3f-8260-a3136d85d5f5" />

##     + Không resolve portname.

<img width="893" height="663" alt="image" src="https://github.com/user-attachments/assets/861da0f3-34d1-4721-9097-6028cabc36fb" />

##     + Display process name/PID.

<img width="1078" height="584" alt="image" src="https://github.com/user-attachments/assets/c991eb01-9bb8-424d-858d-38c245cd0cb9" />

##     + Chỉ hiển thị socket TCP.

<img width="778" height="192" alt="image" src="https://github.com/user-attachments/assets/58fe7de6-a7c1-49a3-b399-05bee76a3e3f" />

##     + Chỉ hiển thị socket UDP.

<img width="775" height="196" alt="image" src="https://github.com/user-attachments/assets/ed2e4a3c-4c30-4557-a075-f24a550b33fa" />


##   - Sort Command:

<img width="802" height="550" alt="image" src="https://github.com/user-attachments/assets/8ab7668f-0e7a-4f7d-a63b-e38f4bbd576a" />

##   - Uniq Command:

<img width="804" height="329" alt="image" src="https://github.com/user-attachments/assets/3114c52b-2f27-45eb-b914-ef3af0a3e536" />


##   - Wc Command:

<img width="1288" height="248" alt="image" src="https://github.com/user-attachments/assets/d18431d2-f95d-4135-a546-4b45fbe50791" />

##   - Chmod, Chown, Chattr Command:

<img width="830" height="182" alt="image" src="https://github.com/user-attachments/assets/217791ad-a6e0-4757-9f83-9e5b3a36e353" />

## - Df Command:

<img width="727" height="266" alt="image" src="https://github.com/user-attachments/assets/d7a037c9-cfc9-4332-8cef-0a1e788b8a95" />

## 2. Phân vùng `/` là gì?

Phân vùng `/` gọi là:

```text
Root Filesystem
```

Đây là phân vùng chính của Linux.

Mọi thứ trong hệ thống đều nằm bên dưới `/`.

Ví dụ:

| Thư mục | Chức năng |
|---|---|
| `/home` | User data |
| `/etc` | File cấu hình |
| `/var` | Log, cache |
| `/usr` | Application |
| `/boot` | Kernel boot |
| `/tmp` | File tạm |

Ví dụ:

```text
/
├── home
├── etc
├── var
├── usr
└── boot
```

Nếu phân vùng `/` đầy:

- hệ thống có thể chậm
- không ghi được log
- service lỗi
- server crash

# Free Command

Lệnh `free` dùng để kiểm tra dung lượng RAM và Swap trên Linux.

---

## Xem thông tin RAM

Lệnh:

```bash
free -h
```

Kết quả ví dụ:

```text
               total        used        free      shared  buff/cache   available
Mem:            15Gi       4.2Gi       6.8Gi       512Mi       4.0Gi        10Gi
Swap:           2.0Gi          0B       2.0Gi
```

---

# Giải thích các thông số RAM

| Cột | Ý nghĩa |
|---|---|
| total | Tổng dung lượng RAM |
| used | RAM đang sử dụng |
| free | RAM trống hoàn toàn |
| shared | RAM dùng chung giữa process |
| buff/cache | RAM dùng làm cache/buffer |
| available | RAM còn có thể sử dụng thực tế |


## TOP COMMAND

<img width="1113" height="982" alt="image" src="https://github.com/user-attachments/assets/48814fea-067b-4647-b687-0584aed0c37f" />




