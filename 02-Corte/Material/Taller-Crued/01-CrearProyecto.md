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

![image](https://github.com/crodrigr/programacion-java-2023-02/assets/31961588/85d2079b-c453-422b-9fc1-a96788bd2575)


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



![image](https://github.com/crodrigr/programacion-java-2023-02/assets/31961588/bf795689-0cf1-4eba-97cf-06f801bffb5f)



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


<br>
<br>
<br>
<br>


## 9. Vistas html


<br>
<br>

### 9.1 listar.html

<br>
<br>

```html

<!DOCTYPE html>
<html xmlns:th="http://www.thymeleaf.org">
<head>
<meta charset="UTF-8" />
<title th:text="${titulo}">Insert title here</title>
<link rel="stylesheet"
	href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css">
</head>
<body>

	<nav class="navbar navbar-expand-lg navbar-dark bg-dark">
		<a class="navbar-brand" href="#">Spring Boot</a>
		<button class="navbar-toggler" type="button" data-toggle="collapse"
			data-target="#navbarNav" aria-controls="navbarNav"
			aria-expanded="false" aria-label="Toggle navigation">
			<span class="navbar-toggler-icon"></span>
		</button>
		<div class="collapse navbar-collapse" id="navbarNav">
			<ul class="navbar-nav">
				<li class="nav-item active"><a class="nav-link" href="#">Home
						<span class="sr-only">(current)</span>
				</a></li>
				<li class="nav-item"><a class="nav-link" th:href="@{/listar}">Clientes</a>
				</li>
			</ul>
		</div>
	</nav>

	<div class="container">
		<h1
			class="text-secondary border border-success border-top-0 border-left-0 border-right-0"
			th:text="${titulo}"></h1>
		<p><a th:href="@{/form}" class="btn btn-success btn-xs">crear cliente</a></p>
		<table class="table table-striped">
			<thead>
				<tr>
					<th>id</th>
					<th>nombre</th>
					<th>apellido</th>
					<th>email</th>
					<th>fecha</th>
					<th>editar</th>
					<th>eliminar</th>
				</tr>
			</thead>
			<tbody>
				<tr th:each="cliente: ${clientes}">
					<td th:text="${cliente.id}"></td>
					<td th:text="${cliente.nombre}"></td>
					<td th:text="${cliente.apellido}"></td>
					<td th:text="${cliente.email}"></td>
					<td th:text="${cliente.createAt}"></td>
					<td><a class="btn btn-primary btn-xs" th:href="@{/form/} + ${cliente.id}" th:text="'editar'"></a></td>
					<td><a class="btn btn-danger btn-xs" th:href="@{/eliminar/} + ${cliente.id}" th:text="'eliminar'" onclick="return confirm('Estás seguro que quieres eliminar?');"></a></td>
				</tr>
			</tbody>

		</table>
	</div>
	<script src="https://code.jquery.com/jquery-3.3.1.slim.min.js"></script>
	<script
		src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.7/umd/popper.min.js"></script>
	<script
		src="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/js/bootstrap.min.js"></script>
</body>
</html>

```


<br>
<br>
<br>
<br>

### 9.2 form.html

<br>
<br>

```html

<!DOCTYPE html>
<html xmlns:th="http://www.thymeleaf.org">
<head>
<meta charset="UTF-8" />
<title th:text="${titulo}">Insert title here</title>
<link rel="stylesheet"
	href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css">
</head>
<body>

	<nav class="navbar navbar-expand-lg navbar-dark bg-dark">
		<a class="navbar-brand" href="#">Spring Boot</a>
		<button class="navbar-toggler" type="button" data-toggle="collapse"
			data-target="#navbarNav" aria-controls="navbarNav"
			aria-expanded="false" aria-label="Toggle navigation">
			<span class="navbar-toggler-icon"></span>
		</button>
		<div class="collapse navbar-collapse" id="navbarNav">
			<ul class="navbar-nav">
				<li class="nav-item active"><a class="nav-link" href="#">Home</a></li>
				<li class="nav-item"><a class="nav-link" th:href="@{/listar}">Clientes</a></li>
			</ul>
		</div>
	</nav>

	<div class="container">
		<h1 th:text="${titulo}"
			class="text-secondary border border-success border-top-0 border-left-0 border-right-0"></h1>

		<div th:object="${cliente}" th:remove="tag">
			
		</div>
		<form th:action="@{/form}" th:object="${cliente}" method="post">
			<div class="form-group row">
				<label class="col-sm-2 col-form-label">Nombre</label>
				<div class="col-sm-6">
					<input type="text" th:field="*{nombre}" class="form-control"/> 
				</div>
			</div>
			<div class="form-group row">
				<label class="col-sm-2 col-form-label">Apellido</label>
				<div class="col-sm-6">
					<input type="text" th:field="*{apellido}" class="form-control" /> 
				</div>
			</div>
			<div class="form-group row">
				<label class="col-sm-2 col-form-label">Email</label>
				<div class="col-sm-6">
					<input type="text" th:field="*{email}" class="form-control" /> 
				</div>
			</div>
			<div class="form-group row">
				<label class="col-sm-2 col-form-label">Fecha</label>
				<div class="col-sm-6">
					<input type="text" class="form-control" th:field="*{createAt}" />
				</div>
			</div>
			<div class="form-group row">
				<div class="col-sm-6">
					<input type="submit" value="Crear Cliente" class="btn btn-primary" />
				</div>
			</div>

		</form>
	</div>
</body>
</html>


```

<br>
<br>
<br>
<br>
