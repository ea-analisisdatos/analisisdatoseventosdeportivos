# Proyecto
En este reto, métete en la piel de un analista de datos que trabaja para una empresa de eventos deportivos. La empresa ha recopilado datos de sus eventos, los aficionados que asistieron y las promociones publicitarias realizadas para atraer a más asistentes. Tu tarea será procesar y analizar estos datos utilizando Python y la librería Pandas, combinando la información para extraer 'insights' clave que ayuden a mejorar la planificación de futuros eventos y promociones.

## Criterios de calificación

**Análisis de datos y respuestas a preguntas de negocio**
- El alumno debe haber respondido correctamente a las preguntas de negocio, utilizando métodos como groupby(), max(), y cut(). Las respuestas deben ser claras y basadas en un análisis correcto de los datos.
- Peso: 30%

**Combinación de DataFrames**
- Se evaluará si los DataFrames se han combinado correctamente utilizando merge() o join(), con el uso adecuado de la clave id_evento para alinear los datos de forma coherente. Se evaluará que los DataFrames combinados reflejen relaciones precisas entre eventos, aficionados y promociones.
- Peso: 30%

**Carga y limpieza de datos**
- El alumno debe haber cargado correctamente los tres archivos CSV (eventos.csv, aficionados.csv, promociones.csv) en DataFrames de Pandas. Se evaluará que el alumno haya limpiado los datos eliminando las filas con valores nulos. Esto debe aplicarse correctamente a todos los DataFrames.
- Peso: 25%

**Exportación y presentación de los resultados**
- Se evaluará si el DataFrame final con los análisis ha sido exportado correctamente a un archivo CSV llamado reporte_eventos.csv. El archivo CSV debe estar en un formato legible y bien organizado, con las columnas relevantes claramente etiquetadas.
- Peso: 15%

## Requisitos

**Carga de los datos:**

- Carga los datos desde los archivos CSV que están presentes en el proyecto. Las rutas de los archivos deben ser absolutas, como se muestra a continuación:
    - /workspace/eventos.csv
    - /workspace/aficionados.csv
    - /workspace/promociones.csv

- Utiliza estas rutas absolutas para asegurarte de que los datos se carguen correctamente en los DataFrames.
- **Limpieza de datos:** recuerda que es obligatorio eliminar las filas con valores nulos.
- **Combinación de DataFrames:** deberás combinar los tres DataFrames.
- **Análisis de datos. Debes responder a las siguientes preguntas de negocio:**
    - ¿Cuál es el evento con mayor asistencia total?
    - ¿Cuál es el rango de edad que asiste más frecuentemente a los eventos?
    - ¿Qué medio publicitario ha generado mayor impacto en términos de asistencia?
    - ¿Cuál es la ubicación de residencia que más aficionados aporta a los eventos?
- **Exportación:**
    - El DataFrame final debe ser exportado en formato CSV con el nombre reporte_eventos.csv. Asegúrate de que el archivo se guarde en la carpeta /workspace, usando una ruta absoluta.


## Instrucciones:

- Deberás trabajar con tres conjuntos de datos que contienen información sobre los siguienters puntos:

- **Eventos deportivos:** datos como el nombre del evento, la fecha, ubicación y el número total de asistentes.

- **Aficionados:** datos demográficos como la edad, género y lugar de residencia de los aficionados que asistieron a los eventos.

- **Promociones publicitarias:** información sobre las promociones realizadas, incluyendo el medio publicitario utilizado, el presupuesto y la duración de la promoción.

- Tu misión será realizar la limpieza de datos, combinarlos y responder a preguntas críticas de negocio como cuál fue el evento más exitoso en términos de asistencia, qué medio publicitario fue el más efectivo y qué grupo de edad es el más frecuente en los eventos. Además, deberás realizar algunas transformaciones adicionales para medir el impacto de las promociones y la duración de las mismas.


**A continuación te ofrecemos las pautas que debes seguir, ¡toma nota!**

**1. Preparar el entorno de trabajo**
- Crea un nuevo archivo Jupyter Notebook llamado analisis_eventos.ipynb.

**2. Importar las librerías necesarias**
- Importa las librerías Pandas que necesitarás para realizar el análisis.

**3. Cargar los datos (lectura y procesamiento de datos con Pandas)**
- Utiliza Pandas para cargar los archivos CSV: eventos.csv, aficionados.csv y promociones.csv. Guarda los datos en tres DataFrames distintos.

**4. Limpieza de datos**
- Elimina las filas con valores nulos en los DataFrames para asegurarte de trabajar con datos completos. Utiliza el método dropna().

**5. Combinación de los DataFrames**
- Para poder analizar los datos en conjunto, deberás combinarlos. Utiliza merge() o join() para combinar los DataFrames de eventos, aficionados y promociones. - - Elige la columna id_evento para relacionar las tablas.

**6. Responde las siguientes preguntas de negocio**
- ¿Cuál es el evento con mayor asistencia total?
- Usa max() en la columna asistentes_totales para identificar el evento con mayor número de asistentes.
- ¿Qué rango de edad asiste más frecuentemente a los eventos?
- Utiliza pd.cut() para agrupar a los aficionados en rangos de edad y luego cuenta cuántos aficionados hay en cada grupo.
- ¿Qué medio publicitario ha generado mayor impacto en términos de asistencia?
- Crea una columna impacto_promoción que divida el número de asistentes totales por el presupuesto de la promoción y agrupa por medio_publicitario.
- ¿Cuál es la ubicación de residencia que más aficionados aporta a los eventos?
- Usa groupby() para sumar los aficionados por ubicación de residencia.

**7. Exportación de los resultados:**
- Guarda el DataFrame resultante con todas las transformaciones y análisis en un archivo CSV llamado reporte_eventos.csv utilizando la función df.to_csv().


## Tecnologías a utilizar
- Pandas