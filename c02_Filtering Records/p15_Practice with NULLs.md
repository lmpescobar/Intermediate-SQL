### **Título: Práctica con valores nulos (NULLs)**

---

#### **Descripción:**

Los valores nulos (NULL) en SQL representan datos faltantes o desconocidos, y son esenciales para entender y manejar bases de datos en el mundo real, ya que estos valores pueden afectar el análisis de los datos. En este ejercicio, explorarás cómo trabajar con estos valores en la tabla `films`.

---

### **Instrucciones:**

#### **1. Listar los títulos de películas que no tienen información de presupuesto.**
1. **Código SQL:**
```sql
-- Listar los títulos de las películas que no tienen información de presupuesto
SELECT title AS no_budget_info
FROM films
WHERE budget IS NULL;
```

**Explicación:**
- **SELECT title**: Selecciona los títulos de las películas.
- **AS no_budget_info**: Asigna un alias (nombre) a la columna de resultados para que aparezca como `no_budget_info`.
- **FROM films**: Obtiene los datos de la tabla `films`.
- **WHERE budget IS NULL**: Filtra las películas que no tienen información de presupuesto (presupuesto nulo).

Este código selecciona los títulos de todas las películas que tienen un valor nulo en el campo de presupuesto. El alias `no_budget_info` hace que los resultados sean más comprensibles al renombrar la columna.

#### **Resultado esperado:**
- Los títulos de las películas con presupuestos faltantes aparecerán listados en la columna con el alias `no_budget_info`.

---

#### **2. Contar la cantidad de películas con un idioma asociado.**
1. **Código SQL:**
```sql
-- Contar la cantidad de películas con datos sobre el idioma
SELECT COUNT(*) AS count_language_known
FROM films
WHERE language IS NOT NULL;
```

**Explicación:**
- **SELECT COUNT(*)**: Utiliza la función `COUNT()` para contar el número total de registros (películas).
- **AS count_language_known**: Asigna un alias para que el resultado aparezca bajo el nombre `count_language_known`.
- **FROM films**: Los datos son obtenidos de la tabla `films`.
- **WHERE language IS NOT NULL**: Filtra para que solo se incluyan las películas que tienen un valor no nulo en el campo de idioma (`language`).

Este código cuenta todas las películas que tienen información de idioma disponible, excluyendo aquellas que tienen un valor nulo en el campo `language`.

#### **Resultado esperado:**
- El resultado será un solo valor numérico, que indica cuántas películas tienen un idioma registrado.

---

**Conclusión:**

Trabajar con valores nulos es crucial en la manipulación y análisis de datos, ya que en la mayoría de los conjuntos de datos del mundo real, algunos valores estarán ausentes debido a errores humanos o a la falta de información. Con estos ejercicios, hemos aprendido a identificar las películas con presupuestos faltantes y a contar cuántas tienen información sobre el idioma.