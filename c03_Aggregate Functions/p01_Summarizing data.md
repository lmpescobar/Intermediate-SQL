### **1. Introducción a la Resumen de Datos**

Cuando analizamos datos, a menudo no solo nos interesa cada registro individual, sino también una visión general del conjunto de datos. Para ello, podemos usar las **funciones agregadas de SQL**, que calculan valores a partir de varias filas y devuelven un único resultado.

**Definición**: Las funciones agregadas en SQL nos permiten realizar operaciones como encontrar promedios, sumas, mínimos y máximos de campos específicos de una tabla.

---

### **2. Funciones agregadas principales en SQL**

#### **COUNT()**
Esta función ya la hemos usado antes. Nos permite contar la cantidad de valores en un campo. Por ejemplo:

```sql
SELECT COUNT(*)
FROM films;
```

Este comando contaría el número total de películas en la tabla `films`.

#### **AVERAGE (AVG())**
Encuentra el valor promedio de un campo numérico. Si quisiéramos saber el presupuesto promedio de las películas, utilizaríamos:

```sql
SELECT AVG(budget) 
FROM films;
```

Esto devolvería el presupuesto promedio de todas las películas en la tabla.

#### **SUM()**
Suma todos los valores en un campo. Si queremos saber el presupuesto total de todas las películas:

```sql
SELECT SUM(budget)
FROM films;
```

Esta consulta sumaría todos los valores del campo `budget`, dándonos el presupuesto total.

#### **MIN()**
Devuelve el valor mínimo en un campo. Para encontrar la película con el presupuesto más bajo:

```sql
SELECT MIN(budget)
FROM films;
```

Esto devolvería el valor más bajo en el campo de presupuesto.

#### **MAX()**
Devuelve el valor más alto en un campo. Si quisiéramos saber cuál es el presupuesto más alto de una película:

```sql
SELECT MAX(budget)
FROM films;
```

Este comando nos devolvería el presupuesto más alto.

---

### **3. Uso de funciones agregadas con datos no numéricos**

Aunque las funciones como `AVG()` y `SUM()` solo funcionan con números, otras funciones como `COUNT()`, `MIN()`, y `MAX()` también pueden ser usadas con campos no numéricos.

**Ejemplos:**
- Podemos usar `MIN()` y `MAX()` con campos de texto para obtener el valor alfabéticamente más bajo y más alto.
  
```sql
SELECT MIN(country), MAX(country)
FROM films;
```

Esto devolvería el país que aparece primero y el último en orden alfabético.

#### **Nota**:
- **MIN()** y **MAX()** con fechas devolverán la fecha más antigua y la más reciente, respectivamente.
- **COUNT()** nos permite contar la cantidad de registros no nulos en un campo, sin importar el tipo de datos.

---

### **4. Buenas prácticas: Uso de alias en funciones agregadas**

Cuando usamos funciones agregadas, el nombre del campo de resultado cambiará automáticamente al nombre de la función aplicada (por ejemplo, `min` o `max`). Para hacer los resultados más legibles, es una buena práctica usar **alias** con `AS` para renombrar las columnas de resultado.

```sql
SELECT MAX(budget) AS highest_budget
FROM films;
```

Esto hará que el resultado muestre `highest_budget` en lugar de `MAX(budget)` en la columna de resultado.

---

### **Conclusión**

Las funciones agregadas son esenciales para resumir grandes cantidades de datos y obtener una comprensión general del conjunto. Aprendimos cómo usar `COUNT()`, `AVG()`, `SUM()`, `MIN()`, y `MAX()` tanto con datos numéricos como no numéricos. También vimos la importancia de usar alias para hacer nuestros resultados más comprensibles.

¡Ahora es el momento de practicar!