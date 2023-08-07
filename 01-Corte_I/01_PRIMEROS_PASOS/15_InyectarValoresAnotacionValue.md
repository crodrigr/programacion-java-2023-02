# Inyectando valores usando @Anotacion Value

<br>
<br>

La anotación `@Value` en Spring se utiliza para inyectar valores de propiedades configurables en los campos de una clase. Puedes utilizar esta anotación para acceder a valores definidos en archivos de propiedades, variables de entorno u otras fuentes de configuración y asignar esos valores a campos en tus componentes de Spring.

Aquí hay un ejemplo de cómo se utiliza `@Value` en una clase de Spring:

```java
import org.springframework.beans.factory.annotation.Value;
import org.springframework.stereotype.Component;

@Component
public class MyComponent {

    @Value("${app.title}")
    private String appTitle;

    public String getAppTitle() {
        return appTitle;
    }
}
```

En este ejemplo:

- `@Value("${app.title}")`: La anotación `@Value` se utiliza para inyectar el valor de la propiedad `app.title` en el campo `appTitle` de la clase. El valor se lee de un archivo de propiedades configurado en la aplicación.

Luego, puedes acceder al valor inyectado llamando al método `getAppTitle()` en una instancia de `MyComponent`.

Esta anotación es especialmente útil para inyectar configuraciones externas en tus componentes de Spring, lo que permite una mayor flexibilidad y configurabilidad en tu aplicación.

Ten en cuenta que para que `@Value` funcione, debes asegurarte de que la configuración adecuada para la resolución de propiedades (como la ubicación de los archivos de propiedades) esté configurada en tu aplicación Spring.

<br>
<br>

## 1. Crear archivo de textos en el resources diferente al application.properties

### 1.1
![image](https://user-images.githubusercontent.com/31961588/219501578-2ebc4505-6c66-459e-a19f-75525d0c9db9.png)

<br>
<br>

 ### 1.2
![image](https://user-images.githubusercontent.com/31961588/219501750-31308958-3312-489c-8373-adcdd49e2ab8.png)

<br>
<br>

 ### 1.3
![image](https://user-images.githubusercontent.com/31961588/219503320-fc68b710-cd18-4b7c-bc05-fceee17ce3f6.png)

<br>
<br>

## 2. Implementar el texto de configuración a través del operado value

![image](https://user-images.githubusercontent.com/31961588/219501687-53f28998-93cf-4679-9615-57d65bf1a2c2.png)
<br>
<br>