<h1 align="center"><strong>Proyecto Individual #2 - Analisis de datos Interenet Argentina</strong></h1>


![herramientas-de-analisis-de-datos](https://github.com/user-attachments/assets/e76e31f4-53b6-4546-9a21-11e0b1e8c4ee)



## Descripción

Este proyecto implementa un profundo analisis de datos utilizando conocimientos en python y power bi, desarrollado como parte de mi formación en SoyHenry. El analisis permite observar mas a fondo sobre el internet en argentina para obtener posibles recomendacion a la empresa interesada

He desarrollado un Dashboard que interactúa con los datos cargados, permitiendo a los usuarios observar la información detallada . ademas el dashboard contiene kpis claves para la proyeccion del proximo trimestre planteando metricas claves y un objetivo a tener en cuenta

Este proyecto me permitió poner en práctica conocimientos teóricos adquiridos en el curso y profundizar en  herramientas como Power BI y python , además de trabajar con librerías como `pandas`, `seaborn`, `matplotlib`, y `warnings` para la visualización y el tratamiento previo de los datos.

## Tabla de Contenidos
✦  [Instalación y Requisitos](#instalación-y-requisitos)  
✦  [Estructura del Proyecto](#estructura-del-proyecto)  
✦  [Metodología del Proyecto](#metodología-del-proyecto)  
✦  [Datos y Fuentes](#datos-y-fuentes)    
✦  [Análisis Teórico del Modelo](#análisis-teórico-del-modelo)  
✦  [Resultados](#resultados)  

---

## Instalación y Requisitos

### Pasos para instalar el proyecto:

1. Clonar el repositorio:

     ![image](https://github.com/user-attachments/assets/48635476-a253-484a-8710-8ad9657f863f)

2. Crear un entorno virtual: python -m venv entorno_virtual

     ![image](https://github.com/user-attachments/assets/b3223ca8-8dba-49a9-970d-775d2a9da147)

3. Activar el entorno virtual:
     * Windows: entorno_virtual\Scripts\activate 
     * macOS/Linux: source venv/bin/activate
4. Instalar las dependencias: pip install -r requirements.txt
     
     ![image](https://github.com/user-attachments/assets/5846bbe4-1f82-42a6-b6f3-9b02cbd2bc82)
     
5. Instalacion de power bi
     * Windows: Descargar directamente de la tienda microsoft
     * macOS/Linux: Crear un entorno virtual windows para realizar la descarga o usar la version web de power BI


## Estructura del Proyecto

✦ Archivos para el analisis exploratorio: Carpeta que contiene los archivos utilizados para el analaisis de datos en excel ademas de contener el notebook del EDA y los kpis realizados.

✦ Archivos Finales: Carpeta con un archivo Power BI que ofrece una visualización dinamica de los datos y de los kpis junto con los archivos en parquet que fueron utilizados.

✦ README.md: Documentación del proyecto.

  
## Metodología del Proyecto

### Herramientas Utilizadas:

✦ Visual Studio Code: Editor de código para desarrollar y modificar el proyecto en un entorno virtual local.

✦ GitHub: Plataforma para almacenar el proyecto de forma global.

✦ Git Bash: Utilizado para crear el entorno virtual, configurar el repositorio y subir cambios locales a GitHub.

✦ PowerBI: Herramienta utilizada para Desarrollar el dashboard dinamico.

### Proceso de Desarrollo:

✦ Análisis Exploratorio de Datos (EDA)
1. Carga:
En esta fase se comenzo con la carga individual de las hojas del archivo excell descargado de la pagina https://indicadores.enacom.gob.ar/Files/Datos_Abiertos/Internet.xlsx en dataframes individuales para una mejor visualizacion. Al dar un vistazo rapido a los datos decidi eliminar las hojas que contuvieran informacion explayada por Partido y/o Localidad ya que mi enfoque para el analisis es por Provincia por lo tanto las hojas 'Acc_vel_loc_sinrangos', 'Accesos_tecnologia_localidad', 'Totales VMD', 'Totales Dial-BAf', 'Dial-BAf', 'Penetracion-totales' y 'Totales Accesos por velocidad' son descartadas.

2. Manejo de Datos Faltantes:
Se revisaron las columnas con valores faltantes por hoja, afortunadamente solo 2 hojas tenian datos faltantes la hoja de velocidad sin rangos era una fila completamente vacia que se elimino y la hoja accesos por tecnologia tenia 2 filas con una nota dejada dentro por lo cual se elimino . Este paso fue crucial para mantener un dataset limpio y manejable, sin perder información importante para el análisis.

3. Correccion de Datos :
Se pudieron observar algunos errores en los datos de año y trimestre en algunas hojas que contenian un * dentro de los datos lo cual se manejo y se limpiaron esos datos sin necesidad de eliminarlos

3. Manejo de Datos Duplicados:
No se observaron datos duplicados en ninguna de las hojas tomadas para el analisis

12. Detección y Análisis de Outliers:
Utilizando gráficos de caja (boxplots), se identificaron outliers en varias variables. Se realizó un análisis más detallado, concluyendo que los outliers en la hoja de accesos por tecnologia se debe a que no se estaba considerando que los accesos totales por provincia dependen de la cantidad de poblacion que maneje cada provincia, se corrigio calculando la proporcion y se observo una mejoria en los datos

13. Análisis de tecnologias:
Se exploró la tendencia en las tecnologias con el paso de los años observando una caida pronunciada en el ADSL y al mismo tiempo un ascenso de la fibra optica mientras que el CableModem y el wireless manejan tasas de crecimiento sostenido.

14. Analisis de provincia:
Al analizar los accesos por provincia y las tecnologias que predominan en cada una de ellas se noto una clara disparidad teniendo que las ciudades principales con una alta poblacion como buenos aires, cordoba, neuquen, entre otras cuentan con una velocidad media por encima de las 100 megas y que provincias con poca poblacion sobre todo al sur del pais cuentan con velocidades medias por debajo de las 50 megas .

17. Analisis de tecnologia mas usada:
Se examinó la distribucion de las tecnologias y se obtuvo una imagen clara de que CableModem es la tecnologia mas usada actualmente en el pais desde el año 2018 debido a su bajo coste de infraestructura y la posibilidad de ofrecer velocidades medias comodas para los usuarios, anterior a eso el ADSL era la tecnologia mas usada pero ha sido desplazada debido a su obsoletidad en velocidades.

18. Distribucion de ingresos:
Al mismo tiempo que la fibra optica ha empezado a crecer se puede observar un crecimiento exponencial de los ingresos en internet en argentina.

19. Análisis de accesos por hogares:
A partir del 2018 se ve un aumento significativo en el acceso por hogares en las provincias, aun asi hay provincias que se destacan por accesibilidad como Capital federa, Tierra del fuego y San Luis.

22. Análisis de Wireless:
Finalmente, se analizaron las tecnologias mas usadas por cada provincia y se observo que las provincias que usaban Wireless tenian una buena velocidad media y buenos accesos a internet como San Luis.

Gracias a este análisis exhaustivo, se identificaron las características más relevantes para la construcción del Dashboard.  
> **Nota:** "Para observar en mayor profundidad los gráficos y el análisis realizado, puede consultar el Notebook de EDA disponible [aquí]().".  

✦ Optimizacion: Tras el análisis exploratorio, se realizo una organizacion final de los datos que iban a ser cargados en power bi se inicio con la hoja velocidad sin rangos calculando las 30 velocidades mas frecuentes y guardandolas en un dataframe, Luego se realizo una union entre 3 hojas (penetracion de poblacion, penetracion de hogares, velocidad por provincia) que contenian la misma informacion con una sola columna diferencial, se creo un dataframe con las latitudes y longitudes para la utilizacion en los mapas de power bi, despues de esto se procedio a guardar los datos en archivos con formato parquet

✦ Calculo de Kpis: Se creo un notebook que contiene los 2 kpis planteados y el kpi obligatorio de manera explicativa

✦ Creacion del dashboard: Para realizar el dashboard se cargaron los archivos parquet se realizaron sus respectivas relaciones, la primera hoja contiene un informe general de los accesos, tecnologias, ingresos los cuales pueden verse mas detalladamente por año y trimestre mediante filtros dentro de la pagina, luego podemos observar el primer kpi siendo la Proyeccion de acceso por hogares con un aumento del 2% para el trimestre 2 del año 2024 siendo dinamico segun la provincia donde queramos observar mas detalladamente, lueo obtenemos la proyeccion para el proximo trimestre con un aumento del 3.5% en la velocidad media de cada provincia, por ultimo observamos un crecimiento en la proyeccion del aumento del 10% de la penetracion de la fibra optica en las provincias donde la fibra optica tiene bajos accesos  y finalmente encontramos una hoja con la visualizacion de los accesos por provincia teniendo un rango de velocidad observando las velocidades mas comunes por provincia.

## Datos y Fuentes
Los datos utilizados para este proyecto se encuentran en la pagina oficial del gobierno de argentina "(https://indicadores.enacom.gob.ar/Files/Datos_Abiertos/Internet.xlsx)". A continuación, se presentan los archivos finales utilizados para el analisis y la creacion del dashboard

✦ Dataset de accesos por velocidad:

Este dataset contiene información sobre las velocidades por rango de cada provincia.

![image](https://github.com/user-attachments/assets/3c85e9bb-2909-4405-9af6-674bcd04a53d)

✦ Dataset de ingresos:

En este dataset se almacena información clave sobre los ingresos obtenidos entre el año 201 y el primer trimestre del año 2024.

![image](https://github.com/user-attachments/assets/c4eec84f-18f0-4628-913e-d5c4b8f5689e)


✦ Dataset accesos totales por provincia:

Este dataset da informacion sobre los accesos por hogares del primer trimestre del 2024 y la proyeccion del 2%  para el trimestre 2 del 2024 por cada pronvincia ademas de obtener la velocidad media y la proyeccion con el aumento del 3.5% para el proximo trimestre.

![image](https://github.com/user-attachments/assets/51d4dc18-809a-419f-8dde-4321f85f6ce5)

✦ Dataset accesos totales por provincia:

Este dataset da informacion sobre los accesos por tecnologia y provincia del primer trimestre del 2024 y la proyeccion del 10%  para el trimestre 2 del 2024 respecto a la penetracion de fibra optica en las provincias con bajos accesos en dicha tecnologia

![image](https://github.com/user-attachments/assets/53e4c5a1-6346-42ba-97fb-51c0df9f0aef)

✦ Dataset accesos totales por provincia:

Este dataset da informacion sobre el total de accesos por tecnologia sin tener en cuenta la provincia basado unicamente en el año y el trimestre

![image](https://github.com/user-attachments/assets/12b3192d-bdc3-447b-bd1e-269190357493)

✦ Dataset accesos totales por provincia:

Este dataset fue creado para obtener la informacion de las latitudes y las longitudes para una correcta visualizacion en los mapas a usar

![image](https://github.com/user-attachments/assets/28e2c96c-0284-4944-b18e-fb87f19a1abf)

## Dashboard

1. Portada = coloca algo  
   
3. Resumen general = visualizacion de los accesos totales, accesos por tecnologia, evolucion de tecnologias entre 2014 y 2024, Tendencia de los ingresos entre 2014 y 2024, tarjetas con visualizaciones de la tasa de creciemiento anual todo esto se puede observar de manera dinamica mediante filtros de año y trimestre  
   
4. Proyeccion de accesos por cada 100 hogares: Visualizacion de un mapa con las provincias segmentadas segun los accesos a internet por hogares siendo bajo(azul) menores a 50 accesos, Medio (verde) entre 51 y 70 accesos y Alto (rosa) mayores a 71 accesos, ademas una comparativa de barras de los accesos por cada provincia es una hoja dinamica mediante un filtro por provincia
   
5. Proyeccion de velocidad media: Visualizacion de un mapa con las provincias segmentadas segun la velocidad media siendo bajo(azul) velocidades menores a 50 megas, Medio (verde) velocidades entre 50 y 95 megas  y Alto (rosa) velocidades mayores a 95 megas, ademas una comparativa de barras de la velocidad media por cada provincia es una hoja dinamica mediante un filtro por provincia
   
6. Proyeccion de penetracion de fibra optica: mediante un grafico de areas apiladas se observa el crecimiento esperado para el proximo trimestre en las provincias con baja penetracion teniendo en cuenta el objetivo del 10% del kpi, ademas se observa cual es la velocidad media de dichas provincias  


## Análisis Teórico

A lo largo del proyecto, se analizo y grafico los datos obteniendo:

✦. analisis de la hoja velocidad sin rangos:
Las 30 velocidades mas frecuentes varian entre las 6 megas y las 50 megas dando un entendimiento donde los usuarios prefieren velocidades mas altas y estables
![image](https://github.com/user-attachments/assets/54c14a05-4f96-4c75-9cfc-51bafddf9d54)


✦. analisis de la hoja velocidad media por provincia:
Se observo una tendencia ascendente en las velocidades medias indicando una migracion de tecnologias con bajas velocidades a una con conexiones mas estables y rapidas como fibra optica, ademas se visualizo una desigualdad regional con picos en capital federal de 229 megas y chubut con 20.5 megas dando un mercado potencial en las provincias con velocidades medias bajas.
al analizar la variacion estacional se observo que el cuarto trimestre es cuando se alcanzan las velocidades mas altas de internet, lo que podria sugerir un mayor consumo de servicios digitales durante el fin de año, coincidiendo con eventos y celebraciones.
![image](https://github.com/user-attachments/assets/d5dece08-033f-451f-a91b-75fd7108d4d4)

✦. analisis de la hoja Totales accesos por tecnologia:
La adopción de tecnologias más modernas está reemplazando a las más antiguas, reflejando una tendencia hacia una mayor conectividad y acceso a Internet.
La tasa de crecimiento anual de Fibra Óptica (2014-2024) es de: 38.95%
La tasa de crecimiento anual de ADSL (2014-2024) es de: -14.62%
La tasa de crecimiento anual de Cablemodem (2014-2024) es de: 8.97%
La tasa de crecimiento anual de Wireless (2014-2024) es de: 22.77%

![image](https://github.com/user-attachments/assets/e0ffb53b-5287-4d6e-9d83-551e4a0ed3b3)


✦. analisis de la hoja accesos por tecnologia:
Las provincias muestran una enorme disparidad en el acceso a internet aun teniendo en cuenta su poblacion

![image](https://github.com/user-attachments/assets/62ea65eb-3a1c-4d58-896d-726ff6e8ebec)

✦. analisis de la hoja penetracion poblacional:
El analisis se realizo sobre las provincias donde el acceso por cada 100 habitantes era menor.

![image](https://github.com/user-attachments/assets/f06eb66c-93d1-4608-adf1-ba764133be53)

✦. analisis de la hoja penetracion por hogares:
Se observo un aumento constante en los accesos a internet, especialmente en el trimestre 1 del 2023 y 2024

![image](https://github.com/user-attachments/assets/776fdf62-5802-41d4-a728-a6fd1f5e627d)

✦. analisis de la hoja ingresos:
Crecimiento Acelerado: A partir de 2020, los ingresos muestran un incremento más marcado, posiblemente impulsado por factores externos como la pandemia y la mayor digitalización. Esto indica un cambio positivo en la estrategia o el mercado.

![image](https://github.com/user-attachments/assets/2d53281d-3429-4f50-b065-13c1a471a6a3)


Con estas observaciones, se pudo obtener una idea mas clara sobre las recomendaciones a realizar a la empresa

## Resultados

añadir recomendacion basados en los kpis 

## Autor

✦ Este proyecto fue realizado por **Karen Lizeth Barbosa Rojas**.
