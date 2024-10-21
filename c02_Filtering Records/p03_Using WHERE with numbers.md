### Ejercicio 1: Filtrar películas con un puntaje IMDb mayor a 7.0

**Consulta SQL:**
```sql
-- Seleccionar las películas con un puntaje IMDb mayor a 7.0
SELECT film_id, imdb_score
FROM reviews
WHERE imdb_score > 7.0;
```

**Explicación:**
- Estamos seleccionando las columnas `film_id` (el identificador de la película) y `imdb_score` (el puntaje de IMDb).
- La cláusula `WHERE` está filtrando las filas de la tabla `reviews` para mostrar solo aquellas películas que tengan un puntaje superior a 7.0.

---

### Ejercicio 2: Seleccionar las primeras 10 películas con menos de 1000 "Me Gusta" en Facebook

**Consulta SQL:**
```sql
-- Seleccionar las películas con menos de 1000 "Me Gusta" en Facebook
SELECT film_id, facebook_likes
FROM reviews
WHERE facebook_likes < 1000
LIMIT 10;
```

**Explicación:**
- Esta consulta selecciona las columnas `film_id` y `facebook_likes` de las películas que tienen menos de 1000 "Me Gusta" en Facebook.
- La cláusula `WHERE` filtra las películas que cumplen esta condición, y `LIMIT 10` asegura que solo las primeras 10 películas que cumplan con el criterio se devuelvan en los resultados.

---

### Ejercicio 3: Contar películas con al menos 100,000 votos

**Consulta SQL:**
```sql
-- Contar cuántas películas tienen al menos 100,000 votos
SELECT COUNT(num_votes) AS films_over_100K_votes
FROM reviews
WHERE num_votes >= 100000;
```

**Explicación:**
- En esta consulta estamos utilizando `COUNT` para contar el número de películas que tienen 100,000 votos o más.
- El filtro se aplica en la cláusula `WHERE`, seleccionando solo las películas con al menos 100,000 votos (`num_votes >= 100000`).
- El alias `films_over_100K_votes` se utiliza para que el resultado de la cuenta tenga un nombre más descriptivo.

---

### Conceptos Clave:

1. **Cláusula `WHERE`**: Utilizada para filtrar filas en función de una condición. Puede aplicarse a datos numéricos, textos y fechas.
2. **Operadores de comparación**:
   - `>`: Mayor que.
   - `<`: Menor que.
   - `>=`: Mayor o igual que.
   - `<=`: Menor o igual que.
   - `=`: Igual a.
   - `!=` o `<>`: Diferente de.
3. **Filtrado de registros**: Es útil para centrarse solo en los datos relevantes a partir de condiciones específicas.
4. **Uso de `LIMIT`**: Permite limitar el número de registros devueltos en una consulta.
5. **Contar registros**: Con `COUNT()` podemos contar cuántas filas cumplen con una condición específica, como en el ejemplo de contar películas con más de 100,000 votos.