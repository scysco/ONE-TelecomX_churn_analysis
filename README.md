# 📊 Análisis de Evasión de Clientes (Churn) - Telecom X

![Python](https://img.shields.io/badge/Python-3.10%2B-blue.svg?style=for-the-badge&logo=python)
![Pandas](https://img.shields.io/badge/Pandas-2.x-blue.svg?style=for-the-badge&logo=pandas)
![Plotly](https://img.shields.io/badge/Plotly-5.x-blue.svg?style=for-the-badge&logo=plotly)
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/scysco/ONE-TelecomX_churn_analysis/blob/main/TelecomX_LATAM.ipynb)

---

## 📜 Tabla de Contenidos
1.  [Visión General del Proyecto](#%EF%B8%8F-visión-general-del-proyecto)
2.  [Instalación y Dependencias](#-instalación-y-dependencias)
3.  [Diccionario de Datos](#-diccionario-de-datos)
4.  [Resumen del Análisis](#-resumen-del-análisis)
5.  [Conclusiones Principales](#-conclusiones-principales)
6.  [Recomendaciones Estratégicas](#-recomendaciones-estratégicas)
7.  [Cómo Utilizar este Repositorio](#-cómo-utilizar-este-repositorio)

---

## 🎯 Visión General del Proyecto
Este proyecto presenta un análisis exploratorio de datos (EDA) de extremo a extremo sobre un conjunto de datos de una empresa de telecomunicaciones ficticia, "Telecom X". El objetivo principal es identificar los factores y perfiles de clientes que están más asociados con la evasión (churn), con el fin de proporcionar insights accionables para el negocio y preparar los datos para la construcción de un futuro modelo de machine learning predictivo.

---

## 🔧 Instalación y Dependencias
Para ejecutar el análisis contenido en el notebook de Jupyter, necesitarás tener Python 3.10 o superior y las siguientes librerías instaladas. Se recomienda crear un entorno virtual.

```bash
pip install pandas plotly jupyterlab
````

-----

## 📖 Diccionario de Datos

A continuación se describen las columnas clave del dataset final (`df_final`):

| Columna | Descripción | Tipo de Dato | Ejemplo |
|---|---|---|---|
| **`Churn`** | Variable objetivo. 1 si el cliente se fue, 0 si permanece. | `int64` | `1`, `0` |
| **`tenure`** | Meses de antigüedad del cliente en la compañía. | `int64` | `12`, `72` |
| **`Contract`** | Tipo de contrato del cliente. | `category` | `Month-to-month`, `One year` |
| **`InternetService`** | Tipo de servicio de internet contratado. | `category` | `Fiber optic`, `DSL`, `No` |
| **`TechSupport`** | Si el cliente tiene o no soporte técnico (1/0). | `category` | `1`, `0` |
| **`Charges.Monthly`**| Gasto mensual del cliente. | `float64` | `75.50` |
| **`Cuentas_Diarias`**| Gasto diario promedio del cliente. | `float64` | `2.48` |

-----

## 🔬 Resumen del Análisis

El análisis se llevó a cabo en varias fases metodológicas:

1.  **Extracción y Limpieza**: Los datos se cargaron desde un JSON, se normalizaron y se sometieron a un riguroso proceso de limpieza para manejar valores nulos, vacíos y tipos de datos incorrectos.
2.  **Optimización y Feature Engineering**: Los tipos de datos fueron optimizados para mejorar el rendimiento y se creó la característica `Cuentas_Diarias` para un análisis más granular.
3.  **Análisis Exploratorio de Datos (EDA)**: Se analizó la tasa de evasión general (26.54%) y se desglosó por múltiples variables demográficas, de contratación y de servicios para identificar los factores de mayor impacto.
4.  **Análisis de Segmentación**: Se combinaron los hallazgos para construir perfiles de clientes de "Alto Riesgo" y "Ultra Alto Riesgo", identificando los arquetipos de clientes con la mayor probabilidad de abandono.

-----

## 💡 Conclusiones Principales

El análisis reveló que la evasión no es aleatoria y está fuertemente correlacionada con:

  * **Tipo de Contrato**: El contrato **Mes a Mes** es el principal impulsor del churn.
  * **Servicios Clave**: La falta de **Soporte Técnico** y **Seguridad en Línea** aumenta drásticamente el riesgo de evasión.
  * **Tipo de Internet**: Clientes con **Fibra Óptica** tienen una tasa de churn significativamente más alta.
  * **Método de Pago**: El **Cheque Electrónico** está asociado a la tasa de churn más alta entre los métodos de pago.

Se identificó un perfil de **"Ultra Alto Riesgo"** (Contrato Mes a Mes + Fibra Óptica + Sin Soporte Técnico) con una **tasa de evasión del 57.52%**.

-----

## 🚀 Recomendaciones Estratégicas

1.  **Fidelizar Clientes "Mes a Mes"**: Crear campañas para migrar a clientes de alto riesgo a contratos de 1 o 2 años.
2.  **Empaquetar Servicios de Retención**: Ofrecer proactivamente Soporte Técnico y Seguridad en Línea a clientes de Fibra Óptica.
3.  **Optimizar la Experiencia de Pago**: Incentivar el cambio de Cheque Electrónico a métodos de pago automáticos.
4.  **Implementar un Modelo Predictivo**: Usar este dataset para que el equipo de Data Science construya un modelo que prediga el riesgo de churn de cada cliente.

-----

## 💻 Cómo Utilizar este Repositorio

Hay dos maneras de ejecutar este análisis:

### 1. Ejecución Local (con Jupyter)

1.  Clona el repositorio:
    ```bash
    git clone https://github.com/scysco/ONE-TelecomX_churn_analysis.git
    ```
2.  Navega a la carpeta del proyecto e instala las dependencias mencionadas anteriormente.
3.  Inicia Jupyter Lab:
    ```bash
    jupyter lab
    ```
4.  Abre el notebook `TelecomX_Analisis.ipynb` y ejecuta las celdas en orden.

### 2\. Ejecución en la Nube (con Google Colab)

Puedes abrir y ejecutar este notebook directamente en Google Colab.

  * **Opción A (Recomendada)**: Haz clic en el botón "Open In Colab" que se encuentra en la parte superior de este README.

  * **Opción B (Manual)**:
    1.  Ve a [Google Colab](https://colab.research.google.com/).
    2.  Selecciona la pestaña "GitHub", pega la URL de tu repositorio y presiona Enter.
    3.  Selecciona el notebook de la lista para abrirlo.

<!-- end list -->