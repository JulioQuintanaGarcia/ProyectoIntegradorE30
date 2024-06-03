# Análisis Exploratorio de Datos (EDA)

Este repositorio contiene el código y la documentación asociada con el Análisis Exploratorio de Datos (EDA) realizado en un conjunto de datos específico. El objetivo de este README es proporcionar una visión general del EDA realizado y los hallazgos clave.

## A - En esta etapa se busca crear una variedad de modelos de ensamble para solucionar el problema planteado. Para ello, deberán tomar en cuenta las siguientes consideraciones:

### -Incluir la optimización de hiperparámetros para los modelos más relevantes.

### -Utilizar algoritmos que apliquen tanto estrategias de ensamble homogéneas como heterogéneas.

### -Para las estrategias de stacking y/o blending, se deberán emplear los modelos individuales de mejor rendimiento obtenidos en la fase anterior.

![STACKING](https://github.com/JulioQuintanaGarcia/ProyectoIntegradorE30/blob/main/images/Stacking.png)

![BLENDING](https://github.com/JulioQuintanaGarcia/ProyectoIntegradorE30/blob/0d6bf8576fce30263b6098820fdb83d53e6cd606/images/Blending.png)


## B-Una vez que se han generado los modelos de ensamble, sintetizar los resultados en una tabla comparativa en la que se incluyan los modelos individuales de la fase previa. 

### -Los modelos deben ser ordenados por la métrica principal, pero el resumen debe incorporar otras métricas pertinentes.

### -Se deberán incluir también los tiempos de entrenamiento.

### -Se elige el modelo final alineado con los objetivos y necesidades del negocio.

Basado en las métricas de error (MSE y MAE) y el coeficiente de determinación (R²):

![BLENDING](https://github.com/JulioQuintanaGarcia/ProyectoIntegradorE30/blob/0d6bf8576fce30263b6098820fdb83d53e6cd606/images/residuos.PNG)

*Stacking* parece ser el mejor modelo para realizar predicciones, ya que tiene el MSE más bajo en el conjunto de prueba y un R² positivo, aunque bajo.

*Blending* tiene un MAE ligeramente mejor, pero sus valores negativos de R² indican que podría no ser confiable en capturar la variabilidad de los datos.

Utilizar el modelo Stacking para las predicciones, ya que proporciona el equilibrio más favorable entre MSE, MAE y un R² positivo.

Se comparte tabla comparativa:

![TABLA COMPARATIVA](https://github.com/JulioQuintanaGarcia/ProyectoIntegradorE30/blob/main/images/tabla.png)

En la tabla comparativa podemos observar el tiempo que se tardaron en ejecutar los modelos principales, como dato adicional, queremos comentar que se estuvieron trabajando con distintos hiperparámetros a partir del GridSearch, con la finalidad de encontrar los mejores hiperparámetros para tener un mejor rendimiento del modelo, pero al final, solo utilizamos parámetros "pequeños o controlados", ya que en ocasiones los modelos en ejecución se tardaban mas de 30 minutos corriendo. 

Se adjuntan algunas imágenes con el tiempo de ejecución con GridSearch, con tiempos de ejecución largos.

![TIEMPOS DE EJECUCIÓN](https://github.com/JulioQuintanaGarcia/ProyectoIntegradorE30/blob/main/images/grids.png)

## C- Del modelo elegido, generar algunos gráficos significativos con su interpretación. La siguiente lista proporciona ejemplos, pero no es exhaustiva:

## **Concentración de Residuos:** 

La mayoría de los residuos están extremadamente concentrados alrededor de cero. Esto indica que el modelo tiene una alta precisión, ya que la mayoría de las predicciones están muy cerca de los valores reales.

La gráfica ajustada confirma que el modelo de Stacking está realizando predicciones con una alta precisión, ya que la mayoría de los residuos están concentrados cerca de cero y la distribución es simétrica. Esto sugiere que el modelo no está sesgado y está prediciendo los valores de manera bastante precisa.

![DISTRIBUCIÓN DE RESIDUOS](https://github.com/JulioQuintanaGarcia/ProyectoIntegradorE30/blob/main/images/residuos.png)

## **Gráfico de Residuos:**

La mayoría de los residuos se agrupan cerca del valor predicho de cero, lo cual es un buen indicio de que el modelo tiene un buen desempeño en la mayoría de las predicciones.

Hay algunos puntos de residuos que se alejan significativamente de cero. Estos puntos pueden ser considerados como outliers o valores atípicos donde el modelo no predijo bien.

![GRAFICO DE RESIDUOS](https://github.com/JulioQuintanaGarcia/ProyectoIntegradorE30/blob/main/images/residuos2.png)


## **Importancia de Características:**

Podemos observar acorde a la imagen, el orden de impoartancia de nuestras variables de entrada DownStart_dia, DownStart_mes, PRoduction_Goal, etc. Se comparte una interpretación de acuerdo a los resultados obtenidos.

### DownStart_dia:

Es la característica más importante sugiere que el día en el que ocurre el inicio de una caída (probablemente relacionado con fallos o interrupciones) tiene un impacto significativo en la duración total.

Podría ser que ciertos días específicos tienen patrones de fallos recurrentes o que la carga de trabajo varía considerablemente dependiendo del día. Esto podría ser un indicador de problemas de planificación o mantenimiento que son específicos de ciertos días.

### DownStart_mes:

La importancia de "DownStart_mes" sugiere que el mes también juega un papel crucial en la predicción de la duración total. Esto podría indicar la presencia de factores estacionales o mensuales que afectan el rendimiento.

Podría haber variaciones estacionales en la demanda, en el mantenimiento programado, o en otros factores operativos que influyen en la duración de las interrupciones. Por ejemplo, ciertos meses pueden estar asociados con mayor actividad, lo que aumenta la probabilidad de fallos.

### Production_Goal:

La meta de producción ("Production_Goal") también es una variable importante, lo que sugiere que las metas de producción establecidas tienen una relación directa con la duración de las operaciones o interrupciones.

Las metas de producción más altas podrían estar correlacionadas con un mayor esfuerzo operativo, lo que podría llevar a una mayor probabilidad de fallos o interrupciones debido al estrés en los sistemas y equipos. Alternativamente, metas muy bajas podrían indicar periodos de mantenimiento o baja actividad, lo que también afecta la duración total.

![IMPORTANCIA DE CARACTERISTICAS](https://github.com/JulioQuintanaGarcia/ProyectoIntegradorE30/blob/main/images/caracteristicas.png)


