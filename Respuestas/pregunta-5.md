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
