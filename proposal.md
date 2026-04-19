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
Sistema de gestión para hoteles que permite administrar reservas, check-in/check-out, facturación de estadías y servicios adicionales. Optimiza la operación hotelera automatizando procesos clave y mejorando la experiencia del cliente.

### Modelo
<img width="1771" height="841" alt="MD-Desarrollo drawio (1)" src="https://github.com/user-attachments/assets/ddd5da8a-29e9-4d6b-be96-46bf7d7c20da" />


#### Alcance Funcional

### Alcance Mínimo

**CRUD Simples:**

| CRUD |
|:-|
| CRUD Categoría Habitación |
| CRUD Adicional Servicio |
| CRUD Ciudad |

**CRUD Dependientes:**

| CRUD | Dependencia |
|:-|:-|
| CRUD Habitación | {depende de} CRUD Categoría Habitación |
| CRUD Huésped | {depende de} CRUD Ciudad |

**Listados con Filtro + Detalle:**

| Listado | Filtro |
|:-|:-|
| Listado de Habitaciones | Filtrado por categoría de habitación |
| Listado de Reservas | Filtrado por rango de fechas |

**Casos de Uso/Epic:**

| Caso de Uso | Descripción |
|:-|:-|
| Realizar Reserva de Habitación | Crear nueva reserva para un huésped en una habitación específica |
| Procesar Check-in de Reserva | Registrar la entrada del huésped y cambiar estado de habitación |

### Adicionales para Aprobación

**CRUDs de todas las clases de negocio:**

| CRUD | 
|:-|
| CRUD Categoría Habitación | 
| CRUD Adicional Servicio | 
| CRUD Ciudad | 
| CRUD Provincia |
| CRUD Habitación (dependiente de Categoría) |
| CRUD Huésped (dependiente de Ciudad) |
| CRUD Personal Hotelero | 

**Casos de Uso/Epic:**

| Caso de Uso | Descripción |
|:-|:-|
| Realizar Reserva de Habitación | Crear nueva reserva seleccionando huésped, habitación y fechas |
| Procesar Check-in de Reserva | Registrar entrada del huésped usando datos de la reserva |
| Procesar Check-out y Facturación | Registrar salida, calcular montos, incluir servicios consumidos y generar factura |

### Alcance Adicional Voluntario

| Tipo | Detalle |
|:-|:-|
| Listados Complejos | 1. Habitaciones ocupadas hoy <br>2. Historial de reservas por huésped |
| Casos de Uso Adicionales | 1. Modificar reserva (cambio de fechas o habitación)<br>2. Consumir servicios adicionales durante la estadía<br>3. Cancelar reserva |
| Notificaciones | 1. Email de confirmación de reserva<br>2. Recordatorio de check-out 24 horas antes|
| Reportes | 1. Reporte de ocupación por período<br>2. Reporte de servicios más consumidos |
| Otros | 1. Validación automática de disponibilidad en tiempo real |
