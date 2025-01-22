#### Basic
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


#### Read Material
[Monitoring and Error Tracking in Laravel | by Mohammad Roshandelpoor | Medium](https://medium.com/@mohammad.roshandelpoor/monitoring-and-error-tracking-in-laravel-59c31b985c0d)
[Global livewire notifications with SweetAlert - DEV Community](https://dev.to/ph7jack/global-livewire-notifications-3aba)
[Using Pest to test Laravel Livewire validation rules | C.S. Rhymes](https://www.csrhymes.com/2022/08/12/testing-livewire-validation-rules-with-pest.html)
[Peasy way to Show Alerts in Laravel Livewire - DEV Community](https://dev.to/abrardev99/peasy-way-to-show-alerts-in-laravel-livewire-26j)
[Laravel Testing with Pest: The Complete Guide for Beginners | by Abu Sayed | Medium](https://abu-sayed.medium.com/laravel-testing-with-pest-the-complete-guide-for-beginners-a0b6680cfd71)