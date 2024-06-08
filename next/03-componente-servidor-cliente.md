# COMPONENTES DEL LADO DEL SERVIDOR Y CLIENTE

## COMPONENTE SERVIDOR

- Permite escribir UI.
- Rendimiento: optimiza el rendimiento.
- Seguridad: permiten mantener datos y lógica confidenciales en el servidor, como tokens y claves API.
- Optimización de motores de busqueda:

## COMPONENTE CLIENTE

- Interactividad: pueden ocupar detectores de estados, efectos y eventos.
- API del navegador: tienen acceso a las API del navegador, como la geolocalización.o almacenamiento local.

```js
'use client'
 
import { useState } from 'react'
 
export default function Counter() {
  const [count, setCount] = useState(0)
 
  return (
    <div>
      <p>You clicked {count} times</p>
      <button onClick={() => setCount(count + 1)}>Click me</button>
    </div>
  )
}
```
