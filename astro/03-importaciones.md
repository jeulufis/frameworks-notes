# IMPORTACIONES

```js
import imgReference from './image.png'; // img === '/src/image.png'
import svgReference from './image.svg'; // svg === '/src/image.svg'
import txtReference from './words.txt'; // txt === '/src/words.txt'
```

## ALIAS

```astro
---
import Button from '@components/Button';
import logoUrl from '@assets/logo.png?url';
---
```

`tsconfig.json`

```astro
{
  "compilerOptions": {
    "baseUrl": ".",
    "paths": {
      "@components/*": ["src/components/*"],
      "@assets/*": ["src/assets/*"]
    }
  }
}
```
