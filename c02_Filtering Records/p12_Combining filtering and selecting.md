### Explicación del ejercicio:

#### **Instrucciones del ejercicio:**

**Título: "Combining filtering and selecting" (Combinando filtrado y selección)**

Este ejercicio presenta un desafío que combina varias cláusulas SQL que hemos aprendido hasta ahora: `COUNT()`, `DISTINCT`, `LIMIT`, `WHERE`, `OR`, `AND`, `BETWEEN`, `LIKE`, `NOT LIKE`, y `IN`. El objetivo es construir una consulta más compleja que reúna estas funciones.

**Descripción**: 
El objetivo es descubrir las películas de los años 90 en nuestra base de datos que sean adecuadas para adolescentes angloparlantes. Para hacerlo, vamos a filtrar por año de lanzamiento, idioma y clasificación de películas.

#### **Consulta SQL y pasos detallados**:

1. **Contar los títulos únicos de la base de datos de películas (films)**.
2. **Filtrar solo películas con un año de lanzamiento entre 1990 y 1999** (ambos inclusive).
3. **Filtrar para incluir solo las películas en idioma inglés**.
4. **Finalmente, aplicar un filtro para limitar las películas con las clasificaciones `G`, `PG` o `PG-13`**.

```sql
-- Contar los títulos únicos
SELECT COUNT(DISTINCT title) AS nineties_english_films_for_teens
FROM films
-- Filtrar por años de lanzamiento entre 1990 y 1999
WHERE release_year BETWEEN 1990 AND 1999
-- Filtrar por películas en idioma inglés
AND language = 'English'
-- Filtrar por clasificaciones G, PG y PG-13
AND certification IN ('G', 'PG', 'PG-13');
```

#### **Explicación paso a paso**:

1. **Contar títulos únicos con `COUNT(DISTINCT)`**:
   - Aquí estamos utilizando la función `COUNT()` para contar los títulos. Añadimos `DISTINCT` para asegurarnos de que solo estamos contando títulos únicos (no repetidos) en nuestra base de datos.
   - Le damos un alias (`AS`) a esta columna calculada para que el resultado se llame `nineties_english_films_for_teens`.

2. **Filtrado por año de lanzamiento (`WHERE release_year BETWEEN 1990 AND 1999`)**:
   - Utilizamos `BETWEEN` para seleccionar todas las películas cuyo año de lanzamiento esté entre 1990 y 1999 (ambos inclusive).
   - Esta es una técnica común cuando estamos interesados en un rango de valores.

3. **Filtrado por idioma inglés (`AND language = 'English'`)**:
   - Este `AND` adicional limita los resultados a películas en las que el idioma es inglés. 
   - La cláusula `WHERE` se está expandiendo con más condiciones.

4. **Filtrado por clasificación (`AND certification IN ('G', 'PG', 'PG-13')`)**:
   - Aquí usamos `IN` para especificar que solo queremos películas con certificaciones aptas para adolescentes: `G`, `PG`, o `PG-13`. 
   - Usar `IN` hace que el código sea más limpio y fácil de leer, en lugar de encadenar múltiples condiciones `OR`.

---

Este ejercicio combina varios conceptos importantes y nos ayuda a practicar cómo estructurar consultas más complejas en SQL. La consulta selecciona únicamente las películas que cumplan con todos los criterios mencionados y cuenta cuántos títulos únicos cumplen estos filtros.