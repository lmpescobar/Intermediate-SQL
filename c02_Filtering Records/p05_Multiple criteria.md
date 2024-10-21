### Masterclass: **Filtrando con Múltiples Criterios en SQL**

---

**Introducción**

¡Felicidades por tu progreso filtrando números en SQL! Ahora vamos a dar un paso más y aprenderemos cómo filtrar utilizando múltiples criterios a la vez. En la vida real, a menudo necesitamos analizar datos con más de una condición. Así que, en lugar de filtrar por un solo criterio, podemos ampliar nuestras consultas para que incluyan más de una condición, haciendo nuestras búsquedas más específicas.

---

### **Filtrando con Múltiples Criterios**

Imaginemos que estamos eligiendo un abrigo. Tal vez no solo queramos uno de un color específico, sino también de una longitud particular. Así que podríamos querer abrigos **amarillos** y que además sean **cortos**.

Para lograr este tipo de filtrado en SQL, usaremos palabras clave adicionales que nos permitirán incluir varios criterios al mismo tiempo. Las principales que aprenderemos hoy son **OR**, **AND**, y **BETWEEN**.

---

### **Operador OR: Cumplir al Menos una Condición**

El operador **OR** nos permite aplicar filtros donde solo se necesita cumplir **una** de las condiciones especificadas. Esto es útil si queremos seleccionar registros que se ajusten a una u otra condición.

- **Ejemplo**: Queremos seleccionar películas lanzadas en 1994 **o** en 2000. La consulta sería:

```sql
SELECT title
FROM films
WHERE release_year = 1994 OR release_year = 2000;
```

**Nota**: Cada condición debe ser completamente especificada, incluyendo el nombre del campo y el operador. Es decir, no podemos omitir el campo en la segunda parte de la condición, como se muestra a continuación, que sería inválido:

```sql
-- Esto es incorrecto
SELECT title
FROM films
WHERE release_year = 1994 OR 2000;
```

---

### **Operador AND: Cumplir Todas las Condiciones**

Cuando queremos que nuestros registros cumplan **todas** las condiciones que definamos, utilizamos el operador **AND**.

- **Ejemplo**: Para filtrar las películas lanzadas entre 1994 y 2000, podemos escribir:

```sql
SELECT title
FROM films
WHERE release_year >= 1994 AND release_year <= 2000;
```

Al igual que con **OR**, necesitamos especificar el nombre del campo y el operador en cada condición.

---

### **Combinando AND y OR: Filtros más Complejos**

Podemos combinar **AND** y **OR** en una misma consulta cuando necesitemos múltiples filtros. Sin embargo, es importante usar paréntesis para asegurarnos de que las condiciones se procesen en el orden correcto.

- **Ejemplo**: Queremos seleccionar películas lanzadas en 1994 **o** en 1995, **y** cuya certificación sea **PG** o **R**. Aquí la consulta correcta sería:

```sql
SELECT title
FROM films
WHERE (release_year = 1994 OR release_year = 1995)
  AND (certification = 'PG' OR certification = 'R');
```

Los paréntesis son esenciales para que SQL procese correctamente las condiciones de **AND** y **OR**.

---

### **BETWEEN: Filtrar Rangos**

El operador **BETWEEN** es muy útil cuando necesitamos filtrar datos dentro de un rango. Es un atajo conveniente en lugar de usar **AND** con operadores de comparación como **>=** y **<=**.

- **Ejemplo**: Queremos seleccionar películas lanzadas entre 1994 y 2000, ambos incluidos:

```sql
SELECT title
FROM films
WHERE release_year BETWEEN 1994 AND 2000;
```

**Importante**: **BETWEEN** es inclusivo, lo que significa que **incluye** los valores iniciales y finales del rango.

---

### **Combinando BETWEEN con AND y OR**

Al igual que con **WHERE**, **BETWEEN** también puede combinarse con **AND** y **OR** para crear filtros más complejos.

- **Ejemplo**: Queremos seleccionar todas las películas lanzadas entre 1994 y 2000 que sean del Reino Unido:

```sql
SELECT title
FROM films
WHERE release_year BETWEEN 1994 AND 2000
  AND country = 'United Kingdom';
```

Esto nos permite filtrar no solo por rango de años, sino también por otro criterio, como el país.

---

### **Conclusión**

El uso de múltiples criterios en SQL nos permite realizar consultas mucho más precisas y útiles. Con **OR**, **AND**, y **BETWEEN**, podemos refinar nuestros filtros y aplicar condiciones complejas, haciendo que nuestras consultas sean más potentes y adaptables a diferentes preguntas de negocio.

Es hora de practicar estas técnicas en la base de datos de películas. ¡Manos a la obra!