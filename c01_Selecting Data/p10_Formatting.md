### Ejercicio: **Formateo de Consultas SQL**

---

**Descripción**

El código SQL debe seguir un formato legible y estructurado para facilitar su comprensión, especialmente en ambientes colaborativos o profesionales. Sin un buen formateo, el código puede ser difícil de entender y mantener.

---

### Instrucciones:

1. Corrige el código proporcionado para que cumpla con los **estándares de formateo** adecuados.

---

#### **Código con mal formateo**:

```sql
select person_id, role from roles limit 10
```

---

#### **Código con buen formateo**:

```sql
-- Reescribe esta consulta
SELECT person_id, role
FROM roles
LIMIT 10;
```

---

### **Explicación del código**

1. **SELECT person_id, role**  
   Selecciona las columnas `person_id` y `role` de la tabla.
   
2. **FROM roles**  
   Indica que los datos provienen de la tabla `roles`.
   
3. **LIMIT 10**  
   Limita los resultados a las primeras 10 filas.

---

### **Mejoras en el Formateo**

- **Palabras clave en mayúsculas**: Se utiliza mayúsculas en `SELECT`, `FROM` y `LIMIT`, lo cual es una buena práctica en SQL.
- **Separación en líneas**: Cada palabra clave importante tiene su propia línea para mejorar la legibilidad.
- **Punto y coma al final**: Añadir un punto y coma al final es recomendable para indicar el final de la consulta y evitar errores en sistemas que lo requieren.

Este es el formato adecuado para escribir consultas SQL claras, manteniendo el código ordenado y fácil de leer para cualquier desarrollador.