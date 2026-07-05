# EMPLEADO

| N° | Nombre | Descripción | Tipo | Longitud | PK/FK | Enlace |
| -- | ------ | ----------- | ---- | -------- | ----- | ------- |
| 1 | Cedula | Número de identificación del empleado | VARCHAR | 20 | PK | - |
| 2 | Nombre | Nombre completo del empleado | VARCHAR | 100 | - | - |

# CENTRO_COSTOS

| N° | Nombre | Descripción | Tipo | Longitud | PK/FK | Enlace |
| -- | ------ | ----------- | ---- | -------- | ----- | ------- |
| 1 | Codigo_Centro | Código único del centro de costos | VARCHAR | 10 | PK | - |
| 2 | Nombre_Centro | Nombre del centro de costos | VARCHAR | 100 | - | - |

# RUBRO_PRESUPUESTAL

| N° | Nombre | Descripción | Tipo | Longitud | PK/FK | Enlace |
| -- | ------ | ----------- | ---- | -------- | ----- | ------- |
| 1 | Codigo_Rubro | Código único del rubro presupuestal | VARCHAR | 10 | PK | - |
| 2 | Nombre_Rubro | Nombre del rubro presupuestal | VARCHAR | 100 | - | - |

# SOLICITUD

| N° | Nombre | Descripción | Tipo | Longitud | PK/FK | Enlace |
| -- | ------ | ----------- | ---- | -------- | ----- | ------- |
| 1 | Numero_Solicitud | Número único de la solicitud | INT | 11 | PK | - |
| 2 | Fecha | Fecha en que se registra la solicitud | DATE | - | - | - |
| 3 | Valor_Total | Valor total de la solicitud | DECIMAL | 12,2 | - | - |

# ITEM

| N° | Nombre | Descripción | Tipo | Longitud | PK/FK | Enlace |
| -- | ------ | ----------- | ---- | -------- | ----- | ------- |
| 1 | Codigo_Universal | Código único del bien | VARCHAR | 20 | PK | - |
| 2 | Nombre_Bien | Nombre del bien | VARCHAR | 100 | - | - |
| 3 | Tipo_Bien | Tipo o categoría del bien | VARCHAR | 50 | - | - |

# ITEM_SOLICITUD

| N° | Nombre | Descripción | Tipo | Longitud | PK/FK | Enlace |
| -- | ------ | ----------- | ---- | -------- | ----- | ------- |
| 1 | Item | Número del ítem dentro de la solicitud | INT | 11 | PK | - |
| 2 | Numero_Solicitud | Solicitud a la que pertenece el ítem | INT | 11 | PK, FK | SOLICITUD |
| 3 | Codigo_Universal | Bien solicitado | VARCHAR | 20 | PK, FK | BIEN |
| 4 | Codigo_Centro | Centro de costos asociado | VARCHAR | 10 | FK | CENTRO_COSTOS |
| 5 | Codigo_Rubro | Rubro presupuestal asociado | VARCHAR | 10 | FK | RUBRO_PRESUPUESTAL |
| 6 | Cantidad_Solicitada | Cantidad solicitada | INT | 11 | - | - |
| 7 | Unidad_Medida | Unidad de medida del bien | VARCHAR | 20 | - | - |
| 8 | Valor_Unitario | Valor unitario del bien | DECIMAL | 12,2 | - | - |
| 9 | Valor_Total | Valor total del ítem | DECIMAL | 12,2 | - | - |

# AUTORIZACION

| N° | Nombre | Descripción | Tipo | Longitud | PK/FK | Enlace |
| -- | ------ | ----------- | ---- | -------- | ----- | ------- |
| 1 | Numero_Solicitud | Solicitud autorizada | INT | 11 | PK, FK | SOLICITUD |
| 2 | Cedula_Empleado | Empleado que autoriza | VARCHAR | 20 | PK, FK | EMPLEADO |
| 3 | Tipo_Autorizacion | Tipo de autorización realizada | VARCHAR | 50 | - | - |
| 4 | Fecha_Autorizacion | Fecha de autorización | DATE | - | - | - |

# COTIZACION

| N° | Nombre | Descripción | Tipo | Longitud | PK/FK | Enlace |
| -- | ------ | ----------- | ---- | -------- | ----- | ------- |
| 1 | Numero_Cotizacion | Número único de la cotización | INT | 11 | PK | - |
| 2 | Fecha_Cotizacion | Fecha de la cotización | DATE | - | - | - |
| 3 | Numero_Solicitud | Solicitud cotizada | INT | 11 | FK | SOLICITUD |

# DETALLE_COTIZACION

| N° | Nombre | Descripción | Tipo | Longitud | PK/FK | Enlace |
| -- | ------ | ----------- | ---- | -------- | ----- | ------- |
| 1 | Numero_Cotizacion | Número de la cotización | INT | 11 | PK, FK | COTIZACION |
| 2 | NIT_Proveedor | Proveedor que presenta la oferta | VARCHAR | 20 | PK, FK | PROVEEDOR |
| 3 | Valor_Cotizado | Valor ofrecido para el bien | DECIMAL | 12,2 | - | - |

# PROVEEDOR

| N° | Nombre | Descripción | Tipo | Longitud | PK/FK | Enlace |
| -- | ------ | ----------- | ---- | -------- | ----- | ------- |
| 1 | NIT | Número de identificación tributaria del proveedor | VARCHAR | 20 | PK | - |
| 2 | Nombre_Proveedor | Nombre o razón social del proveedor | VARCHAR | 100 | - | - |

# ORDEN_CONTRACTUAL

| N° | Nombre | Descripción | Tipo | Longitud | PK/FK | Enlace |
| -- | ------ | ----------- | ---- | -------- | ----- | ------- |
| 1 | Numero_Orden | Número único de la orden contractual | INT | 11 | PK | - |
| 2 | NIT_Proveedor | Proveedor adjudicado | VARCHAR | 20 | FK | PROVEEDOR |
| 3 | Cedula_Aprueba | Empleado que aprueba la orden | VARCHAR | 20 | FK | EMPLEADO |
| 4 | Fecha_Orden | Fecha de emisión de la orden | DATE | - | - | - |
| 5 | Monto_Total | Valor total de la orden | DECIMAL | 12,2 | - | - |
| 6 | Fecha_Entrega | Fecha prevista de entrega | DATE | - | - | - |
| 7 | Nombre_Bien | Nombre del bien contratado | VARCHAR | 100 | - | - |

# ITEM_ORDEN

| N° | Nombre | Descripción | Tipo | Longitud | PK/FK | Enlace |
| -- | ------ | ----------- | ---- | -------- | ----- | ------- |
| 1 | Numero_Orden | Orden contractual asociada | INT | 11 | PK, FK | ORDEN_CONTRACTUAL |
| 2 | Item | Número del ítem de la orden | INT | 11 | PK | - |
| 3 | Numero_Solicitud | Solicitud de origen | INT | 11 | FK | SOLICITUD |
| 4 | Cantidad_Solicitada | Cantidad solicitada | INT | 11 | - | - |
| 5 | Cantidad_Despachada | Cantidad efectivamente despachada | INT | 11 | - | - |
| 6 | Unidad_Medida | Unidad de medida | VARCHAR | 20 | - | - |
| 7 | Valor_Unitario | Valor unitario del bien | DECIMAL | 12,2 | - | - |
| 8 | Valor_Total | Valor total del ítem | DECIMAL | 12,2 | - | - |
