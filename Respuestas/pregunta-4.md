# Pregunta 4

**Nombre:** Javier Turcios  
**Número:** 56  
**Grupo:** D

## Actualizar año a 2022

Actualizar el año del documento insertado en la Pregunta 2 (`"Introduccion a NoSQL"`) a `2022`:

```js
use biblioteca

db.libros.updateOne(
  { titulo: "Introduccion a NoSQL", autor: "Carlos Ruiz" },
  { $set: { anio: 2022 } }
)
```

### Explicación

- **Filtro:** se busca el documento por `titulo` y `autor` para identificarlo de forma única.
- **`$set`:** operador que actualiza sólo el campo indicado (`anio`) sin modificar el resto del documento.
