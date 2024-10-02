<h1 align="center"><strong>Proyecto Individual #2 - Análisis de Datos de Internet en Argentina</strong></h1>  

<p align="center">
  <img src="https://github.com/user-attachments/assets/e76e31f4-53b6-4546-9a21-11e0b1e8c4ee" alt="herramientas-de-analisis-de-datos">
</p>

## Descripción

Este proyecto implementa un análisis profundo de los datos de conectividad a Internet en Argentina, utilizando herramientas de Python y Power BI. Fue desarrollado como parte de mi formación en **SoyHenry**. El análisis ofrece insights detallados para identificar oportunidades y desafíos en la conectividad a Internet en Argentina, además de proporcionar recomendaciones para mejorar el servicio de una empresa interesada en este mercado.

El **dashboard interactivo** desarrollado en Power BI permite visualizar los datos de forma dinámica. Incluye **KPIs clave** para la proyección del próximo trimestre, estableciendo métricas de rendimiento con objetivos claros.

Este proyecto me permitió aplicar conocimientos teóricos y prácticos, así como mejorar mis habilidades en **Python**, **Power BI**, y el uso de librerías como `pandas`, `seaborn`, `matplotlib`, entre otras.

---

## Tabla de Contenidos

- [Instalación y Requisitos](#instalación-y-requisitos)
- [Estructura del Proyecto](#estructura-del-proyecto)
- [Metodología del Proyecto](#metodología-del-proyecto)
- [Datos y Fuentes](#datos-y-fuentes)
- [Resultados](#resultados)

---

## Instalación y Requisitos

### Pasos para instalar el proyecto:

1. Clonar el repositorio:
   
     ![image](https://github.com/user-attachments/assets/48635476-a253-484a-8710-8ad9657f863f)

3. Crear un entorno virtual: python -m venv entorno_virtual

     ![image](https://github.com/user-attachments/assets/b3223ca8-8dba-49a9-970d-775d2a9da147)

4. Activar el entorno virtual:
     - Windows: entorno_virtual\Scripts\activate 
     - macOS/Linux: source venv/bin/activate

5. Instalar las dependencias: pip install -r requirements.txt
     
     ![image](https://github.com/user-attachments/assets/5846bbe4-1f82-42a6-b6f3-9b02cbd2bc82)
     
6. Instalacion de power bi
     - Windows: Descargar directamente de la tienda microsoft
     - macOS/Linux: Crear un entorno virtual windows para realizar la descarga o usar la version web de power BI


# Proyecto de Análisis de Conectividad a Internet en Argentina

## Estructura del Proyecto

- **Archivos para el análisis exploratorio**: Contiene los archivos utilizados para el análisis de datos en formato Excel, junto con los notebooks utilizados para el análisis exploratorio de datos (EDA) y la creación de los KPIs.  
- **Archivos Finales**: Incluye el archivo Power BI con una visualización interactiva de los datos y KPIs, además de los archivos en formato parquet, optimizados para su uso en Power BI.  
- **README.md**: Documentación completa del proyecto.

## Metodología del Proyecto

### Herramientas Utilizadas

- **Visual Studio Code**: Para desarrollar y modificar el código del proyecto en un entorno de desarrollo local.
- **GitHub**: Utilizado como repositorio para gestionar el control de versiones y almacenar el proyecto.
- **Git Bash**: Empleado para crear el entorno virtual, configurar el repositorio y realizar la subida de cambios locales a GitHub.
- **Power BI**: Herramienta utilizada para desarrollar el dashboard interactivo y dinámico.

### Proceso de Desarrollo

#### Análisis Exploratorio de Datos (EDA)

1. **Carga de Datos**  
   Se inició con la carga de las hojas del archivo Excel descargado desde la página oficial de ENACOM, distribuyendo los datos en dataframes individuales para facilitar la visualización. Se eliminaron las hojas que contenían datos a nivel de Partido o Localidad, ya que el análisis se realizó a nivel provincial.

2. **Manejo de Datos Faltantes**  
   Se realizó una revisión detallada de cada hoja, identificando y eliminando filas con valores faltantes o no válidos para asegurar la integridad del dataset.

3. **Corrección de Datos**  
   Durante el proceso, se detectaron y corrigieron errores en los datos de años y trimestres, incluyendo la presencia de caracteres no válidos que fueron limpiados sin necesidad de eliminar registros.

4. **Manejo de Datos Duplicados**  
   Se comprobó que no existían datos duplicados en las hojas seleccionadas para el análisis.

5. **Detección y Análisis de Outliers**  
   Utilizando gráficos de caja (boxplots), se identificaron y analizaron outliers en diversas variables. En particular, se ajustaron los outliers de accesos por tecnología de acuerdo con la proporción de la población en cada provincia.

6. **Análisis de Tecnologías**  
   Se observó una tendencia de caída en el uso de ADSL, mientras que las tecnologías de fibra óptica y CableModem presentaron un crecimiento sostenido, con Wireless también mostrando incrementos considerables.

7. **Análisis por Provincia**  
   Se identificaron diferencias significativas en las velocidades medias de acceso a internet entre provincias con alta y baja densidad de población.

8. **Análisis de Tecnología Más Usada**  
   Desde 2018, CableModem se consolidó como la tecnología más utilizada debido a su balance entre coste de infraestructura y velocidad proporcionada a los usuarios.

9. **Distribución de Ingresos**  
   Los ingresos generados por servicios de internet en Argentina han mostrado un crecimiento exponencial, impulsado principalmente por la mayor penetración de la fibra óptica.

10. **Análisis de Accesos por Hogares**  
   A partir de 2018, se detectó un aumento significativo en los accesos a internet por hogares, siendo Capital Federal, Tierra del Fuego y San Luis las provincias más destacadas en este aspecto.

11. **Análisis de Wireless**  
   Provincias como San Luis, que cuentan con una importante adopción de tecnología Wireless, presentaron una velocidad media de conexión competitiva y un número de accesos significativo.

12. **Optimización de Datos**  
   Tras la organización final de los datos, se generaron archivos en formato parquet, lo que optimizó el procesamiento y análisis en Power BI.

13. **Cálculo de KPIs**  
   Se desarrolló un notebook con los KPIs clave, detallando tanto su cálculo como su justificación en el contexto del análisis.

14. **Creación del Dashboard**  
   El dashboard en Power BI incluye filtros dinámicos para explorar el acceso a internet por tecnologías, provincias y trimestres, junto con la proyección de KPIs clave, como un crecimiento del 2% en accesos por hogar, un aumento del 3.5% en la velocidad media por provincia, y una penetración del 10% de fibra óptica en provincias con baja adopción.

## Datos y Fuentes

Los datos utilizados en este proyecto provienen de la página oficial del gobierno de Argentina: [ENACOM - Datos Abiertos](https://indicadores.enacom.gob.ar/Files/Datos_Abiertos/Internet.xlsx). A continuación, se describen los principales datasets utilizados para el análisis y la creación del dashboard:

### ✦ **Dataset de Accesos por Velocidad**

Este dataset contiene información detallada sobre los accesos a internet clasificados por rangos de velocidad para cada provincia. Los datos son clave para entender la distribución de accesos a internet por velocidad en todo el país, y para identificar las provincias con mayor y menor adopción de conexiones de alta velocidad.

![Dataset de Accesos por Velocidad](https://github.com/user-attachments/assets/3c85e9bb-2909-4405-9af6-674bcd04a53d)

### ✦ **Dataset de Ingresos**

En este dataset se recopila información sobre los ingresos generados por servicios de internet desde el año 2014 hasta el primer trimestre de 2024. Este dataset es fundamental para analizar las tendencias de crecimiento en los ingresos asociados a la conectividad y cómo estos varían entre los diferentes trimestres.

![Dataset de Ingresos](https://github.com/user-attachments/assets/c4eec84f-18f0-4628-913e-d5c4b8f5689e)

### ✦ **Dataset de Accesos Totales por Provincia**

Este dataset proporciona información sobre los accesos a internet por hogares para el primer trimestre de 2024, así como una proyección de crecimiento del 2% para el segundo trimestre de 2024. Además, incluye datos sobre la velocidad media por provincia y una proyección de aumento del 3.5% para el próximo trimestre.

![Dataset de Accesos Totales por Provincia](https://github.com/user-attachments/assets/51d4dc18-809a-419f-8dde-4321f85f6ce5)

### ✦ **Dataset de Accesos por Tecnología y Provincia**

En este dataset se detalla la cantidad de accesos a internet por cada tecnología (fibra óptica, ADSL, Cablemodem, etc.) y provincia durante el primer trimestre de 2024. También incluye una proyección del 10% de aumento en la penetración de fibra óptica para el segundo trimestre de 2024 en provincias con baja adopción de esta tecnología.

![Dataset de Accesos por Tecnología y Provincia](https://github.com/user-attachments/assets/53e4c5a1-6346-42ba-97fb-51c0df9f0aef)

### ✦ **Dataset de Accesos Totales por Tecnología**

Este dataset recopila el total de accesos a internet por cada tecnología, sin diferenciar por provincia, basándose únicamente en el año y trimestre. Permite observar tendencias generales de adopción de tecnologías en el país.

![Dataset de Accesos Totales por Tecnología](https://github.com/user-attachments/assets/12b3192d-bdc3-447b-bd1e-269190357493)

### ✦ **Dataset de Coordenadas (Latitud y Longitud)**

Este dataset fue creado para obtener la información geográfica (latitud y longitud) de cada provincia. Es fundamental para la correcta visualización de los datos en los mapas utilizados en el análisis y el dashboard.

![Dataset de Coordenadas](https://github.com/user-attachments/assets/28e2c96c-0284-4944-b18e-fb87f19a1abf)
# Dashboard

1. **Portada:** Visualización general del estado actual de la conectividad en Argentina, destacando las tecnologías predominantes y el alcance de la conectividad por provincia. *(Aquí puedes agregar una imagen o descripción personalizada)*.

2. **Resumen General:**  
   Este dashboard incluye las siguientes visualizaciones interactivas:  
   - **Accesos Totales:** Gráfico de barras apiladas mostrando el total de accesos por tecnología.  
   - **Evolución por Tecnología (2014-2024):** Gráfico de líneas que permite observar la evolución de las tecnologías, segmentado por provincia y filtro por trimestre.  
   - **Ingresos por Trimestre:** Tarjetas dinámicas que muestran la tasa de crecimiento anual de los ingresos del sector de Internet entre 2014 y 2024.  
   
   Todo esto se puede analizar a través de filtros por año y trimestre, ofreciendo una visión clara del crecimiento en la penetración de Internet y los ingresos a nivel nacional y provincial.

3. **Proyección de Accesos por Cada 100 Hogares:**  
   Visualización de un mapa de provincias segmentadas según el nivel de acceso a internet:  
   - **Bajo (Azul):** Menores a 50 accesos.  
   - **Medio (Verde):** Entre 51 y 70 accesos.  
   - **Alto (Rosa):** Más de 71 accesos.  
   
   También incluye una comparativa de barras de los accesos por provincia, con la posibilidad de filtrar por región. El objetivo es identificar las provincias que necesitan más inversión en infraestructura de conectividad.

4. **Proyección de Velocidad Media:**  
   Mapa segmentado por velocidad media:  
   - **Bajo (Azul):** Velocidades menores a 50 Mbps.  
   - **Medio (Verde):** Entre 50 y 95 Mbps.  
   - **Alto (Rosa):** Más de 95 Mbps.  
   
   Además, incluye una comparativa de barras por provincia con la opción de aplicar filtros para evaluar la evolución de la velocidad media por región.

5. **Proyección de Penetración de Fibra Óptica:**  
   Mediante un gráfico de áreas apiladas, se visualiza el crecimiento proyectado de la penetración de fibra óptica para el próximo trimestre en las provincias con menor adopción, teniendo en cuenta un objetivo del 10% de crecimiento del KPI. Adicionalmente, se analiza la velocidad media en estas provincias para evaluar el impacto potencial de las mejoras en infraestructura.

---

## Análisis Teórico

A lo largo del proyecto, se realizaron varios análisis clave sobre la conectividad en Argentina:

✦ **Análisis de la Hoja Velocidad Sin Rangos:**  
   Se identificaron las 30 velocidades más frecuentes, que varían entre 6 Mbps y 50 Mbps. Esto refleja una tendencia hacia velocidades más altas y estables, que son preferidas por los usuarios.  
   ![Velocidades Frecuentes](https://github.com/user-attachments/assets/54c14a05-4f96-4c75-9cfc-51bafddf9d54)

✦ **Análisis de la Hoja Velocidad Media por Provincia:**  
   Se observó una tendencia ascendente en la velocidad media de conexión, lo que sugiere una migración hacia tecnologías más rápidas y estables como la fibra óptica. Sin embargo, existe una notable desigualdad regional, con picos en Ciudad de Buenos Aires de 229 Mbps y Chubut con 20.5 Mbps, lo que representa un mercado potencial en provincias con velocidades medias bajas.  
   ![Velocidad Media](https://github.com/user-attachments/assets/d5dece08-033f-451f-a91b-75fd7108d4d4)

✦ **Análisis de la Hoja Totales Accesos por Tecnología:**  
   Se observó un crecimiento significativo en tecnologías modernas, como la fibra óptica, en detrimento de las tecnologías más antiguas, como el ADSL:  
   - **Crecimiento Anual de Fibra Óptica (2014-2024):** 38.95%  
   - **Crecimiento Anual de ADSL (2014-2024):** -14.62%  
   - **Crecimiento Anual de Cablemodem (2014-2024):** 8.97%  
   - **Crecimiento Anual de Wireless (2014-2024):** 22.77%  
   ![Accesos por Tecnología](https://github.com/user-attachments/assets/e0ffb53b-5287-4d6e-9d83-551e4a0ed3b3)

✦ **Análisis de la Hoja Accesos por Tecnología:**  
   Las provincias muestran una enorme disparidad en el acceso a Internet, lo que sugiere oportunidades significativas para mejorar la conectividad en áreas rurales y menos desarrolladas.  
   ![Accesos por Tecnología](https://github.com/user-attachments/assets/62ea65eb-3a1c-4d58-896d-726ff6e8ebec)

✦ **Análisis de la Hoja Penetración Poblacional:**  
   Se analizaron las provincias con menor acceso por cada 100 habitantes, destacando aquellas que podrían beneficiarse de una mayor inversión en infraestructura de conectividad.  
   ![Penetración Poblacional](https://github.com/user-attachments/assets/f06eb66c-93d1-4608-adf1-ba764133be53)

✦ **Análisis de la Hoja Penetración por Hogares:**  
   Se observó un aumento constante en los accesos a internet, especialmente en el primer trimestre de 2023 y 2024.  
   ![Penetración por Hogares](https://github.com/user-attachments/assets/776fdf62-5802-41d4-a728-a6fd1f5e627d)

✦ **Análisis de la Hoja Ingresos:**  
   El análisis muestra un crecimiento acelerado de los ingresos a partir de 2020, impulsado posiblemente por factores externos como la pandemia y la mayor digitalización. Esto sugiere un cambio positivo en la estrategia del mercado.  
   ![Ingresos](https://github.com/user-attachments/assets/2d53281d-3429-4f50-b065-13c1a471a6a3)

Con estas observaciones, se pudo obtener una idea más clara sobre las recomendaciones a realizar a la empresa.

---

## Resultados

Basado en los KPIs analizados, se sugieren las siguientes recomendaciones:

1. **Optimización de Infraestructura:** Invertir en mejorar la infraestructura de fibra óptica en provincias con baja penetración, apuntando a un crecimiento del 10% anual en la adopción de fibra óptica.
   
2. **Focalización Regional:** Desarrollar campañas de marketing dirigidas a provincias con menores velocidades medias de internet, enfocándose en la migración hacia conexiones de mayor velocidad.
   
3. **Mejora en Tecnologías Obsoletas:** Reducir progresivamente el acceso a tecnologías obsoletas como ADSL, priorizando la migración hacia tecnologías más modernas como el cablemódem y fibra óptica.
   
4. **Promociones Estacionales:** Lanzar promociones de servicios de internet de alta velocidad en el cuarto trimestre del año, aprovechando el aumento del consumo digital durante eventos y festividades de fin de año.

---

## Autor

✦ Este proyecto fue realizado por **Karen Lizeth Barbosa Rojas**.
