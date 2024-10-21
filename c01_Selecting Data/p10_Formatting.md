### Ejercicio: **Formateo en SQL**

---

**Descripción**

En este ejercicio aprenderás a corregir código SQL mal escrito para que cumpla con los estándares de estilo adecuados. Es fundamental que el código sea legible y claro, ya que en un entorno profesional, es probable que otras personas necesiten comprender tu código o explicarlo.

---

### **Instrucciones**

1. **Ajustar el código de ejemplo**: Corrige el código dado para que esté en línea con las mejores prácticas de SQL, según lo discutido en la lección.

```sql
-- Reescribe esta consulta con formato adecuado
SELECT 
    person_id, 
    role 
FROM 
    roles 
LIMIT 
    10;
```

---

### **Explicación**

1. **Capitalización de palabras clave**: 
   - Las palabras clave **SELECT**, **FROM**, y **LIMIT** están en mayúsculas, lo cual sigue las mejores prácticas y mejora la legibilidad.
   
2. **Separar cada campo seleccionado en una nueva línea**: 
   - Escribir cada columna en su propia línea hace que sea más fácil agregar o eliminar columnas en futuras modificaciones.

3. **Indentación y líneas en blanco**:
   - Utilizar sangría para los campos y separar bloques de código (como las palabras clave y las tablas) en diferentes líneas facilita la lectura y el mantenimiento del código.

Este formato es más claro y sigue las mejores prácticas, lo que lo hace fácil de entender y modificar en el futuro.