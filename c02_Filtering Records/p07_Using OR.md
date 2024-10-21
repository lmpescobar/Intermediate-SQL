### Actividad de la lección "Using OR"

---

#### Instrucción 1/3
**Enunciado:**
Este ejercicio te pedirá escribir una consulta para obtener el `título` y el `año de lanzamiento` de películas lanzadas en 1990 o 1999, que estén en inglés o español, y que hayan recaudado más de $2,000,000 de *gross*.

Parece mucho, pero puedes construir la consulta paso a paso para familiarizarte con el concepto subyacente en cada paso. ¡Empecemos!

**Instrucción:**
Selecciona el `título` y el `año de lanzamiento` de películas lanzadas en 1990 o 1999 usando solo `WHERE` y `OR`.

---

**Código SQL incorrecto:**  
```sql
-- Find the title and year of films from the 1990 or 1999
SELECT title, release_year
FROM films
WHERE release_year = 1990
OR release_year = 1999;
```

**Explicación del código:**
- Este código filtra películas lanzadas en los años 1990 o 1999 usando el operador `OR`. Este operador evalúa si alguna de las condiciones es verdadera.
- La consulta busca en la tabla `films` por el `release_year` y devuelve aquellas cuyo año de lanzamiento es 1990 o 1999.
  
---  

#### Instrucción 2/3
**Enunciado:**
Filtra los registros para incluir solo películas en inglés o español.

---

**Código SQL corregido:**
```sql
-- Find the title and year of films from the 1990 or 1999
SELECT title, release_year
FROM films
WHERE (release_year = 1990 OR release_year = 1999)
  AND (language = 'English' OR language = 'Spanish');
```

**Explicación del código:**
- Aquí hemos agregado un segundo filtro. Además del año de lanzamiento (`release_year`), hemos incluido el filtro para que solo devuelva películas en inglés o español.
- Usamos `AND` para combinar estas dos condiciones (año de lanzamiento y lenguaje), asegurando que ambas se cumplan.

---

#### Instrucción 3/3
**Enunciado:**
Finalmente, restringe la consulta para que solo retorne películas que hayan recaudado más de $2,000,000 en *gross*.

---

**Código SQL final:**
```sql
-- Find the title and year of films from the 1990 or 1999
SELECT title, release_year
FROM films
WHERE (release_year = 1990 OR release_year = 1999)
  AND (language = 'English' OR language = 'Spanish')
  AND (gross > 2000000);
```

**Explicación del código:**
- El último filtro añade una condición sobre el *gross* de la película, asegurando que la recaudación sea mayor a $2,000,000.
- El uso de `AND` sigue uniendo las condiciones lógicas para filtrar solo los resultados que cumplen con todos los criterios: año, idioma y recaudación.

---

### Conclusión:
- En este ejercicio, utilizamos operadores como `OR`, `AND`, y condiciones lógicas para filtrar registros de una tabla SQL de manera más específica.
- Aprendimos a aplicar múltiples criterios de búsqueda para obtener resultados precisos y relevantes.