# MANEJO DE RUTAS 😀

## RUTAS BASICAS
`app/dashboard/app.tsx`

http://localhost:8081/dashboard

`app/contact/app.tsx`

http://localhost:8081/contact


## RUTAS ANIDADAS
`app/blog/articulo-1/app.tsx`

http://localhost:8081/blog/articulo-1

`app/contact/juan/app.tsx`

http://localhost:8081/contact/juan

## RUTAS DINAMICAS
`app/productos/[productId]/app.tsx`

http://localhost:8081/productos/1

Codigo:
```jsx
export default function ProductoDetails({params}) {
  <h1>Product: {params.productId}</h1>
}

```

## RUTAS OCULTAS

## RUTAS AGRUPADAS
