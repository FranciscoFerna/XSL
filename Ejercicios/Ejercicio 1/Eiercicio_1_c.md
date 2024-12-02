### Ejercicio 1.c - Consultas usando `xmllint --shell` para archivo XML de predicción

En este ejercicio, trabajaremos con la herramienta `xmllint --shell` para consultar un archivo XML que contiene datos de predicción meteorológica, utilizando la URL proporcionada para acceder al archivo. Las consultas que se realizarán están relacionadas con la humedad, fechas, temperaturas y rachas máximas. A continuación, te guiaré paso a paso sobre cómo hacerlo.

#### 1. **Descarga del archivo XML usando `xmllint --shell`**

El comando para acceder al archivo XML con `xmllint` es el siguiente:

```bash
xmllint --shell "http://www.aemet.es/xml/municipios/localidad_08019.xml"
```

Este comando permite realizar consultas sobre el archivo XML de forma interactiva, sin necesidad de descargarlo previamente.
