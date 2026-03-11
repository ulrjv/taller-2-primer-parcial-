# Pregunta 9

**Nombre:** Javier Turcios  
**Número:** 56  
**Grupo:** D

## Consulta que devuelva solo `titulo`

```js
use biblioteca

db.libros.find({}, { titulo: 1, _id: 0 })
```

### Explicación

- El **primer parámetro** `{}` es el filtro; al estar vacío devuelve todos los documentos.
- El **segundo parámetro** es la **proyección**:
  - `titulo: 1` → incluye el campo `titulo` en el resultado.
  - `_id: 0` → excluye el campo `_id` (que MongoDB incluye por defecto).

### Resultado esperado

```json
{ "titulo": "Introduccion a NoSQL" }
{ "titulo": "MongoDB Guia Practica" }
{ "titulo": "Aprendiendo Python" }
{ "titulo": "Java para Profesionales" }
{ "titulo": "Machine Learning Basico" }
... (20 documentos en total)
```
