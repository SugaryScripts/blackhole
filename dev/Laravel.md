# Installation
## Windows
- install xampp -> set xampp control to administrator
- install composer.exe -> check dev?  verify with composer --version 
- composer self-update

# Artisan Command
## make:model
`php artisan make:model User -mcr`
-a
-m migration
-c controller
-r resource
-f factory
-s seed

# Remove package composer
1. Remove declaration from composer.json (in “require” section)
2. **Remove Service Provider from** app/config/app.php (reference in “providers” array)
3. Remove any Class Aliases from app/config/app.php
4. Remove any references to the package from your code
5. Run composer update vendor/package-name. This will remove the package folder from vendor folder and will rebuild composer autoloading map.
6. Manually delete the published files

``` sh
composer clearcache
composer dump -o
```

# Localization

```sh
composer require --dev laravel-lang/common
php artisan lang:add id
```

config/app.php
``` php
/*  
|-------------------------------------------------------------------  
| Application Timezone  
|-------------------------------------------------------------------  
|  
| Here you may specify the default timezone for your application, which  
| will be used by the PHP date and date-time functions. We have gone  
| ahead and set this to a sensible default for you out of the box.  
|  
*/'timezone' => 'Asia/Jakarta',/*  
|-------------------------------------------------------------------  
| Application Locale Configuration  
|-------------------------------------------------------------------  
|  
| The application locale determines the default locale that will be used  
| by the translation service provider. You are free to set this value  
| to any of the locales which will be supported by the application.  
|  
*/'locale' => 'id',/*  
|-------------------------------------------------------------------  
| Application Fallback Locale  
|-------------------------------------------------------------------  
|  
| The fallback locale determines the locale to use when the current one  
| is not available. You may change the value to correspond to any of  
| the language folders that are provided through your application.  
|  
*/'fallback_locale' => 'id',/*  
|-------------------------------------------------------------------  
| Faker Locale  
|-------------------------------------------------------------------  
|  
| This locale will be used by the Faker PHP library when generating fake  
| data for your database seeds. For example, this will be used to get  
| localized telephone numbers, street address information and more.  
|  
*/'faker_locale' => 'id_ID',
```