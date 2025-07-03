# Análisis y Modelado de Popularidad de Canciones con SMUSIC.csv
![pca_3d_suave](https://github.com/user-attachments/assets/35b2a338-d14f-4540-864a-41d77de456e1)

## Descripción

Este proyecto aborda un análisis profundo y completo del dataset `SMUSIC.csv`, que contiene información detallada sobre canciones y artistas. El objetivo principal es entender qué factores influyen en la popularidad de una canción y construir un modelo predictivo robusto para predecir si una canción será popular o no.

La experiencia abarca desde la exploración inicial de datos hasta la construcción de modelos avanzados y la implementación de un sistema interactivo para la toma de decisiones basadas en los resultados.

---

## Análisis realizado

### Análisis Exploratorio Descriptivo

- Se examinaron las distribuciones de las variables numéricas y categóricas con estadísticas básicas, histogramas y boxplots.
- Se detectaron valores atípicos (outliers) y se evaluó la presencia de valores nulos.
- Se analizaron las características principales del dataset, como la cardinalidad de variables categóricas y la relación entre variables mediante matrices de correlación.
![1output](https://github.com/user-attachments/assets/c5f5120d-43f4-4ddd-bcfb-dd8c999d40a2)

### Análisis Diagnóstico

- Se identificaron problemas potenciales en los datos, como valores faltantes en `genres` y alta correlación entre variables (`artist_popularity` y `track_popularity`).
- Se evaluó la distribución de la variable objetivo (`popular`) y la presencia de clases desbalanceadas.
- Se examinaron variables numéricas para detectar outliers que pudieran afectar el modelado.

Este enfoque diagnóstico permitió tomar decisiones informadas sobre el preprocesamiento necesario para preparar el dataset para modelado.

---

## Modelado Predictivo

- Se seleccionaron y entrenaron diversos modelos de clasificación supervisada:  
  - Regresión Logística  
  - Random Forest  
  - Support Vector Machine (SVM)  
  - Gradient Boosting (XGBoost)  
- Se combinó un modelo de ensamble por votación (VotingClassifier) para aprovechar la complementariedad de los modelos individuales y mejorar la robustez y precisión.
![output](https://github.com/user-attachments/assets/82909de2-4b2b-4425-824d-7a0a1cb7576a)

- Se implementó un pipeline completo de preprocesamiento, que incluyó:  
  - Imputación de valores faltantes  
  - Codificación de variables categóricas  
  - Escalado de características numéricas  
  - Selección y separación de variables predictoras y objetivo  

- El desempeño del ensamble fue evaluado con métricas clave como precisión, recall, F1-score y matriz de confusión, mostrando resultados sólidos para la tarea de predicción.

---

## Análisis Prescriptivo e Interactividad

- Se desarrolló un dashboard interactivo utilizando Dash para explorar el impacto de modificar variables clave en la probabilidad de popularidad predicha.
- Este enfoque prescriptivo permite simular escenarios y entender cómo diferentes características musicales afectan la popularidad estimada, facilitando la toma de decisiones basadas en datos reales.

---

## Archivos y Scripts

- `eda_descriptivo.py` – Análisis descriptivo y visualización exploratoria.  
- `eda_diagnostico.py` – Análisis de calidad de datos y diagnóstico de problemas.  
- `preprocesamiento.py` – Limpieza, imputación, codificación y escalado.  
- `modelado.py` – Entrenamiento, evaluación y ensamblaje de modelos.  
- `dashboard_prescriptivo.py` – Dashboard para simulación y predicción interactiva.  
- Modelos y objetos guardados (`modelo_voting.pkl`, `scaler.pkl`, `feature_names.pkl`).

---

## Requisitos

- Python 3.8+  
- pandas, numpy, scikit-learn, matplotlib, seaborn, plotly, dash, joblib, scipy

Instalar con:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn plotly dash joblib scipy
