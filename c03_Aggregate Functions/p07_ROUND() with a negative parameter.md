En este ejercicio, se está utilizando la función `ROUND()` con un parámetro negativo para redondear el promedio del presupuesto de las películas a los **miles más cercanos**. Aquí está la explicación detallada:

### Código SQL:
```sql
-- Calcular el presupuesto promedio redondeado a los miles
SELECT ROUND(AVG(budget), -3) AS avg_budget_thousands
FROM films;
```

### Explicación:
1. **AVG(budget)**: Calcula el **promedio** de la columna `budget` en la tabla `films`. Este valor representa el presupuesto promedio de todas las películas presentes en la base de datos.

2. **ROUND(AVG(budget), -3)**: Utiliza la función `ROUND()` para redondear el valor del promedio calculado al número más cercano en miles. 
   - El segundo parámetro **-3** indica que se debe redondear a **tres posiciones a la izquierda** del punto decimal, lo que significa que estamos redondeando a los **miles** más cercanos. Por ejemplo, si el promedio es 3,903,000, será redondeado a esa cantidad exacta.

3. **AS avg_budget_thousands**: Se asigna un **alias** al resultado de la columna, lo que facilita su interpretación al nombrarla como `avg_budget_thousands`, lo que indica que el valor está expresado en miles de dólares.

### Contexto adicional sobre `ROUND()` con un parámetro negativo:
Este método de redondeo es útil cuando deseas obtener una visión general más simplificada de los datos financieros sin preocuparte por detalles pequeños, como centavos o unidades. En este caso, dado que los presupuestos de películas tienden a ser grandes, tiene más sentido mostrar la cantidad en miles para tener una mejor perspectiva.