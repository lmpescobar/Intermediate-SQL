En este ejercicio, estás utilizando la función `ROUND()` para redondear el resultado de un valor numérico en SQL. Aquí está el desglose de lo que hace esta consulta:

### Consulta SQL:
```sql
-- Redondear el promedio de facebook_likes a un decimal
SELECT ROUND(AVG(facebook_likes), 1) AS avg_facebook_likes
FROM reviews;
```

### Explicación de la consulta:

1. **AVG(facebook_likes)**: Esto calcula el **promedio** de la columna `facebook_likes` en la tabla `reviews`.
   
2. **ROUND(AVG(facebook_likes), 1)**: Redondea el promedio de `facebook_likes` a **un decimal**. El primer argumento es el valor que queremos redondear (el promedio de `facebook_likes`), y el segundo argumento indica cuántos decimales deseamos mantener. En este caso, 1 decimal.

3. **AS avg_facebook_likes**: Utilizamos un **alias** para renombrar el resultado de la columna como `avg_facebook_likes`, lo que facilita la lectura y comprensión del resultado.

### Contexto de la función `ROUND()`:
La función `ROUND()` es muy útil cuando estamos trabajando con números que pueden tener muchos decimales, especialmente en contextos donde no necesitamos ese nivel de precisión, como en datos financieros o métricas de redes sociales.

El objetivo de este ejercicio es hacer que los resultados numéricos sean más manejables y presentables, como en este caso, redondeando el número promedio de likes de Facebook a un decimal.