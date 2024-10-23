Esta lección cubre el uso de **aritmética** y **aliasing** en SQL, brindando una visión general sobre cómo puedes realizar cálculos básicos y mejorar la legibilidad de los resultados usando alias. Vamos a profundizar en los puntos clave que cubriste en el resumen.

### Aritmética en SQL
SQL permite realizar operaciones matemáticas básicas como:
- **Suma**: Utilizando el símbolo `+`.
- **Resta**: Utilizando el símbolo `-`.
- **Multiplicación**: Utilizando el símbolo `*`.
- **División**: Utilizando el símbolo `/`.

Un aspecto importante de SQL es el uso de **paréntesis** para definir el orden de las operaciones, especialmente en consultas que involucran varias operaciones aritméticas.

#### Ejemplo básico:
```sql
SELECT 5 + 3 AS suma, 10 - 4 AS resta, 2 * 6 AS multiplicacion, 10 / 2 AS division;
```
Este ejemplo devuelve los resultados de sumar, restar, multiplicar y dividir. Los paréntesis no son necesarios aquí, ya que solo hay una operación por cálculo, pero añaden claridad a consultas más complejas.

### Precisión en la división
Cuando realizamos una **división entre enteros**, SQL devolverá un **entero**. Esto significa que si divides `10 / 3`, el resultado será `3`, no `3.33`. Para evitar esto y obtener más precisión, puedes convertir los números a decimales.

#### Ejemplo de precisión:
```sql
SELECT 4.0 / 3.0 AS division_con_decimales;
```
El resultado será `1.3333` en lugar de `1`, debido a que ambos números ahora son decimales.

### Funciones agregadas vs. Aritmética
- **Funciones agregadas** como `SUM()` o `AVG()` operan **verticalmente** sobre todos los registros en una columna.
- Las **operaciones aritméticas** entre columnas en SQL se realizan **horizontalmente** por fila.

Por ejemplo:
```sql
SELECT SUM(budget) AS total_budget FROM films;
```
Aquí, `SUM()` opera sobre la columna `budget` sumando todos los presupuestos.

### Alias en operaciones aritméticas
Cuando utilizas operaciones aritméticas en SQL, es buena práctica asignar **alias** usando la palabra clave `AS`. Los alias permiten darle un nombre más comprensible a la columna calculada.

#### Ejemplo de alias:
```sql
SELECT gross - budget AS profit FROM films;
```
En este ejemplo, calculamos las ganancias (`profit`) restando el presupuesto (`budget`) del ingreso bruto (`gross`), y le asignamos un alias a la nueva columna calculada para que sea más claro.

### Importancia del alias con funciones
Cuando usamos funciones como `MAX()` en una consulta compleja que devuelve varios resultados, es crucial asignar alias para evitar ambigüedad en los nombres de las columnas. Esto asegura que los resultados sean fácilmente legibles y comprensibles.

#### Ejemplo con múltiples alias:
```sql
SELECT MAX(budget) AS max_budget, MAX(gross) AS max_gross FROM films;
```
Asignamos alias diferentes (`max_budget` y `max_gross`) para evitar confusión.

### Orden de ejecución de las consultas
El **orden de ejecución** en SQL sigue la siguiente secuencia:
1. **FROM**: Define la tabla de origen.
2. **WHERE**: Filtra los datos antes de la selección.
3. **SELECT**: Elige las columnas a mostrar y realiza los cálculos.
4. **LIMIT**: Limita la cantidad de registros devueltos.

Es importante recordar que el alias no está disponible en la cláusula `WHERE`, ya que SQL aún no lo ha procesado en esa etapa.

#### Ejemplo:
Este código generaría un error porque el alias `profit` no está disponible en la cláusula `WHERE`:
```sql
SELECT gross - budget AS profit 
FROM films
WHERE profit > 1000000;
```
### Resumen
- Puedes realizar operaciones aritméticas básicas en SQL para obtener resultados directamente de los datos.
- Usa alias para hacer que tus resultados sean más claros y legibles.
- Recuerda que SQL sigue un orden de ejecución, por lo que los alias no se pueden usar en `WHERE`.
- Cuando realices múltiples cálculos, asignar alias es clave para evitar confusión.

Ahora que entiendes cómo combinar aritmética y aliasing, ¡es momento de ponerlo en práctica!