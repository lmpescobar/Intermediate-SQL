### Masterclass: **Consultando una Base de Datos con SQL**

---

**Introducción**

Bienvenidos a esta masterclass sobre cómo consultar bases de datos utilizando SQL para transformar datos en bruto en valiosos conocimientos. Mi nombre es Jasmin Ludolf y seré su guía en este recorrido. Nuestro objetivo es aprovechar los fundamentos ya adquiridos de SQL para profundizar en la obtención de información y presentar resultados de manera clara y precisa. A lo largo de esta sesión, entenderemos cómo realizar consultas avanzadas que nos permitirán obtener insights claros y útiles.

---

### **Mapa del Curso: Entendiendo el Poder de las Consultas SQL**

Si bien SQL se puede utilizar para crear y modificar bases de datos, el enfoque de esta masterclass será **consultar** bases de datos. Una **consulta** es una solicitud de datos a una base de datos, y aquí aprenderemos cómo ejecutar consultas de manera eficiente utilizando diversas palabras clave.

En el transcurso de esta clase, veremos cómo:
1. **Contar registros** y visualizarlos de acuerdo con lo que necesitemos.
2. Resolver errores comunes en SQL.
3. Seguir las mejores **guías de estilo** en nuestras consultas.
4. Filtrar y agrupar datos de manera efectiva.
5. Aplicar **funciones agregadas** para realizar cálculos sobre múltiples registros.

Además, usaremos **PostgreSQL** como sistema gestor de bases de datos a lo largo del curso.

---

### **Nuestra Base de Datos de Películas**

Para ilustrar los conceptos, trabajaremos con una base de datos que contiene cuatro tablas:
- **films** (películas),
- **reviews** (reseñas),
- **people** (personas),
- **roles** (roles).

La **estructura de nuestra base de datos** incluye los nombres de las tablas, los campos, y los tipos de datos. Esta visión nos permite comprender qué datos están disponibles y cómo podemos acceder a ellos de manera organizada.

---

### **Función COUNT(): Contando Registros de una Tabla**

Ahora, profundicemos en una de las funciones más útiles en SQL: **COUNT()**. Esta función nos permite contar el número de registros que contienen un valor en un campo determinado.

Ejemplo: Si queremos contar cuántas fechas de nacimiento tenemos en la tabla **people**, utilizamos la consulta:

```sql
SELECT COUNT(birthdate) AS count_birthdates FROM people;
```

El resultado de esta consulta nos indica que tenemos **6152 fechas de nacimiento** en la tabla. Observa cómo hemos utilizado el alias **"count_birthdates"** para mejorar la legibilidad de los resultados.

---

### **Contando Múltiples Campos con COUNT()**

¿Qué sucede si queremos contar más de un campo? Podemos usar la función COUNT en múltiples ocasiones dentro de la misma consulta. Por ejemplo, podemos contar tanto los nombres como las fechas de nacimiento en la tabla **people**:

```sql
SELECT COUNT(name), COUNT(birthdate) FROM people;
```

Este enfoque nos proporciona dos resultados en una sola consulta.

---

### **Contando Todos los Registros con COUNT(*)**

Usar COUNT con un nombre de campo específico nos indica cuántos valores hay en ese campo. Sin embargo, si queremos **contar el total de registros en una tabla**, podemos utilizar un asterisco (*) para contar todas las filas:

```sql
SELECT COUNT(*) FROM people;
```

Esta es una manera rápida de obtener el número total de registros en cualquier tabla.

---

### **Eliminando Duplicados con DISTINCT**

Muchas veces, nuestros resultados incluirán valores duplicados. Para extraer únicamente los valores únicos, utilizamos la palabra clave **DISTINCT**.

Ejemplo: Si deseamos saber cuántos idiomas únicos se representan en la tabla de películas **films**, utilizamos:

```sql
SELECT DISTINCT(language) FROM films;
```

Esto asegura que no tengamos valores repetidos en los resultados.

---

### **Combinando COUNT() con DISTINCT**

Para contar cuántos valores únicos existen en un campo, podemos combinar **COUNT** y **DISTINCT**:

```sql
SELECT COUNT(DISTINCT birthdate) FROM people;
```

En este caso, estamos contando cuántas **fechas de nacimiento únicas** existen en la tabla **people**. El número será menor que el conteo total porque algunas personas podrían compartir la misma fecha de nacimiento.

---

### **Conclusión y Práctica**

Ahora que hemos cubierto cómo utilizar las funciones **COUNT** y **DISTINCT** en SQL, es hora de poner manos a la obra. Recuerden: las funciones agregadas son una herramienta poderosa para resumir y organizar grandes conjuntos de datos. A medida que avanzamos, continuaremos explorando cómo aplicar estos conocimientos para obtener información clara y accionable de nuestras bases de datos.

¡Es hora de practicar y consolidar lo aprendido!