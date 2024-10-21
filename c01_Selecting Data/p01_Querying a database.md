### Masterclass: **Consultando una Base de Datos con SQL**

---

**Introducción**

Bienvenidos a esta masterclass sobre cómo consultar bases de datos utilizando SQL para transformar datos en bruto en valiosos conocimientos. Mi nombre es Jasmin Ludolf, y seré su guía en este recorrido. Nuestro objetivo es profundizar en el uso de SQL para obtener insights y presentar los resultados de manera clara y precisa. A lo largo de esta sesión, aprenderemos a realizar consultas avanzadas que nos permitirán extraer información útil y accionable.

---

### **Mapa del Curso: Entendiendo el Poder de las Consultas SQL**

Aunque SQL puede ser usado para crear y modificar bases de datos, el enfoque de esta clase será **consultar** bases de datos. Una **consulta** es una solicitud de información, y aquí aprenderemos a ejecutar consultas de forma eficiente usando varias palabras clave.

Durante esta clase, aprenderemos a:

1. **Contar registros** y visualizarlos según nuestras necesidades.
2. Evitar errores comunes en SQL.
3. Aplicar las mejores **prácticas de estilo** en nuestras consultas.
4. **Filtrar** y **agrupar** datos de forma efectiva.
5. Usar **funciones agregadas** para calcular valores sobre múltiples registros.

Usaremos **PostgreSQL** como el sistema gestor de bases de datos para realizar todas nuestras consultas.

---

### **Nuestra Base de Datos de Películas**

Para ilustrar los conceptos, trabajaremos con una base de datos que contiene cuatro tablas principales:
- **films** (películas),
- **reviews** (reseñas),
- **people** (personas),
- **roles** (roles).

La **estructura de nuestra base de datos** está claramente definida, lo que nos permitirá comprender los datos disponibles y cómo acceder a ellos de manera eficiente.

---

### **Función COUNT(): Contando Registros en una Tabla**

La función **COUNT()** es esencial para contar el número de registros en una tabla. Nos dice cuántos valores existen en un campo determinado.

Por ejemplo, para contar cuántas fechas de nacimiento hay en la tabla **people**, podemos usar la siguiente consulta:

```sql
SELECT COUNT(birthdate) AS count_birthdates
FROM people;
```

El resultado nos indica que hay **6152 fechas de nacimiento** registradas. En este caso, hemos usado el alias **"count_birthdates"** para hacer más legible el resultado.

---

### **Contando Múltiples Campos con COUNT()**

Si queremos contar más de un campo en una sola consulta, podemos usar **COUNT** en varias ocasiones. Por ejemplo, para contar tanto los nombres como las fechas de nacimiento en la tabla **people**, usamos:

```sql
SELECT COUNT(name), COUNT(birthdate)
FROM people;
```

Este enfoque nos devuelve dos resultados en una sola consulta, lo que es muy útil para obtener múltiples métricas al mismo tiempo.

---

### **Contando Todos los Registros con COUNT(*)**

Si queremos **contar el total de registros** en una tabla, usamos **COUNT(*)**, donde el asterisco representa todas las filas. 

Por ejemplo:

```sql
SELECT COUNT(*)
FROM people;
```

Esta es una manera rápida de obtener el número total de registros en una tabla, sin importar cuántos campos o valores contenga.

---

### **Eliminando Duplicados con DISTINCT**

Cuando los resultados incluyen valores duplicados, podemos utilizar la palabra clave **DISTINCT** para seleccionar solo valores únicos. 

Por ejemplo, para obtener una lista de todos los idiomas únicos representados en la tabla **films**, usamos:

```sql
SELECT DISTINCT(language)
FROM films;
```

Esto asegura que los resultados no contengan valores repetidos.

---

### **Combinando COUNT() con DISTINCT**

Para contar el número de valores únicos en un campo, combinamos **COUNT()** con **DISTINCT**. 

Por ejemplo:

```sql
SELECT COUNT(DISTINCT birthdate)
FROM people;
```

Esta consulta cuenta cuántas **fechas de nacimiento únicas** existen en la tabla **people**. El resultado será menor que el total de fechas de nacimiento, ya que algunas personas comparten la misma fecha.

---

### **Conclusión y Práctica**

Hemos cubierto cómo utilizar las funciones **COUNT()** y **DISTINCT** en SQL para contar registros y eliminar duplicados. Estas funciones son fundamentales para resumir y organizar grandes conjuntos de datos. A medida que avancemos, continuaremos aplicando estos conocimientos para obtener información clara y útil de nuestras bases de datos.

¡Es hora de practicar y consolidar lo aprendido!