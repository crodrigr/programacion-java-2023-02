# El Objeto Modelo

<br>
<br>
Una clase POJO (Plain Old Java Object) es un término utilizado en la programación Java para describir una clase simple y común que no depende de ningún marco o biblioteca específica. En esencia, un POJO es una clase Java que sigue ciertas convenciones y prácticas para mantener su simplicidad y reutilización.

Las características de una clase POJO incluyen:

1. **No dependencia de marcos externos**: Una clase POJO no debe depender de ninguna biblioteca o marco específico. No contiene anotaciones o interfaces especiales de bibliotecas como Spring, Hibernate, Java EE, etc.

2. **Utiliza los estándares de Java**: Una clase POJO sigue las convenciones estándar de Java para definir atributos (variables de instancia), constructores, métodos getters y setters, y otros métodos de utilidad.

3. **Serialización y deserialización sencillas**: Los objetos POJO se pueden serializar y deserializar fácilmente a y desde diferentes formatos, como JSON o XML.

4. **Facilita la reutilización y el mantenimiento**: Al no estar vinculados a marcos específicos, los POJO son más portátiles y pueden reutilizarse en diferentes proyectos.

5. **Enfocado en la lógica del dominio**: Los POJOs suelen representar entidades del mundo real y encapsulan la lógica relacionada con el dominio de la aplicación.

Aquí hay un ejemplo simple de una clase POJO:

```java
public class Person {
    private String firstName;
    private String lastName;
    private int age;

    // Constructor
    public Person(String firstName, String lastName, int age) {
        this.firstName = firstName;
        this.lastName = lastName;
        this.age = age;
    }

    // Getters y Setters
    public String getFirstName() {
        return firstName;
    }

    public void setFirstName(String firstName) {
        this.firstName = firstName;
    }

    public String getLastName() {
        return lastName;
    }

    public void setLastName(String lastName) {
        this.lastName = lastName;
    }

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        this.age = age;
    }
}
```

En resumen, una clase POJO es simplemente una clase Java ordinaria que sigue ciertas convenciones para mantener la simplicidad y la reutilización. Estas clases son una parte fundamental en la programación Java y son ampliamente utilizadas en varios contextos, incluyendo el desarrollo de aplicaciones y la comunicación entre componentes.


<br>
<br>

## 1. Crear la clase Usuario

Esta clase en un clase POJO de java que va estar dentro el paquete model. 

Atributos y métodos constructores

![image](https://user-images.githubusercontent.com/31961588/218343459-cc38980f-14a2-4135-8e58-f9db1f8f32e0.png)

Métodos getter y setter

![image](https://user-images.githubusercontent.com/31961588/218343483-5f2589e9-f340-4f04-aa31-c417a442a3e9.png)

## 2. IndexController crear un nuevo servicio

En el IndexController se crea un nuevo servicio con requestMapping que va desplegar la información del usuario en un vista perfil

![image](https://user-images.githubusercontent.com/31961588/218343925-5b3afc7b-064d-49bc-9d64-bbae8cfd0d1a.png)

### 2.1 Perfil.html

![image](https://user-images.githubusercontent.com/31961588/218343951-47af6673-bbd5-4753-9a6c-9d5dc69cd22b.png)


### 2.2  Ejecución

![image](https://user-images.githubusercontent.com/31961588/218343972-e5f791f9-09ce-44d0-863b-3517bb445ac9.png)
