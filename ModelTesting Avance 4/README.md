# Resumen de Evaluaciones de Modelos

Este documento resume los resultados de las evaluaciones de tres enfoques diferentes para entrenar y probar un modelo de clasificación.

## Escenario 1: Modelo Best Performance

### Datos Utilizados
- Todos los datos disponibles

### División de Datos
- 80% entrenamiento, 20% prueba

### Métricas en Entrenamiento
- **Precision**: 0.93
- **Recall**: 0.90
- **F1-Score**: 0.91

### Métricas en Prueba
- **Precision**: 0.85
- **Recall**: 0.80
- **F1-Score**: 0.82

## Escenario 2: Modelo con Datos de las Últimas Tres Semanas

### Datos Utilizados
- Datos correspondientes a las últimas tres semanas

### División de Datos
- 80% entrenamiento, 20% prueba

### Métricas en Entrenamiento
- **Precision**: 0.88
- **Recall**: 0.86
- **F1-Score**: 0.87

### Métricas en Prueba
- **Precision**: 0.80
- **Recall**: 0.78
- **F1-Score**: 0.79

## Escenario 3: Modelo con 30% de Datos para Entrenamiento

### Datos Utilizados
- Todos los datos disponibles

### División de Datos
- 30% entrenamiento, 70% prueba

### Métricas en Entrenamiento
- **Precision**: 0.92
- **Recall**: 0.91
- **F1-Score**: 0.91

### Métricas en Prueba
- **Precision**: 0.82
- **Recall**: 0.78
- **F1-Score**: 0.80

## Comparaciones y Conclusiones

### Cantidad de Datos y Efecto en Métricas

1. **Best Performance**: Utilizando todos los datos disponibles con una división tradicional (80/20) mostró la mejor estabilidad entre las métricas de entrenamiento y prueba. Las métricas en prueba son las más altas comparadas con los otros dos enfoques.
2. **Últimas Tres Semanas**: Al limitar los datos a solo tres semanas, las métricas tanto de entrenamiento como de prueba disminuyeron ligeramente, sugiriendo que el modelo se beneficia de tener más datos históricos.
3. **30% para Entrenamiento**: Utilizando solo el 30% de los datos para entrenamiento y el 70% para prueba, el modelo logró métricas de entrenamiento comparables al modelo Best Performance, pero mostró una disminución en las métricas de prueba, indicando que quizás no tuvo suficientes datos para generalizar adecuadamente.

### Relación Entre Métricas de Entrenamiento y Prueba

- En el **modelo Best Performance**, la diferencia entre las métricas de entrenamiento y prueba es razonablemente pequeña, lo que indica un buen equilibrio entre entrenamiento y generalización.
- Para el **modelo con datos de las últimas tres semanas**, se observa una caída más significativa en las métricas de prueba, lo cual podría ser debido a la falta de diversidad en los datos más recientes.
- En el **modelo con 30% de datos para entrenamiento**, aunque las métricas de entrenamiento son altas, hay una caída notable en las métricas de prueba, lo que sugiere sobreajuste debido al menor volumen de datos de entrenamiento.

### Conclusiones

- El **modelo Best Performance** es el más robusto, logrando un buen equilibrio entre las métricas de entrenamiento y prueba.
- Limitar los datos a solo las últimas tres semanas puede no ser suficiente para capturar la diversidad necesaria para un buen rendimiento del modelo.
- Reducir el tamaño del conjunto de entrenamiento al 30% puede llevar a sobreajuste y una menor capacidad de generalización.

Esta comparación sugiere que, siempre que sea posible, es mejor utilizar la mayor cantidad de datos históricos disponibles con una división adecuada (80/20) para entrenar el modelo y asegurar su capacidad de generalización en datos no vistos.
