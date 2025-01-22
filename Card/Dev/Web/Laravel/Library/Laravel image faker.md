
#### Image faker
##### Default
factory
```php
$image = $this->faker->image(  
    'public/storage/' . config('file_paths.article'), 
    640,  
    480,  
    'animals',  
    false  
);
return [
	'image_filename' => $image,  
	'image_original_name' => basename($image),
]
```
##### Beautiful image
url:: [Fake beautiful images with picsum.photos in Laravel | by smknstd | Sep, 2021 | Medium | Medium](https://smknstd.medium.com/fake-beautiful-images-in-laravel-51062967d1db)
source:: [GitHub - smknstd/fakerphp-picsum-images: Alternative image provider for fakerphp using picsum](https://github.com/smknstd/fakerphp-picsum-images)

```sh
composer require --dev smknstd/fakerphp-picsum-images
php artisan make:provider FakerServiceProvider
```
fake service provider
```php
use Faker\{Factory,Generator};  
use Illuminate\Support\ServiceProvider;  
use Smknstd\FakerPicsumImages\FakerPicsumImagesProvider;

public function register() {  
	$this->app->singleton(Generator::class, function () {  
	$faker = Factory::_create_();  
	$faker->addProvider(new FakerPicsumImagesProvider($faker));  
	return $faker;  
	});
}
```
app service provider
```php
public function register()   {  
     ...     
     if (!$this->app->environment('production')) {  
$this->app->register('App\Providers\FakerServiceProvider');  
     }  
}
```
