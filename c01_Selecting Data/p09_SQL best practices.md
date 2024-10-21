### SQL Best Practices

Es importante seguir una guía de estilo en SQL para garantizar que el código sea fácil de leer y mantener. Estas prácticas están basadas en la guía de estilo de Holywell y otros estándares comunes en la comunidad SQL.

### Buenas Prácticas
1. **Capitalizar las palabras clave**: Las palabras clave SQL como `SELECT`, `FROM`, y `WHERE` deben estar en mayúsculas para que sean fácilmente distinguibles de los nombres de tablas y columnas.
2. **Usar guiones bajos en los nombres de los campos en lugar de espacios**: Es mejor usar nombres como `first_name` o `last_name` en lugar de usar espacios, lo que podría generar errores.
3. **Finalizar las consultas con punto y coma**: Aunque PostgreSQL no requiere un punto y coma al final de una consulta, otras bases de datos como SQL Server sí lo hacen. Terminar la consulta con `;` facilita la migración de consultas entre diferentes sistemas.

### Malas Prácticas
1. **No capitalizar las palabras clave**: Esto hace que el código sea más difícil de leer.
2. **Escribir múltiples consultas sin punto y coma**: No cerrar correctamente las consultas puede crear problemas cuando se trabaja con más de una consulta en un archivo o en sistemas que lo requieran.
3. **Escribir la consulta en una sola línea**: Aunque el SQL permite escribir consultas en una sola línea, esto hace que sea más complicado leer y entender el código, especialmente cuando las consultas son largas o complejas.