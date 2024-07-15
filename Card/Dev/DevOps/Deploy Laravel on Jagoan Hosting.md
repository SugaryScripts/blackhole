up:: home
tags:: #dev/laravel #sys/incomplete
dates:: 2024 (3)March 20th - Wednesday
times:: 03:51
sources:: 
url:: 
people::
related:: 

# How

## Update laravel apps on server
```sh
php artisan down
git pull origin master
composer install
php artisan route:cache
php artisan view:cache
php artisan config:cache
php artisan up
```


