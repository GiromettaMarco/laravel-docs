# Laravel - Getting Started On Windows with Sail, WSL and Docker

## Requirements

- Ubuntu 20.04 on Windows (or equivalent)
- Windows Subsystem for Linux 2 (WSL2)
- Docker Desktop

## Installation

From Ubuntu terminal:

```
curl -s https://laravel.build/example-app | bash

cd example-app
 
./vendor/bin/sail up
```

Open dir in Visual Studio Code:

```
code .
```

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

## Usage

Use 'sail' instead of 'php':

```
sail artisan migrate
```

Start Docker Container:

```
sail up
```