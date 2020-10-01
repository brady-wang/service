# 各种服务一键启动

git clone git@github.com:brady-wang/service.git 

cd service  

docker-composer up 启动 
docker-compose up -d 后台启动
docker-composer down 删除
docker-composer restart 重启

## rabbitmq

1 端口 5672 

2 管理后台 http://ip:15672  admin  admin

## redis 

1 密码 123456

## elasticsearch 


## mysql8 

1 用户名密码
root  root

2 授权远程登录 

docker exec -it docker_mysql /bin/bash
mysql -uroot -p
root


create user 'brady'@'%' identified by 'brady';
GRANT ALL PRIVILEGES ON *.* TO 'brady'@'%';
ALTER USER 'brady'@'%' IDENTIFIED WITH mysql_native_password BY 'brady';
FLUSH PRIVILEGES;
