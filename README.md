- docker run php:8.0.3-fpm-buster php -m
- docker-compose up
- docker-compose exec -T app composer install
- docker-compose exec -T app cp .env.example .env
- docker-compose exec -T app php artisan key:generate
- docker-compose exec app /bin/bash
- chmod -R 777 /var/www/storage/logs/
- chmod -R 777 /var/www/storage/framework/sessions/
- chmod -R 777 /var/www/storage/framework/views/
- docker-compose exec -T app php artisan config:clear
- docker-compose exec -T app php artisan migrate
- docker-compose exec -T app composer require laravel/socialite
- docker kill $(docker ps -q)
- docker-compose exec -T app composer require predis/predis
- docker-compose exec -T app php artisan make:mail TestMail

[Tutorial](https://www.linkedin.com/pulse/how-create-laravel-development-environment-using-docker-isaac-souza/)

# curly-system
