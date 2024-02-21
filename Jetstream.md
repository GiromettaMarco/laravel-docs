# Laravel - Jetstream installation and usage

This document is a memorandum for installation and usage of Laravel Jetstream in a new Laravel project.

This document assumes that you are using Laravel Sail.

## Installation

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

```
sail artisan vendor:publish --tag=jetstream-views
```



## Reference

- [Laravel Jetstream documentation](https://jetstream.laravel.com/2.x/introduction.html)
- [Laravel Livewire documentation](https://laravel-livewire.com/docs/2.x/quickstart)
- [Laravel Vite/Sail fix](https://github.com/laravel/vite-plugin/pull/42)
