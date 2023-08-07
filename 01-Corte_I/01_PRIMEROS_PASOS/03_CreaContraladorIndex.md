# Crear controlador y index

<br>
<br>

Las anotaciones en Spring Boot son una parte fundamental del enfoque de programación basado en metadatos que Spring proporciona. Estas anotaciones se utilizan para configurar, personalizar y administrar varios aspectos de una aplicación Spring Boot. Aquí hay algunas anotaciones clave que se utilizan comúnmente en Spring Boot:

1. **@SpringBootApplication**: Esta es una anotación compuesta que se utiliza en la clase principal de la aplicación Spring Boot. Combina varias anotaciones, incluidas `@Configuration`, `@EnableAutoConfiguration` y `@ComponentScan`, lo que permite la configuración automática y el escaneo de componentes.

2. **@Controller**: Marca una clase como un controlador de Spring MVC, que maneja las solicitudes HTTP.

3. **@RestController**: Es una versión especializada de `@Controller` que combina `@Controller` y `@ResponseBody`, lo que hace que los métodos del controlador devuelvan datos en lugar de vistas.

4. **@Service**: Indica que una clase es un servicio que contiene la lógica de negocio de la aplicación.

5. **@Repository**: Se utiliza para marcar una clase como un repositorio de Spring Data, que maneja la interacción con la base de datos.

6. **@Component**: Es una anotación genérica que indica que una clase es un componente gestionado por Spring. Puede ser utilizado para cualquier componente.

7. **@Autowired**: Se utiliza para inyectar dependencias automáticamente en los beans. Puede aplicarse a campos, constructores y métodos setters.

8. **@Value**: Se utiliza para inyectar valores de propiedades configurables en los beans.

9. **@RequestMapping**: Mapea las solicitudes HTTP a métodos de controlador específicos. Puede especificar la URL, el método HTTP y otros atributos.

10. **@PathVariable**: Se utiliza para mapear valores de variables de la URL a parámetros de método en un controlador.

11. **@RequestParam**: Se utiliza para inyectar parámetros de solicitud HTTP en un método de controlador.

12. **@ResponseBody**: Indica que el valor devuelto por un método de controlador debe ser serializado y devuelto en el cuerpo de la respuesta HTTP.

13. **@Entity**: Se utiliza para marcar una clase como una entidad JPA, que se asigna a una tabla en la base de datos.

14. **@Transactional**: Indica que un método o clase debe estar involucrado en una transacción.

15. **@EnableAutoConfiguration**: Habilita la configuración automática de Spring Boot basada en las dependencias en el proyecto.

Estas son solo algunas de las anotaciones más comunes en Spring Boot. Cada anotación tiene un propósito específico y te permite personalizar y configurar diferentes aspectos de tu aplicación de manera declarativa.

<br>
<br>

### 1. Crear el IndexController

![image](https://user-images.githubusercontent.com/31961588/217998843-2ea5bd68-c0f6-4043-81cd-371e98e58395.png)

<br>
<br>

### 2. Crear el template index.html

![image](https://user-images.githubusercontent.com/31961588/217997551-15eb0f39-5894-44a1-b83f-bd5d42aeb9c1.png)

<br>
<br>

#### 2.1 Validar que se UTF-8

![image](https://user-images.githubusercontent.com/31961588/217998367-aa345a85-e580-42ff-8535-3e984f1cbb35.png)



##### En index.html clic derecho propiedades 

![image](https://user-images.githubusercontent.com/31961588/217998574-550ef87d-82e3-43f0-b880-d3bd0fc8f400.png)

<br>
<br>

### 3. Lanzar el proyecto

#### 3.1 Lanzar proyecto
![image](https://user-images.githubusercontent.com/31961588/217998915-1d2d9e67-832e-4ae3-aba9-51b858215e04.png)


<br>

#### 3.2 servidor tomcat
![image](https://user-images.githubusercontent.com/31961588/217999007-3a7b094a-490a-4cc6-a292-531d2c853ea6.png)


<br>

#### 3.3 http://localhost:8080/index
![image](https://user-images.githubusercontent.com/31961588/217999067-d59f9d64-af7f-4fe3-96f0-c8d8711e5a0a.png)

#### 3.4 Si no reconoce index.html 

Colocar en properties

[Error no load index](https://stackoverflow.com/questions/31944355/error-resolving-template-index-template-might-not-exist-or-might-not-be-acces)

```Properties
spring.thymeleaf.prefix=classpath:/templates/
spring.thymeleaf.suffix=.html
```
