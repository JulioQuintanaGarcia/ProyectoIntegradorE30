# Análisis Exploratorio de Datos (EDA) - Avance 2

Este repositorio contiene el código y la documentación asociada con el Análisis Exploratorio de Datos (EDA) realizado en un conjunto de datos específico. El objetivo de este README es proporcionar una visión general del EDA realizado y los hallazgos clave.

## A) Se aplicarán operaciones comunes para convertir los datos crudos del mundo real, en un conjunto de variables útiles para el aprendizaje automático. El procesamiento puede incluir:

-Generación de nuevas características

-Discretización o binning

-Codificación (ordinal, one hot,…)

-Escalamiento (normalización, estandarización, min – max,…)

-Transformación (logarítmica, exponencial, raíz cuadrada, Box – Cox, Yeo – Johnson,…)

### Normalización y estandarización:

La normalización y estandarización pueden ayudar a mejorar la precisión y la estabilidad del modelo de regresión lineal al reducir el impacto de las características con mayor escala y mejorar la convergencia del algoritmo de entrenamiento.

Al aplicar *StandardScaler*, normalizamos las características numéricas para que tengan una media de cero y una desviación estándar de uno. Esto es importante porque muchos modelos de regresión (como la regresión lineal) asumen que las características están en la misma escala. La estandarización asegura que todas las características contribuyan de manera equitativa al modelo.
Codificación de variables categóricas:

*OneHotEncoder* se utiliza para convertir variables categóricas en una representación numérica adecuada para los modelos de regresión. Esto es necesario porque la mayoría de los modelos de regresión no pueden manejar variables categóricas directamente. La codificación one-hot crea una columna binaria para cada categoría única, lo que permite al modelo capturar las relaciones no lineales entre las categorías y la variable objetivo.

![One hot encoding](https://github.com/JulioQuintanaGarcia/ProyectoIntegradorE30/blob/main/images/onehot_encoding.png)

## B) Además, se utilizarán métodos de filtrado para la selección de características y técnicas de extracción de características, permitiendo reducir los requerimientos de almacenamiento, la complejidad del modelo y el tiempo de entrenamiento. Los ejemplos siguientes son ilustrativos, pero no exhaustivos, de lo que se podría aplicar:

-Umbral de varianza

-Correlación

-Chi-cuadrado

-ANOVA

-Análisis de componentes principales (PCA)

-Análisis factorial (FA)

La selección de características y la extracción de características son técnicas importantes para reducir la dimensionalidad del conjunto de datos y mejorar el rendimiento del modelo de aprendizaje automático. Esto se logra identificando y seleccionando las características más relevantes e informativas del conjunto de datos, y transformando o combinando las características existentes para crear nuevas características más útiles.

### Correlación
Se estuvieron utilizando distintintos metodos para la selección de características, como puede ser la correlación entre variables, un rango de correlación de -0.3 a 0.3 sugiere que las relaciones entre las variables son relativamente débiles. Esto significa que eliminar las variables con correlaciones bajas podría no tener un impacto significativo en el rendimiento del modelo. Como se puede ver en la imagen.

![Correlación](https://github.com/JulioQuintanaGarcia/ProyectoIntegradorE30/blob/main/images/correlacion.png)

Se decide realizar otros métodos de para la selección de características.

### Reducción de la dimensionalidad:
El PCA se utiliza para reducir la dimensionalidad del conjunto de datos al proyectarlo en un espacio de características de menor dimensión mientras se conserva la mayor cantidad posible de la variabilidad original de los datos. Esto puede ser beneficioso cuando se trabaja con conjuntos de datos de alta dimensionalidad para reducir el riesgo de sobreajuste y mejorar la generalización del modelo. Además, al reducir la dimensionalidad, también podemos reducir el tiempo de entrenamiento del modelo y los requisitos de memoria.

La justificación de la aplicación de estos pasos específicos radica en su capacidad para mejorar la calidad de los datos y la capacidad predictiva del modelo de regresión resultante. Al normalizar y codificar adecuadamente las características y reducir la dimensionalidad del conjunto de datos, podemos preparar un conjunto de datos más limpio y estructurado que pueda ser más fácilmente interpretado por el modelo de regresión, lo que potencialmente resultará en mejores predicciones.

![PCA](https://github.com/JulioQuintanaGarcia/ProyectoIntegradorE30/blob/main/images/PCA.png)

-Los componentes principales con mayor varianza explicada son los más importantes para representar la información original del conjunto de datos.

-Se considera que los componentes que explican al menos el 80% de la varianza total son suficientes para capturar la mayor parte de la información relevante.

## C) Incluir conclusiones de la fase de "Preparación de los datos" en el contexto de la metodología CRISP-ML.

### 1. Limpieza y transformación de datos:

-Se realizó una limpieza exhaustiva de los datos para eliminar valores faltantes, inconsistencias y errores.

-Se transformaron las variables según fue necesario, incluyendo escalado, codificación y creación de nuevas características.

-Se aplicaron técnicas de normalización y estandarización para mejorar la comparabilidad de las variables.

### 2. Selección de características:

-Se utilizaron métodos de filtrado como la correlación y el umbral de varianza para identificar y eliminar características irrelevantes o redundantes.

-Se aplicaron técnicas de extracción de características como el Análisis de Componentes Principales (PCA) para reducir la dimensionalidad del conjunto de datos.

### 3. Resultados:

La preparación de datos dio como resultado un conjunto de datos limpio, estructurado y de menor dimensionalidad, listo para ser utilizado en el entrenamiento del modelo de Machine Learning.
Se espera que la calidad mejorada de los datos conduzca a un mejor rendimiento del modelo, mayor precisión en las predicciones y una mejor generalización.

### 4. Consideraciones adicionales:

-La selección de técnicas de preprocesamiento y selección de características fue específica para este conjunto de datos y problema.

-Se recomienda monitorear el rendimiento del modelo y realizar ajustes en el preprocesamiento de datos si es necesario.

## Contribuciones y Contacto
Si tienes alguna pregunta o sugerencia sobre el análisis realizado o el código asociado, no dudes en contactar al equipo a través de [Julio Quintana](A01793661@tec.mx) | [Pablo Colunga](A01793671@tec.mx) | [Marco Antonio Lopez](A01113135@tec.mx) .

¡Gracias por tu interés en nuestro análisis exploratorio de datos! 
