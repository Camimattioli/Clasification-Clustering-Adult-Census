# Clasificación y Clustering - Adult Census Income

Predicción de nivel de ingreso (>50K o <=50K anuales) y segmentación de 
personas a partir del dataset Adult Census (UCI), con análisis de riesgos 
éticos asociados.

## Objetivo
predecir si una persona gana más o menos de USD 50.000 anuales a partir de variables demográficas y laborales (dataset Adult de UCI
Machine Learning Repository), aplicando un proceso completo de limpieza, preprocesamiento, clasificación (Decision Tree) y clustering (DBSCAN).

## Herramientas utilizadas
- Python (pandas, numpy)
- scikit-learn (MinMaxScaler, OneHotEncoder, LabelEncoder, DecisionTreeClassifier, DBSCAN, PCA, entre otras)
- matplotlib, seaborn

## Proceso
1. Limpieza de valores nulos
2. Detección de outliers
3. Codificación de variables 
4. Clasificación con Decision Tree
5. Clustering con DBSCAN (con y sin PCA)

## Resultados principales
- Tras la limpieza (eliminación de nulos en 'workclass', 'occupation' y 'native-country') se trabajó con un dataset reducido pero consistente, sin introducir sesgos relevantes ya que los nulos no se concentraban en una clase particular de ingreso.
- El Decision Tree alcanzó un accuracy de 0.82, aceptable como primer modelo base, aunque insuficiente por sí solo dado el desbalance de clases del dataset (se recomienda complementar con métricas como precision/recall o F1 por clase).

- El DBSCAN con reducción PCA permitió identificar agrupamientos naturales en los datos, aunque con pérdida de interpretabilidad de las variables originales; la comparación sin PCA confirmó que la reducción de dimensionalidad era necesaria para obtener clusters interpretables en tiempos razonables.
- Un análisis ético señala que variables como race, sex y native-country requieren tratamiento cuidadoso para evitar tanto la identificación indirecta de personas como el uso discriminatorio de las predicciones del modelo en contextos sensibles (ej. crédito, contratación).

## Ver el notebook completo
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Camimattioli/Clasificacion-Clustering-Adult-Census/blob/main/Adult_Census_Analisis.ipynb)
