#  Corporate Financial Health Scoring & Bankruptcy Risk Intelligence
### End-to-End Data Pipeline for Enterprise Risk Management

**Autor:** Rafael Aguayo  
**Fecha:** Julio 2026  
**Estado:** ✅ Completado y Desplegado  
**Tecnologías:** Python, BigQuery, Scikit-Learn, Google Data Studio

---

##  Resumen Ejecutivo

Este proyecto desarrolla una **plataforma de inteligencia de riesgo financiero** que transforma 96 variables financieras crudas en un **Índice de Salud Corporativa (0-100)** y un sistema de clasificación de riesgo (BAJO/MEDIO/ALTO/CRÍTICO). 

El sistema logró identificar al **92.2% de las quiebras** concentrándolas en el 25% de la población con mayor riesgo, alcanzando un **AUC de 0.9266** basado en un **sistema heurístico de scoring financiero validado mediante análisis estadístico riguroso**.

---

## 🎯 Impacto de Negocio

###  **Valor Generado:**
- **Detección Temprana:** Identificación de empresas con alto riesgo financiero antes de la quiebra.
- **Optimización de Recursos:** Priorización de auditorías y análisis crediticios en el 25% de la cartera que concentra el 92% del riesgo.
- **Reducción de Pérdidas:** Alertas preventivas que permiten actuar antes del colapso financiero.
- **Segmentación Automática:** Clasificación de clientes según salud financiera para políticas de crédito diferenciadas.
- **Dashboard Ejecutivo:** Visualización en tiempo real para toma de decisiones estratégicas.

###  **ROI Potencial:**
Si una empresa con cartera de $100M tiene una tasa de quiebra del 3.2% ($3.2M en riesgo), este sistema permite:
- Detectar el 92% de las quiebras anticipadamente.
- Reducir pérdidas en ~$2.9M mediante acciones preventivas.
- Optimizar costos de auditoría enfocándose solo en el 25% de alto riesgo.

---

## 🛠️ Stack Tecnológico

| Categoría | Herramientas |
|:---|:---|
| **Lenguaje** | Python 3.10+ |
| **Procesamiento** | Pandas, NumPy, SciPy |
| **Machine Learning** | Scikit-Learn (RobustScaler, métricas de clasificación) |
| **Cloud Warehouse** | Google BigQuery |
| **Computación** | Google Colab |
| **Business Intelligence** | Google Data Studio (Looker Studio) |
| **Visualización** | Matplotlib, Seaborn |
| **Formatos** | CSV, Parquet |

---

## 📂 Recursos del Proyecto

📁 **Repositorio Completo:**  
🔗 [Taiwan Bankruptcy Project - GitHub](https://github.com/Rafael-Aguayo/Taiwan-Bankruptcy-Prediction-End-to-End-Data-Pipeline-Risk-Intelligence)

📁 **Carpeta de Google Drive (Notebooks y Datos):**  
 [Acceso a Notebooks y Dataset](https://drive.google.com/drive/folders/1CRgVVyBJtoazWdRA5vq6FLeH5ZrRFjsZ?usp=sharing)

📊 **Dashboard Interactivo:**  
🔗 [Data Studio Dashboard - Enlace Público](https://datastudio.google.com/reporting/c436128b-68d5-4f0f-aa00-3912d5982a56)

---

## ️ Arquitectura del Pipeline

```text
[Fuente: data.csv - 96 variables] 
       │
       ▼ (Fase 1: Limpieza de Esquema con Regex)
[BigQuery: datos_crudos] ─(Extracción vía API)──
       │                                          │
       ▼ (Fase 2: Transformación en Colab)        │
[Google Colab: Pandas/Scikit-Learn]              │
       ├─► Feature Selection (96 → 10 vars)       │
       ├─► RobustScaler + Clipping (±3 IQR)       │
       ├─► Inversión de variables negativas       │
       └─► Clasificación por percentiles          │
       │                                          │
       ▼ (Checkpoint de Calidad: Parquet)         │
[Google Drive: datos_analisis_final.parquet]      │
       │                                          │
       ▼ (Fase 3: Carga Idempotente)              │
[BigQuery: datos_analisis_final] ◄───────────────┘
       │
       ▼
[Data Studio: Dashboard Ejecutivo]
       ▼
[Data Studio: Dashboard de Inteligencia de Riesgo]

```

### 📊 SECCIÓN 1: Vista Ejecutiva y Distribución de Riesgo

![Vista Ejecutiva](https://raw.githubusercontent.com/Rafael-Aguayo/Taiwan-Bankruptcy-Prediction-End-to-End-Data-Pipeline-Risk-Intelligence/main/dashboard1.png)

---

### 📉 SECCIÓN 2: Análisis de Quiebras y Poder Predictivo

![Análisis de Quiebras](https://raw.githubusercontent.com/Rafael-Aguayo/Taiwan-Bankruptcy-Prediction-End-to-End-Data-Pipeline-Risk-Intelligence/main/dasboard2.png)

---

### 📈 SECCIÓN 3: Distribución Estadística y Correlaciones

![Distribución Estadística](https://raw.githubusercontent.com/Rafael-Aguayo/Taiwan-Bankruptcy-Prediction-End-to-End-Data-Pipeline-Risk-Intelligence/main/dashboard3.png)

---

### 🧠 SECCIÓN 4: Análisis Multidimensional de Factores de Riesgo

![Análisis Multidimensional](https://raw.githubusercontent.com/Rafael-Aguayo/Taiwan-Bankruptcy-Prediction-End-to-End-Data-Pipeline-Risk-Intelligence/main/dashboard4.PNG)
