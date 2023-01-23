## Migration

Remove Vite

```
npm remove vite laravel-vite-plugin
```

Replace npm scripts in ```package.json```:

```diff
"scripts": {
    // ...
-    "dev": "vite",
-    "build": "vite build"
+    "dev": "npm run development",
+    "development": "mix",
+    "watch": "mix watch",
+    "watch-poll": "mix watch -- --watch-options-poll=1000",
+    "hot": "mix watch --hot",
+    "prod": "npm run production",
+    "production": "mix --production"
}
```

Change your environment configuration (```.env```) by replacing ```VITE_``` with ```MIX_```.

In ```resources/js/bootstrap.js``` replace ```VITE_``` with ```MIX_```.

Delete ```vite.config.js```.

Install Laravel Mix npm package:
```
npm i laravel-mix --save-dev
```

Create ```webpack.mix.js```:

```js
const mix = require('laravel-mix');

mix.js('resources/js/app.js', 'public/js')
.sass('resources/sass/app.scss', 'public/css').sourceMaps();
```

## Reference

[Migrating from Vite to Laravel Mix](https://github.com/laravel/vite-plugin/blob/main/UPGRADE.md#migrating-from-vite-to-laravel-mix)
