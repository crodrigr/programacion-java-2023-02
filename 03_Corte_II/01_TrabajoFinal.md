# :volcano: Trabajo final

<br>

## 1. Problema :fire:

Una organización no gubernamental se encarga de enviar ayuda material (medicamentos y alimentos) y
ayuda humanitaria (personal sanitario) a campos de refugiados. Esta organización obtiene sus ingresos de
las cuotas de los socios, de los que se desea conocer los datos personales, la cuenta bancaria en donde se
realizan los cargos anuales, la fecha de pago y el tipo de cuota. En la actualidad hay tres tipos de cuotas,
pudiendo variar en el futuro: mínima (**10 US anuales**), media (**20 US anuales**) o máxima (**30 US
anuales**).

Cada socio pertenece a una de las sedes de la organización, cada una de ellas ubicada en una ciudad
distinta. De las sedes se desea conocer el domicilio y el nombre de su director.
La organización cuenta con dos tipos de voluntarios: los que realizan labores humanitarias (personal
sanitario) y los que realizan labores administrativas (personal administrativo). De los primeros se desea
conocer su profesión (médico, ATS, etc.), su disponibilidad actual (sí/no) y el número de trabajos en los que
ha participado. De todos los voluntarios se desea conocer los datos personales y la sede en la que se
inscribieron.

Cada envío tiene un destino y una fecha de salida. Para identificar los envíos, se les asigna un código
único. Además, cada envío es organizado por una o varias sedes. Los envíos de ayuda material pueden ser
de alimentos, debiéndose conocer el número de toneladas de cada alimento que se manda; o pueden ser de
medicamentos, debiéndose conocer el número de unidades de cada medicamento. De los envíos de ayuda
humanitaria se debe conocer el número de voluntarios que se mandan de cada profesión (por ejemplo: 10
médicos, 20 ATS) y quienes son cada uno de ellos.

## 2. Solución :trophy:

### Desarrollo de una API de Gestión para una Organización No Gubernamental de Ayuda Humanitaria

**Descripción:**
Se requiere el desarrollo de una API RESTful con Spring Boot para administrar una organización no gubernamental (ONG) que se dedica a proporcionar ayuda material (medicamentos y alimentos) y ayuda humanitaria (personal sanitario) a campos de refugiados. La ONG obtiene sus ingresos de las cuotas de los socios y opera a nivel de múltiples sedes.


**Requisitos Funcionales:**

1. **Gestión de Socios:**
   - Registrar nuevos socios con información personal, cuenta bancaria y tipo de cuota.
   - Consultar, actualizar y eliminar información de socios existentes.
   - Listar socios por tipo de cuota.

2. **Gestión de Sedes:**
   - Registrar nuevas sedes con información de dirección y director.
   - Consultar, actualizar y eliminar información de sedes existentes.
   - Listar todas las sedes.

3. **Gestión de Voluntarios:**
   - Registrar voluntarios con información personal, profesión, disponibilidad y sede a la que están asignados.
   - Consultar, actualizar y eliminar información de voluntarios existentes.
   - Listar voluntarios por profesión y sede.

4. **Gestión de Envíos de Ayuda:**
   - Crear un nuevo envio: datos del envio, idrefugio, detalles del envio y sedes.
   - Obtener un envio por id. Que trae los datos del envio, detalles del envio, datos completos del refugio, y datos completos de las sedes. 


**Tecnologías Utilizadas:**
- Spring Boot para el desarrollo del API RESTful.
- Spring Data JPA para el acceso a la base de datos.
- Usar DTO. En la capa externa (**controllers**) no se debe exponer las clases entities, por lo tanto, se debe usar DTO, además de ser un buena práctica se soluciona el problema de loop de **serializable** y no es necesario de resolverlo con **@JsonIgnoreProperties**
- Base de datos relacional **H2** (Opcional por ejemplo, MySQL, PostgreSQL) para almacenar los datos.
- Datos de prueba. Se debe tener un archivo **import.sql** que cargue datos de pruebas en todas la tablas. 


**Entregables:**
- Código fuente de la API desarrollada en Spring Boot.
- Diagrama de clases

**Plazo de Entrega:**
El proyecto debe ser entregado para el 2 de Diciembre.

---

