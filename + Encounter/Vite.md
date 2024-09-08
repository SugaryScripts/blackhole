##### Setup
Project: package.json - vite.config.js
[GitHub - antfu-collective/vite-plugin-inspect: Inspect the intermediate state of Vite plugins](https://github.com/antfu-collective/vite-plugin-inspect)
```sh
npm i -D vite-plugin-inspect
yarn add -D vite-plugin-inspect
# add import
yarn install
```

```json
// vite.config.ts
import Inspect from 'vite-plugin-inspect'

export default {
  plugins: [
    Inspect(),
    laravel({  
	    // assets must be add here before calling them on the html
	    input: ['resources/css/app.css', 'resources/js/app.js'],  
	    refresh: true,  
	}),
  ],
}
```

```sh
@vite(['resources/css/app.css', 'resources/js/app.js'])
npm run dev
php artisan serve
```