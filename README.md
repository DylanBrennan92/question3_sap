main
````setup
    docker network create dylans_network
    sudo docker run -d -p 3000 -e MYSQL_ROOT_PASSWORD=my-secret-password --name db --net dylans_network
    sudo docker run -d -p 8082:80 -e PMA_HOST=db --name phpmyadmin --net dylans_network phpmyadmin:5.1-apache
````


