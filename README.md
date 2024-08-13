# Predicción de Churn en Clientes

## Descripción del Proyecto
Este proyecto tiene como objetivo predecir la probabilidad de que un cliente haga "churn", es decir, que abandone el servicio ofrecido por una empresa. Para lograrlo, se han utilizado varios modelos de clasificación, junto con técnicas avanzadas de balanceo de clases y optimización de hiperparámetros.

## Estructura del Proyecto

- Preprocesamiento de Datos: Análisis exploratorio de datos, limpieza y transformación de características.
- Normalización: Los datos fueron escalados utilizando StandardScaler para garantizar que todas las características tengan una escala similar, lo cual es crucial para ciertos modelos de machine learning.
- División de Datos: Los datos se dividieron en conjuntos de entrenamiento y prueba en una proporción de 70-30.

## Técnicas de Balanceo de Clases:

- SMOTE (Synthetic Minority Over-sampling Technique): Se utilizó SMOTE para crear ejemplos sintéticos de la clase minoritaria (clientes que hacen churn) y así balancear las clases en el conjunto de datos de entrenamiento.
- Técnicas Combinadas (Over-Under Sampling): Se utilizó una combinación de submuestreo de la clase mayoritaria y sobremuestreo de la clase minoritaria para explorar mejoras en el rendimiento del modelo.

## Modelos Utilizados:

- Modelos Base:
    - Logistic Regression
    - Random Forest
    - XGBoost
    - K-Nearest Neighbors
    - Gradient Boosting
    - Decision Tree
    
- Stacking: Los mejores modelos fueron combinados utilizando un Stacking Classifier con optimización bayesiana para mejorar el rendimiento general.

## Optimización de Hiperparámetros: 

- Se utilizó Grid Search y BayesSearchCV para optimizar los hiperparámetros de los modelos y mejorar su rendimiento en términos de AUROC.

## Evaluación de Modelos:

- Métricas Evaluadas: Accuracy, Precision, F1 Score, AUROC.
- Análisis de Importancia de Características: Se utilizó SHAP para interpretar la importancia de las características en el modelo final.
- Resultados Comparativos: Se generaron tablas comparativas para analizar los resultados de las diferentes técnicas y modelos.

## Resultados

- Los modelos entrenados con SMOTE y técnicas combinadas de sobremuestreo y submuestreo mostraron diferencias en rendimiento, destacándose el AUROC como la métrica principal para evaluar la capacidad del modelo en discriminar entre clases.
- El Stacking Classifier optimizado con técnicas de balanceo combinadas y optimización bayesiana resultó en el mejor rendimiento general, logrando un AUROC de X.XXX (rellenar con tu valor).

## Conclusiones

- Importancia del Balanceo de Clases: El uso de técnicas de balanceo de clases, especialmente combinando sobremuestreo y submuestreo, es crucial en datasets con desbalanceo significativo, como es el caso del churn.
- Mejora Continua: Aunque la Logistic Regression mostró un buen rendimiento inicial, la combinación de modelos en un Stacking Classifier y la optimización de hiperparámetros llevó a una mejora significativa en la capacidad predictiva del modelo.
- Métricas Clave: Dado que el objetivo principal es identificar clientes que harán churn, la Precision y el AUROC fueron las métricas clave para este análisis, asegurando tanto la correcta identificación de clientes en riesgo como la discriminación efectiva entre las clases.

## Requisitos

- Python 3.x
- Bibliotecas necesarias (instalables mediante requirements.txt):
    - scikit-learn
    - imbalanced-learn
    - xgboost
    - shap
    - matplotlib
    - bayesian-optimization

## Instalacion

1. Clonar el repositorio:
```
git clone
```

2. Instalar las dependencias:
```
pip install -r requirements.txt
```

3. Ejecutar el notebook:
```
jupyter notebook
```

## Autor
Rooberto Olson