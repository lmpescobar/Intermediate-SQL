### **SQL - Uso de LIKE y NOT LIKE**

### Descripción:
Los operadores `LIKE` y `NOT LIKE` en SQL se utilizan para encontrar registros que coincidan (o no) con un patrón específico. Estos operadores se pueden combinar con comodines como `%` y `_`. El símbolo `%` se utiliza para coincidir con cero o más caracteres, mientras que `_` coincide con un solo carácter.

Este ejercicio nos ayudará a practicar cómo usar `LIKE` y `NOT LIKE` con diferentes patrones para filtrar datos textuales de forma eficiente.

---

### **Instrucciones del ejercicio:**

**Instrucción 1/3:**
1. Seleccionar los nombres de todas las personas cuyos nombres comienzan con 'B'.

**Instrucción 2/3:**
2. Seleccionar los nombres de personas cuyos nombres tienen 'r' como la segunda letra.

**Instrucción 3/3:**
3. Seleccionar los nombres de personas cuyos nombres no comienzan con 'A'.

---

### **Explicación del código paso a paso:**

1. **Primera consulta - Nombres que comienzan con 'B':**

```sql
-- Seleccionar los nombres que comienzan con 'B'
SELECT name
FROM people
WHERE name LIKE 'B%';
```

- **`SELECT name`**: Selecciona la columna `name` de la tabla.
- **`FROM people`**: La fuente de datos es la tabla `people`.
- **`WHERE name LIKE 'B%'`**: Aquí estamos utilizando el operador `LIKE` con el patrón `'B%'`. Esto significa que estamos buscando todos los nombres que comienzan con la letra 'B' y pueden tener cualquier combinación de caracteres después de la 'B', representados por el comodín `%`.

Resultado: Esto retornará nombres como "B.J. Novak", "Babak Najafi", entre otros.

---

2. **Segunda consulta - Nombres que tienen 'r' como segunda letra:**

```sql
-- Seleccionar los nombres que tienen 'r' como segunda letra
SELECT name
FROM people
WHERE name LIKE '_r%';
```

- **`LIKE '_r%'`**: Aquí, el uso del comodín `_` indica que buscamos nombres donde la segunda letra sea una 'r'. El carácter `_` coincide con exactamente un carácter, y el `%` indica cualquier número de caracteres después.

Resultado: Esta consulta devolverá nombres donde la segunda letra es 'r', como "Brad Pitt", "Chris Pratt", etc.

---

3. **Tercera consulta - Nombres que no comienzan con 'A':**

```sql
-- Seleccionar los nombres que no comienzan con 'A'
SELECT name
FROM people
WHERE name NOT LIKE 'A%';
```

- **`NOT LIKE 'A%'`**: En esta consulta, utilizamos `NOT LIKE` para excluir aquellos nombres que comienzan con 'A'. De esta manera, obtenemos los nombres que comienzan con cualquier otra letra.

Resultado: Se devolverán todos los nombres que no comienzan con 'A', como "B.J. Novak", "Babak Najafi", entre otros.

---

### **Reflexión sobre el uso de `LIKE` y `NOT LIKE`**:
- El operador `LIKE` es muy útil cuando se necesita buscar patrones en los datos textuales. Los comodines permiten hacer búsquedas flexibles para encontrar registros que cumplan con ciertos criterios.
- Es importante recordar que `NOT LIKE` se usa para excluir aquellos registros que coinciden con el patrón especificado.
- Ambos operadores son útiles en análisis de bases de datos donde los nombres, descripciones o cualquier dato textual requieren ser filtrados de manera precisa.