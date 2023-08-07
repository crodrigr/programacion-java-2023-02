# Retornando redirect y forward como respuesta en métodos del controlador 

<br>
<br>
`redirect` y `forward` son dos técnicas utilizadas en el manejo de solicitudes y respuestas en aplicaciones web. Ambas tienen diferentes propósitos y comportamientos en el contexto de una aplicación web.

**Forward (Reenvío):**

- El reenvío (forward) es un proceso en el que el servidor web recibe una solicitud de un cliente (navegador), luego el servidor reenvía (forward) la solicitud a otro recurso en el mismo servidor, como otro servlet o JSP, para su procesamiento adicional.

- El cliente no está al tanto de que ha ocurrido un reenvío. La URL en la barra de direcciones del navegador permanece sin cambios.

- Se utiliza para procesos internos en el servidor donde múltiples componentes trabajan juntos para generar la respuesta final al cliente.

- Puede ser más eficiente en términos de rendimiento ya que no implica una nueva solicitud HTTP del cliente.

**Redirect (Redireccionamiento):**

- El redireccionamiento (redirect) es un proceso en el que el servidor web envía una respuesta de redireccionamiento al cliente con una nueva URL a la que debe dirigirse.

- El cliente recibe la respuesta de redireccionamiento y realiza una nueva solicitud HTTP a la URL proporcionada.

- El cliente puede ver el cambio en la URL en la barra de direcciones del navegador.

- Se utiliza cuando deseas enviar al cliente a una nueva ubicación, como después de realizar una acción que debe llevar a una nueva página.

- Puede tener un impacto en el rendimiento, ya que implica una nueva solicitud y respuesta HTTP.

En resumen, el `forward` es un proceso interno en el servidor donde se reenvía una solicitud a otro recurso para su procesamiento, mientras que el `redirect` implica enviar una respuesta al cliente para que realice una nueva solicitud a una ubicación diferente. La elección entre ambos depende de los requisitos específicos de tu aplicación web y de cómo deseas manejar las respuestas y las direcciones URL.

<br>
<br>

## 1. ControllerHome redirect

![image](https://user-images.githubusercontent.com/31961588/219504329-3763e108-843b-4c4a-ae7d-e1ef155b9113.png)

<br>
<br>

## 2. ControllerHome forward

Direcciona a la pagina pero no cambia la ruta de la url. Ejecuta un RequestDispacher.foward() 

![image](https://user-images.githubusercontent.com/31961588/219504090-91a19e3e-a245-4380-8f9f-1bfecf13baf3.png)

<br>
<br>