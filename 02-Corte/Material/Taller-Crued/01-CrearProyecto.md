# Spring boot

<br>
<br>

## 1. Plantilla proyecto


<br>
<br>

![image](https://github.com/crodrigr/programacion-java-2023-02/assets/31961588/6d54a55f-37de-49e1-9684-b85786588c7b)


<br>
<br>
<br>
<br>

## 2. Crear estructura proyecto

<br>
<br>

Este proyecto va tener tres capas: controllers, businnes, persistences

![image](https://github.com/crodrigr/programacion-java-2023-02/assets/31961588/2f43b349-9502-4076-a2e6-4cc1c57b7fec)


<br>
<br>
<br>
<br>

## 2. ClienteDocument

<br>
<br>

Dentro del paquete **persistences** se crea un nuevo paqute **documents**, en el cual, van todas las clases de tipo documents. Se crea **ClienteDocument.java** va ser la clase se que va a mapear con la base de datos de mongo.


![image](https://github.com/crodrigr/programacion-java-2023-02/assets/31961588/033ebe9e-aace-4f87-a282-b3ad4451ee5d)

<br>
<br>
<br>
<br>

## 3. ClienteRepository

<br>
<br>

Se crea dentro del paqute **persistences** el paquete **repositories**, cual va tener la inferface **ClienteRepository.java** que hereda de **CruedRepository** que tiene métodos del **crued** que va aplicar para **ClienteDocument**

![image](https://github.com/crodrigr/programacion-java-2023-02/assets/31961588/a9848d93-a5cc-4e8f-a9f0-41ef7896bce1)

<br>
<br>
<br>
<br>

## 4. ClienteService

<br>
<br>

En la capa **businnes** se crea la interface **ClienteService** que tiene la logica del negocio, este caso, los métodos del crud**.

![image](https://github.com/crodrigr/programacion-java-2023-02/assets/31961588/15300544-32c0-4936-85e5-ff88818bd476)


<br>
<br>
<br>
<br>

## 5. ClienteServiceImpl


<br>
<br>

Se crea el paqute **impl** donde se coloca la implementación de las interfaces de servicio. En esta caso **ClienteServiceImpl**. En esta clase se define como **@Service**, se inyecta **ClienteRepository** y se implementa todos los métodos del crued.

![image](https://github.com/crodrigr/programacion-java-2023-02/assets/31961588/109705b0-07f8-4447-ba09-cdd4d4048a4a)

<br>
<br>
<br>
<br>


## 6. ClienteController


<br>
<br>

Se crea la clase de tipo controller, la cual, van se consume los servicios que están en la capa **businness** a través de la inyección de independencia. 

![image](https://github.com/crodrigr/programacion-java-2023-02/assets/31961588/fd95a86b-5c15-49ba-acb6-8b3c71723ca5)


<br>
<br>
<br>
<br>


### 6.1 ClienteController - /istar


<br>
<br>

![image](https://github.com/crodrigr/programacion-java-2023-02/assets/31961588/334512ba-a7d2-41c0-ae74-4f29dd6c0fec)


<br>
<br>
<br>
<br>

### 6.2 ClienteController - /form


<br>
<br>import javax.validation.Valid;


![image](https://github.com/crodrigr/programacion-java-2023-02/assets/31961588/dd826bb4-e449-4eb5-a336-e0e26cebaa17)

<br>
<br>
<br>
<br>

### 6.3 ClienteController - /form/{id}


<br>
<br>


![image](https://github.com/crodrigr/programacion-java-2023-02/assets/31961588/7075f17e-f3c9-4dc5-a4ea-6ec6513e807f)


<br>
<br>
<br>
<br>


### 6.4 ClienteController - /form  post


<br>
<br>



![image](https://github.com/crodrigr/programacion-java-2023-02/assets/31961588/3f68db53-8d55-4946-b459-474d9ad37226)


<br>
<br>

Para usar **@Valid** de debe colocar la siguiente dependencia en el **pom.xml** y se importa **import javax.validation.Valid;**

![image](https://github.com/crodrigr/programacion-java-2023-02/assets/31961588/43dc8805-415e-45c8-8ade-5c8a695d2622)


<br>
<br>
<br>
<br>



### 6.5 ClienteController - /eliminar


<br>
<br>


![image](https://github.com/crodrigr/programacion-java-2023-02/assets/31961588/fb2e9115-2a45-48aa-90ba-10cb962a0130)

<br>
<br>
<br>
<br>

## 7. Configuración base datos en mongo


<br>
<br>


![image](https://github.com/crodrigr/programacion-java-2023-02/assets/31961588/1574f2db-437f-4d07-8cda-6f0b4221b306)

<br>
<br>
<br>
<br>


## 8. Configuración messages.properties


<br>
<br>



![image](https://github.com/crodrigr/programacion-java-2023-02/assets/31961588/9b3b9310-3225-4455-a599-af90d8f73271)
