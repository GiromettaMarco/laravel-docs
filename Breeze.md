# Laravel - Breeze installation and usage

This document is a memorandum for installation and usage of Laravel Breeze in a new Laravel project.

This document assumes that you are using Laravel Sail.

## Installation

Configure your database, and run your database migrations. Then install Laravel Breeze using Composer:

```
sail composer require laravel/breeze --dev
```

### Inertia stack

```
sail artisan breeze:install vue
```
```
sail npm install
```
```
sail npm run dev
```

## Reference

- [Laravel Breeze documentation](https://laravel.com/docs/9.x/starter-kits#laravel-breeze)
