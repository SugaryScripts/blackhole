- [[Vite]]
- [[Setup Laravel]]
	- [[Installing]]
	- [[Composer]]
- [[Basic Command]]
- [[Storage & Link & Upload]]
- [[Case]]
	- [[Migrate Laravel Mix Vite]]
	- [[Migrate tailwind to bootstrap]]
	- [[Localization]]
	- [[Recursive Table Relation Laravel]]
	  [[Gsheet Laravel]]
- Deployment
	- [[Hostinger Laravel]]
- GUIDE
	- [GitHub - michael-rubel: Livewire Best Practices](https://github.com/michael-rubel/livewire-best-practices?tab=readme-ov-file)
	- [02 - Extract Properties to Form Objects | Laravel Daily](https://laraveldaily.com/lesson/livewire-3/extract-properties-to-form-objects)
	- [Laravel Naming Conventions - Web dev etc - my software development blog](https://webdevetc.com/blog/laravel-naming-conventions/)
	- **Upgrade laravel version**? check dependency [Laravel Shift - Can I upgrade Laravel yet?](https://laravelshift.com/can-i-upgrade-laravel/)
	- 



# Recommended Library
- [[Hashid Vinkla]]
- [[Laravel image faker]]
- [[Livewire]]
- [[Pest]]


# Extras
Great tutorials:
Manage layout component livewire
[Josh Hanley](https://joshhanley.com.au/articles/how-to-structure-your-layout-file-for-livewire)

Understanding slot include layout
[Laravel Flexible Layouts: Yields, Includes, Slots](https://dcblog.dev/creating-flexible-layouts-in-laravel-with-yields-includes-and-slots)

Pass object into anonymous component
[php - Pass Anonymous Components Attribute as object - Stack Overflow](https://stackoverflow.com/questions/69274581/pass-anonymous-components-attribute-as-object)



# Theory Basics
## Structure
#### Public
Assets placed in the `public` folder are served directly without any processing. This is useful for static assets that do not need to be transformed or optimized, such as favicon files or static images that rarely change.
**Pros**:
- **Direct Access**: Assets are directly accessible at the root URL (e.g., `http://your-app.com/image.png`).
- **No Build Required**: Suitable for assets that don’t need processing.
#### Resource
Assets placed in the `resources` folder are intended to be processed by your build tool (Vite). This is useful for assets that might be transformed, optimized, or versioned during the build process. For example, if you have images, fonts, or other files that need to be bundled or optimized, placing them in `resources` makes sense.
**Pros**:
- **Build Process**: Assets can be optimized, hashed, and versioned during the build.
- **Modular**: Keeps source assets together with your source code.


# Trouble shoots
## Maximum execution time of 30 seconds exceeded
```sh
sudo vim /etc/php/php.ini
/execution to 360
lamp restart
```

## Vite Sourcemap for ... points to missing source files



# Most Used command
```sh
make:view
make:component __ --view
```

# Reading material
#### sweet alert
[laracasts.com/discuss/channels/laravel/livewire-with-sweetalert2](https://laracasts.com/discuss/channels/laravel/livewire-with-sweetalert2)
[Site Unreachable](https://dev.to/abrardev99/peasy-way-to-show-alerts-in-laravel-livewire-26j)
