# LINK Y ROUTER CLIENT
`<Link>` is a React component that extends the HTML `<a>`

- `href` (required)

```jsx
import Link from 'next/link'
 
function Home() {
  return (
    <ul>
      <li>
        <Link href="/">Home</Link>
      </li>
      <li>
        <Link href="/about">About Us</Link>
      </li>
      <li>
        <Link href="/blog/hello-world">Blog Post</Link>
      </li>
    </ul>
  )
}
 
export default Home
```

- `scroll` El comportamiento predeterminado de <Link> es desplazarse hasta la parte superior de una nueva ruta o mantener la posición de desplazamiento para navegar hacia adelante y hacia atrás.

```jsx
import Link from 'next/link'
 
export default function Page() {
  return (
    <Link href="/dashboard" scroll={false}>
      Dashboard
    </Link>
  )
}
```

## RUTAS DINAMICAS
```jsx
import Link from 'next/link'
 
function Posts({ posts }) {
  return (
    <ul>
      {posts.map((post) => (
        <li key={post.id}>
          <Link href={`/blog/${post.slug}`}>{post.title}</Link>
        </li>
      ))}
    </ul>
  )
}
 
export default Posts
```
