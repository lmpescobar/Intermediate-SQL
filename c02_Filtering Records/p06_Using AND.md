### Masterclass: **Filtrado con Múltiples Criterios en SQL**

---

**Introducción**

¡Excelente trabajo en el filtrado de números! A medida que avanzamos en nuestras habilidades con SQL, ahora veremos cómo filtrar utilizando múltiples criterios, lo que nos permitirá refinar aún más nuestras consultas y obtener resultados precisos de nuestras bases de datos.

---

### **Filtrando con Múltiples Criterios: Operadores Lógicos**

A menudo, nos encontraremos con situaciones donde necesitamos cumplir con más de un criterio en nuestras consultas. Para ello, en SQL, tenemos tres operadores lógicos que nos permiten combinar y refinar nuestras consultas de filtrado:

1. **AND**: Para que ambas condiciones se cumplan.
2. **OR**: Para que al menos una de las condiciones sea verdadera.
3. **BETWEEN**: Para filtrar entre un rango de valores.

---

### **Ejemplo con el Operador AND**

Vamos a aplicar el operador **AND** para seleccionar todas las películas en alemán lanzadas antes del año 2000. Este operador requiere que ambas condiciones (año y lenguaje) sean verdaderas para que los registros aparezcan en los resultados.

Consulta SQL:
```sql
SELECT title, release_year
FROM films
WHERE release_year < 2000
AND language = 'German';
```

---

### **Filtrando Películas en Alemán después del 2000**

Ahora, actualizaremos nuestra consulta para mostrar únicamente las películas en alemán lanzadas después del año 2000.

Consulta SQL:
```sql
SELECT title, release_year
FROM films
WHERE release_year > 2000
AND language = 'German';
```

---

### **Combinando AND para un Rango de Fechas**

Finalmente, seleccionaremos todas las películas en alemán lanzadas después del año 2000 y antes del 2010 utilizando **AND**. Esta consulta asegura que los registros cumplan ambas condiciones dentro del rango.

Consulta SQL:
```sql
SELECT *
FROM films
WHERE release_year > 2000
AND release_year < 2010
AND language = 'German';
```

---

**Conclusión**

Al combinar operadores lógicos como **AND** y **OR**, podemos realizar consultas más complejas y precisas, lo que es esencial para el análisis de datos en situaciones del mundo real. El uso correcto de estos operadores te permitirá refinar tus búsquedas y obtener resultados relevantes que respondan exactamente a tus preguntas de negocio.

¡Es hora de practicar!