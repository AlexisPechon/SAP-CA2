# SAP-CA2

```
$ docker network create

docker run -d -p 3306:3306 --name mysql-docker-container -e MYSQL_ROOT_PASSWORD=my-secret-password -e MYSQL_DATABASE=sap_ca2 -e MYSQL_USER=alexispechon -e MYSQL_PASSWORD=my-secret-password mysql/mysql-server:latest

docker run -d -p 8082:80 \
    -e PMA_HOST=mysqldb \
    --name phpmyadmin \
    --net mysql-network \
    phpmyadmin:5.1-apache
 ```
