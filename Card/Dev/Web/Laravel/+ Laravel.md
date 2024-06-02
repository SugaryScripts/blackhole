- [[Setup Laravel]]
- [[Installing]]
- [[Basic Command]]
- [[Case]]
	- [[Migrate Laravel Mix Vite]]
	- [[Localization]]



# Structure
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

