Direcciones:
| N° | Nombre | Descripcion | Tipo | Longitud | PK/FK | Enlace |
| :-: | :-: | :-: | :-: | :-: | :-: | :-: |
| 1 | ID | Clave Unica | INT | 15 | PK | - |
| 2 | Numero | Numero de Direccion | INT | 20 | - | - | 
| 3 | Calle | Nombre de la calle | VARCHAR | 30 | - | - |
| 4 | Ciudad | Nombre de la ciudad | VARCHAR | 30 | - | - |
| 5 | Comuna | Numero de Comuna | INT | 20 | - | - |

Clientes:
| N° | Nombre | Descripcion | Tipo | Longitud | PK/FK | Enlace |
| :-: | :-: | :-: | :-: | :-: | :-: | :-: |
| 1 | Num_Cliente | Clave Unica | INT | 15 | PK | - |
| 2 | Descuento | Descuento realizado | DECIMAL | 25 | - | - |
| 3 | Limite_Cred | Limite del credito | DECIMAL | 30 | - | - | 
| 4 | Saldo | Saldo disponible | DECIMAL | 35 | - | - |
| 5 | Direccion | Direccion del Cliente | INT | 15 | FK | Direcciones |

Pedidos:
| N° | Nombre | Descripcion | Tipo | Longitud | PK/FK | Enlace |
| :-: | :-: | :-: | :-: | :-: | :-: | :-: |
| 1 | ID | Clave Unica | INT | 15 | PK | - |
| 2 | Cantidad | Cantidad de Productos | INT | 20 | - | - |
| 3 | Num_Cliente | Numero de Cliente | INT | 15 | FK | Clientes |
| 4 | Direccion | Direccion de envio | INT | 15 | FK | Direcciones |
| 5 | Fecha | Fecha del pedido | DATETIME | 20 | - | - |
| 6 | Articulo | Numero de Articulo | INT | 15 | FK | Articulos |

Articulos:
| N° | Nombre | Descripcion | Tipo | Longitud | PK/FK | Enlace |
| :-: | :-: | :-: | :-: | :-: | :-: | :-: |
| 1 | Num_art | Clave Unica | INT | 15 | PK | - |
| 2 | Stock_Fab | Stock en la fabrica | INT| 20 | - | - |
| 3 | Fabricas | Cantidad de Fabricas que exportan | INT | 10 | - | - |
| 4 | Descripcion | Descripcion del Articulo | VARCHAR | 80 | - | - |
