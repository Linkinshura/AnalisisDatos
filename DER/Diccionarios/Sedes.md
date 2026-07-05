# SEDE

| N° | Nombre | Descripción | Tipo | Longitud | PK/FK | Enlace |
| -- | ------ | ----------- | ---- | -------- | ----- | ------- |
| 1 | N° | Número identificador de la sede | INT | 11 | PK | - |
| 2 | Cant_Comple | Cantidad de complejos que posee la sede | INT | 11 | - | - |
| 3 | Presupuesto | Presupuesto asignado a la sede | DECIMAL | 12,2 | - | - |

# COMPLEJO

| N° | Nombre | Descripción | Tipo | Longitud | PK/FK | Enlace |
| -- | ------ | ----------- | ---- | -------- | ----- | ------- |
| 1 | ID | Identificador único del complejo | INT | 11 | PK | - |
| 2 | Tipo | Tipo de complejo deportivo | VARCHAR | 50 | - | - |
| 3 | Localizacion | Ubicación del complejo | VARCHAR | 100 | - | - |
| 4 | Jefe | Nombre o identificador del jefe del complejo | VARCHAR | 100 | - | - |
| 5 | Area_Total | Área total del complejo | DECIMAL | 10,2 | - | - |
| 6 | Sede | Sede a la que pertenece el complejo | INT | 11 | FK | SEDE |

# EVENTO

| N° | Nombre | Descripción | Tipo | Longitud | PK/FK | Enlace |
| -- | ------ | ----------- | ---- | -------- | ----- | ------- |
| 1 | ID | Identificador único del evento | INT | 11 | PK | - |
| 2 | Duracion | Duración del evento | INT | 11 | - | - |
| 3 | Cant_Parti | Cantidad de participantes | INT | 11 | - | - |
| 4 | Cant_Comis | Cantidad de comisarios requeridos | INT | 11 | - | - |
| 5 | Complejo | Complejo donde se realiza el evento | INT | 11 | FK | COMPLEJO |

# COMISARIO

| N° | Nombre | Descripción | Tipo | Longitud | PK/FK | Enlace |
| -- | ------ | ----------- | ---- | -------- | ----- | ------- |
| 1 | ID | Identificador único del comisario | INT | 11 | PK | - |
| 2 | Rol | Rol desempeñado por el comisario | VARCHAR | 50 | - | - |
| 3 | Equipamiento | Equipamiento asignado al comisario | VARCHAR | 100 | - | - |

# COMI_EVENTO

| N° | Nombre | Descripción | Tipo | Longitud | PK/FK | Enlace |
| -- | ------ | ----------- | ---- | -------- | ----- | ------- |
| 1 | Id_Contrato | Identificador del contrato | INT | 11 | PK | - |
| 2 | Evento | Evento al que fue asignado el comisario | INT | 11 | FK | EVENTO |
| 3 | Comisario | Comisario contratado para el evento | INT | 11 | FK | COMISARIO |
