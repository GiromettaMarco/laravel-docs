## Installation

```
composer require --dev barryvdh/laravel-ide-helper
```

## Usage

Clear ```bootstrap/compiled.php``` first:

```
php artisan clear-compiled
```

Generate ```_ide_helper.php```:

```
php artisan ide-helper:generate
```

Add Model helpers:

```
php artisan ide-helper:models
```

Generate ```.phpstorm.meta.php``` for PhpStorm:

```
php artisan ide-helper:meta
```

Add ```_ide_helper.php``` and ```.phpstorm.meta.php``` to ```.gitignore```

Configure your ```composer.json``` to do this each time you update your dependencies:

```
"scripts": {
    "post-update-cmd": [
        "Illuminate\\Foundation\\ComposerScripts::postUpdate",
        "@php artisan ide-helper:generate",
        "@php artisan ide-helper:meta"
    ]
},
```


## Reference

- [GitHub Repository](https://github.com/barryvdh/laravel-ide-helper)
- [Commands](https://github.com/barryvdh/laravel-ide-helper#automatic-phpdoc-generation-for-laravel-facades)
