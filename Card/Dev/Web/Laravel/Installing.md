#### Bootstrap
```sh
yarn install
yarn add -D bootstrap @popperjs/core sass
```
sass is optional
**CSS**
```blade
@vite(['resources/css/app.css', 'resources/js/app.js'])
```
```css
@import 'bootstrap/dist/css/bootstrap.min.css';
```
```js
import 'bootstrap/dist/js/bootstrap.bundle.js';
```
**SASS**
```blade
@vite('resources/js/app.js')
```
```scss
@import '../../node_modules/bootstrap/scss/bootstrap.scss';
```
```js
import '../scss/app.scss';
import * as bootstrap from 'bootstrap';
```
#### Bootstrap Scaffolding Laravel/UI **SASS**
```sh
composer require laravel/ui --dev
php artisan ui bootstrap --auth
npm install bootstrap-icons --save-dev
nano resources/sass/app.scss
npm install
```

```sass
// fonts
@import url(..),
// variables
@import 'variables';
// Bootstrap
@import 'bootstrap/scss/bootstrap';
// add this
@import 'bootstrap-icons/font/bootstrap-icons.css';
```


#### Basic
```
composer require laravel/jetstream
php artisan jetstream:install livewire --dark
php artisan livewire:publish --config
```