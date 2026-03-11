# Pregunta 6

**Nombre:** Javier Turcios  
**Número:** 56  
**Grupo:** D

## Índice en `categoria`

```js
use biblioteca

db.libros.createIndex({ categoria: 1 })
```

### Explicación

- Se crea un índice **ascendente** (`1`) sobre el campo `categoria`.
- Este índice mejora el rendimiento de las consultas que filtran o agrupan por `categoria`, como las de las preguntas 3, 5 y 8.
- Sin índice, MongoDB realiza un **COLLSCAN** (escaneo completo de la colección). Con el índice, pasa a usar un **IXSCAN** (escaneo de índice), que es significativamente más eficiente.
