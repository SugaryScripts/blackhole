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
