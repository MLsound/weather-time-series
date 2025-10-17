# Análisis Exploratorio (EDA) de Series de Tiempo Climáticas

Este repositorio contiene un **Análisis Exploratorio de Datos (EDA)** detallado sobre un conjunto de datos meteorológicos a largo plazo, enfocándose en la identificación de patrones, características estacionales y relaciones entre las variables atmosféricas.

## 🇬🇧 English Summary

This repository presents a detailed **Exploratory Data Analysis (EDA)** of the **Weather Long-term Time Series Forecasting** dataset from Kaggle. The project focuses on cleaning, visualizing, and analyzing over 52,000 high-frequency meteorological records from the **Max Planck Institute** during the entire year of **2020**. Key activities include feature recognition, descriptive statistics, identification of extreme weather events, and a thorough correlation analysis between atmospheric variables like temperature, humidity, pressure, and solar radiation.

---

## 📝 Descripción del Proyecto

El notebook `Weather-TS-EDA.ipynb` realiza un estudio exhaustivo de un conjunto de datos de series de tiempo climáticas.

* **Origen de Datos:** El dataset proviene de [Kaggle Dataset](https://www.kaggle.com/datasets/alistairking/weather-long-term-time-series-forecasting).
* **Contenido del Dataset:** El conjunto de datos abarca mediciones tomadas cada **10 minutos** a lo largo de todo el **año 2020**, sumando más de **52.560 puntos de datos** por variable. Incluye **20 indicadores meteorológicos** (temperatura, humedad, patrones de viento, radiación, precipitación y cantidades derivadas) medidos en una estación del **Instituto Max Planck**.
* **Objetivo:** Preparar los datos y obtener *insights* valiosos que servirán de base para futuros proyectos de *Machine Learning* y pronóstico de series de tiempo.

## 🚀 Contenido del Notebook (`Weather-TS-EDA.ipynb`)

El análisis está estructurado en las siguientes secciones principales:

1.  **Importación y Descripción del Dataset:** Carga de datos, reconocimiento de *features* (variables) y estadísticas descriptivas básicas (`df.head()`, `df.info()`, `df.describe().T`).
2.  **Ingeniería de Características de Tiempo:** Extracción de variables temporales (`hour`, `month`, `day`) e identificación de **Eventos Extremos** (máximas y mínimas de temperatura, viento y lluvia diaria).
3.  **Análisis de Correlación entre Variables:** Estudio de las relaciones lineales entre los indicadores meteorológicos.
    * Se observa una fuerte correlación positiva entre las variables de temperatura (`T`, `Tpot`, `Tdew`).
    * Existe una correlación negativa entre la **Radiación de Onda Corta ($SWDR$)** y la **Humedad Relativa ($rh$)** (días más soleados son menos húmedos).
    * Las variables de **Lluvia** muestran una correlación muy débil con la mayoría de los otros indicadores, lo que sugiere su naturaleza estocástica.

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
Asegúrate de que el archivo de datos ([cleaned_weather.csv](cleaned_weather.csv)) esté en el directorio raíz o en la ruta especificada en la celda de importación de datos.

Alternativamente puede ser descargado desde [Kaggle](https://www.kaggle.com/datasets/alistairking/weather-long-term-time-series-forecasting).

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