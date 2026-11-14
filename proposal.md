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
|CRUD simple|1. CRUD Room Category<br>2. CRUD Amenity<br>3. CRUD Province|
|CRUD dependiente|1. CRUD Room {depende de} CRUD Room Category<br>2. CRUD Guest {depende de} CRUD City|
|Listado<br>+<br>detalle|1. Listado de Rooms filtrado por Room Category, disponibilidad entre fechas y cantidad de personas, muestra number, Room Category y pricePerNight => detalle CRUD Room<br>2. Listado de Reservations filtrado por rango de fechas, muestra number de Room, startDate y endDate de la estadía, status y nombre del Guest => detalle muestra datos completos de la Reservation y del Guest|
|CUU/Epic|1. Reservar una Room para la estadía<br>2. Realizar el check-in de una Reservation|

Adicionales para Aprobación
|Req|Detalle|
|:-|:-|
|CRUD|1. CRUD Room Category<br>2. CRUD Amenity<br>3. CRUD Province<br>4. CRUD City<br>5. CRUD Room<br>6. CRUD Guest<br>7. CRUD Employee<br>8. CRUD Amenity Quota<br>9. CRUD Amenity Price<br>10. CRUD Reservation<br>11. CRUD Reservation Amenity<br>12. CRUD User<br>13. CRUD Pricing Rule|
|CUU/Epic|1. Reservar una Room para la estadía<br>2. Realizar el check-in de una Reservation<br>3. Realizar el check-out y generar el comprobante de pago de la estadía y los Amenities consumidos|

### Alcance Adicional Voluntario

|Req|Detalle|
|:-|:-|
|Listados|1. Rooms ocupadas hoy, muestra number, floor y Room Category, y si el Guest ya hizo el check-in o está esperando hacerlo<br>2. Historial de Reservations por Guest, muestra startDate, endDate, status y Room de cada Reservation|
|CUU/Epic|1. Consumir Amenities adicionales durante la estadía<br>2. Cancelación de Reservation<br>3. Modificar Reservation (cambio de fechas o Room)<br>4. Registro de Guests y gestión de Users por role<br>5. Reservation en autoservicio: el Guest reserva, modifica las fechas y cancela sus propias Reservations|
|Otros|1. Validación automática de disponibilidad de la Room al reservar<br>2. Tarifa dinámica: el precio por noche se ajusta según la ocupación de la Room Category y la antelación de la Reservation, con Pricing Rules configurables<br>3. Baja automática de las Reservations pendientes que llegan a su endDate sin check-in, liberando sus Amenities<br>4. Restricciones de borrado: no se puede eliminar una Reservation en curso, un Guest con Reservations activas ni una Room ocupada o con Reservations pendientes|

