# 各种服务一键启动

git clone git@github.com:brady-wang/service.git 

cd service  

docker-composer up 启动 
docker-compose up -d 后台启动
docker-composer down 删除
docker-composer restart 重启


## mysql8 授权远程登录 

docker exec -it docker_mysql /bin/bash
mysql -uroot -p
root


create user 'brady'@'%' identified by 'brady';
GRANT ALL PRIVILEGES ON *.* TO 'brady'@'%';
ALTER USER 'brady'@'%' IDENTIFIED WITH mysql_native_password BY 'brady';
FLUSH PRIVILEGES;
