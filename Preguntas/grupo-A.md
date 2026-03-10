# EXAMEN GRUPO A

### Pregunta 1 — Tipo de base de datos (1 punto)

Una empresa quiere analizar rutas entre ciudades.
Cada ciudad puede conectarse con muchas otras y se necesitan consultas como:

* caminos mínimos
* conexiones indirectas
* análisis de redes

Indique qué tipo de base de datos es más adecuada.

### Pregunta 2 — Inserción (1 punto)

Insertar en la colección `cursos` el documento:

```JS
nombre: "MongoDB Avanzado"
nivel: "intermedio"
creditos: 5
departamento: "Informatica"
```

### Pregunta 3 — Consulta (1 punto)

Consultar cursos con:

```JS
nivel = "intermedio"
```

### Pregunta 4 — Update (1 punto)

Actualizar el curso `"MongoDB Avanzado"` para que tenga ​6 créditos​.

### Pregunta 5 — Aggregation Framework (2 puntos)

Calcular el ​número de cursos por nivel​.

### Pregunta 6 — Índice (1 punto)

Crear índice sobre:

```JS
nivel
```

### Pregunta 7 — Índice compuesto (1 punto)

Crear índice compuesto sobre:

```JS
nivel + creditos
```

### Pregunta 8 — Explain (1 punto)

Ejecutar una consulta con `explain("executionStats")` sobre:

```JS
nivel = "intermedio"
```

## Pregunta 9 — Consulta optimizada (1 punto)

Realizar una consulta que devuelva solo el campo nombre de los cursos.

