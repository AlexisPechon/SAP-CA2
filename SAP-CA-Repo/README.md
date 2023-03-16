```
$ docker network create

docker run -d -p 3306:3306 --name mysql-docker-container -e MYSQL_ROOT_PASSWORD=sergey -e MYSQL_DATABASE=photo_app -e MYSQL_USER=sergey -e MYSQL_PASSWORD=sergey mysql/mysql-server:latest

docker run -d -p 8082:80 \
    -e PMA_HOST=mysqldb \
    --name phpmyadmin \
    --net mysql-network \
    phpmyadmin:5.1-apache
```
