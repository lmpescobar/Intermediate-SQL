### Masterclass: **Filtrando Resultados con SQL: Operadores y Cadenas de Texto**

---

**Introducción**

Bienvenidos de nuevo. Ahora que hemos dominado la selección y el conteo de datos en SQL, vamos a aprender una habilidad clave: **filtrar los resultados**. Filtrar datos es esencial para responder preguntas empresariales específicas, enfocando nuestros análisis en la información relevante.

---

### **Cláusula WHERE: El Filtro de SQL**

Para realizar un filtro en SQL, utilizamos la cláusula **WHERE**. Esta nos permite seleccionar únicamente los datos que cumplen ciertas condiciones. Pensemos en esto como si estuviéramos eligiendo un abrigo en un armario: podemos seleccionar solo los abrigos que cumplen con un criterio específico, como el color.

---

### **Filtrando Números: Operadores de Comparación**

Vamos a comenzar filtrando números. Para esto, SQL ofrece operadores de comparación, como **mayor que** o **menor que**.

- **Ejemplo 1**: Para ver las películas estrenadas después del año 1960, usamos el operador de mayor que (>):
  ```sql
  SELECT title
  FROM films
  WHERE release_year > 1960;
  ```

---

### **Otros Operadores Comunes en SQL**

1. **Menor que (<)**: Para ver películas lanzadas antes de 1960:
   ```sql
   SELECT title
   FROM films
   WHERE release_year < 1960;
   ```
2. **Menor o igual (<=)**: Para ver películas lanzadas en o antes de 1960:
   ```sql
   SELECT title
   FROM films
   WHERE release_year <= 1960;
   ```
3. **Igual a (=)**: Para ver películas de un año específico:
   ```sql
   SELECT title
   FROM films
   WHERE release_year = 1960;
   ```

4. **Diferente de (<> ó !=)**: Para ver todas las películas **excepto** las lanzadas en 1960:
   ```sql
   SELECT title
   FROM films
   WHERE release_year <> 1960;
   ```

---

### **Operadores de Comparación: Resumen**

Con **WHERE** podemos usar los siguientes operadores para filtrar números:
- **>** (mayor que)
- **<** (menor que)
- **=** (igual a)
- **<=** (menor o igual a)
- **>=** (mayor o igual a)
- **<>** o **!=** (diferente de)

---

### **Filtrando Texto: Usando WHERE con Cadenas**

Además de filtrar números, **WHERE** también funciona con texto. Cuando usamos cadenas de texto, debemos incluir las comillas simples (**' '**) alrededor del valor que estamos filtrando.

- **Ejemplo**: Para filtrar películas donde el idioma sea "Español", usamos la siguiente consulta:
  ```sql
  SELECT COUNT(language) AS count_spanish
  FROM films
  WHERE language = 'Spanish';
  ```

---

### **Orden de Ejecución en SQL**

Es importante recordar que aunque escribamos las consultas en el orden **SELECT, FROM, WHERE, LIMIT**, SQL ejecuta las cláusulas en un orden diferente. Primero identifica la tabla (**FROM**), luego filtra los datos (**WHERE**), y finalmente selecciona los resultados (**SELECT**) y los limita (**LIMIT**).

- Orden de escritura:  
  ```sql
  SELECT title  
  FROM films  
  WHERE release_year > 2000  
  LIMIT 5;
  ```
- Orden de ejecución:  
  1. **FROM**
  2. **WHERE**
  3. **SELECT**
  4. **LIMIT**

---

### **Conclusión**

La cláusula **WHERE** es una herramienta poderosa que nos permite filtrar tanto números como texto. Esta funcionalidad es crucial para responder preguntas detalladas y específicas sobre nuestros datos.

Es hora de practicar estas técnicas en la siguiente sección. ¡Manos a la obra!