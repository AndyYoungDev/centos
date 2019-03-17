#centos7 nginx
# 流程
1.更换阿里云源
```bash
sudo wget -O /etc/yum.repos.d/CentOS-Base.repo http://mirrors.aliyun.com/repo/Centos-7.repo
sudo yum makecache
sudo yum -y update
```
2.下载nginx压缩包
```bash
sudo wget -O nginx.tar.gz http://nginx.org/download/nginx-1.14.2.tar.gz
```
3.解压nginx
```bash
sudo tar -xvzf nginx.tar.gz
```
4.安装pcre
```bash
sudo yum install pcre
sudo yum install pcre-devel.x86_64
```
5.编译nginx
```bash
./configure
```
5.安装nginx
```bash
sudo make
sudo make install
```
