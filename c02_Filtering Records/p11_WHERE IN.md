### Ejercicio y explicación detallada:

#### Instrucciones del ejercicio:

**Título: "WHERE IN"**

El enunciado indica que ahora conocemos el operador `IN`, el cual nos permite consultar múltiples condiciones dentro de un `WHERE` usando paréntesis. Es una herramienta valiosa para mantener nuestras consultas concisas. Se nos pide que practiquemos el uso de este operador.

#### Ejemplo de consultas y resultados:

**1.** Encuentra el título y el año de lanzamiento de todas las películas lanzadas en 1990 o 2000 que duren más de dos horas.

```sql
-- Encuentra el título y el año de lanzamiento de todas las películas lanzadas en 1990 o 2000 que duren más de dos horas
SELECT title, release_year
FROM films
WHERE release_year IN (1990, 2000)
AND duration > 120;
```

**Explicación**: 
- Utilizamos `IN` para filtrar aquellas películas lanzadas en los años 1990 o 2000.
- Luego, añadimos la condición `AND` para asegurarnos de que sólo se seleccionen las que tienen una duración superior a 120 minutos (dos horas).

---

**2.** Encuentra el título y el idioma de todas las películas en inglés, español o francés usando `IN`.

```sql
-- Encuentra el título y el idioma de todas las películas en inglés, español o francés
SELECT title, language
FROM films
WHERE language IN ('English', 'Spanish', 'French');
```

**Explicación**: 
- Aquí estamos filtrando por el campo `language` para devolver únicamente películas cuyo idioma sea inglés, español o francés.
- Usamos el operador `IN` para especificar múltiples valores que buscamos en la columna `language`, evitando múltiples condiciones `OR`.

---

**3.** Selecciona el título, certificación e idioma de todas las películas con clasificación NC-17 o R que estén en inglés, italiano o griego.

```sql
-- Encuentra el título, certificación e idioma de todas las películas con clasificación NC-17 o R y que estén en inglés, italiano o griego
SELECT title, certification, language
FROM films
WHERE certification IN ('NC-17', 'R')
AND language IN ('English', 'Italian', 'Greek');
```

**Explicación**: 
- Usamos `IN` para seleccionar películas clasificadas como `NC-17` o `R` y también las limitamos a los idiomas inglés, italiano o griego.
- Con la combinación de `IN` y `AND`, podemos aplicar varios criterios a la vez de manera limpia y eficiente.

---

Este conjunto de ejercicios nos ayuda a practicar el uso del operador `IN`, el cual es muy útil cuando necesitamos buscar múltiples valores dentro de una columna en lugar de escribir múltiples condiciones `OR`.