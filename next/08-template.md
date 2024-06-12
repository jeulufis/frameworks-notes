# TEMPLATE

Un archivo de plantilla es similar a un diseño en el sentido de que envuelve cada diseño o página secundario.
A diferencia de los diseños que persisten en las rutas y mantienen el estado, las plantillas crean una nueva instancia para cada uno de sus hijos en la navegación.

`app/template.tsx`

```tsx
export default function Template({ children }: { children: React.ReactNode }) {
  return <div>{children}</div>
}
```

Si no quieres compartir estados o efectos en otras paginas, ocupa template y lo limpiara (cuando cambies de pagina).
