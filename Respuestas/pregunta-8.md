# Pregunta 8

**Nombre:** Javier Turcios  
**Número:** 56  
**Grupo:** D

## Explain de consulta por categoría

```js
use biblioteca

db.libros.find({ categoria: "bases de datos" }).explain("executionStats")
```

### Explicación

- **`explain("executionStats")`** muestra el plan de ejecución detallado de la consulta.
- Permite analizar si MongoDB usa un índice o hace un escaneo completo.

### Campos clave del resultado

| Campo | Descripción |
|-------|-------------|
| `winningPlan.stage` | Tipo de operación: `IXSCAN` (usa índice) o `COLLSCAN` (escaneo completo) |
| `executionStats.nReturned` | Número de documentos devueltos |
| `executionStats.totalDocsExamined` | Documentos examinados (menor = mejor rendimiento) |
| `executionStats.totalKeysExamined` | Claves de índice examinadas |
| `executionStats.executionTimeMillis` | Tiempo de ejecución en milisegundos |

### Comparación sin/con índice

- **Sin índice:** `stage: COLLSCAN`, `totalDocsExamined = 20` (todos los documentos).
- **Con índice en `categoria`:** `stage: IXSCAN`, `totalDocsExamined = 5` (solo los relevantes).
