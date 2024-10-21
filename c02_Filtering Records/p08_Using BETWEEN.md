### 1. **Instrucción 1/4**: Filtrando por un rango de años usando `BETWEEN`

#### Código SQL:
```sql
-- Select the title and release_year for films released between 1990 and 2000
SELECT title, release_year
FROM films
WHERE release_year BETWEEN 1990 AND 2000;
```

#### Explicación:
En este caso, estamos utilizando la cláusula `BETWEEN` para seleccionar todas las películas lanzadas entre 1990 y 2000, inclusive. Esta cláusula se usa con el operador `WHERE` para simplificar la consulta y devolver todas las filas cuyo año de lanzamiento esté dentro de ese rango.

---

### 2. **Instrucción 2/4**: Añadir filtro para películas con presupuesto mayor a $100 millones

#### Código SQL:
```sql
-- Narrow down your query to films with budgets > $100 million
SELECT title, release_year
FROM films
WHERE release_year BETWEEN 1990 AND 2000
AND budget > 100000000;
```

#### Explicación:
Aquí se añade un filtro adicional que selecciona solo las películas que tienen un presupuesto mayor a $100 millones. Esto se hace utilizando el operador `AND` para combinar las dos condiciones: el rango de años (`BETWEEN`) y el filtro de presupuesto (`budget > 100000000`).

---

### 3. **Instrucción 3/4**: Restringir la consulta para que solo devuelva películas en español

#### Código SQL:
```sql
-- Restrict the query to only Spanish-language films
SELECT title, release_year
FROM films
WHERE release_year BETWEEN 1990 AND 2000
AND budget > 100000000
AND language = 'Spanish';
```

#### Explicación:
Ahora se restringe la consulta solo a películas que estén en español (`language = 'Spanish'`). Se sigue utilizando el operador `AND` para asegurar que todas las condiciones (rango de años, presupuesto y idioma) se cumplan simultáneamente.

---

### 4. **Instrucción 4/4**: Incluir películas en español o francés con los mismos criterios

#### Código SQL:
```sql
-- Amend the query to include Spanish or French-language films
SELECT title, release_year
FROM films
WHERE release_year BETWEEN 1990 AND 2000
AND budget > 100000000
AND (language = 'Spanish' OR language = 'French');
```

#### Explicación:
En este último paso, se modifica la consulta para incluir películas en español o en francés. Para hacer esto, se utiliza el operador `OR` dentro de un paréntesis, indicando que la película puede estar en cualquiera de esos dos idiomas, siempre que cumpla con los criterios de año y presupuesto.

---

Este es un excelente ejemplo de cómo las cláusulas `WHERE`, `BETWEEN`, `AND`, y `OR` se combinan en SQL para filtrar datos en función de múltiples criterios. Esto ayuda a obtener resultados específicos, basados en diferentes parámetros en una sola consulta.