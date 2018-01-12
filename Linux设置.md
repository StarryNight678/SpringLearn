# Linux设置

## 无密码登录

ssh-keygen -t rsa 

cp id_rsa.pub authorized_keys

将各个节点的id_rsa.pub 复制到同一个authorized_keys文件中


## 设置时间


date -s "2018-01-12 11:30:00"
clock -w