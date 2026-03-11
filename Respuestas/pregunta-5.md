# Pregunta 5

**Nombre:** Javier Turcios  
**Número:** 56  
**Grupo:** D

## Aggregation: Cantidad de libros por categoría

```js
use biblioteca

db.libros.aggregate([
  {
    $group: {
      _id: "$categoria",
      totalLibros: { $sum: 1 }
    }
  },
  {
    $sort: { totalLibros: -1 }
  }
])
```

### Explicación

- **`$group`:** agrupa todos los documentos por el campo `categoria` y cuenta cuántos hay en cada grupo usando `$sum: 1`.
- **`$sort`:** ordena el resultado de mayor a menor cantidad de libros.

### Resultado esperado

| Categoría              | Total |
|------------------------|-------|
| bases de datos         | 5     |
| infraestructura        | 3     |
| inteligencia artificial| 3     |
| computacion            | 3     |
| datos                  | 3     |
| programacion           | 2     |
| redes                  | 1     |
| seguridad              | 1     |
