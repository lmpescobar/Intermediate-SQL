### 1. **Filtrar texto**
Hasta ahora hemos trabajado principalmente con números, pero es importante saber que también podemos usar la cláusula `WHERE` para filtrar texto. Hasta ahora hemos especificado texto exacto, pero en muchos casos queremos filtrar con base en patrones.

### 2. **Introducción a LIKE, NOT LIKE, e IN**
En SQL, hay operadores que nos permiten buscar patrones de texto y no solo coincidencias exactas. Estos operadores son:
- `LIKE`: Se usa para buscar coincidencias parciales o patrones en cadenas de texto.
- `NOT LIKE`: Es lo opuesto, filtra aquellos registros que no coinciden con el patrón dado.
- `IN`: Permite simplificar la búsqueda de múltiples valores en un campo.

### 3. **Uso de LIKE**
El operador `LIKE` se combina con `WHERE` para buscar patrones en los campos de texto. Utiliza **comodines** para representar valores variables:
- **Porcentaje (%)**: Coincide con cero, uno o muchos caracteres.
    - Ejemplo: `WHERE name LIKE 'A%'` buscaría todos los nombres que comienzan con "A", como *Adel*, *Adelaide*, *Aden*, etc.
- **Guión bajo (_)**: Coincide con un solo carácter.
    - Ejemplo: `WHERE name LIKE '_ve'` buscaría nombres como *Eve*, pero no *Eva* o *Evelyn*.

### 4. **Uso de NOT LIKE**
El operador `NOT LIKE` se utiliza para excluir los registros que coinciden con un patrón específico. Recuerda que `LIKE` y `NOT LIKE` son sensibles a mayúsculas y minúsculas, por lo que es importante considerar la forma exacta del texto que se está buscando.

### 5. **Posición de los comodines**
Puedes colocar los comodines `%` y `_` en cualquier posición:
- **Al inicio**: `'%r'` busca todos los nombres que terminan en "r".
- **En medio**: `'_t%'` busca todos los nombres cuyo tercer carácter sea "t".
- **En cualquier lugar**: Puedes colocar estos comodines donde sea necesario para encontrar patrones específicos.

### 6. **Uso de OR con WHERE**
Cuando queremos filtrar basándonos en varias condiciones, como años específicos o valores que no siguen un patrón predecible, podemos usar `OR`. Sin embargo, esto puede volverse complicado si hay muchas condiciones, por lo que SQL nos ofrece una alternativa más eficiente: el operador `IN`.

### 7. **Uso de IN**
El operador `IN` simplifica consultas con múltiples valores, por ejemplo:
```sql
WHERE release_year IN (1920, 1930, 1940)
```
Esto reemplaza múltiples condiciones `OR`, haciéndolo más legible y eficiente.

### 8. **IN con texto**
`IN` también se puede usar con texto. Por ejemplo, para buscar títulos donde el país asociado sea Alemania o Francia:
```sql
WHERE country IN ('Germany', 'France')
```
Esto te permite manejar conjuntos de valores sin necesidad de escribir múltiples `OR`.

### 9. **Práctica**
¡Ahora es momento de practicar! Aquí podemos aplicar todo lo que hemos aprendido usando `LIKE`, `NOT LIKE`, e `IN` para filtrar registros con texto, buscar patrones y manejar múltiples valores en un solo campo.

Espero que esta clase te haya dado claridad sobre cómo manejar datos textuales y patrones en SQL de manera eficiente. ¡Vamos a ponerlo en práctica!