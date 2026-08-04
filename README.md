# Classification and Clustering - Adult Census Income

Income level prediction (>50K or <=50K per year) and population segmentation 
based on the Adult Census dataset (UCI).

## Objective
Predict whether a person earns more or less than USD 50,000 per year based on 
demographic and employment variables (the Adult dataset from the UCI Machine 
Learning Repository), applying a full process of cleaning, preprocessing, 
classification (Decision Tree), and clustering (DBSCAN).

## Tools used
- Python (pandas, numpy)
- scikit-learn (MinMaxScaler, OneHotEncoder, LabelEncoder, DecisionTreeClassifier, DBSCAN, PCA, among others)
- matplotlib, seaborn

## Process
1. Handling missing values
2. Outlier detection
3. Variable encoding
4. Classification with Decision Tree
5. Clustering with DBSCAN (with and without PCA)

## Main results
- After cleaning (removing nulls in 'workclass', 'occupation', and 'native-country'), the resulting dataset was smaller but consistent, without introducing significant bias since the nulls were not concentrated in a particular income class.
- The Decision Tree achieved an accuracy of 0.82, acceptable as a first baseline model, though insufficient on its own given the dataset's class imbalance (it is recommended to complement it with metrics such as precision/recall or F1 per class).
- DBSCAN with PCA reduction made it possible to identify natural groupings in the data, although with some loss of interpretability of the original variables; the comparison without PCA confirmed that dimensionality reduction was necessary to obtain interpretable clusters within a reasonable amount of time.

## Notebook
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Camimattioli/Clasificacion-Clustering-Adult-Census/blob/main/Adult_Census_Analisis.ipynb)

--------------------------------------

# Clasificación y Clustering - Adult Census Income

Predicción de nivel de ingreso (>50K o <=50K anuales) y segmentación de 
personas a partir del dataset Adult Census (UCI).

## Objetivo
Predecir si una persona gana más o menos de USD 50.000 anuales a partir de variables demográficas y laborales (dataset Adult de UCI
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

## Ver el notebook completo
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Camimattioli/Clasificacion-Clustering-Adult-Census/blob/main/Adult_Census_Analisis.ipynb)
