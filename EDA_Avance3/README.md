# Análisis Exploratorio de Datos (EDA)

Este repositorio contiene el código y la documentación asociada con el Análisis Exploratorio de Datos (EDA) realizado en un conjunto de datos específico. El objetivo de este README es proporcionar una visión general del EDA realizado y los hallazgos clave.

## Preguntas Abordadas a través del EDA

### ¿Qué algoritmo se puede utilizar como baseline para predecir las variables objetivo? 

### ¿El modelo está sub/sobreajustando los datos de entrenamiento?

### ¿Cuál es la métrica adecuada para este problema de negocio? 


Utilizamos el Decision Tree, Random Forest, SVM, KNN

Mostando los siguientes resultados:

## Decision Tree

-Entrenamiento:

MSE: 0.784

MAE: 0.037

R²: 0.331

-Prueba:

MSE: 0.264

MAE: 0.043

R²: 0.166

### Interpretación: 

El modelo muestra un rendimiento aceptable pero con un cierto grado de sobreajuste, ya que el rendimiento en el conjunto de entrenamiento es mejor que en el de prueba.

## Gradient Boosting

-Entrenamiento:

MSE: 1.073

MAE: 0.061

R²: 0.084

-Prueba:

MSE: 0.260

MAE: 0.058

R²: 0.179

### Interpretación: 

Aunque el MSE en el conjunto de entrenamiento es mayor, el rendimiento en el conjunto de prueba es mejor que en los modelos anteriores, indicando una mejor generalización.

## Support Vector Regressor (SVR)

-Entrenamiento:

MSE: 1.172

MAE: 0.123

R²: -0.001

-Prueba:

MSE: 0.317

MAE: 0.119

R²: -0.003

### Interpretación: 

SVR muestra un pobre rendimiento, tanto en entrenamiento como en prueba, con valores R² negativos indicando que el modelo no se ajusta bien a los datos.

## K-Nearest Neighbors (KNN)

-Entrenamiento:

MSE: 1.021

MAE: 0.053

R²: 0.128

-Prueba:

MSE: 0.445

MAE: 0.053

R²: -0.407

### Interpretación: 

KNN presenta un rendimiento aceptable en el entrenamiento, pero su rendimiento en prueba es muy pobre, indicando problemas significativos de sobreajuste y generalización.

## Neural Network

-Entrenamiento:

MSE: 1.061

MAE: 0.140

R²: 0.094

-Prueba:

MSE: 0.315

MAE: 0.144

R²: 0.006

## Interpretación: 

La red neuronal muestra un rendimiento aceptable, pero podría beneficiarse de una mayor optimización de hiperparámetros y arquitectura para mejorar su capacidad de generalización.

Compartirmos algunas imágenes del comportamiento de las métricas en cada no de los modelos de ML aplicados

  ![Patrones de Ausencia](https://github.com/JulioQuintanaGarcia/ProyectoIntegradorE30/blob/main/images/MSE.png)

  ![Patrones de Ausencia](https://github.com/JulioQuintanaGarcia/ProyectoIntegradorE30/blob/main/images/MAE.png)

  ![Patrones de Ausencia](https://github.com/JulioQuintanaGarcia/ProyectoIntegradorE30/blob/main/images/R2.png)
