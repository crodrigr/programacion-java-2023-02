# Taller de Relaciones

**Spring boot**, **Srping Data**, **Base datos SQL**, **Relaciones**

Basado en este diagrama de clase, se oberva una relación de asociación entre **libro** y **autor** para este escenario es una relación **unidirecional** de libro a autor
de **uno a muchos**

![image](https://github.com/crodrigr/programacion-java-2023-02/assets/31961588/924d128d-0bbc-4229-88d4-581d7ad8346d)

Desarrolle un **api** que va tener un dos servicios:

  - Listar todos los libros con sus autores: **"/libros/"**
  - Obtener un libro por **ISBN**:           **"/libros/058bn4"**

La base de datos a utilizar es **h2** y debe generar los scripts haga el insert de 10 ejemplares con sus respectivos autores. Cree libros donde tenga uno o varios autores.

El diseño de la base datos y sus relaciones se va realizar **firstCode**, es decir, se diseña las clases entities las cuales usa las anotaciones respectivas para hacer el mapeo de los objetos en la capa de persistencia, tener encuenta las relaciones. Por otra parte, el proyecto debe manejar esta estructura de capas: controllers, services y repositories. 

![image](https://github.com/crodrigr/programacion-java-2023-02/assets/31961588/be9e08c5-a147-4122-98d5-555b0c98a8f8)




    

  
