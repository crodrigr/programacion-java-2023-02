# Anotación @PathVariable

<br>
<br>

La anotación `@PathVariable` en Spring MVC se utiliza para extraer los valores de las variables de la URL (segmentos de la URL) y vincularlos a los parámetros de los métodos controladores. Es especialmente útil cuando deseas capturar valores dinámicos de la URL y utilizarlos en el procesamiento de la solicitud.

La anotación `@PathVariable` se utiliza en combinación con una variable en el método controlador y se coloca en el nivel de parámetros del método. Puedes especificar el nombre de la variable de la URL que deseas capturar.

Aquí hay un ejemplo de cómo se utiliza `@PathVariable` en un controlador de Spring MVC:

```java
import org.springframework.stereotype.Controller;
import org.springframework.ui.Model;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.PathVariable;

@Controller
public class MyController {

    @GetMapping("/hello/{name}")
    public String sayHello(@PathVariable String name, Model model) {
        String greeting = "Hello, " + name + "!";
        model.addAttribute("greeting", greeting);
        return "hello";
    }
}
```

En este ejemplo, el método controlador maneja las solicitudes GET en una URL que incluye un segmento de variable `{name}`. La anotación `@PathVariable` se utiliza para vincular el valor del segmento de la URL al parámetro `String name` del método.

En la vista correspondiente (por ejemplo, "hello.html"), puedes acceder al valor del parámetro utilizando la sintaxis Thymeleaf:

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

Cuando se accede a la URL "/hello/John", el valor "John" se captura del segmento de la URL y se utiliza en el mensaje de saludo.

En resumen, `@PathVariable` es una anotación en Spring MVC que te permite capturar y utilizar valores dinámicos de los segmentos de la URL en tus métodos controladores para procesar la solicitud de manera efectiva.

<br>
<br>

## 1. Creamos un controlador que tiene un handler que recibe un pathVariable

![image](https://user-images.githubusercontent.com/31961588/218347788-48484de4-d428-4467-9de7-59e3a7fc772e.png)

<br>
<br>

## 2. Creamos la vista /variables/ver

![image](https://user-images.githubusercontent.com/31961588/218347976-a86de1ab-f5f3-4c80-8abb-2fb85d38d66d.png)

## 3. Ejecutar

![image](https://user-images.githubusercontent.com/31961588/218348095-f0c2aca3-8938-47d9-81fc-64739be168a3.png)

<br>
<br>

## 4. Enviar varios valores por pathVariables. Es mas limpia y amigable para los navegadores. 

![image](https://user-images.githubusercontent.com/31961588/218348173-c0a65793-e2ef-4aa0-93c4-fa582fee6c3b.png)

<br>
<br>

## 5. Ejecutar

![image](https://user-images.githubusercontent.com/31961588/218348256-44d5663d-2edb-4d4d-90bd-039fe537af1d.png)
