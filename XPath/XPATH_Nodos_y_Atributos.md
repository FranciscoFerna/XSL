# XPath: Nodos y Atributos

XPath es un lenguaje que permite seleccionar nodos y atributos dentro de un documento XML. A continuación, se presentan algunos ejemplos prácticos para mostrar cómo se utilizan las expresiones XPath en diferentes situaciones.

## Estructura del Documento XML

Consideremos el siguiente documento XML de ejemplo:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<bookstore>
  <book>
    <title lang="en">Harry Potter</title>
    <price>29.99</price>
  </book>
  <book>
    <title lang="en">Learning XML</title>
    <price>39.95</price>
  </book>
</bookstore>
```

## Ejemplos de Expresiones XPath

### 1. **Seleccionar los nodos con el nombre `bookstore`**

```xpath
/bookstore
```

Este XPath selecciona el nodo `<bookstore>` desde la raíz del documento.

### 2. **Seleccionar los elementos `title` dentro de `bookstore`**

```xpath
/bookstore/book/title
```

Este XPath selecciona los elementos `<title>` que están dentro de los elementos `<book>`, que a su vez están dentro de `<bookstore>`. Los resultados serían:

```xml
<title lang="en">Harry Potter</title>
<title lang="en">Learning XML</title>
```

### 3. **Seleccionar todos los elementos `title` en todo el documento**

```xpath
//title
```

Este XPath selecciona todos los elementos `<title>` dentro del documento XML, independientemente de dónde se encuentren. Los resultados serían:

```xml
<title lang="en">Harry Potter</title>
<title lang="en">Learning XML</title>
```

### 4. **Seleccionar todos los elementos `book` descendientes de `bookstore`**

```xpath
/bookstore//book
```

Este XPath selecciona todos los elementos `<book>` que son descendientes de `<bookstore>`, sin importar si son descendientes directos o no. En este caso, los resultados serían:

```xml
<book>
  <title lang="en">Harry Potter</title>
  <price>29.99</price>
</book>
<book>
  <title lang="en">Learning XML</title>
  <price>39.95</price>
</book>
```

### 5. **Seleccionar todos los atributos `lang`**

```xpath
//@lang
```

Este XPath selecciona todos los atributos `lang` en el documento. Los resultados serían:

```xml
lang="en"
lang="en"
```

### 6. **Seleccionar el nodo padre del nodo `title`**

```xpath
//title/../..
```

Este XPath selecciona el nodo `bookstore`, que es el nodo raíz del documento, subiendo desde los elementos `title` y `book`. Los resultados serían:

```xml
<bookstore>
  <book>
    <title lang="en">Harry Potter</title>
    <price>29.99</price>
  </book>
  <book>
    <title lang="en">Learning XML</title>
    <price>39.95</price>
  </book>
</bookstore>
```

### 7. **Seleccionar el nodo padre inmediato del nodo `title`**

```xpath
//title/./..
```

Este XPath selecciona el nodo `book` que es el padre inmediato de los elementos `title`. Los resultados serían:

```xml
<book>
  <title lang="en">Harry Potter</title>
  <price>29.99</price>
</book>
<book>
  <title lang="en">Learning XML</title>
  <price>39.95</price>
</book>
```

### 8. **Seleccionar el atributo `lang` dentro de los elementos `title`**

```xpath
//title/@lang
```

Este XPath selecciona el atributo `lang` dentro de los elementos `<title>`. Los resultados serían:

```xml
lang="en"
lang="en"
```

## Resumen

Las expresiones XPath permiten navegar a través de la estructura jerárquica de un documento XML para seleccionar nodos y atributos específicos. Usando XPath, puedes seleccionar nodos según su nombre, atributos, o su relación con otros nodos en el documento. Los ejemplos anteriores ilustran las formas más comunes de hacer estas selecciones.

## Recursos Adicionales

- [Documentación de XPath - W3C](https://www.w3.org/TR/xpath/)
