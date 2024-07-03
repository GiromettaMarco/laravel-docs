# Ziggy with TypeScript

This document is a memorandum for using Ziggy in a TypeScript project.

## Config

Update ```tsconfig.json``` compiler options with:

```
{
  "compilerOptions": {
    "paths": {
      "ziggy-js": ["./vendor/tightenco/ziggy"]
    }
  }
}
```

## Generate Types

Generate the file ```.\resources\js\ziggy.d.ts``` with:

```
php artisan ziggy:generate --types-only
```

Then add the following code on top:

```
import { route as routeFn } from 'ziggy-js'

declare module '@vue/runtime-core' {
  interface ComponentCustomProperties {
    route: typeof routeFn
  }
}

declare global {
  var route: typeof routeFn
}
```

Format the document with 2 spaces tab and remove ```export {};``` at the end if you want.


## Reference

- [Ziggy documentation](https://github.com/tighten/ziggy?tab=readme-ov-file#typescript)
- [ComponentCustomProperties](https://github.com/vuejs/language-tools/blame/1b90234ec6f10a3c0f080d0310711c2cd8de02dd/extensions/vscode-vue-language-features/README.md#L95-L100)
