# Pregunta 3

**Nombre:** Javier Turcios  
**Número:** 56  
**Grupo:** D

## Consultar libros de "bases de datos"

```js
use biblioteca

db.libros.find({ categoria: "bases de datos" })
```

### Resultado esperado

Devuelve todos los documentos donde el campo `categoria` sea igual a `"bases de datos"`:

- Introduccion a NoSQL
- MongoDB Guia Practica
- Bases de Datos Distribuidas
- Neo4j en Produccion
