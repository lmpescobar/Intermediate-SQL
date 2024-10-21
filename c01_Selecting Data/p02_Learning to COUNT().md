# Aprendiendo a usar la función COUNT()

### Descripción del ejercicio:

En este ejercicio, aprenderemos a utilizar la función `COUNT()` en SQL. Esta función nos permite contar la cantidad de registros que contienen un valor específico en una columna de una tabla.

La consulta proporcionada en el ejercicio es la siguiente:

```sql
SELECT COUNT(film_id) AS count_film_id 
FROM reviews;
```

### Instrucciones:

1. La consulta cuenta cuántos registros contienen un valor en la columna `film_id` de la tabla `reviews`.
2. Debes seleccionar la respuesta que correctamente describa qué retornará la consulta.

### Opciones posibles:

1. **The number of unique films in the reviews table.**  
   - Incorrecta. La consulta no utiliza `DISTINCT`, por lo tanto, no cuenta valores únicos.
   
2. **The number of records containing a film_id.**  
   - Correcta. La función `COUNT(film_id)` cuenta cuántos registros tienen un valor en la columna `film_id` en la tabla `reviews`. No necesariamente cuenta valores únicos, simplemente cuenta cuántos registros tienen un valor asignado.
   
3. **The total number of records in the reviews table.**  
   - Incorrecta. Para contar el total de registros en la tabla, sin importar si contienen o no un valor en una columna específica, deberíamos usar `COUNT(*)`.
   
4. **The sum of the film_id field.**  
   - Incorrecta. `COUNT()` no suma los valores de una columna, solo cuenta cuántos registros tienen un valor en esa columna.

### Explicación:

- **COUNT()** es una función agregada en SQL que cuenta cuántos registros contienen un valor en una columna específica. Si queremos contar los registros totales, utilizamos `COUNT(*)`, pero si queremos contar solo los registros que tienen un valor en una columna específica (en este caso, `film_id`), utilizamos `COUNT(film_id)`.
- En la consulta proporcionada, estamos contando cuántos registros contienen un valor en la columna `film_id` de la tabla `reviews`, y el resultado será el número de registros que contienen un `film_id`.