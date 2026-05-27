## B1: TẠO DOMAIN
# Tạo domain WordPress
/usr/local/vesta/bin/v-add-domain admin wp.caolong.vietnix.tech

# Tạo domain Laravel
/usr/local/vesta/bin/v-add-domain admin laravel.caolong.vietnix.tech

# Kiểm tra
/usr/local/vesta/bin/v-list-web-domains admin

<img width="1258" height="229" alt="image" src="https://github.com/user-attachments/assets/fafb83a7-873d-4a31-80fc-bfc6747c0b09" />

<img width="1748" height="1026" alt="image" src="https://github.com/user-attachments/assets/bc5b74f1-ad1c-4aca-9b3b-2961344ab76e" />

## B2: Cấu hình PHP-FPM 8.1 cho 2 domain

# Kiểm tra socket PHP 8.1 đang chạy chưa

```ls /run/php/php8.1-fpm.sock```

- tạo config
```
# Tạo config nginx cho wp.caolong.vietnix.tech dùng PHP 8.1
cat > /home/admin/conf/web/nginx.wp.caolong.vietnix.tech.conf_lnginx << 'EOF'
location ~ \.php$ {
    fastcgi_pass unix:/run/php/php8.1-fpm.sock;
    fastcgi_index index.php;
    fastcgi_param SCRIPT_FILENAME $document_root$fastcgi_script_name;
    include fastcgi_params;
}
EOF

# Tương tự cho Laravel
cat > /home/admin/conf/web/nginx.laravel.caolong.vietnix.tech.conf_lnginx << 'EOF'
location ~ \.php$ {
    fastcgi_pass unix:/run/php/php8.1-fpm.sock;
    fastcgi_index index.php;
    fastcgi_param SCRIPT_FILENAME $document_root$fastcgi_script_name;
    include fastcgi_params;
}
EOF

systemctl reload nginx

```
<img width="1252" height="442" alt="image" src="https://github.com/user-attachments/assets/7ac5b8ab-7b19-42d4-bd6a-f1a7c07e3be5" />

## B3: Upload dữ liệu website
# Web root của 2 domain
```
ls /home/admin/web/wp.caolong.vietnix.tech/public_html/
ls /home/admin/web/laravel.caolong.vietnix.tech/public_html/

```


## Upload từ máy local (chạy trên máy local của bạn) 
```
scp -r /home/longtc/Downloads/project/source_wp root@14.225.207.233:/home/admin/web/wp.caolong.vietnix.tech/public_html/ 

scp -r /home/longtc/Downloads/project/ laravel_source root@14.225.207.233:/home/admin/web/laravel.caolong.vietnix.tech/public_html/
```
<img width="1856" height="283" alt="image" src="https://github.com/user-attachments/assets/ce564b20-0f75-4c0c-a864-e4f812b6ebca" />


# Phân quyền
```
chown -R admin:admin /home/admin/web/wp.caolong.vietnix.tech/public_html/
chown -R admin:admin /home/admin/web/laravel.caolong.vietnix.tech/public_html/
```
<img width="1483" height="890" alt="image" src="https://github.com/user-attachments/assets/9470613b-c1cc-40ed-892d-119879c0cec8" />

## B4:Cài SSL Free bằng command line

# Cài SSL bằng cli trong vesta
```
/usr/local/vesta/bin/v-add-letsencrypt-domain admin wp.caolong.vietnix.tech
/usr/local/vesta/bin/v-add-letsencrypt-domain admin laravel.caolong.vietnix.tech
```
# Update cert bằng certbot đã tạo trước đó

Vì lệnh v-add-web-domain-ssl và v-change-web-domain-sslcert của VestaCP yêu cầu một thư mục chứa các file cert đặt tên đúng format:
```
# Tạo thư mục trước
mkdir -p /etc/ssl/vesta/wp.caolong.vietnix.tech
mkdir -p /etc/ssl/vesta/laravel.caolong.vietnix.tech

# Sau đó copy cert
cp /etc/letsencrypt/live/wp.caolong.vietnix.tech/fullchain.pem \
   /etc/ssl/vesta/wp.caolong.vietnix.tech/wp.caolong.vietnix.tech.crt
cp /etc/letsencrypt/live/wp.caolong.vietnix.tech/privkey.pem \
   /etc/ssl/vesta/wp.caolong.vietnix.tech/wp.caolong.vietnix.tech.key
cp /etc/letsencrypt/live/wp.caolong.vietnix.tech/chain.pem \
   /etc/ssl/vesta/wp.caolong.vietnix.tech/wp.caolong.vietnix.tech.ca
```
---

## update cert
```
/usr/local/vesta/bin/v-add-web-domain-ssl admin wp.caolong.vietnix.tech \
>   /etc/ssl/vesta/wp.caolong.vietnix.tech
--- 
/usr/local/vesta/bin/v-add-web-domain-ssl admin laravel.caolong.vietnix.tech \
>   /etc/ssl/vesta/laravel.caolong.vietnix.tech

```

# Kiểm tra

-  laravel

<img width="1568" height="1024" alt="image" src="https://github.com/user-attachments/assets/f8583834-aad0-435a-a743-14f073cea0c1" />

- wordpress

<img width="1677" height="1000" alt="image" src="https://github.com/user-attachments/assets/9ca49cbd-2759-4be2-9fbb-0262b1a345e4" />


## import database

<img width="1589" height="536" alt="image" src="https://github.com/user-attachments/assets/eb514492-bcee-4368-a8ce-389ef8f4cb1c" />

<img width="1698" height="816" alt="image" src="https://github.com/user-attachments/assets/f8897357-866f-404a-a6c9-cdc39948ce59" />

- chuyển data từ local
  <img width="1843" height="303" alt="image" src="https://github.com/user-attachments/assets/16e89729-6119-4a4e-9c0b-09793b44be1b" />

<img width="1842" height="684" alt="image" src="https://github.com/user-attachments/assets/1fc39015-7808-41c8-b477-f6c7e57d0f7c" />

<img width="1829" height="1007" alt="image" src="https://github.com/user-attachments/assets/c5c74fff-c9ed-4afe-8b27-33f2f962e198" />
<img width="1844" height="1034" alt="image" src="https://github.com/user-attachments/assets/7cf12537-7ccd-409b-ac18-9bffeb403486" />

