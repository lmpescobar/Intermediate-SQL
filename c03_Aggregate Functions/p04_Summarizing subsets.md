### Clase sobre la combinación de filtrado y funciones agregadas en SQL

#### Resumen y objetivos
En esta lección, vamos a combinar nuestras habilidades de filtrado con nuestras nuevas habilidades de resumen usando funciones agregadas en SQL. Esto nos permitirá obtener insights más profundos al filtrar datos específicos antes de aplicar cálculos como sumas, promedios, máximos, mínimos y más.

### 1. Uso de `WHERE` con funciones agregadas
Es importante recordar que en SQL, la cláusula `WHERE` se evalúa antes de la instrucción `SELECT`. Esto significa que podemos aplicar filtros a los datos antes de realizar cálculos con funciones agregadas. Aquí algunos ejemplos:

- **Obtener el presupuesto promedio de las películas hechas en 2010 o después**:
  
  ```sql
  SELECT AVG(budget) 
  FROM films 
  WHERE release_year >= 2010;
  ```

  En este ejemplo, estamos filtrando las películas con un año de lanzamiento de 2010 o posterior y calculamos el presupuesto promedio para ese subconjunto de datos.

### 2. Ejemplos adicionales con funciones agregadas y `WHERE`
Podemos usar la cláusula `WHERE` con otras funciones agregadas para obtener diferentes resúmenes. Aquí algunos ejemplos:

- **Presupuesto total de las películas hechas en 2010**:
  
  ```sql
  SELECT SUM(budget) 
  FROM films 
  WHERE release_year = 2010;
  ```

  Esto devolverá la suma total de los presupuestos de todas las películas lanzadas en 2010.

- **Presupuesto más bajo de las películas de 2010**:

  ```sql
  SELECT MIN(budget) 
  FROM films 
  WHERE release_year = 2010;
  ```

  Esto devuelve el valor mínimo (presupuesto más bajo) para las películas de ese año.

- **Presupuesto más alto de las películas de 2010**:

  ```sql
  SELECT MAX(budget) 
  FROM films 
  WHERE release_year = 2010;
  ```

  Esta consulta encuentra el presupuesto más alto en 2010. Es importante notar que algunos presupuestos pueden estar en diferentes monedas, lo que podría requerir ajustes adicionales en algunos casos.

- **Número de películas con presupuestos registrados en 2010**:

  ```sql
  SELECT COUNT(budget) 
  FROM films 
  WHERE release_year = 2010;
  ```

  Esta consulta cuenta cuántos presupuestos fueron registrados en 2010, excluyendo aquellos que son `NULL`.

### 3. Redondeo de resultados con `ROUND()`
A veces, cuando trabajamos con valores numéricos, los decimales pueden ser demasiados. Para redondear estos valores a una cantidad más manejable, SQL proporciona la función `ROUND()`. Esta función permite redondear un número a un número específico de decimales.

- **Ejemplo básico de uso de `ROUND()`**:

  ```sql
  SELECT ROUND(AVG(budget), 2) 
  FROM films 
  WHERE release_year >= 2010;
  ```

  En este ejemplo, redondeamos el promedio de los presupuestos de las películas a dos decimales.

- **Redondeo a un número entero**:

  Si no especificamos un segundo parámetro, `ROUND()` redondea al número entero más cercano:

  ```sql
  SELECT ROUND(AVG(budget)) 
  FROM films 
  WHERE release_year >= 2010;
  ```

  También podríamos haber usado `ROUND(AVG(budget), 0)` para obtener el mismo resultado.

- **Redondeo a la izquierda del punto decimal**:

  Puedes usar un número negativo en el segundo parámetro de `ROUND()` para redondear a la izquierda del punto decimal. Por ejemplo:

  ```sql
  SELECT ROUND(AVG(budget), -5) 
  FROM films 
  WHERE release_year >= 2010;
  ```

  Esto redondearía el valor a los cientos de miles.

### 4. Aplicación práctica
Ahora que has aprendido a combinar el filtrado y las funciones agregadas, es hora de practicar estas habilidades en situaciones reales. Utiliza los ejemplos proporcionados y prueba cómo los filtros afectan los resultados resumidos de tus datos.

### Reflexión final
Combinar el filtrado con el uso de funciones agregadas es una técnica fundamental en SQL. Nos permite no solo analizar grandes conjuntos de datos, sino también enfocarnos en subconjuntos específicos para obtener estadísticas más útiles y dirigidas.

Ahora que has comprendido estas ideas, puedes realizar análisis más complejos y precisos, combinando funciones de resumen con criterios específicos de filtrado para generar informes detallados.