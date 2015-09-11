1) docker build -t php-server:1.0 .

2) docker run --name db -e MYSQL_HOST=localhost -e MYSQL_DATABASE=homestead -e MYSQL_USER=homestead -e MYSQL_PASSWORD=secret -d mysql:5.6

3) docker run --name web --link db:mysql -d -p 8081:80 -v /docker-final-project/worldapi php-server:1.0

