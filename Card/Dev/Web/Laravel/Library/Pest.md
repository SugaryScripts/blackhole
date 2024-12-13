Install
```sh
composer require pestphp/pest --dev --with-all-dependencies
./vendor/bin/pest --init
./vendor/bin/pest --migrate

composer require pestphp/pest-plugin-laravel --dev
```

replace unit test
composer.json
```json
"scripts": {
    "test": "vendor/bin/pest"
}
```
```sh
php artisan test
composer test
./vendor/bin/pest
```