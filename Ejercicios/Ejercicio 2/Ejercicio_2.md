#### **Descripción del ejercicio**
El objetivo de este ejercicio es aprender a utilizar consultas XPath para extraer información de un archivo XML, empleando la herramienta `xmllint` en modo shell. Se deben realizar una serie de consultas específicas sobre un archivo XML con datos meteorológicos. Los resultados obtenidos deben cumplir con los criterios definidos para cada consulta.

#### **Herramienta utilizada**
`xmllint` es una herramienta de línea de comandos que permite trabajar con documentos XML. En este caso, usaremos su modo shell para ejecutar consultas XPath.

---

### **Consultas requeridas**
1. **Temperatura máxima y mínima para pasado mañana:**
   - Debes realizar dos consultas separadas: una para la temperatura máxima y otra para la mínima, en la fecha correspondiente a pasado mañana.

2. **Temperatura prevista para hoy a las seis de la tarde:**
   - Extraer el valor de la temperatura registrada en el nodo correspondiente a las 18:00 horas del día actual.

3. **Descripción del estado del cielo de hoy:**
   - Seleccionar un único resultado que describa el estado del cielo (por ejemplo, "Despejado", "Nublado"). Si hay múltiples descripciones disponibles, elegir una tomando decisiones razonadas.

4. **Cota de nieve para mañana:**
   - Localizar el nodo que indica la cota de nieve prevista para el día siguiente.

5. **Humedad relativa de esta tarde:**
   - Recuperar el dato de humedad registrado en las horas de la tarde del día actual.

6. **Todos los índices UV:**
   - Realizar una consulta que retorne todos los valores de índice UV presentes en el XML.

7. **Fechas de los días con predicción:**
   - Extraer todas las fechas de los días que contienen predicciones climáticas en el archivo XML.
