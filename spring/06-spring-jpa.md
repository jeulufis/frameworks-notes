# SPRING JPA

`application.properties`

```
spring.datasource.url=jdbc:mysql://localhost:3306/spring-data-jpa-example
spring.datasource.password=password
spring.datasource.username=root
spring.datasource.driver-class=com.mysql.cj.jdbc.Driver

spring.jpa.hibernate.ddl-auto=create-drop // crear entidades y despues borrar -> solo ambiente de pruebas
spring.jpa.show-sql=true // muestra las consultas
```

- https://howtodoinjava.com/spring-boot2/datasource-configuration/

las tablas de mysql se manejan en prural y las entitades en singular

## CREAR ENTIDAD
- proyecto
  - App.java
    - `persistence`
      - `entity`
        - `Address.java`

```java
@Entity // ->  necesaria para definir entidades
@Table(name = "addresses") // -> conectarla a la tabla addresses
public class Address {

  @Id // -> llave primaria
  @GeneratedValue(strategy = GenerationType.IDENTITY) // -> autoincremental
  private Long id;

  @Column(name = "country")
  private String country;

  @Column(name = "address")
  private String address;

  // GETTERS AND SETTERS

  // TO STRING
}

```

## CREAR REPOSITORIO
- proyecto
  - App.java
    - `persistence`
      - entity
        - Address.java
      - `repository`
        - `AddressRepository.java`
       
```java
// data.repository
public interface AddressRepository extends Repository<Customer, Long> {
  // Customer -> entidad
  // Long -> Tipo de dato del id

  List<Address> findAll(); // java.utils.List

  Optional<Address> findById(); // java.utils.Optional

  Customer save(Customer customer);

  voide deleteById();
}
```

## REPOSITORY RECOMENDADO

```java
public interface AddressRepository extends JpaRepository<Customer, Long> {

}
```

- `CrudRepository` Proporciona principalmente funciones CRUD.
- `PagingAndSortingRepository` proporciona métodos para paginar y ordenar registros.
- `JpaRepository` proporciona algunos métodos relacionados con JPA, como vaciar el contexto de persistencia y eliminar registros en un lote.

## TAREAS

- [ ] Configurar application properties
- [ ] Correr Spring Boot
- [ ] MYSQL datos
- [ ] Crear entidad
- [ ] Crear repositorio
