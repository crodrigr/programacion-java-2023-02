# Pasar datos a la vista

<br>
<br>

En el contexto de desarrollo de aplicaciones, especialmente en arquitecturas MVC (Modelo-Vista-Controlador) como Spring Boot, un "Model" se refiere a la representación de los datos y la lógica de negocio de una aplicación. El Model es la capa encargada de manejar los datos, realizar cálculos, aplicar reglas de negocio y en general, gestionar la lógica subyacente de la aplicación.

En Spring Boot y en muchos otros frameworks MVC, el Model puede ser representado por clases Java que encapsulan los datos y la funcionalidad relacionada con esos datos. Estas clases pueden estar enriquecidas con anotaciones y métodos que describen cómo se deben tratar y manipular los datos.

El Model trabaja en conjunto con las otras dos capas de la arquitectura MVC:

1. **Vista (View)**: Es la capa encargada de presentar los datos al usuario y de recibir las interacciones del usuario. En general, la Vista utiliza los datos proporcionados por el Modelo para renderizar la interfaz de usuario.

2. **Controlador (Controller)**: El Controlador actúa como intermediario entre la Vista y el Modelo. Recibe las interacciones del usuario desde la Vista, solicita los datos necesarios al Modelo y luego devuelve los datos adecuados a la Vista.

En resumen, en el contexto de Spring Boot y otras arquitecturas MVC, el "Model" representa la capa de la aplicación que maneja los datos y la lógica de negocio. Proporciona una abstracción del mundo real en forma de objetos Java y asegura que los datos se manipulen y se utilicen de manera coherente y según las reglas de negocio definidas.

<br>
<br>

### 1. A través de la interfaz model se envia valores a la interfaz

![image](https://user-images.githubusercontent.com/31961588/218002895-a12821c1-92e2-474f-ba29-f2f3a7106baa.png)

<br>
<br>

### 2. En la vista usar los datos pasados por el controlador

![image](https://user-images.githubusercontent.com/31961588/218003491-b824d939-227a-49fa-b4d7-5362e96f9824.png)


<br>
<br>

### 3. En title del index 

![image](https://user-images.githubusercontent.com/31961588/218003652-2395a84d-f142-4810-8c0b-0b97787ef1eb.png)
