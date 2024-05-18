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
