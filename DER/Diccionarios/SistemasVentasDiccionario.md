Proveedores:
| N° | Nombre | Descripcion | Tipo | Longitud | PK/FK | Enlace |
| :-: | :-: | :-: | :-: | :-: | :-: | :-: |
| 1 | RUT | Clave Unica | INT | 15 | PK | - |
| 2 | Pagina | Pagina Web del Proveedor | VARCHAR | 60 | - | - |
| 3 | Telefono | Telefono del Proveedor | INT | 15 | - | - |
| 4 | Nombre | Nombre del proveedor | VARCHAR | 20 | - | - |
| 5 | Direccion | Numero de Direccion | INT | 15 | FK | Direcciones |

Direcciones:
| N° | Nombre | Descripcion | Tipo | Longitud | PK/FK | Enlace |
| :-: | :-: | :-: | :-: | :-: | :-: | :-: |
| 1 | ID | Clave Unica | INT | 15 | PK | - |
| 2 | Calle | Nombre de la calle | VARCHAR | 30 | - | - |
| 3 | Ciudad | Nombre de la ciudad | VARCHAR | 30 | - | - |
| 4 | Comuna | Numero de Comuna | INT | 20 | - | - |

Categorias:
| N° | Nombre | Descripcion | Tipo | Longitud | PK/FK | Enlace |
| :-: | :-: | :-: | :-: | :-: | :-: | :-: |
| 1 | ID | Clave Unica | INT | 15 | PK | - |
| 2 | Nombre | Nombre de la categoria | VARCHAR | 40 | - | - |
| 3 | Descripcion | Descripcion de la categoria | VARCHAR | 80 | - | - |

Productos:
| N° | Nombre | Descripcion | Tipo | Longitud | PK/FK | Enlace |
| :-: | :-: | :-: | :-: | :-: | :-: | :-: |
| 1 | ID | Clave Unica | INT | 15 | PK | - |
| 2 | Stock | Stock del producto | INT | 20 | - | - |
| 3 | Precio_act | Precio actual del producto | DECIMAL | 10 | - | - |
| 4 | Nombre | Nombre del producto | VARCHAR | 10 | - | - |
| 5 | Proveedor | Num de proveedor | INT | 15 | FK | Proveedores |
| 6 | Categoria | Num de categoria | INT | 15 | FK | Categorias |

Clientes:
| N° | Nombre | Descripcion | Tipo | Longitud | PK/FK | Enlace |
| :-: | :-: | :-: | :-: | :-: | :-: | :-: |
| 1 | RUT | Clave Unica | INT | 15 | PK | - |
| 2 | Nombre | Nombre del Cliente | VARCHAR | 15 | - | - |
| 3 | Telefonos | Telefonos del Cliente | INT | 15 | - | - |
| 4 | Direccion | Numero de direccion | INT | 15 | FK | Direcciones |

Ventas:
| N° | Nombre | Descripcion | Tipo | Longitud | PK/FK | Enlace |
| :-: | :-: | :-: | :-: | :-: | :-: | :-: |
| 1 | ID | Clave Unica | INT | 15 | PK | - |
| 2 | Monto_t_p | Monto total de producto(cant * precio) | DECIMAL | 25 | - | - |
| 3 | cant | Cantidad de productos en la venta | INT | 10 | - | - |
| 4 | Fecha | Fecha de la venta | DATETIME | 20 | - | - |
| 5 | Descuento | Descuento realizado | DECIMAL | 10 | - | - |
| 6 | Precio_Caja | Precio en caja del producto | DECIMAL | 15 | - | - |
| 7 | Monto_F | Monto Final de la venta | DECIMAL | 30 | - | - |
| 8 | Cliente | Numero de cliente | INT | 15 | FK | Clientes |
