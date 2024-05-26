# Laravel - Useful commands

A list of frequently used commands for Laravel.

This document assumes that you are using Laravel Sail. Replace ```sail``` with ```php``` in all commands otherwise.

## Migrations

Create a table:

```
sail artisan make:migration create_books_table
```

The pivot table naming convection is *singlularNameA_singularNameB*. The names are in alphabetical order.

Migrate:

```
sail artisan migrate
```
```
sail artisan migrate:rollback
```

Create Model and Migration:

```
sail artisan make:model Book --migration
```

Create Model, Controller and Migration:

```
sail artisan make:model Book -m -c
```

## Resource

```
sail artisan make:resource BookResource
```
```
sail artisan make:resource BookCollection
```

## Component

```
sail artisan make:component Alert
```

## Encryption

```
sail artisan key:generate
```

## PHP commands

```
php artisan make:migration create_books_table
```
```
php artisan migrate
```
```
php artisan migrate:rollback
```
```
php artisan make:model Book --migration
```
```
php artisan make:model Book -m -c
```
```
php artisan make:resource BookResource
```
```
php artisan make:resource BookCollection
```
```
php artisan make:component Alert
```
```
php artisan key:generate
```
