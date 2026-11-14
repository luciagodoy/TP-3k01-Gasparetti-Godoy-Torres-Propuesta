# Propuesta TP DSW

## Grupo
### Integrantes
* 54049 - Gasparetti, María Victoria
* 54095 - Godoy, Lucía María
* 54351 - Torres, Matías

### Repositorios
* [frontend app](https://github.com/luciagodoy/TP-3k01-Gasparetti-Godoy-Torres-Frontend.git)
* [backend app](https://github.com/luciagodoy/TP-3k01-Gasparetti-Godoy-Torres-Backend.git)

## Tema
### Descripción
Sistema de gestión para hoteles que permite administrar reservas, check-in/check-out, facturación de estadías y servicios adicionales. Los huéspedes pueden buscar habitaciones disponibles, reservar y contratar servicios; el personal del hotel opera las reservas y el administrador gestiona empleados y usuarios. Optimiza la operación hotelera automatizando procesos clave y mejorando la experiencia del cliente.

### Modelo

<img width="3709" height="1564" alt="image" src="https://github.com/user-attachments/assets/38b2f2c6-8ec8-4c06-8d12-2059fc82df99" />



## Alcance Funcional

### Alcance Mínimo

Regularidad:
|Req|Detalle|
|:-|:-|
|CRUD simple|1. CRUD Categoría Habitación<br>2. CRUD Servicio<br>3. CRUD Provincia|
|CRUD dependiente|1. CRUD Habitación {depende de} CRUD Categoría Habitación<br>2. CRUD Huésped {depende de} CRUD Ciudad|
|Listado<br>+<br>detalle|1. Listado de habitaciones filtrado por categoría, disponibilidad entre fechas y cantidad de personas, muestra nro, categoría y precio por noche => detalle CRUD Habitación<br>2. Listado de reservas filtrado por rango de fechas, muestra nro de habitación, fecha inicio y fin de estadía, estado y nombre del huésped => detalle muestra datos completos de la reserva y del huésped|
|CUU/Epic|1. Reservar una habitación para la estadía<br>2. Realizar el check-in de una reserva|

Adicionales para Aprobación
|Req|Detalle|
|:-|:-|
|CRUD|1. CRUD Categoría Habitación<br>2. CRUD Servicio<br>3. CRUD Provincia<br>4. CRUD Ciudad<br>5. CRUD Habitación<br>6. CRUD Huésped<br>7. CRUD Empleado<br>8. CRUD Cupo<br>9. CRUD Precio Servicio<br>10. CRUD Reserva<br>11. CRUD Reserva Servicio<br>12. CRUD Usuario|
|CUU/Epic|1. Reservar una habitación para la estadía<br>2. Realizar el check-in de una reserva<br>3. Realizar el check-out y generar el comprobante de pago de la estadía y los servicios consumidos|

### Alcance Adicional Voluntario

|Req|Detalle|
|:-|:-|
|Listados|1. Habitaciones ocupadas hoy, muestra nro, piso y categoría, y si el huésped ya hizo el check-in o está esperando hacerlo<br>2. Historial de reservas por huésped, muestra fechas, estado y habitación de cada reserva|
|CUU/Epic|1. Consumir servicios adicionales durante la estadía<br>2. Cancelación de reserva<br>3. Modificar reserva (cambio de fechas o habitación)<br>4. Registro de huéspedes y gestión de usuarios por rol<br>5. Reserva en autoservicio: el huésped reserva, modifica las fechas y cancela sus propias reservas|
|Otros|1. Validación automática de disponibilidad de la habitación al reservar<br>2. Tarifa dinámica: el precio por noche se ajusta según la ocupación de la categoría y la antelación de la reserva, con reglas configurables<br>3. Baja automática de las reservas pendientes que llegan a su fecha de salida sin check-in, liberando sus servicios<br>4. Restricciones de borrado: no se puede eliminar una reserva en curso, un huésped con reservas activas ni una habitación ocupada o con reservas pendientes|


