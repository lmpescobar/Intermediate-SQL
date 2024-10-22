### Practice with aggregate functions:

1. **Instrucción 1/4**: 
   - Debes utilizar la función `SUM()` para calcular la suma total de las duraciones de todas las películas en la tabla `films`. Se te pide que utilices el alias `total_duration` para el resultado.
   
   ```sql
   SELECT SUM(duration) AS total_duration
   FROM films;
   ```
   Esta consulta devuelve la suma total de todas las duraciones de las películas.

2. **Instrucción 2/4**: 
   - Luego, debes calcular la duración promedio de todas las películas utilizando la función `AVG()` y el alias `average_duration`.
   
   ```sql
   SELECT AVG(duration) AS average_duration
   FROM films;
   ```
   Esta consulta te dará el promedio de duración de las películas.

3. **Instrucción 3/4**:
   - Ahora se te pide que encuentres el año más reciente de lanzamiento (`release_year`) utilizando la función `MAX()` y lo aliases como `latest_year`.

   ```sql
   SELECT MAX(release_year) AS latest_year
   FROM films;
   ```

4. **Instrucción 4/4**:
   - Finalmente, debes encontrar la duración de la película más corta utilizando la función `MIN()` y alias como `shortest_film`.

   ```sql
   SELECT MIN(duration) AS shortest_film
   FROM films;
   ```

### Explicación general de las funciones agregadas:

- **SUM()**: Suma todos los valores de una columna numérica.
- **AVG()**: Calcula el promedio de los valores en una columna numérica.
- **MIN()**: Encuentra el valor mínimo de una columna, ya sea numérica o no.
- **MAX()**: Encuentra el valor máximo de una columna.
- **COUNT()**: Cuenta la cantidad de filas, excluyendo `NULL`.

Estas funciones agregadas son fundamentales cuando necesitas hacer resúmenes o análisis de grandes volúmenes de datos en SQL, ya que te permiten obtener rápidamente métricas clave, como totales, promedios, mínimos y máximos.