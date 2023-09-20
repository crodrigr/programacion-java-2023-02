# Spring boot

<br>
<br>

## 1. Plantilla proyecto


<br>
<br>

![image](https://github.com/crodrigr/programacion-java-2023-02/assets/31961588/a3085a58-833a-441b-b08d-ed5d7f90a019)

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

![image](https://github.com/crodrigr/programacion-java-2023-02/assets/31961588/068da043-92eb-4497-869f-ac027b1b6482)

<br>
<br>
<br>
<br>
