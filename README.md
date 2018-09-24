# Ventilando los datos abiertos sobre calidad del aire.

<!-- TOC depthFrom:2 orderedList:true -->

1. [Contexto](#contexto)
2. [Descripción de notebooks](#descripción-de-notebooks)

<!-- /TOC -->

## Contexto

Se utilizaron datos abiertos sobre calidad del aire de las estaciones del país reportadas a SINAICA y disponibles desde el portal de [datos.gob](https://datos.gob.mx/)  

Los datos se analizaron y se escribió un post (agregar liga) ilustrando el proceso.

## Descripción de notebooks

El procesamiento de los datos se hizo en Python con ayuda de la herramienta Jupyter Notebook, los archivos que procesan la información están en la carpeta [notebooks](https://github.com/opintel/calidad-del-aire/blob/master/notebooks/) y están divididos por partes:

1. [Obtener_datos_calidad_del_aire](https://github.com/opintel/calidad-del-aire/blob/master/notebooks/1_obtener_datos_calidad_del_aire.ipynb): en este notebook se descargan los datos de calidad del aire a nivel nacional usando un [cliente de México Abierto](https://github.com/mxabierto/api_python_client/tree/master/datosgobmx). Se obtienen datos de las estaciones de calidad del aire, como su nombre y coordenadas, y todas las mediciones de contaminantes reportadas a nivel nacional. **Este notebook es la base de todos los análisis posteriores, ya que aquí se obtienen todos los datos.**

1. [EDA_1](https://github.com/opintel/calidad-del-aire/blob/master/notebooks/2_EDA_1.ipynb): Análisis exploratorio del ozono y comparación de los niveles promedio de este contaminante en las ciudades con más estaciones de monitoreo. 

1. [EDA_2](https://github.com/opintel/calidad-del-aire/blob/master/notebooks/3_EDA_2.ipynb): Visualizaciones de la evolución de contaminantes durante el día y comparaciones de contingencias entre la Ciudad de México y Guadalajara.

1. [Ozono_vs_poblacion](https://github.com/opintel/calidad-del-aire/blob/master/notebooks/4_ozono_vs_poblacion.ipynb): Se obtienen datos de población por área metropolitana para ver el comportamiento del ozono cada 100 mil habitantes de las ciudades con más estaciones de monitoreo.

1. [Prediccion_ozono_CDMX_GDL](https://github.com/opintel/calidad-del-aire/blob/master/notebooks/5_prediccion_ozono_CDMX_GDL.ipynb): Modelo de predicción de series de tiempo para el ozono en la Ciudad de México y Guadalajara usando el modelo [Prophet](https://github.com/facebook/prophet).

1. [Mapas_interactivos_y_gifs](https://github.com/opintel/calidad-del-aire/blob/master/notebooks/6_mapas_interactivos_y_gifs.ipynb): Generación de mapas interactivos en formato html y gifs de evolución de ozono durante el día. El de la CDMX se ve así:
<img src="https://media.giphy.com/media/2UEYcoLYl2A1t6omx9/giphy.gif" width="380" height="240" />
