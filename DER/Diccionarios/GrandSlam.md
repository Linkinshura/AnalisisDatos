# TORNEO

| N° | Nombre | Descripción | Tipo | Longitud | PK/FK | Enlace |
| -- | ------ | ----------- | ---- | -------- | ----- | ------- |
| 1 | Codigo_Torneo | Código único del torneo | INT | 11 | PK | - |
| 2 | Nombre_Torneo | Nombre del torneo | VARCHAR | 100 | - | - |
| 3 | Pais | País donde se realiza el torneo | VARCHAR | 50 | - | - |

# EDICION

| N° | Nombre | Descripción | Tipo | Longitud | PK/FK | Enlace |
| -- | ------ | ----------- | ---- | -------- | ----- | ------- |
| 1 | Codigo_Edicion | Código único de la edición | INT | 11 | PK | - |
| 2 | Anio | Año en que se realiza la edición | YEAR | 4 | - | - |
| 3 | Lugar | Lugar donde se disputa la edición | VARCHAR | 100 | - | - |
| 4 | Codigo_Torneo | Torneo al que pertenece la edición | INT | 11 | FK | TORNEO |

# MODALIDAD

| N° | Nombre | Descripción | Tipo | Longitud | PK/FK | Enlace |
| -- | ------ | ----------- | ---- | -------- | ----- | ------- |
| 1 | Codigo_Modalidad | Código único de la modalidad | INT | 11 | PK | - |
| 2 | Nombre_Modalidad | Nombre de la modalidad | VARCHAR | 50 | - | - |

# FASE

| N° | Nombre | Descripción | Tipo | Longitud | PK/FK | Enlace |
| -- | ------ | ----------- | ---- | -------- | ----- | ------- |
| 1 | Codigo_Fase | Código único de la fase | INT | 11 | PK | - |
| 2 | Nombre_Fase | Nombre de la fase | VARCHAR | 50 | - | - |

# PREMIO

| N° | Nombre | Descripción | Tipo | Longitud | PK/FK | Enlace |
| -- | ------ | ----------- | ---- | -------- | ----- | ------- |
| 1 | Codigo_Premio | Código único del premio | INT | 11 | PK | - |
| 2 | Monto | Valor monetario del premio | DECIMAL | 12,2 | - | - |
| 3 | Codigo_Edicion | Edición que otorga el premio | INT | 11 | FK | EDICION |
| 4 | Codigo_Modalidad | Modalidad asociada al premio | INT | 11 | FK | MODALIDAD |
| 5 | Codigo_Fase | Fase correspondiente al premio | INT | 11 | FK | FASE |

# PARTIDO

| N° | Nombre | Descripción | Tipo | Longitud | PK/FK | Enlace |
| -- | ------ | ----------- | ---- | -------- | ----- | ------- |
| 1 | Codigo_Partido | Código único del partido | INT | 11 | PK | - |
| 2 | Fecha | Fecha en la que se disputa el partido | DATE | - | - | - |
| 3 | Codigo_Edicion | Edición a la que pertenece el partido | INT | 11 | FK | EDICION |
| 4 | Codigo_Modalidad | Modalidad del partido | INT | 11 | FK | MODALIDAD |
| 5 | Codigo_Fase | Fase del torneo en la que se juega | INT | 11 | FK | FASE |

# SET_PARTIDO

| N° | Nombre | Descripción | Tipo | Longitud | PK/FK | Enlace |
| -- | ------ | ----------- | ---- | -------- | ----- | ------- |
| 1 | Numero_Set | Número del set | INT | 11 | PK | - |
| 2 | Codigo_Partido | Partido al que pertenece el set | INT | 11 | PK, FK | PARTIDO |
| 3 | Juegos_Equipo1 | Juegos ganados por el primer jugador/equipo | INT | 2 | - | - |
| 4 | Juegos_Equipo2 | Juegos ganados por el segundo jugador/equipo | INT | 2 | - | - |

# ARBITRO

| N° | Nombre | Descripción | Tipo | Longitud | PK/FK | Enlace |
| -- | ------ | ----------- | ---- | -------- | ----- | ------- |
| 1 | Codigo_Arbitro | Código único del árbitro | INT | 11 | PK | - |
| 2 | Nombre_Arbitro | Nombre del árbitro | VARCHAR | 100 | - | - |

# JUGADOR

| N° | Nombre | Descripción | Tipo | Longitud | PK/FK | Enlace |
| -- | ------ | ----------- | ---- | -------- | ----- | ------- |
| 1 | Codigo_Jugador | Código único del jugador | INT | 11 | PK | - |
| 2 | Nombre_Jugador | Nombre del jugador | VARCHAR | 100 | - | - |

# PAIS

| N° | Nombre | Descripción | Tipo | Longitud | PK/FK | Enlace |
| -- | ------ | ----------- | ---- | -------- | ----- | ------- |
| 1 | Codigo_Pais | Código único del país | INT | 11 | PK | - |
| 2 | Nombre_Pais | Nombre del país | VARCHAR | 100 | - | - |

# PARTICIPACION

| N° | Nombre | Descripción | Tipo | Longitud | PK/FK | Enlace |
| -- | ------ | ----------- | ---- | -------- | ----- | ------- |
| 1 | Codigo_Jugador | Jugador participante | INT | 11 | PK, FK | JUGADOR |
| 2 | Codigo_Partido | Partido en el que participa | INT | 11 | PK, FK | PARTIDO |
| 3 | Numero_Equipo | Número del jugador o equipo dentro del partido | INT | 2 | - | - |
| 4 | Resultado | Resultado obtenido por el jugador | VARCHAR | 20 | - | - |

# ENTRENADOR

| N° | Nombre | Descripción | Tipo | Longitud | PK/FK | Enlace |
| -- | ------ | ----------- | ---- | -------- | ----- | ------- |
| 1 | Codigo_Entrenador | Código único del entrenador | INT | 11 | PK | - |
| 2 | Nombre_Entrenador | Nombre del entrenador | VARCHAR | 100 | - | - |

# ENTRENAMIENTO

| N° | Nombre | Descripción | Tipo | Longitud | PK/FK | Enlace |
| -- | ------ | ----------- | ---- | -------- | ----- | ------- |
| 1 | Codigo_Entrenador | Entrenador responsable | INT | 11 | PK, FK | ENTRENADOR |
| 2 | Codigo_Jugador | Jugador entrenado | INT | 11 | PK, FK | JUGADOR |
| 3 | Codigo_Edicion | Edición durante la cual se realiza el entrenamiento | INT | 11 | PK, FK | EDICION |
| 4 | Fecha_Inicio | Fecha de inicio del entrenamiento | DATE | - | - | - |
| 5 | Fecha_Fin | Fecha de finalización del entrenamiento | DATE | - | - | - |
