# Laravel - Getting Started On Windows with Sail, WSL and Docker

## Requirements

- Ubuntu 20.04 on Windows (or equivalent)
- Windows Subsystem for Linux 2 (WSL2)
- Docker Desktop

## Installation

Start Docker Desktop.

From Ubuntu terminal:

```
curl -s https://laravel.build/[app-name] | bash
```

```
cd [app-name] && sail up
```

Open dir in Visual Studio Code:

```
code .
```

## Vite Fix (Laravel 9)

Fix Vite configuration for Sail as mentioned [here](https://github.com/laravel/vite-plugin/pull/42) by editing ```vite.config.js```:

```diff
import { defineConfig } from 'vite';
import laravel from 'laravel-vite-plugin';

export default defineConfig({
    plugins: [
        laravel({
            input: ['resources/css/app.css', 'resources/js/app.js'],
            refresh: true,
        }),
    ],
+    server: {
+        hmr: {
+            host: 'localhost',
+        },
+    },
});
```

## Usage

Use ```sail``` instead of ```php```:

```
sail artisan migrate
```

Start Docker Container:

```
sail up
```