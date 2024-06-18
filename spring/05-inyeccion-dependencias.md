# INYECCION DE DEPENDENCIAS 

Es un patron de software, tambien conocido como inversion de control, en que puedes conseguir un codigo mas desacoplado, que facilita en hacer test y cambiar funcionalidades.

Suministra objetos ya creados a una clase o función.

En el constructor de la clase o en la definición de la función, se solicitará un objeto que la misma clase o función utilizará internamente.



Spring `@Autowired` es una de las anotaciones más habituales cuando trabajamos con Spring Framework ya que se trata de la anotación que permite inyectar unas dependencias con otras dentro de Spring .

```java
@Repository
public MiRepository {
	....
}

@Service
public MiService {

  @Autowire
  private MiRepository repository;

}
```

Si queremos ocupar inyeccion de dependencias necesitamos que los anteriores `bean` tambien tengan otras inyecciones.

## Ejemplo practico
- Componente `controller` utiliza el `service`
- Componente `service` utiliza el `repository` para la bd.

Ayuda mucho al momento de escribir un código limpio y mantenible. 
Recuerden qué debemos escribir un código para que los otros lean, y quien sabe, hasta que nuestros "yo" del futuro entiendan pasado unos meses.
