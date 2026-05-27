
## 1. Cài VestaCP trên VPS

## B1:Download installer
<img width="1744" height="923" alt="image" src="https://github.com/user-attachments/assets/82a4f143-7fac-4a1a-8f9b-9ca1c54ba208" />

# Download installation script

curl -O https://vestacp.com/pub/vst-install.sh


# Run it

bash vst-install.sh --nginx yes --apache yes --phpfpm no --vsftpd yes --proftpd no --exim yes --dovecot yes --spamassassin yes --clamav yes --named yes --iptables yes --fail2ban yes --softaculous yes --remi yes --quota no --mysql no --postgresql no --hostname training-caolong.com --email trancaolong0912@gmail.com --port 8083 --password nj8EL4Rx2P552UB5a4PyglvY

## B2:Cài VestaCP với PHP 8.1
VestaCP gốc hơi cũ, thường mặc định PHP thấp.Nên sẽ cài thêm PHP 8.1 sau khi cài xong VestaCP

<img width="1850" height="385" alt="image" src="https://github.com/user-attachments/assets/6d61eb94-e621-4720-9ee3-83d750e48d86" />

<img width="1108" height="158" alt="image" src="https://github.com/user-attachments/assets/5e6bd3d1-40f2-4336-8074-06ae5415ace9" />

sau khi cài xong được cấp username, password để vào control panel
<img width="1393" height="498" alt="image" src="https://github.com/user-attachments/assets/91e22f32-5e3d-4c04-ab4e-8af148b68658" />
<img width="1784" height="1013" alt="image" src="https://github.com/user-attachments/assets/f6dcb427-ee11-4b03-9bdd-62286e641ab4" />

- tải php8.1:
  Ubuntu 18 mặc định không có PHP 8.1, Nên sẽ biên dịch từ mã nguồn
# Cài dependencies
apt-get install -y build-essential autoconf bison re2c \
  libxml2-dev libsqlite3-dev libssl-dev libcurl4-openssl-dev \
  libpng-dev libjpeg-dev libfreetype6-dev libzip-dev \
  libonig-dev pkg-config

# Tải PHP 8.1 source
cd /usr/local/src
wget https://www.php.net/distributions/php-8.1.32.tar.gz
tar -xzf php-8.1.32.tar.gz
cd php-8.1.32

# Compile và cài
./configure \
  --prefix=/usr/local/php81 \
  --with-fpm-user=www-data \
  --with-fpm-group=www-data \
  --enable-fpm \
  --with-openssl \
  --with-curl \
  --with-zlib \
  --enable-mbstring \
  --with-mysqli \
  --with-pdo-mysql \
  --enable-opcache \
  --with-zip

make -j$(nproc)
make install

## SET UP PHP8.1

## Kiểm tra PHP 8.1
/usr/local/php81/bin/php -v

## Tạo symlink để dùng lệnh php8.1
ln -s /usr/local/php81/bin/php /usr/local/bin/php8.1
ln -s /usr/local/php81/sbin/php-fpm /usr/local/bin/php-fpm8.1

## Cấu hình PHP-FPM
cp /usr/local/php81/etc/php-fpm.conf.default /usr/local/php81/etc/php-fpm.conf
cp /usr/local/php81/etc/php-fpm.d/www.conf.default /usr/local/php81/etc/php-fpm.d/www.conf

## Sửa config PHP-FPM để dùng unix socket
sed -i 's|listen = 127.0.0.1:9000|listen = /run/php/php8.1-fpm.sock|' /usr/local/php81/etc/php-fpm.d/www.conf
sed -i 's|;listen.owner = nobody|listen.owner = www-data|' /usr/local/php81/etc/php-fpm.d/www.conf
sed -i 's|;listen.group = nobody|listen.group = www-data|' /usr/local/php81/etc/php-fpm.d/www.conf
sed -i 's|user = nobody|user = www-data|' /usr/local/php81/etc/php-fpm.d/www.conf
sed -i 's|group = nobody|group = www-data|' /usr/local/php81/etc/php-fpm.d/www.conf

## Tạo thư mục socket
mkdir -p /run/php

## Tạo systemd service
cat > /etc/systemd/system/php8.1-fpm.service << 'EOF'
[Unit]
Description=PHP 8.1 FastCGI Process Manager
After=network.target

[Service]
Type=simple
PIDFile=/run/php/php8.1-fpm.pid
ExecStart=/usr/local/php81/sbin/php-fpm --nodaemonize --fpm-config /usr/local/php81/etc/php-fpm.conf
ExecReload=/bin/kill -USR2 $MAINPID
Restart=on-failure

[Install]
WantedBy=multi-user.target
EOF

## Start PHP-FPM 8.1
systemctl daemon-reload
systemctl start php8.1-fpm
systemctl enable php8.1-fpm
systemctl status php8.1-fpm
