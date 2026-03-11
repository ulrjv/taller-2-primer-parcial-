```js
use biblioteca

db.libros.updateOne(
  { titulo: "Introduccion a NoSQL", autor: "Carlos Ruiz" },
  { $set: { anio: 2022 } }
)
```
