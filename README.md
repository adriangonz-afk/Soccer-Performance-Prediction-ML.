# Sports Performance Analytics: Cebollitas FC

End-to-end sports analytics system. Predicts match outcomes using Random Forest (R²=0.83) vs Linear Regression, and segments players via K-Means Clustering & PCA. Includes Deep Learning implementation with PyTorch and NLP for sentiment analysis.

## Executive Summary
Sistema integral de análisis de datos deportivos que combina Machine Learning Supervisado para predicción de resultados y Clustering No Supervisado para segmentación de jugadores. El proyecto evoluciona desde un análisis descriptivo hasta la implementación de Pipelines automatizados y redes neuronales con PyTorch.

Logro Técnico: Se mejoró la capacidad predictiva de la diferencia de goles, pasando de un modelo lineal ineficiente (R² aprox 0) a un modelo de Random Forest con un R² de 0.83 y un error absoluto medio (MAE) de 0.67 goles.

## Tech Stack & Advanced Techniques
* Core: Python, Pandas, NumPy.
* Machine Learning: Scikit-Learn (Random Forest, Linear Regression, K-Means, PCA).
* Deep Learning: PyTorch (Red Neuronal Feed-forward para clasificación).
* Automation: Scikit-Learn Pipelines (Pipeline, StandardScaler).
* NLP: Análisis de sentimientos en comentarios de aficionados (Regex/WordCloud).

## Model Performance

| Modelo | RMSE | R² Score | Conclusión |
| :--- | :--- | :--- | :--- |
| Linear Regression | 2.23 | -0.03 | Underfitting severo (No captura no-linealidad) |
| Random Forest | 0.90 | 0.83 | Modelo Seleccionado (Alta precisión) |

## Key Features

### 1. Player Segmentation (K-Means + PCA)
Se segmentó la plantilla en 3 clústeres basados en rendimiento (Goles, Asistencias, Precisión). [cite_start]El análisis de componentes principales (PCA) explicó el 67% de la varianza, validando visualmente la separación de roles tácticos[cite: 3].

### 2. Automated Pipelines
Implementación de sklearn.pipeline para encapsular el preprocesamiento (StandardScaler) y el modelado, evitando data leakage y facilitando el despliegue en producción.

### 3. Deep Learning Integration
Diseño de una red neuronal simple con PyTorch (RedSimple) utilizando optimizador Adam y función de pérdida BCELoss para tareas de clasificación binaria complementarias.

## Project Structure
* /data: Datasets de partidos y jugadores.
* PROYECTO_CEBOLLITAS_ML.ipynb: Notebook principal con todo el flujo de trabajo.
