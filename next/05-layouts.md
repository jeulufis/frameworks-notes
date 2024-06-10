# MANEJO DE LAYOUT

![image](https://github.com/jeulufis/frameworks-notes/assets/92868937/49d9d25f-de2e-46cc-b9c1-8e323df6c519)


Un layout es una interfaz de usuario que se comparte entre rutas.

`app/dashborad/layout.tsx`
```js
export default function DashboardLayout({
  children,
}: {
  children: React.ReactNode
}) {
  return <section>{children}</section>
}
```


