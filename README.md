# Análisis Exploratorio (EDA) de Series de Tiempo Climáticas

Este repositorio contiene un **Análisis Exploratorio de Datos (EDA)** detallado sobre un conjunto de datos meteorológicos a largo plazo, enfocándose en la identificación de patrones, características estacionales y relaciones entre las variables atmosféricas.

## 🇬🇧 English Summary

This repository presents a detailed **Exploratory Data Analysis (EDA)** of the **Weather Long-term Time Series Forecasting** dataset from Kaggle. The project focuses on cleaning, visualizing, and analyzing over 473,111 high-frequency meteorological records from the **Max Planck Institute** during **8 years**. Key activities include feature recognition, descriptive statistics, identification of extreme weather events, and a thorough correlation analysis between atmospheric variables like temperature, humidity, pressure, and solar radiation.

---

## 📝 Descripción del Proyecto

El notebook `Weather-TS-EDA.ipynb` realiza un estudio exhaustivo de un conjunto de datos de series de tiempo climáticas correspondientes al período 2009 a 2016 y del año 2020.

* **Origen de Datos:** se dispone de 2 datasets provientes de Kaggle:
    1. [Dataset year 2020](https://www.kaggle.com/datasets/alistairking/weather-long-term-time-series-forecasting)
    2. [Dataset years 2009-2016](https://www.kaggle.com/datasets/arashnic/max-planck-weather-dataset)

* **Contenido del Dataset:** El conjunto de datos abarca mediciones tomadas cada **10 minutos** a lo largo de **8 años**, **473.111 puntos de datos** con **+14 indicadores meteorológicos** (temperatura, humedad, patrones de viento, radiación, precipitación y cantidades derivadas) medidos en una estación del **Instituto Max Planck**.

    1. **Datos 2020:** Incluye **52.560 puntos de datos** con **20 indicadores meteorológicos** (temperatura, humedad, patrones de viento y cantidades derivadas). Cuenta además con 6 indicadores adicionales (de precipitación y radiación solar). [**Resultados EDA**](Weather-TS-EDA.ipynb)
    2. **Datos 2009-2016:** Incluye **420.551 puntos de datos** con **14 indicadores meteorológicos** (temperatura, humedad, patrones de viento y cantidades derivadas). [**Resultados EDA**](Weather-TS-EDA2.ipynb)

* **Objetivo:** Preparar los datos y obtener *insights* valiosos que servirán de base para futuros proyectos de *Machine Learning* y pronóstico de series de tiempo.

## 🚀 Contenido del Notebook (`Weather-TS-EDA.ipynb`)

El análisis está estructurado en las siguientes secciones principales:

1.  **Importación y Descripción del Dataset:** Carga de datos, reconocimiento de *features* (variables) y estadísticas descriptivas básicas.
2.  **Ingeniería de Características de Tiempo:** Extracción de variables temporales (`hour`, `month`, `day`) e identificación de **Eventos Extremos** (máximas y mínimas de temperatura, viento y lluvia diaria).
3.  **Análisis de Correlación entre Variables:** Estudio de las relaciones lineales entre los indicadores meteorológicos.
    * Se observa una fuerte correlación positiva entre las variables de temperatura (`T`, `Tpot`, `Tdew`).
    * Existe una correlación negativa entre la **Radiación de Onda Corta ($SWDR$)** y la **Humedad Relativa ($rh$)** (días más soleados son menos húmedos).
    * Las variables de **Lluvia** muestran una correlación muy débil con la mayoría de los otros indicadores, lo que sugiere su naturaleza estocástica.

***NOTA:*** este Notebook fue utilizado para ambos subconjuntos con pequeñas modificaciones.

## 🛠️ Tecnologías y Requisitos

Este proyecto requiere un entorno de Python 3 y las siguientes librerías:

* `jupyter`
* `pandas`
* `numpy`
* `matplotlib.pyplot`
* `seaborn`
* `statsmodels` (para análisis de series de tiempo)

## 💻 Instrucciones de Ejecución

Sigue estos pasos para configurar tu entorno y ejecutar el análisis:

### 1. Inicializa el Entorno
Si no tienes **Jupyter Notebook** instalado, puedes instalarlo (junto con el resto de librerías esenciales) usando `pip`:

```bash
pip install jupyter
```

### 2. Obten el Dataset
Asegúrate de que el archivo de datos CSV correspondiente esté en el directorio raíz o en la ruta especificada en la celda de importación de datos.

Alternativamente pueden ser descargados desde Kaggle: [2020](https://www.kaggle.com/datasets/alistairking/weather-long-term-time-series-forecasting) / [2009-2016](https://www.kaggle.com/datasets/arashnic/max-planck-weather-dataset)

### 3. Abre el Notebook
Una vez que tengas Jupyter instalado, inicia y abre el archivo en tu navegador:

```bash
jupyter notebook Weather-TS-EDA.ipynb
```

### 4. Instala las dependencias
Pueden ser instaladas dentro del cuaderno Jupyter o ejecutando el siguiente comando:

```bash
pip install pandas numpy matplotlib seaborn statsmodels
```

### 5. Ejecuta el Análisis
Dentro del entorno Jupyter, ejecuta las celdas secuencialmente para replicar todo el proceso de Análisis Exploratorio de Datos (EDA).