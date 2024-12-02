# XPath: Condicionales

En XPath, los **condicionales** son muy útiles para seleccionar nodos específicos que cumplen con ciertos criterios. Estos condicionales permiten filtrar nodos según su posición, atributos o valores dentro de un documento XML.

## Ejemplos de Condicionales en XPath

### 1. **Seleccionar el primer elemento `book` dentro de `bookstore`**

```xpath
/bookstore/book[1]
```

Esta expresión selecciona el primer elemento `<book>` que es hijo directo del elemento `<bookstore>`.

### 2. **Seleccionar el último elemento `book` dentro de `bookstore`**

```xpath
/bookstore/book[last()]
```

Esta expresión selecciona el último elemento `<book>` que es hijo directo de `<bookstore>`.

### 3. **Seleccionar el penúltimo elemento `book` dentro de `bookstore`**

```xpath
/bookstore/book[last()-1]
```

Esta expresión selecciona el penúltimo elemento `<book>` que es hijo directo de `<bookstore>`.

### 4. **Seleccionar los dos primeros elementos `book` dentro de `bookstore`**

```xpath
/bookstore/book[position()<3]
```

Esta expresión selecciona los dos primeros elementos `<book>` dentro de `<bookstore>`. El predicado `position()<3` filtra los nodos según su posición.

### 5. **Seleccionar todos los elementos `title` que tienen un atributo `lang`**

```xpath
//title[@lang]
```

Esta expresión selecciona todos los elementos `<title>` que tienen un atributo llamado `lang`, independientemente del valor del atributo.

### 6. **Seleccionar todos los elementos `title` con el atributo `lang` igual a "en"**

```xpath
//title[@lang='en']
```

Esta expresión selecciona todos los elementos `<title>` que tienen un atributo `lang` con el valor igual a `"en"`.

### 7. **Seleccionar los elementos `book` cuyo precio sea superior a 35.00**

```xpath
/bookstore/book[price>35.00]
```

Esta expresión selecciona todos los elementos `<book>` que tienen un elemento `<price>` cuyo valor es mayor que `35.00`.

### 8. **Seleccionar los títulos de los libros cuyo precio sea superior a 35.00**

```xpath
/bookstore/book[price>35.00]/title
```

Esta expresión selecciona todos los elementos `<title>` de los libros que tienen un `<price>` superior a `35.00`.

## Resumen de Condicionales en XPath

- **Posición**: Puedes usar `position()` para seleccionar nodos en una posición específica, como el primer, último o penúltimo nodo.
- **Atributos**: Puedes filtrar nodos por atributos utilizando la sintaxis `[@atributo]` o `[@atributo='valor']`.
- **Valores**: Puedes seleccionar nodos basados en los valores de otros nodos, como el valor de un precio o cualquier otro dato contenido en el nodo.

## Ejemplo de Documento XML

Supongamos que tenemos el siguiente documento XML:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<bookstore>
  <book>
    <title lang="en">Harry Potter</title>
    <price>29.99</price>
  </book>
  <book>
    <title lang="es">El Alquimista</title>
    <price>19.99</price>
  </book>
  <book>
    <title lang="en">Learning XML</title>
    <price>39.95</price>
  </book>
  <book>
    <title lang="en">XPath for Beginners</title>
    <price>45.00</price>
  </book>
</bookstore>
```

Con este documento XML, las expresiones XPath proporcionadas devolverían los siguientes resultados:

1. `/bookstore/book[1]`:
   ```xml
   <book>
     <title lang="en">Harry Potter</title>
     <price>29.99</price>
   </book>
   ```

2. `/bookstore/book[last()]`:
   ```xml
   <book>
     <title lang="en">XPath for Beginners</title>
     <price>45.00</price>
   </book>
   ```

3. `/bookstore/book[last()-1]`:
   ```xml
   <book>
     <title lang="en">Learning XML</title>
     <price>39.95</price>
   </book>
   ```

4. `/bookstore/book[position()<3]`:
   ```xml
   <book>
     <title lang="en">Harry Potter</title>
     <price>29.99</price>
   </book>
   <book>
     <title lang="es">El Alquimista</title>
     <price>19.99</price>
   </book>
   ```

5. `//title[@lang]`:
   ```xml
   <title lang="en">Harry Potter</title>
   <title lang="es">El Alquimista</title>
   <title lang="en">Learning XML</title>
   <title lang="en">XPath for Beginners</title>
   ```

6. `//title[@lang='en']`:
   ```xml
   <title lang="en">Harry Potter</title>
   <title lang="en">Learning XML</title>
   <title lang="en">XPath for Beginners</title>
   ```

7. `/bookstore/book[price>35.00]`:
   ```xml
   <book>
     <title lang="en">Learning XML</title>
     <price>39.95</price>
   </book>
   <book>
     <title lang="en">XPath for Beginners</title>
     <price>45.00</price>
   </book>
   ```

8. `/bookstore/book[price>35.00]/title`:
   ```xml
   <title lang="en">Learning XML</title>
   <title lang="en">XPath for Beginners</title>
   ```

## Conclusión

Las expresiones condicionales en XPath permiten realizar consultas más precisas y flexibles en documentos XML, facilitando la selección de nodos con características o valores específicos. Puedes filtrar nodos según su posición, atributos, o incluso sus valores, lo que hace que XPath sea una herramienta muy poderosa para trabajar con XML.

## Recursos Adicionales

- [Documentación de XPath - W3C](https://www.w3.org/TR/xpath/)
