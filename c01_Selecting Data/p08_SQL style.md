### Masterclass: **Estilo y Formato en SQL**

---

**Introducción**

¡Gran trabajo hasta ahora! Entendemos cómo funciona SQL, ahora vamos a profundizar en **cómo debería verse** nuestro código SQL. Aunque SQL es flexible en cuanto al formato, seguir algunas mejores prácticas hará que nuestras consultas sean más legibles y fáciles de mantener, especialmente en equipos de trabajo.

---

### **Formato en SQL: Libertad y Flexibilidad**

SQL no requiere que utilicemos saltos de línea, mayúsculas o sangrías, como ocurre en otros lenguajes de programación. Por ejemplo, el siguiente código que selecciona los primeros tres títulos, años de estreno y países de la tabla `films` funcionará perfectamente:

```sql
SELECT title, release_year, country FROM films LIMIT 3;
```

Sin embargo, escribir consultas como esta puede dificultar la lectura a medida que las consultas se vuelven más complejas. Mantener un estilo claro es importante para la legibilidad y colaboración.

---

### **Mejores Prácticas en el Estilo SQL**

Con el tiempo, los usuarios de SQL han desarrollado estándares de estilo aceptados en la industria. En lugar de escribir todo en una línea, una consulta bien formateada se ve así:

```sql
SELECT 
    title, 
    release_year, 
    country 
FROM films 
LIMIT 3;
```

Aquí, las palabras clave (`SELECT`, `FROM`, `LIMIT`) están en mayúsculas y cada campo está en una nueva línea, lo que facilita su lectura.

---

### **Guías de Estilo SQL: Consistencia y Claridad**

Existen diferentes enfoques para el formato de SQL. Algunos usuarios prefieren **sangrar** cada campo seleccionado en una nueva línea cuando se seleccionan múltiples campos, como en el siguiente ejemplo:

```sql
SELECT 
    title, 
    release_year, 
    country 
FROM films;
```

Esta organización ayuda a mantener las consultas estructuradas y fáciles de entender, especialmente en equipos grandes o al trabajar en proyectos a largo plazo.

---

### **La Importancia del Punto y Coma**

En PostgreSQL, el punto y coma (`;`) no es obligatorio al final de una consulta, pero es una **buena práctica** incluirlo. ¿Por qué? Algunas otras versiones de SQL, como SQL Server, requieren el punto y coma, y además, al usarlo, facilitamos la migración de nuestro código a otros sabores de SQL. También, como en una oración, el punto y coma indica el final de la consulta.

---

### **Manejando Nombres de Campos No Estándar**

A veces, encontramos tablas creadas por otras personas con **nombres de campos no estándar** que incluyen espacios. Aunque esto no es recomendable, podemos seguir trabajando con esos nombres de campos envolviéndolos en comillas dobles. Por ejemplo, si alguien hubiera creado un campo llamado `release year` en lugar de `release_year`, la consulta correcta sería:

```sql
SELECT "release year" 
FROM films;
```

Este formato indica que, a pesar del espacio, estamos refiriéndonos a un solo campo.

---

### **¿Por Qué Formatear el Código SQL?**

Seguir las guías de estilo de SQL es importante para facilitar la **colaboración** entre pares. Tener un código claro y legible no solo es valorado en la comunidad profesional, sino que también hace que sea más fácil depurar y entender nuestras consultas en el futuro.

---

### **Conclusión**

Formatear el código de manera legible y clara es un paso esencial para trabajar de manera eficiente con SQL. Si seguimos estas guías, nos aseguramos de que nuestro código sea fácil de leer, mantener y compartir con otros, mejorando la colaboración en entornos profesionales. ¡Es hora de poner en práctica lo aprendido!

---

**¡Ahora, a practicar y mejorar el estilo de nuestras consultas SQL!**