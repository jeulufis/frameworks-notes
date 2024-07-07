# Anatomía de un componente 


Los componentes se dividen en:

- Una clase TS
- Una plantilla HTML
- Un selector CSS


```ts
@Component({
  selector: 'profile-photo',
  template: `<img src="profile-photo.jpg" alt="Your profile photo">`,
  styles: `img { border-radius: 50%; }`,
})
export class ProfilePhoto { }

```

De manera predeterminada el CSS solo afecta a los elementos definidos en la plantilla. 

Manera para importar otros componentes

```ts
@Component({
  selector: 'user-profile',
  template: `
    <profile-photo />
    <button>Upload a new profile photo</button>`,
  ...,
})
export class UserProfile { }
```