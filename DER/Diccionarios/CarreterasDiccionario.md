Carreteras:
| N° | Nombre | Descripcion | Tipo | Longitud | PK/FK | Enlace |
| :-: | :-: | :-: | :-: | :-: | :-: | :-: |
| 1 | ID | Clave unica | INT | 20 | PK | - |
| 2 | Categoria | Categorias de Carreteras | VARCHAR | 15 | - | - |
| 3 | KM_Carretera | Kilometros de la Carretera | INT | 10 | - | - |

Tramos:
| N° | Nombre | Descripcion | Tipo | Longitud | PK/FK | Enlace |
| :-: | :-: | :-: | :-: | :-: | :-: | :-: |
| 1 | ID | Clave Unica | INT | 20 | PK | - | 
| 2 | Comuna_Inicio | Inicio Comuna | INT | 10 | - | - |
| 3 | Comuna_Fin | Fin Comuna | INT | 10 | - | - |
| 4 | Carretera | Carretera a la que pertenece | INT | 20 | FK | Carreteras |

Fin_Carretera:
| N° | Nombre | Descripcion | Tipo | Longitud | PK/FK | Enlace |
| :-: | :-: | :-: | :-: | :-: | :-: | :-: |
| 1 | ID | Clave Unica | INT | 20 | PK | - |
| 2 | KM | Kilometro donde termina | INT | 15 | - | - | 
| 3 | Comuna | Comuna donde termina | INT | 10 | - | - |  
| 4 | Tramo | Tramo al cual pertenece | INT | 20 | FK | Tramos |

