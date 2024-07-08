# Selector components

Tipos de selectores :

- Selectores de tipo
- Selectores de atributos
- Selectores de clase

```ts
@Component({
  selector: 'profile-photo',
  ...
})
export class ProfilePhoto { }
```

Para utilizar un componente, se crea un elemento HTML correspondiente en las plantillas de otros componentes:

```ts
@Component({
  template: `
    <profile-photo />
    <button>Upload a new profile photo</button>`,
  ...,
})
export class UserProfile { }
```

