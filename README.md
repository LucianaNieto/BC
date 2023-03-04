# draft version 

La parte mas importante (que conecta con GEE y demas dependencias esta aca: https://github.com/LucianaNieto/BC/blob/main/pages/1__Images_reporte.py


Esto es parte de la documentacion que habien empezado y quiza ayuda para enterder mejor: 

La aplicación que estamos documentando es una herramienta desarrollada con Streamlit, que permite a los usuarios acceder a las colecciones de imágenes satelitales disponibles en Google Earth Engine y observar el paso del tiempo y cambios en el territorio seleccionado. La primera fase de esta herramienta se enfoca en proveer una interfaz amigable para explorar y visualizar estas imágenes satelitales, pero la idea es que en el futuro se puedan añadir funcionalidades adicionales, como la posibilidad de realizar cálculos y análisis en estos datos. Calculo de superficie, indice de verdor, agua en superficie, etc, datos climaticos (precipitaciones, radiacion, heladas), datos edaficos, etc.
Se pueden agregar diferentes modulos que permiten calcular los ejemplos antes mencionados. 

### Google earth engine

Google Earth Engine (GEE) es una plataforma de código abierto para el procesamiento y análisis de imágenes satelitales a gran escala. 

Ventajas:

- Acceso a gran cantidad de imágenes satelitales: GEE tiene acceso a una gran cantidad de imágenes satelitales, incluyendo imágenes de Landsat, Sentinel y MODIS, lo que permite a los usuarios analizar y comparar imágenes de diferentes fechas y satélites.
- Herramientas de procesamiento y análisis: GEE incluye una variedad de herramientas de procesamiento y análisis, como la detección de cambios, la clasificación de imágenes y el análisis de tendencias, que facilitan el análisis de datos geoespaciales.
- Acceso a datos de terceros: GEE tiene acceso a una gran cantidad de datos de terceros, como mapas de elevación, mapas de vegetación y datos climáticos, lo que permite a los usuarios realizar análisis más complejos.
- Acceso a datos propios: repositorios pueden ser cargados a GEE. La limitante de esto es la memoria asignada, que puede ser esquivada creando proyectos que se conectan a google buckets.
- Acceso a recursos de cómputo: GEE tiene acceso a recursos de cómputo de Google, lo que permite a los usuarios procesar grandes cantidades de datos de manera rápida y eficiente.

Desventajas:

- Requiere una conexión a Internet: GEE requiere una conexión a Internet para acceder a la plataforma y los datos, lo que puede ser un problema en áreas con conexión limitada.
- Tiene un proceso de aprobación para acceder a los datos: para acceder a los datos de GEE, los usuarios deben solicitar una cuenta de desarrollador y obtener la aprobación de Google, lo que puede ser un proceso lento (Streamlit permite agregar un secret token para que corra son problema, actualmente esta asociado a mi cuenta de GEE).
- Requiere habilidades de programación: GEE requiere habilidades de programación para utilizar la plataforma y las herramientas de análisis, lo que puede ser un obstáculo para algunos usuarios (si bien el nativo de GEE es java script el paquete gee en python permite trabajar sin mayores problemas accediendo a practicamente todas las capacidades de GEE).


### Librerias 
- **`ee`** es un módulo de la biblioteca de Google Earth Engine. Se utiliza para acceder a la plataforma de Google Earth Engine y realizar operaciones en imágenes satelitales, como la recuperación de imágenes, el procesamiento y el análisis.
- **`datetime`** es un módulo estándar de Python que proporciona funcionalidades para trabajar con fechas y horas.
- **`geopandas`** es una biblioteca basada en pandas que proporciona funcionalidades para trabajar con datos geoespaciales, como la lectura y escritura de datos en formatos GIS, el análisis y la visualización.
- **`folium`** es una biblioteca de Python que permite crear mapas interactivos utilizando el marco de trabajo leaflet.js
geemap es una biblioteca de Python que se construye sobre folium y ee, y proporciona una interfaz amigable para acceder a los datos y las funciones de Google Earth Engine. Con geemap, los usuarios pueden acceder a los datos de imágenes satelitales de GEE, realizar operaciones de procesamiento y análisis, y crear visualizaciones de mapas interactivos. También proporciona un conjunto de funciones y métodos adicionales para facilitar el trabajo con GEE.
