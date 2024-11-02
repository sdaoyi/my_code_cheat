### mysql 

####  树莓派的mysql docker 配置
```

docker pull beercan1989/arm-mysql:latest


docker run -it \
  -e 'MYSQL_ROOT_PASSWORD=123456' \
  -e 'MYSQL_DATABASE=data1' \
  -e 'MYSQL_USER=sdaoyi' \
  -e 'MYSQL_PASSWORD=toor' \
  -p '3306:3306' \
  -v datadir:/var/lib/mysql \
  --name mysql1 \
  -d beercan1989/arm-mysql:latest

#  创建支持插入汉字的数据库
CREATE DATABASE data1 CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;