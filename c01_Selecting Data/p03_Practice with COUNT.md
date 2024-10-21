## **Practicando con COUNT()**

La función `COUNT()` en SQL nos dice cuántos registros hay en una tabla. Sin embargo, si deseas contar el número de valores **no nulos** en un campo específico, puedes usar `COUNT()` solo en ese campo.

En estos ejercicios, practicamos cómo contar registros con la función `COUNT()`, utilizando la tabla `people` y `films`.

### Instrucción 1/3: Contar todos los registros en una tabla

En este primer ejercicio, se pide contar el **total de registros** en la tabla `people`. Usamos la función `COUNT(*)` que cuenta todas las filas en la tabla, sin importar los valores en los campos. Además, usamos un alias (`count_records`) para nombrar el resultado de manera descriptiva.

```sql
-- Contar el número de registros en la tabla people
SELECT COUNT(*) AS count_records
FROM people;
```

**Resultado**: 
- El total de registros en la tabla es **8397**.

### Instrucción 2/3: Contar registros con valores no nulos en un campo específico

Ahora, contamos cuántos registros contienen un valor en el campo `birthdate` (fecha de nacimiento) en la tabla `people`. Esto significa contar solo los registros que no tienen valores nulos en ese campo específico.

```sql
-- Contar el número de registros que tienen una fecha de nacimiento en la tabla people
SELECT COUNT(birthdate) AS count_birthdate
FROM people;
```

**Resultado**: 
- El número de registros con una fecha de nacimiento es **6152**.

### Instrucción 3/3: Contar registros en dos campos diferentes

En este último ejercicio, contamos los registros de dos campos diferentes en la tabla `films`: `language` (idiomas) y `country` (países). Utilizamos dos funciones `COUNT()` para cada campo y les damos alias (`count_languages` y `count_countries`) para identificar los resultados fácilmente.

```sql
-- Contar los registros de idiomas y países representados en la tabla films
SELECT COUNT(language) AS count_languages, COUNT(country) AS count_countries
FROM films;
```

**Resultado**:
- El número de registros con un valor en el campo `language` es **4957**.
- El número de registros con un valor en el campo `country` es **4966**.

---

### Explicación Adicional:

- **COUNT(*)**: Se utiliza para contar el número total de registros en una tabla, sin importar si tienen valores nulos en algún campo.
- **COUNT(campo)**: Cuenta solo los registros que tienen un valor no nulo en el campo especificado. Esto es útil cuando queremos excluir los registros que tienen valores nulos.
- **Alias (`AS`)**: Nos permite renombrar los resultados de nuestras consultas para hacerlas más legibles y descriptivas. En los ejemplos anteriores, hemos usado alias como `count_records`, `count_birthdate`, `count_languages`, y `count_countries` para indicar claramente qué estamos contando.