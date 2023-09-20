# Proyecto de Web Scraping con Selenium

Este proyecto se enfoca en extraer información de trabajos publicados de LinkedIn utilizando la biblioteca Selenium en Python. La información recolectada se procesa y se guarda en un archivo CSV para su posterior análisis.

## Contenido del Proyecto

- `codigo.ipynb`: Este es el archivo principal donde se encuentra el código que realiza el web scraping. Contiene varias funciones, incluyendo:
    - `iniciar_sesion`: Función para iniciar sesión en LinkedIn.
    - `trabajo`: Esta función abre una URL que debe ser una oferta laboral específica (por ejemplo, "analista de datos" en Argentina) y realiza un filtro para mostrar únicamente empleos publicados en las últimas 24 horas.
    - `obtencion_link_trabajos`: Función para obtener los enlaces de los trabajos.
    - (Otras funciones específicas del proyecto)


## Diccionario de Datos

A continuación se presenta un diccionario de datos que describe las principales variables extraídas:

- `titleJobs`: El título del trabajo.
- `comanyName`: El nombre de la empresa que publicó el trabajo.
- `companyLocation`: La ubicación geográfica del trabajo.
- `employeeRank`: Cantidad de empleados que tiene la empresa.
- `workType`: El tipo de trabajo.
- `skill`: Aptitudes que se requiere para el puesto.
- `link`: Link de la publicación de trabajo.
- `workModality`: Modalidad del puesto.
- `date`: La fecha en que el trabajo fue publicado.
- `industry`: La industria del puesto.

## Proceso de Extracción y Transformación

1. Se inicia sesión en LinkedIn utilizando la función `iniciar_sesion`.
2. Se pasa una URL con las ofertas laborales y se filtra los empleos publicados en las últimas 24 horas `trabajo`.
3. Se obtienen los enlaces a los trabajos utilizando la función `obtencion_link_trabajos`.
4. Para cada enlace, se extrae la información del trabajo utilizando las funciones `Extractdata` y `ExtractSkill`.
5. Los datos extraídos se almacenan en un DataFrame y se realiza la transformación necesaria.
6. Los datos nuevos se concatenan con los existentes y se guarda el resultado en `data/linkedinJobs.csv`.

## Uso del Proyecto

Para ejecutar el proyecto, simplemente abre y ejecuta el archivo `codigo.ipynb` en un entorno de Jupyter Notebook compatible con Selenium.

**Nota:** Asegúrate de tener instaladas las bibliotecas necesarias antes de ejecutar el código. Puedes instalarlas utilizando `pip install nombre_de_la_biblioteca`.