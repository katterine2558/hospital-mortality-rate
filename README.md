# 🏥 Hospital Mortality Prediction

Este proyecto implementa un modelo de **Machine Learning** para predecir la **mortalidad hospitalaria de pacientes** a partir de variables clínicas y demográficas.  
El dataset utilizado contiene más de **9.000 registros y 26 variables**, incluyendo información fisiológica, comorbilidades y condiciones hospitalarias.

---

## 📌 Objetivo
Desarrollar un pipeline robusto que permita **preprocesar datos, reducir dimensionalidad y entrenar un modelo de clasificación**, priorizando la correcta detección de pacientes con mayor riesgo de fallecimiento durante la hospitalización.

---

## ⚙️ Metodología

1. **EDA (Exploratory Data Analysis):**
   - Detección de outliers.
   - Análisis de correlaciones.
   - Manejo de valores nulos.

2. **Preprocesamiento:**
   - Escalamiento con **RobustScaler** para mitigar el efecto de outliers.
   - Codificación de variables categóricas con **OneHotEncoder**.

3. **Modelado:**
   - Reducción de dimensionalidad con **PCA**.
   - Clasificación con **Support Vector Machine (SVM)** usando `class_weight="balanced"`.

4. **Optimización:**
   - Búsqueda de hiperparámetros con **GridSearchCV**.
   - Validación cruzada con **K-Fold**.

5. **Evaluación:**
   - Métricas: Recall, Precision, F1-score, ROC-AUC y PR-AUC.
   - Priorización del **recall** por ser clínicamente más importante reducir falsos negativos.

---

## 📊 Resultados

- **ROC-AUC:** 0.94  
- **PR-AUC:** 0.86  
- **Recall (clase positiva):** 0.90  
- **Accuracy global:** 0.86  

El modelo alcanzó un **alto poder discriminativo**, cumpliendo con el objetivo de maximizar la detección de casos positivos (pacientes fallecidos), aunque con una precisión moderada debido a falsos positivos.

---

## 🚀 Futuras mejoras

- Aplicar técnicas de **resampling (SMOTE, undersampling)**.  
- Ajuste de **umbrales de decisión** para balancear recall y precisión.  
- Probar **modelos ensemble** (Random Forest, XGBoost, etc.) para mejorar desempeño.  

---

## 🛠️ Requisitos

El proyecto fue desarrollado en **Python 3.9+** con las siguientes librerías principales:

```bash
pandas
numpy
scikit-learn
matplotlib
seaborn
ydata-profiling  
