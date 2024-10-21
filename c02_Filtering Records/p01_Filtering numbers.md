### Masterclass: **Filtrando Datos en SQL**

---

**Introducción**

¡Bienvenidos de nuevo! En esta clase continuaremos ampliando nuestro repertorio en SQL, pasando de seleccionar y contar datos, a aprender a **filtrar** información específica en nuestras consultas. Esto nos permitirá enfocarnos en los datos más relevantes para nuestras preguntas empresariales o análisis.

---

### **La Cláusula WHERE: Filtrando Datos en SQL**

Para lograr este enfoque más selectivo, introducimos una nueva cláusula: **WHERE**. Esta cláusula es clave para filtrar los datos y enfocarnos solo en la información que realmente necesitamos. Siguiendo con el ejemplo de un armario de abrigos, si quisiéramos seleccionar un abrigo de color verde, **WHERE** sería el equivalente a filtrar los abrigos por color para obtener solo los verdes.

---

### **Uso de Operadores de Comparación con WHERE**

En esta lección nos centraremos en cómo filtrar números. Para ello, empleamos **operadores de comparación** como "mayor que" o "menor que". Un ejemplo común sería filtrar para ver solo películas lanzadas **después del año 1960** usando el operador "mayor que":

```sql
SELECT title, release_year
FROM films
WHERE release_year > 1960;
```

---

### **Otros Operadores de Comparación**

A continuación, revisamos otros operadores de comparación que podemos utilizar con la cláusula WHERE:

1. **Menor que**: Si quisiéramos ver películas lanzadas **antes de 1960**, usaríamos el operador "<":

   ```sql
   SELECT title, release_year
   FROM films
   WHERE release_year < 1960;
   ```

2. **Menor o igual que**: Para ver películas lanzadas **durante o antes de 1960**, podemos utilizar el operador "<=":

   ```sql
   SELECT title, release_year
   FROM films
   WHERE release_year <= 1960;
   ```

3. **Igual a**: Para buscar películas lanzadas en un año específico, por ejemplo, **en 1960**:

   ```sql
   SELECT title, release_year
   FROM films
   WHERE release_year = 1960;
   ```

4. **Diferente a**: Si queremos excluir un año específico, digamos **excluir las películas lanzadas en 1960**, combinamos los símbolos de "mayor que" y "menor que", que es el estándar SQL para **"diferente de"**:

   ```sql
   SELECT title, release_year
   FROM films
   WHERE release_year <> 1960;
   ```

---

### **Resumen de los Operadores de Comparación**

En resumen, estos son los operadores de comparación que podemos usar junto con **WHERE** para filtrar datos numéricos en SQL:

- **>** (mayor que / después de)
- **<** (menor que / antes de)
- **=** (igual a)
- **>=** (mayor o igual a)
- **<=** (menor o igual a)
- **<>** (diferente de / excluir un valor específico)

---

### **Uso de WHERE con Cadenas de Texto**

La cláusula **WHERE** también se puede utilizar con cadenas de texto, en combinación con el operador de igualdad (=). En este caso, necesitamos incluir las cadenas de texto entre comillas simples. Por ejemplo, si queremos filtrar títulos donde el país es **Japón**:

```sql
SELECT title, country
FROM films
WHERE country = 'Japan';
```

---

### **Orden de Ejecución en SQL**

Es importante tener en cuenta el **orden de ejecución** en SQL. Aunque escribimos las consultas en el orden `SELECT`, `FROM`, `WHERE`, `LIMIT`, el motor de SQL ejecuta los pasos en un orden ligeramente diferente:

1. Primero selecciona la tabla con **FROM**.
2. Luego aplica los filtros con **WHERE**.
3. A continuación selecciona los campos con **SELECT**.
4. Por último, limita los resultados con **LIMIT** (si se incluye).

Un buen ejemplo de esto es pensar en la selección de abrigos: primero vamos al armario correcto (**FROM**), luego encontramos los abrigos verdes (**WHERE**), seleccionamos los detalles de esos abrigos (**SELECT**) y finalmente elegimos solo los primeros cinco abrigos (**LIMIT**).

---

### **¡Es Hora de Practicar!**

Ahora que hemos aprendido a usar **WHERE** para filtrar nuestros datos de manera precisa, es hora de poner en práctica este conocimiento. Intenta escribir tus propias consultas y experimenta con los diferentes operadores para obtener los datos más relevantes.

¡Vamos a practicar!