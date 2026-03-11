# Pregunta 7

**Nombre:** Javier Turcios  
**Número:** 56  
**Grupo:** D

## Índice compuesto: `categoria` + `anio`

```js
use biblioteca

db.libros.createIndex({ categoria: 1, anio: -1 })
```

### Explicación

- Se crea un índice **compuesto** sobre `categoria` (ascendente) y `anio` (descendente).
- Es útil para consultas que filtran por `categoria` **y** ordenan o filtran por `anio` al mismo tiempo.
- El orden importa: MongoDB puede usar este índice para consultas que usen solo `categoria`, pero **no** puede usarlo eficientemente si solo se consulta por `anio`.

**Ejemplo de consulta que se beneficia de este índice:**

```js
db.libros.find({ categoria: "bases de datos" }).sort({ anio: -1 })
```
