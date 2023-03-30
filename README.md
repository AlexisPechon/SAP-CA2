# SAP-CA2
This is the main branch.

```
The following code will create the docker network:
docker network create mysql-network

The following code will run a mysql:latest docker image with the name of db with a root password=my-secret-password:
docker run -d -p 3306:3306 \
    --name mysql-docker-container \
    -e MYSQL_ROOT_PASSWORD=my-secret-password \
    -e MYSQL_DATABASE=sap_ca2 \
    -e MYSQL_USER=alexispechon \
    -e MYSQL_PASSWORD=my-secret-password \
    mysql/mysql-server:latest
    
The following code will run the docker image phpmyadmin/phpmyadmin on the network previously created mapping a port of your choice to port 80 of the container:
docker run -d -p 8082:80 \
    -e PMA_HOST=mysql-docker-container \
    --name phpmyadmin \
    --net mysql-network \
    phpmyadmin:5.1-apache

```
