> Ensure you have one of the PHP extensions `bcmath` or `gmp` installed
```sh
composer require vinkla/hashids

# app config to bootstrap provider
Vinkla\Hashids\HashidsServiceProvider::class

php artisan vendor:publish --provider="Vinkla\Hashids\HashidsServiceProvider"
```

[GitHub - vinkla/laravel-hashids: A Hashids bridge for Laravel](https://github.com/vinkla/laravel-hashids)
[Using Hashids and Laravel Route Binding to Obfuscate Auto-Incrementing IDs | by Joe Tannenbaum | Sammich Shop | Medium](https://medium.com/sammich-shop/using-hashids-and-laravel-route-binding-to-obfuscate-auto-incrementing-ids-e6c0a328dfb5)

