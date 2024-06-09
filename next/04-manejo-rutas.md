# MANEJO DE RUTAS 😀

## RUTAS BASICAS

| VSCODE | WEB |
| ------ | ------ |
| `app/dashboard/app.tsx` | http://localhost:8081/dashboard |
| `app/contact/app.tsx` | http://localhost:8081/contact |

## RUTAS ANIDADAS

| VSCODE | WEB |
| ------ | ------ |
| `app/blog/articulo-1/app.tsx` | http://localhost:8081/blog/articulo-1 |
| `app/contact/juan/app.tsx` | http://localhost:8081/contact/juan |

## RUTAS DINAMICAS

| VSCODE | WEB |
| ------ | ------ |
| `app/productos/[productId]/app.tsx` | http://localhost:8081/productos/1 |

Codigo:
```jsx
export default function ProductoDetails({params}) {
  <h1>Product: {params.productId}</h1>
}

```

## RUTAS OCULTAS

| VSCODE | WEB |
| ------ | ------ |
| `app/_oculta/app.tsx` | http://localhost:8081/_oculta |

No muestra en el navegador.

## RUTAS AGRUPADAS

| VSCODE | WEB |
| ------ | ------ |
| `app/(account)/login/app.tsx` | http://localhost:8081/login |
| `app/(account)/register/app.tsx` | http://localhost:8081/register |
| `app/(account)/password/app.tsx` | http://localhost:8081/password |









