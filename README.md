# library

sudo docker run -d --name redis -p 6379:6379 -v redisvolume:/data redis

sudo docker run -d -p 3306:3306 --name mysql -e MYSQL_ROOT_PASSWORD=123 -v mysqlvolume:/var/lib/mysql mysql:latest
