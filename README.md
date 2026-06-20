# EverPeak Retail Analysis – Sprint 6

Este repositorio contiene el proyecto final de análisis de datos enfocado en la calidad de la información, tratamiento de valores atípicos e ingeniería de características (*Feature Engineering*) para el caso de negocio de **EverPeak – SilverBasket**.

## ▶ Cómo abrir el notebook en Google Colab

Haz clic en el siguiente botón para abrir el análisis interactivo directamente en la nube:

[![Open In Colab](https://google.com)](https://google.com)

---

## 🧠 Descripción del Caso EverPeak
La gerencia de marketing y finanzas de EverPeak requiere transformar sus datos crudos de transacciones en información útil para la toma de decisiones estratégicas. El dataset original (`everpeak_retail.csv`) cuenta con 2,000 registros que simulan problemas reales del entorno retail:
- Presencia de valores nulos o ausentes (`NaN`).
- Registros duplicados y valores centinela.
- Valores extremos (*outliers*) que distorsionan los promedios globales de venta.

El objetivo es construir un pipeline automatizado y robusto que limpie los datos, aísle o trate los outliers mediante técnicas estadísticas como la **Winsorización** (capado al percentil 99) y genere una segmentación avanzada de clientes basada en su edad, comportamiento de compra y métodos de pago.

---

## 📂 Contenido del Notebook

El archivo principal `notebooks/everpeak_analysis.ipynb` está estructurado bajo las mejores prácticas analíticas e incluye:
1. **Visión General e Importación de Datos**: Inspección inicial con `.info()` y detección de nulos/duplicados.
2. **Pipeline de Limpieza**: Corrección de tipos de datos y manejo de sentinels.
3. **Estadísticas Descriptivas**: Análisis de la media y la mediana para detectar sesgos (*skewness*).
4. **Detección Formal de Outliers**: Aplicación de la regla del Rango Intercuartílico ($IQR$) y visualización con histogramas y diagramas de caja (*boxplots*).
5. **Tratamiento Estadístico**: Winsorización mediante el uso de `np.clip()` para estabilizar métricas sin eliminar clientes reales.
6. **Feature Engineering (Segmentación)**: Creación de etiquetas lógicas automatizadas con estructuras condicionales avanzadas en Python (`if`/`elif`/`else`) combinadas con `.apply(axis=1)` en Pandas.

---

## 📘 Cómo reproducir el análisis

1. Clonar este repositorio o descargarlo en tu máquina local.
2. Si prefieres trabajar localmente, asegúrate de contar con las librerías instaladas: `pandas`, `numpy`, `matplotlib` y `seaborn`.
3. Abre el entorno (Jupyter Notebook o Google Colab).
4. Ejecuta las celdas del archivo `everpeak_analysis.ipynb` de forma secuencial (de arriba hacia abajo) para asegurar la persistencia de las variables.
# everpeak-analysis
