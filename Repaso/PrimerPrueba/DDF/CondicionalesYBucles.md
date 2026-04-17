# Diagramas de Flujo en Programación (con estructuras de control)

## ¿Qué es?
Un **diagrama de flujo** representa gráficamente la lógica de un algoritmo usando símbolos y flechas para indicar el flujo de ejecución.

---

## Estructuras de control principales

### 🔹 IF (Condicional)
Permite tomar decisiones según una condición.

**Estructura:**
```text
      ┌───────────────┐
      │   Condición   │
      └──────┬────────┘
             ↓
        ┌────┴────┐
       Sí         No
       ↓           ↓
   Acción A    Acción B
        \        /
         ↓      ↓
           Fin

  ```

  ### WHILE

```text
          ┌───────────────┐
        │   Condición   │
        └──────┬────────┘
               ↓
            Verdadero
               ↓
           Proceso
               ↓
           (vuelve)
               ↑
               │
           Falso
               ↓
              Fin
```
### FOR
```text
     Inicialización
            ↓
     ┌───────────────┐
     │   Condición   │
     └──────┬────────┘
            ↓
        Verdadero
            ↓
         Proceso
            ↓
       Incremento
            ↓
        (vuelve)
            ↑
            │
         Falso
            ↓
           Fin
```

