### Filtrado de valores `NULL` en SQL: Guía informativa

Al trabajar con bases de datos, tarde o temprano te encontrarás con valores `NULL`. Estos representan datos faltantes o desconocidos, y su correcto manejo es fundamental para asegurar la integridad de los análisis que realices. En esta guía, aprenderás a manejar estos valores, cómo identificarlos y cómo filtrarlos.

#### ¿Qué son los valores `NULL`?
En SQL, un valor `NULL` indica que no se dispone de datos para un campo específico. Esto no significa que el campo esté vacío, sino que el valor es desconocido o no aplicable. Este concepto es crucial, ya que en el mundo real, las bases de datos suelen tener campos sin información debido a múltiples razones, como errores humanos o simplemente porque el dato aún no está disponible.

Por ejemplo, en una tabla de personas (`people`), podrías tener una columna `birthdate` donde no todos los registros tienen una fecha de nacimiento registrada. Estos valores sin registrar aparecerán como `NULL`.

#### Filtrar datos con `IS NULL` y `IS NOT NULL`

Existen dos formas clave para trabajar con valores `NULL` en SQL: identificarlos o ignorarlos. Aquí te explico cómo puedes lograr ambas cosas:

1. **Identificar valores `NULL` con `IS NULL`**:
   Si quieres identificar registros que tienen datos faltantes, el operador `IS NULL` te permite seleccionar aquellos registros donde un campo específico no tiene información.

   ```sql
   SELECT name 
   FROM people 
   WHERE birthdate IS NULL;
   ```

   Esta consulta devolverá todas las personas en la tabla `people` que no tienen una fecha de nacimiento registrada. Esto es útil si necesitas saber cuántos valores están faltando en tu conjunto de datos.

2. **Excluir valores `NULL` con `IS NOT NULL`**:
   En algunas ocasiones, querrás trabajar únicamente con registros que tengan valores válidos, es decir, aquellos que no contienen `NULL`. El operador `IS NOT NULL` te permite hacer esto.

   ```sql
   SELECT name 
   FROM people 
   WHERE birthdate IS NOT NULL;
   ```

   Aquí, obtendrás solo los nombres de las personas cuya fecha de nacimiento esté registrada, excluyendo aquellas donde el valor es `NULL`.

#### Contar registros con valores `NULL`
Cuando usamos la función `COUNT()` en SQL, los valores `NULL` no son contados a menos que los incluya de manera explícita. Por ejemplo:

- **Contar todos los registros, incluidos los que tienen `NULL`**:
  
  ```sql
  SELECT COUNT(*) 
  FROM people;
  ```

  Aquí se cuentan todos los registros, sin importar si algunos campos tienen valores `NULL`.

- **Contar solo los registros con datos válidos**:
  
  ```sql
  SELECT COUNT(birthdate) 
  FROM people;
  ```

  En esta consulta, solo se contarán aquellos registros donde el campo `birthdate` tenga un valor, excluyendo los valores `NULL`. Otra opción sería usar:

  ```sql
  SELECT COUNT(*) 
  FROM people 
  WHERE birthdate IS NOT NULL;
  ```

  Ambas consultas arrojarán el mismo resultado, ya que solo cuentan los valores que no son `NULL`.

#### ¿Por qué es importante manejar los valores `NULL`?

Ignorar la presencia de valores `NULL` puede llevar a errores en el análisis de datos. Por ejemplo, si no tienes en cuenta que una columna tiene `NULL` en varios registros, podrías hacer suposiciones incorrectas sobre el contenido de tu base de datos. En el caso de la columna `deathdate` en una tabla de personas, si asumieras que todas las personas tienen esa información registrada, podrías calcular erróneamente la cantidad de personas fallecidas en el conjunto de datos.

#### Resumen

- **`NULL`**: Representa un valor faltante o desconocido.
- **`IS NULL`**: Identifica los registros que tienen valores `NULL`.
- **`IS NOT NULL`**: Selecciona solo los registros que contienen datos válidos (no `NULL`).
- **`COUNT()`**: Excluye automáticamente los valores `NULL` a menos que se indique lo contrario.

Saber cómo manejar valores `NULL` es una habilidad básica, pero esencial, al trabajar con bases de datos SQL. Estos valores aparecen con mucha frecuencia en el mundo real y tener herramientas para identificarlos y filtrarlos te permitirá hacer análisis más precisos y tomar decisiones mejor fundamentadas.