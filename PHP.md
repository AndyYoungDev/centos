# centos7 LNMP
# 流程
1.更换阿里云源
```bash
sudo wget -O /etc/yum.repos.d/CentOS-Base.repo http://mirrors.aliyun.com/repo/Centos-7.repo
sudo yum makecache
sudo yum -y update
```
2.下载php压缩包
```bash
sudo wget -O php7.3.3.tar.gz http://hk2.php.net/get/php-7.3.3.tar.gz/from/this/mirror
```
3.解压php
```bash
sudo tar -xzvf php7.3.3.tar.gz
```
4.安装GCC
```bash
sudo yum install -y gcc
```
5.安装libxml2依赖
```bash
sudo yum install -y libxml2
sudo yum install libxml2-devel.x86_64
```
6.编译php
```bash
./configure --prefix=/usr/local/php \
--with-config-file-path=/usr/local/php/ \
--enable-fpm \
--disable-rpath \
--with-openssl \
--with-libxml-dir \
--with-zlib \
--enable-calendar \
--with-curl \
--with-gd \
--with-mhash \
--with-interbase \
--enable-intl \
--enable-mbstring \
--with-pdo-mysql \
--enable-zip \
--enable-sockets


sudo make
sudo make install

```
