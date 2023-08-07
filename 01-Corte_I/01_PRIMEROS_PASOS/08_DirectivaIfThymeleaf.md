# Directiva if de Thymeleaf

<br>
<br>
Thymeleaf es un motor de plantillas para aplicaciones web escritas en Java, especialmente diseñado para trabajar con el framework Spring. Permite crear vistas HTML de manera dinámica, donde puedes mezclar código Java y HTML de forma sencilla y efectiva.

Las características clave de Thymeleaf son:

1. **Fácil Integración con Spring**: Thymeleaf se integra perfectamente con el framework Spring, lo que lo convierte en una opción popular para la capa de vista en aplicaciones Spring y Spring Boot.

2. **Sintaxis Amigable**: La sintaxis de Thymeleaf es similar a HTML, lo que facilita la lectura y escritura de plantillas. Esto permite que los desarrolladores con conocimientos de HTML puedan trabajar cómodamente con Thymeleaf.

3. **Expresiones**: Thymeleaf permite usar expresiones en las plantillas para acceder a datos del modelo (objetos Java) y mostrarlos en la vista.

4. **Iteraciones y Condicionales**: Puedes usar bucles y condicionales en las plantillas para mostrar datos de manera dinámica según la lógica de negocio.

5. **Procesamiento del Lado del Servidor**: Thymeleaf es un motor de plantillas que se procesa en el lado del servidor, lo que significa que las plantillas se convierten en HTML antes de ser enviadas al navegador. Esto es beneficioso para la seguridad y la optimización de la página.

6. **Internacionalización y Localización**: Thymeleaf ofrece soporte integrado para internacionalización y localización de textos en las plantillas.

7. **Acceso a Propiedades y Recursos**: Puedes acceder a propiedades y recursos en las plantillas, lo que facilita la configuración y personalización de la aplicación.

8. **Fragmentos y Plantillas Reutilizables**: Thymeleaf permite la creación de fragmentos reutilizables y plantillas que pueden ser compartidos entre múltiples páginas.

9. **Seguridad**: Thymeleaf proporciona herramientas para prevenir ataques XSS (cross-site scripting) en las plantillas.

Un ejemplo simple de uso de Thymeleaf en una plantilla:

```html
<!DOCTYPE html>
<html xmlns:th="http://www.thymeleaf.org">
<head>
    <title>My Page</title>
</head>
<body>
    <h1 th:text="${pageTitle}">Default Title</h1>
    <p th:if="${showMessage}">Hello, Thymeleaf!</p>
</body>
</html>
```

En este ejemplo, `th:text` y `th:if` son atributos Thymeleaf que permiten mostrar dinámicamente valores del modelo y realizar condicionales en la plantilla.

En resumen, Thymeleaf es una herramienta poderosa y versátil para generar vistas dinámicas en aplicaciones web Java, especialmente en combinación con el framework Spring.

<br>
<br>

## 1. If else si el usuario no tiene correo

![image](https://user-images.githubusercontent.com/31961588/218344104-d0d86c3d-3537-4f3f-99aa-8fc7eb31921e.png)


## 2. Ejecución 

![image](https://user-images.githubusercontent.com/31961588/218344143-3e4f2ed6-4e53-4b79-96af-9297e42dd7af.png)


