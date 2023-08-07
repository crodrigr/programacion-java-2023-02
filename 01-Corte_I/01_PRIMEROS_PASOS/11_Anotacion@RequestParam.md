# Anotación @RequestParam

<br>
<br>

La anotación `@RequestParam` es una anotación de Spring Framework que se utiliza en los controladores para vincular parámetros de solicitud HTTP a los parámetros de los métodos controladores. Permite extraer valores específicos de los parámetros de una solicitud HTTP y pasarlos directamente como argumentos a un método controlador.

Cuando se utiliza `@RequestParam`, Spring buscará el valor del parámetro correspondiente en la URL de la solicitud y lo asignará automáticamente al parámetro del método anotado.

Aquí tienes un ejemplo de cómo se utiliza `@RequestParam` en un controlador de Spring:

```java
import org.springframework.stereotype.Controller;
import org.springframework.ui.Model;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.RequestParam;

@Controller
public class MyController {

    @GetMapping("/hello")
    public String sayHello(@RequestParam(name = "name", required = false, defaultValue = "Guest") String name, Model model) {
        String greeting = "Hello, " + name + "!";
        model.addAttribute("greeting", greeting);
        return "hello";
    }
}
```

En este ejemplo:

- `@GetMapping("/hello")`: Define un método controlador que maneja las solicitudes GET en la URL "/hello".

- `@RequestParam(name = "name", required = false, defaultValue = "Guest")`: La anotación `@RequestParam` se utiliza para vincular el parámetro de solicitud llamado "name" al parámetro `String name` del método controlador. `required = false` indica que el parámetro no es obligatorio en la URL y `defaultValue = "Guest"` proporciona un valor predeterminado en caso de que el parámetro no se especifique en la URL.

El valor del parámetro "name" en la URL se pasa directamente al método controlador, donde se concatena con un mensaje de saludo y se agrega al modelo. Luego, este mensaje se mostrará en la vista correspondiente (por ejemplo, "hello.html") utilizando Thymeleaf.

```html
<!DOCTYPE html>
<html xmlns:th="http://www.thymeleaf.org">
<head>
    <title>Hello Page</title>
</head>
<body>
    <h1 th:text="${greeting}">Default Greeting</h1>
</body>
</html>
```

En resumen, `@RequestParam` es una anotación en Spring que se utiliza para vincular parámetros de solicitud HTTP a los parámetros de los métodos controladores. Esto permite acceder y utilizar los valores de los parámetros de manera conveniente en tus controladores.


<br>
<br>

## 1. Crear un controlador EjemploParamsController

Este param es un handler que recibe un parametro por la url y luego lo muestra

![image](https://user-images.githubusercontent.com/31961588/218346404-a5f1a151-0cd6-4f30-a82c-3399aa9f926a.png)

<br>
<br>

## 2. Vista param/ver.html

![image](https://user-images.githubusercontent.com/31961588/218346479-9862b464-ad07-4b62-ae18-e3a1698f02e3.png)

<br>
<br>

## 3. Ejecutar

![image](https://user-images.githubusercontent.com/31961588/218346582-b1a8c05e-ca75-44c5-a49a-187f1e3f37ce.png)

<br>
<br>

## 4. index

![image](https://user-images.githubusercontent.com/31961588/218347064-3ab2a66c-682c-40fe-a63c-9ae8edd7b7d3.png)

<br>
<br>

## 5. index.html

![image](https://user-images.githubusercontent.com/31961588/218347084-1f1a4f02-ca09-42bc-9204-37a31b53a85a.png)

<br>
<br>

## 6. Ejecutar

![image](https://user-images.githubusercontent.com/31961588/218347041-bbeba664-591e-4c46-ab9a-809141b05544.png)
