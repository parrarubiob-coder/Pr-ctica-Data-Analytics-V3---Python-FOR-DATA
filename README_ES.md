# 📊 Análisis de Marketing Bancario con Python

## 🇬🇧 English Version
➡️ [Read the English version here](README.md)

---

## 🛠️ Tecnologías y Herramientas

![Python](https://img.shields.io/badge/Python-3.12-blue?style=for-the-badge&logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?style=for-the-badge&logo=pandas)
![NumPy](https://img.shields.io/badge/NumPy-Numerical%20Computing-013243?style=for-the-badge&logo=numpy)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-orange?style=for-the-badge)
![Seaborn](https://img.shields.io/badge/Seaborn-Statistical%20Visualization-4C72B0?style=for-the-badge)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter)
![VSCode](https://img.shields.io/badge/VSCode-IDE-007ACC?style=for-the-badge&logo=visualstudiocode)

---

# 📑 Tabla de Contenidos

- [Descripción del Proyecto](#-descripción-del-proyecto)
- [Objetivo de Negocio](#-objetivo-de-negocio)
- [Datasets](#-datasets)
- [Proceso del Proyecto](#-proceso-del-proyecto)
- [Limpieza de Datos](#-limpieza-de-datos)
- [Análisis Exploratorio](#-análisis-exploratorio)
- [Visualizaciones](#-visualizaciones)
- [Principales Hallazgos](#-principales-hallazgos)
- [Recomendaciones de Negocio](#-recomendaciones-de-negocio)
- [Estructura del Proyecto](#-estructura-del-proyecto)

---

# 📌 Descripción del Proyecto

Este proyecto consiste en un Análisis Exploratorio de Datos (EDA) realizado con Python sobre campañas de marketing directo de una institución bancaria portuguesa.

El objetivo principal del proyecto es analizar el comportamiento de los clientes e identificar patrones relacionados con la contratación de depósitos a plazo bancario.

El análisis incluye:

- Limpieza y preprocesamiento de datos
- Análisis exploratorio de datos
- Análisis estadístico
- Visualización de datos
- Generación de insights orientados al negocio

---

# 🎯 Objetivo de Negocio

Las campañas de marketing bancario buscan maximizar la conversión de clientes optimizando recursos y estrategias de comunicación.

Este proyecto tiene como objetivo:

- Identificar perfiles de clientes con mayor probabilidad de conversión
- Detectar variables que influyen en el éxito de las campañas
- Comprender patrones de comportamiento de los clientes
- Generar insights para mejorar futuras campañas de marketing

---

# 🗂️ Datasets

## 1️⃣ bank-additional.csv

Dataset principal con información sobre campañas de marketing bancario.

### Variables principales

| Variable | Descripción |
|---|---|
| age | Edad del cliente |
| job | Profesión |
| marital | Estado civil |
| education | Nivel educativo |
| duration | Duración del último contacto |
| campaign | Número de contactos durante la campaña |
| previous | Número de contactos previos |
| poutcome | Resultado de campañas anteriores |
| euribor3m | Tipo de interés Euribor |
| y | Resultado de conversión (sí/no) |

---

## 2️⃣ customer-details.xlsx

Dataset en Excel con información demográfica y de comportamiento de clientes.

El archivo contiene 3 hojas correspondientes a diferentes años.

### Variables principales

| Variable | Descripción |
|---|---|
| Income | Ingresos anuales |
| Kidhome | Número de niños en el hogar |
| Teenhome | Número de adolescentes en el hogar |
| Dt_Customer | Fecha de alta del cliente |
| NumWebVisitsMonth | Visitas mensuales al sitio web |
| ID | Identificador único del cliente |

---

# ⚙️ Proceso del Proyecto

El proyecto fue desarrollado siguiendo las siguientes etapas:

1. Carga de datos
2. Limpieza y preprocesamiento
3. Unión de datasets
4. Análisis exploratorio
5. Análisis estadístico
6. Visualización de datos
7. Conclusiones y recomendaciones de negocio

---

# 🧹 Limpieza de Datos

Principales tareas realizadas:

- Tratamiento de valores nulos
- Eliminación de duplicados
- Estandarización de nombres de columnas
- Revisión de tipos de datos
- Unión de datasets
- Detección de inconsistencias

### Ejemplo

```python
df.columns = df.columns.str.lower()
```

---

# 🔍 Análisis Exploratorio

El análisis exploratorio se centró en:

- Distribución de variables numéricas
- Análisis de variables categóricas
- Correlación entre variables
- Segmentación de clientes
- Análisis de conversiones
- Patrones de comportamiento

### Técnicas utilizadas

```python
df.describe()
df.groupby()
df.value_counts()
df.corr()
```

---

# 📊 Visualizaciones

El proyecto incluye varias visualizaciones desarrolladas con Matplotlib y Seaborn.

### Principales visualizaciones

- Histogramas
- Countplots
- Boxplots
- Heatmaps de correlación
- Scatterplots
- Gráficos de análisis de conversiones

---

## Heatmap de Correlación

```python
sns.heatmap(correlacion, cmap='coolwarm')
```

![Correlation Heatmap](Images/heatmap.png)

---

## Distribución de Conversiones

Visualización comparando clientes que contrataron el depósito frente a los que no.

![Conversion Distribution](Images/conversion_distribution.png)

---

## Conversión por Profesión

Análisis de las tasas de conversión según perfil profesional.

![Conversion by Job](Images/conversion_by_job.png)

---

# 📈 Principales Hallazgos

- Los clientes con llamadas de mayor duración mostraron mejores tasas de conversión
- Las campañas exitosas previas aumentaron la probabilidad de contratación
- Algunos perfiles profesionales obtuvieron mejores resultados de conversión
- Indicadores económicos como el Euribor influyeron en las decisiones de los clientes
- Los clientes con mayor interacción digital mostraron patrones interesantes de comportamiento

---

# 📌 Métricas Clave

## Tasa de Conversión

La tasa de conversión se calculó utilizando:

```python
conversion_rate = (df['y'].value_counts(normalize=True)['yes']) * 100
```

---

# 💡 Recomendaciones de Negocio

- Priorizar clientes con resultados positivos en campañas anteriores
- Mejorar las estrategias de segmentación de clientes
- Optimizar la duración y timing de las llamadas
- Desarrollar estrategias de marketing más personalizadas
- Incrementar el enfoque en clientes digitalmente activos

---

# 📁 Estructura del Proyecto

```bash
bank-marketing-analysis/
│
├── Data/
│   ├── Raw/
│   │   ├── bank-additional.csv
│   │   └── customer-details.xlsx
│   │
│   └── Processed/
│       └── bank_marketing_clean.csv
│
├── Notebooks/
│   ├── bank_marketing_eda_es.ipynb
│   └── bank_marketing_eda_en.ipynb
│
├── Images/
│   ├── heatmap.png
│   ├── conversion_distribution.png
│   └── conversion_by_job.png
│
├── README.md
├── README_ES.md
├── requirements.txt
└── .gitignore
```

---

# 📚 Principales Librerías Utilizadas

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
```

---

# 👩‍💻 Autor

**Beatriz Parra Rubio**
