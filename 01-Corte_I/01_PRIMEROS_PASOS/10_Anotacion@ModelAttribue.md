# Anotación @ModelAttribute 

<br>
<br>
La anotación `@ModelAttribute` es una anotación de Spring Framework que se utiliza en los controladores de Spring para enlazar datos del modelo a los métodos controladores. Se utiliza para prellenar el modelo con datos antes de que se ejecute un método controlador y para pasar esos datos entre la vista y el controlador.

Cuando se utiliza `@ModelAttribute`, Spring busca un atributo con el nombre especificado en el modelo y lo asigna al parámetro del método anotado. Esto es útil cuando deseas compartir ciertos datos entre diferentes métodos en un controlador o cuando deseas pasar datos iniciales al modelo antes de que se procese una solicitud.

Aquí hay un ejemplo de cómo se puede utilizar `@ModelAttribute` en un controlador de Spring:

```java
import org.springframework.stereotype.Controller;
import org.springframework.ui.Model;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.ModelAttribute;

@Controller
public class MyController {

    @ModelAttribute("welcomeMessage")
    public String getWelcomeMessage() {
        return "Welcome to our website!";
    }

    @GetMapping("/hello")
    public String sayHello(Model model) {
        // El mensaje de bienvenida se prellenará en el modelo
        return "hello";
    }
}
```

En este ejemplo:

- `@ModelAttribute("welcomeMessage")`: Define un método que proporciona un mensaje de bienvenida. El valor devuelto por este método se agrega automáticamente al modelo con el nombre "welcomeMessage".

- `@GetMapping("/hello")`: Define un método controlador que maneja las solicitudes GET en la URL "/hello". El mensaje de bienvenida prellenado se agregará al modelo automáticamente debido a la anotación `@ModelAttribute`.

En la vista correspondiente (por ejemplo, "hello.html"), puedes acceder al mensaje de bienvenida en el modelo utilizando la sintaxis Thymeleaf:

```html
<!DOCTYPE html>
<html xmlns:th="http://www.thymeleaf.org">
<head>
    <title>Hello Page</title>
</head>
<body>
    <h1 th:text="${welcomeMessage}">Default Message</h1>
</body>
</html>
```

En resumen, `@ModelAttribute` es una anotación en Spring que se utiliza para prellenar el modelo con datos antes de que se ejecute un método controlador y para pasar esos datos entre el controlador y la vista. Puede ser especialmente útil para compartir datos comunes entre varios métodos controladores.

<br>
<br>

## @ModelAttribute

Este modelo es común para todas las vistas del controlador, utilizar en todas las vista. 

![image](https://user-images.githubusercontent.com/31961588/218345400-f0e83dca-87a9-4636-9843-d30f8c198863.png)


![image](https://user-images.githubusercontent.com/31961588/218345751-9af6985c-f7d8-4b83-8f05-a2ab6f9de93d.png)


![image](https://user-images.githubusercontent.com/31961588/218345775-fa48aaab-542f-4ec8-9c48-9b4057da2c51.png)
