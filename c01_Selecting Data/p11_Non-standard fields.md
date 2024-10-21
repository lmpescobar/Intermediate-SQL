### Ejercicio: Manejo de campos no estándar

En esta imagen, se presenta un ejercicio sobre cómo manejar **nombres de campos no estándar** en SQL. En algunos casos, las bases de datos pueden contener campos con espacios o caracteres poco comunes, lo que requiere el uso de comillas dobles (`"`) para referenciar esos campos adecuadamente en las consultas.

---

**Problema planteado:**

Se ha proporcionado un esquema de la tabla **reviews**, y es necesario completar la consulta que devuelva tanto el `film_id` como el número de **likes** en Facebook para cada película. El campo en la base de datos que contiene este último dato está mal nombrado y contiene un espacio: `facebook likes`.

---

**Consulta proporcionada:**

```sql
SELECT film_id, --- 
FROM reviews;
```

En este caso, el campo `facebook likes` contiene un espacio, lo que requiere el uso de comillas dobles para que el campo se interprete como una sola unidad:

---

**Posible solución correcta:**

```sql
SELECT film_id, "facebook likes"
FROM reviews;
```

Al usar comillas dobles, la consulta reconoce correctamente `facebook likes` como el nombre completo del campo, lo que evita errores. Esto es una buena práctica cuando se enfrentan campos con nombres mal estructurados o no convencionales.