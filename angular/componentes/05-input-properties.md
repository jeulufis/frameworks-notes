# Pasando datos por input

Las propiedades de entrada son similares a los props de react.

Al crear un componente, puede marcar propiedades de clase específicas como enlazables agregando el @Input decorador en la propiedad:

```ts
@Component({...})
export class CustomSlider {
  @Input() value = 0;
}
```

Esto le permite vincularse a la propiedad en una plantilla:

<custom-slider [value]="50" />

## Entradas requeridas

Tienes que usar `required`>

```ts
@Component({...})
export class CustomSlider {
  @Input({required: true}) value = 0;
}```