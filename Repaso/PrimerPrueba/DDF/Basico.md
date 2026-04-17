# Diagramas de Flujo en Programación

## ¿Qué es un diagrama de flujo?
Un **diagrama de flujo** es una representación gráfica de un algoritmo o proceso. Utiliza símbolos estándar conectados por flechas para mostrar el flujo de ejecución paso a paso.

---

## ¿Para qué sirven?
- Visualizar la lógica de un programa
- Facilitar la comprensión de procesos complejos
- Detectar errores antes de programar
- Documentar algoritmos

---

## Símbolos principales

| Símbolo        | Nombre            | Función |
|----------------|------------------|--------|
| Óvalo          | Inicio/Fin        | Marca el comienzo o final del proceso |
| Rectángulo     | Proceso           | Indica una acción o instrucción |
| Rombo          | Decisión          | Representa una condición (sí/no) |
| Paralelogramo  | Entrada/Salida    | Lectura o impresión de datos |
| Flechas        | Flujo             | Indican la dirección del proceso |

---

## Estructura básica
1. Inicio
2. Entrada de datos (opcional)
3. Procesos (cálculos o instrucciones)
4. Decisiones (condiciones)
5. Salida de resultados
6. Fin

---

## Ejemplo simple

**Problema:** Determinar si un número es par o impar

```text
Inicio
  ↓
Ingresar número
  ↓
¿Número % 2 == 0?
  ↓           ↓
 Sí           No
 ↓             ↓
"Es par"    "Es impar"
  ↓             ↓
       Fin
