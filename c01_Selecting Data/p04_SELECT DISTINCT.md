### **Consulta SQL con `COUNT()`**

En este ejercicio hemos aprendido cómo usar la función `COUNT()` para contar registros en una tabla o contar valores específicos en un campo.

---

#### **Consulta para contar el número de registros con `film_id`:**
```sql
SELECT COUNT(film_id) AS count_film_id
FROM reviews;
```

**Explicación:**
- **`COUNT(film_id)`**: La función `COUNT` cuenta cuántos registros tienen un valor en el campo `film_id`.
- **Alias**: Se usa el alias `count_film_id` para que el resultado sea más fácil de leer.

**Respuesta correcta:** Esta consulta devuelve **el número de registros que contienen un `film_id`** en la tabla `reviews`.

---

### **Práctica con `COUNT()`**

Aquí hemos utilizado la función `COUNT()` de diferentes maneras para contar registros en varias tablas.

#### **Instrucción 1/3: Contar el número total de registros en la tabla `people`:**

```sql
SELECT COUNT(*) AS count_records
FROM people;
```

**Explicación:**
- **`COUNT(*)`**: Contamos el número total de registros en la tabla `people`, sin importar si un campo específico tiene valores nulos o no.
- **Alias**: El resultado se almacena en `count_records` para hacerlo más legible.

**Resultado:** 8397 registros.

---

#### **Instrucción 2/3: Contar los registros que tienen un valor en el campo `birthdate` en la tabla `people`:**

```sql
SELECT COUNT(birthdate) AS count_birthdate
FROM people;
```

**Explicación:**
- **`COUNT(birthdate)`**: Aquí contamos cuántos registros tienen un valor en el campo `birthdate`. Si un registro no tiene una fecha de nacimiento, no se contará.
- **Alias**: El resultado se almacena en `count_birthdate`.

**Resultado:** 6152 registros con fechas de nacimiento.

---

#### **Instrucción 3/3: Contar registros de idiomas y países en la tabla `films`:**

```sql
SELECT COUNT(language) AS count_languages, COUNT(country) AS count_countries
FROM films;
```

**Explicación:**
- **`COUNT(language)`**: Contamos cuántos registros tienen un valor en el campo `language` (idioma).
- **`COUNT(country)`**: Contamos cuántos registros tienen un valor en el campo `country` (país).
- **Alias**: Los resultados se almacenan en `count_languages` y `count_countries`.

**Resultado:** 
- Idiomas: 4957
- Países: 4966

---

### **Uso de `DISTINCT` en SQL**

El comando **`DISTINCT`** se utiliza para eliminar valores duplicados en los resultados de una consulta.

#### **Instrucción 1/2: Seleccionar los países únicos en la tabla `films`:**

```sql
SELECT DISTINCT country
FROM films;
```

**Explicación:**
- **`DISTINCT`**: Este comando asegura que los resultados solo muestren valores únicos en el campo `country`.

---

#### **Instrucción 2/2: Contar los países únicos en la tabla `films`:**

```sql
SELECT COUNT(DISTINCT country) AS count_distinct_countries
FROM films;
```

**Explicación:**
- **`COUNT(DISTINCT country)`**: Contamos cuántos países únicos están presentes en la tabla `films`.
- **Alias**: El resultado se almacena en `count_distinct_countries`.

**Resultado:** 64 países únicos.