# laranginx

A Laravel development environment under Docker. Take a look to [Containerize Nginx, Laravel and MySQL with Docker Compose](https://webomnizz.com/containerize-nginx-laravel-and-mysql-with-docker-compose).

- PHP
- Nginx
- MySQL

docker-compose build
docker-compose up -d
docker ps

docker exec -it f29812e8f5be bash
php artisan -V
docker-compose exec app php artisan -V


sudo chown -R $USER:www-data storage
sudo chown -R $USER:www-data bootstrap/cache

chmod -R 775 storage
chmod -R 775 bootstrap/cache

ps aux|grep nginx|grep -v grep
ps aux | egrep '(apache|httpd)'