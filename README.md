# AnsiblePlaybook
注意：克隆仓库以后通过使用Ansible外部变量指定，文件位置与配置参数
## OpsManage部署平台使用
上传*.yml文件

## 命令行方式使用
安装php
```
ansible-playbook -i hosts install-php.yml --extra-vars="host=192.168.1.235 php_path=/usr/local/webserver/php ansible_php_config=/root/php/files ansible_php_package=/root/php/packages/ php_user=www"
```
安装nginx
```
ansible-playbook -i hosts install-nginx.yml --extra-vars="host=192.168.1.235 nginx_path=/usr/local/webserver/nginx ansible_nginx_config=/root/nginx/files ansible_nginx_package=/root/nginx/packages/ nginx_user=www"
```
配置Nginx虚拟主机
```
ansible-playbook -i hosts install-nginx-vhost.yml --extra-vars="host=192.168.1.235 nginx_path=/usr/local/webserver/nginx ansible_nginx_config=/root/nginx/files port=80 root_dir=/var/www/html domain=www.anc.com"
```
配置MySQL
```
ansible-playbook -i hosts install-mysql.yml --extra-vars="host=192.168.1.235 mysql_path=/usr/local/webserver/mysql ansible_mysql_config=/root/mysql/files ansible_mysql_package=/root/mysql/packages/  port=3306 mysql_user=mysql"
```
