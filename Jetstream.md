# Laravel - Jetstream installation and usage

This document is a memorandum for installation and usage of Laravel Jetstream in a new Laravel project.

This document assumes that you are using Laravel Sail.

## With Laravel installer

The leatest version of the Laravel installer contains a wizard to scaffold a new project with Jetstream.

Install the installer globally (if you haven't already):

```
composer global require laravel/installer
```

Then create a new project and follow the terminal wizard:

```
laravel new [my-app]
```

Update ```.env``` file with database info before running migrations.

## With Composer

Install Laravel Breeze using Composer:

```
sail composer require laravel/jetstream
```

Install a stack:

```
sail artisan jetstream:install
```

Then follow the terminal wizard.

Install npm packages:

```
sail npm i
```
```
sail npm run build
```

Setup your .env, DB and run your migrations:

```
sail artisan migrate
```

## Laravel (9) Vite/Sail Fix

Fix Vite configuration for Sail as mentioned [here](https://github.com/laravel/vite-plugin/pull/42):

```js
export default defineConfig({
    // ...
    server: {
        hmr: {
            host: 'localhost',
        },
    },
});
```

## Publish views

(this is no longer necessary in the latest Jetstream versions)

```
sail artisan vendor:publish --tag=jetstream-views
```



## Reference

- [Laravel Jetstream documentation](https://jetstream.laravel.com/installation.html)
- [Laravel Livewire documentation](https://livewire.laravel.com/docs/quickstart)
- [Laravel Vite/Sail fix](https://github.com/laravel/vite-plugin/pull/42)
