# Proyecto del bank. 

Un sistema de **Ecommerces** para realizar sus ventas en caliente tiene la opción de hacer una solicitud de crédito con el **Banco Nacional**, a través de una api que tiene disponible el banco para los comercios. 

![image](https://github.com/crodrigr/programacion-java-2023-02/assets/31961588/1ba8750d-0d9c-447f-988d-1dcab39a7d71)

**El Banco Nacional** tiene las siguiente politicas de cŕeditos para el proceso de aprobación de una solicitud de credito.


### Cliente con vida créditicia:

  Este escenario tiene los siguientes requerimientos
    - Un cliente con vida créditicia debe tener créditos vigentes o créditos culminados, entonces se debe validar que todos sus 
      créditos esten al día y no tenga ninguna mora.
    - El mónto para aprobación corresponde a la capacidad de **endeudamiento**; tres veces del ingreso mensual, adicional se debe calcular cuanto es 
      el porcentaje total que ha cancelado de los créditos vigentes. A continuación se ve la información de un crédito que tiene un cliente.
      
      ![image](https://github.com/crodrigr/programacion-java-2023-02/assets/31961588/d916d993-e7ab-4c90-a792-ecb159692a92)

      **En este caso este credito lleva un 25% de pago.**

  **Veamos un ejemplo:** El api del banco recibe una petición /fast que hace referencia a un cŕedito rápido que la primer opción. El primer valor corresponde al documento 
    del cliente y el segundo al el monto a solicitar. En este caso se va aplicar el caso el cliente tiene vida créditica, por lo tanto, está registrado en el banco, con 
    créditos vigentes o finalizados. Vamos a simular que el cliente tiene un crédito y con la siguiente información:
    - ingresos mensuales: $3'000000
    - Un credito vigente por **$2'000000** del cual está al día y tiene un pago del **50%**, por lo tanto, su capacidad de endeudamiento es: **2'000000** y su solicitud 
      de crédito es de **$2'000000**. En entoces el banco aprueba el crédito del cliente por el monto solicitado.  

  ![image](https://github.com/crodrigr/programacion-java-2023-02/assets/31961588/80496b3d-b826-45b9-beaf-9347f67e1389)

  ### Cliente sin vida créditicia:
  
   Este escenario el cliento no se encuentra registrado en el banco por lo tanto No tiene ningún credito vigente o culminado. Por lo tanto, la solicitud debe ser completa con la 
   siguente información: 
    - **Datos del cliente:**
         - nombres
         - apellidos
         - documento de identificación
         - email
         - celular
         - direccion
         - ingresos mensuales
         - Capacidad endeudamiento: este es un valor que se calcula con los creditos vigentes si los tiene. 
     - **Datos del credito**
         - fecha del credito
         - monto a solicitar

  **Veamos un ejemplo:** El api del banco recibe una petición **/complete/{meses}/{monto}** que hace referencia a un solicitud completa, el cual, va por el path los meses que va tener el crédito y el monto a solicitar. Por el **BodyRequest** van los datos del cliente, necesario para calcular la capacidad de **endeudamiento** y registrar el cliente en el banco con su crédito si es aprobando. En este caso la solicitud es aprobada por que tiene una capcidad de **6'000000** y como no tiene ningún crédito puede solicitar al 100% de su capacidad de endeudamiento. 
  
![image](https://github.com/crodrigr/programacion-java-2023-02/assets/31961588/707f4c78-cdb5-4863-a8ed-1a87a0e3ba61)

      
## Modelo de paquete y de clases

![image](https://github.com/crodrigr/programacion-java-2023-02/assets/31961588/00fb34b7-fbc0-491c-9a40-c358507413b2)

      
      


