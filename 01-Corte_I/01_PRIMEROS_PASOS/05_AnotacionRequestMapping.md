# Anotación @RequestMapping sobre el controlador

<br>
<br>

La anotación `@RequestMapping` es una de las anotaciones fundamentales en Spring Framework y Spring Boot. Se utiliza para mapear las solicitudes HTTP a métodos específicos en un controlador. Esta anotación le dice a Spring qué método del controlador debe invocarse cuando se recibe una solicitud HTTP con una URL específica y un método HTTP específico (GET, POST, PUT, DELETE, etc.).

Aquí hay un ejemplo básico de cómo se puede utilizar `@RequestMapping` en un controlador de Spring Boot:

```java
import org.springframework.stereotype.Controller;
import org.springframework.web.bind.annotation.RequestMapping;
import org.springframework.web.bind.annotation.RequestMethod;
import org.springframework.web.bind.annotation.ResponseBody;

@Controller
public class MyController {

    @RequestMapping(value = "/hello", method = RequestMethod.GET)
    @ResponseBody
    public String sayHello() {
        return "Hello, world!";
    }
}
```

En este ejemplo:

- `@Controller`: Marca la clase como un controlador de Spring MVC.

- `@RequestMapping(value = "/hello", method = RequestMethod.GET)`: Mapea la URL "/hello" con el método `sayHello()` y especifica que el método debe invocarse cuando se recibe una solicitud HTTP GET en esa URL.

- `@ResponseBody`: Indica que el valor devuelto por el método debe ser serializado y enviado en el cuerpo de la respuesta HTTP.

Cuando se recibe una solicitud GET en la URL "/hello", el método `sayHello()` se ejecutará y devolverá la cadena "Hello, world!", que se enviará como respuesta al cliente.

La anotación `@RequestMapping` es muy versátil y puede configurarse con varios atributos, como `value`, `method`, `params`, `headers`, etc., para personalizar el mapeo de solicitudes. También puedes usar anotaciones específicas para métodos HTTP, como `@GetMapping`, `@PostMapping`, `@PutMapping` y `@DeleteMapping`, que son atajos para definir métodos específicos de solicitud HTTP.

Ten en cuenta que, a partir de versiones más recientes de Spring Boot, es común utilizar estas anotaciones más específicas para mejorar la legibilidad del código y reducir la cantidad de código boilerplate.


<br>
<br>

### 1. RequestMappig /app

Para cualquier servicio (handler) del controlador indexController que se quiera acceder debe estár precedido por /app

![image](https://user-images.githubusercontent.com/31961588/218004845-f3d320d6-2487-4285-a3aa-58d1f59a3063.png)

### 2. /app/index /app/ /app/home

![image](https://user-images.githubusercontent.com/31961588/218005174-ebb0cf6f-a7c3-4f55-b477-8756018f8d58.png)


![image](https://user-images.githubusercontent.com/31961588/218005261-fd437108-d5b2-4ff5-b674-f94e2814c864.png)
