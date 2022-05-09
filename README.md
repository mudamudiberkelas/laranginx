# laranginx

A Laravel development environment under Docker. Take a look to [Containerize Nginx, Laravel and MySQL with Docker Compose](https://webomnizz.com/containerize-nginx-laravel-and-mysql-with-docker-compose).

- PHP
- Nginx
- MySQL

docker-compose build app
docker-compose up -d
docker-compose ps

docker-compose exec app ls -l
docker-compose exec app composer install
docker-compose exec app php artisan key:generate
docker-compose logs nginx
docker-compose down

sudo chown -R $USER:www-data storage
sudo chown -R $USER:www-data bootstrap/cache

chmod -R 775 storage
chmod -R 775 bootstrap/cache

docker-compose build
docker-compose up -d
docker ps

# PHP
docker exec -it 728da5a21fd9 bash
php artisan -V
php artisan key:generate
php artisan config:cache

php artisan migrate
php artisan tinker
\DB::select('show tables'); 
\DB::table('migrations')->get();

ps aux|grep nginx|grep -v grep
ps aux | egrep '(apache|httpd)'

# MYSQL
docker exec -it f29812e8f5be bash
mysql -u lara_user -p lara_password


CREATE TABLE lara_db.places (
	id INT AUTO_INCREMENT,
	name VARCHAR(255),
	visited BOOLEAN,
	PRIMARY KEY(id)
);


INSERT INTO lara_db.places (name, visited) 
VALUES ("Tokyo", false),
("Budapest", true),
("Nairobi", false),
("Berlin", true),
("Lisbon", true),
("Denver", false),
("Moscow", false),
("Olso", false),
("Rio", true),
("Cincinnati", false),
("Helsinki", false);


SELECT * FROM lara_db.places;

laravelapp-nginx
laravelapp-db
laravelapp-app









