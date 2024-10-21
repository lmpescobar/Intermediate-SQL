### Transcripción y Explicación

#### Ejercicio: **Debugging Errors**

---

En este ejercicio estamos aprendiendo a **depurar** código SQL, una habilidad fundamental para identificar y corregir errores comunes. A continuación, transcribo y explico cada una de las tres consultas SQL con sus respectivos errores y cómo solucionarlos.

---

### Instrucciones 1/3

- **Objetivo**: Depurar y corregir el código SQL proporcionado.

**Código Incorrecto:**
```sql
-- Debug this code
SELECT certification 
FROM films 
LIMIT 5;
```

**Errores Identificados**:
1. **Falta de campo válido**: El campo "certification" no está presente en la tabla `films`. Debemos cambiarlo por un campo que sí exista, como `title`.
  
**Código Corregido**:
```sql
-- Debug this code
SELECT title 
FROM films 
LIMIT 5;
```

**Explicación**:
- Se cambió `certification` por `title`, que es un campo válido en la tabla `films`. El error se produjo debido a la referencia a un campo inexistente.

---

### Instrucciones 2/3

- **Objetivo**: Encontrar y corregir dos errores en este código. El mismo error se ha repetido dos veces.

**Código Incorrecto:**
```sql
-- Debug this code
SELECT film_id imdb_score num_votes 
FROM reviews;
```

**Errores Identificados**:
1. **Falta de coma**: Entre `film_id` y `imdb_score` falta una coma que separa los campos.
2. **Falta de coma**: También falta la coma entre `imdb_score` y `num_votes`.

**Código Corregido**:
```sql
-- Debug this code
SELECT film_id, imdb_score, num_votes 
FROM reviews;
```

**Explicación**:
- Se añadieron las comas faltantes para separar correctamente los campos `film_id`, `imdb_score`, y `num_votes`.

---

### Instrucciones 3/3

- **Objetivo**: Encontrar dos errores en esta consulta.

**Código Incorrecto:**
```sql
-- Debug this code
SELECT COUNNT(birthdate) AS count_birthdays 
FROM peeple;
```

**Errores Identificados**:
1. **Error de ortografía** en la función `COUNT`: Se escribió `COUNNT` en lugar de `COUNT`.
2. **Error en el nombre de la tabla**: La tabla se llama `people`, pero en el código está mal escrito como `peeple`.

**Código Corregido**:
```sql
-- Debug this code
SELECT COUNT(birthdate) AS count_birthdays 
FROM people;
```

**Explicación**:
- Se corrigió la ortografía de la función `COUNT` y el nombre de la tabla `people`.

---

### Conclusión

Este ejercicio nos ayudó a practicar cómo identificar y solucionar errores comunes en consultas SQL, como errores tipográficos en palabras clave y campos, así como la importancia de las comas para separar correctamente los campos en una selección.