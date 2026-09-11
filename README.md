## Autores
- Caroline Valentina García Pereira.
- Karol Michelle Benavides Castillo.
- Kevin Duque Delgado.
- Brenk Sneider Bohorquez Vargas.

## Fecha de entrega
11 de Septiembre del 2026.

## Estructura del proyecto

```text
Proyecto/
│
├── .gitignore
├── README.md
├── Requerimientos/
├── bitacora_ia/
├── energydata_complete.csv
└── requirements.txt
```

# Proyecto - Consumo energético de edificio
Modelo de regresión temporal para predecir el consumo energético de electrodomésticos en función de factores ambientales, climáticos y temporales.

# Objetivo
Desarrollar un modelo de regresión que sea capaz de estimar el consumo energético de un edificio de acuerdo a las condiciones externas.

# variable objetivo
Consumo energético

El proyecto se desarrollará mediante las siguientes etapas:

1. Script y carga del dataset
2. Diagnóstico de los datos
3. Diccionario de variables
4. Análisis exploratorio de datos (EDA)
5. Visualizaciones
6. Definición de X e y
7. Ordenamiento temporal de los datos
8. Partición temporal: entrenamiento y prueba
9. Construcción de la línea base temporal
10. Métricas de la línea base
11. Modelo simple: regresión lineal
12. Predicciones del modelo
13. Métricas del modelo
14. Comparación: línea base vs. regresión lineal
15. Cálculo de residuos
16. Análisis y gráficas de residuos
17. Revisión de posibles fugas de información
18. Conclusiones

## Diccionario de variables

El conjunto de datos contiene 19.735 registros y 29 variables. 
La variable objetivo del proyecto es el consumo energético de los electrodomésticos.

La variable `date` corresponde al registro temporal de cada medición, 
mientras que las demás variables contienen información relacionada con el consumo de iluminación, temperatura, humedad y condiciones 
ambientales.

Para el modelo de regresión, `Appliances` se utilizará como variable 
objetivo, mientras que las variables ambientales y de consumo 
disponibles se utilizarán como variables predictoras (X).

# Resultados
La temperatura exterior por sí sola no parece explicar completamente el consumo energético de los electrodomésticos.

# partición de datos
Se realizó una partición temporal de los datos utilizando el 80 % de las
observaciones para entrenamiento y el 20 % restante para prueba debido a que los registros poseen fechas.

# Línea base
MAE → qué tan grande es el error promedio.

RMSE → mide el error y penaliza más los errores grandes.

R² → qué tan bien explica el modelo la variación del consumo.
" 
#Primer modelo

Modelo de regresión lineal, debido a que permite evaluar si las variables predictoras contienen información útil para 
explicar el consumo energético de los electrodomésticos.
La línea base tenía un MAE de aproximadamente 52.68, por lo que el error absoluto promedio disminuyó ligeramente. En cuanto a la regresión Lineal consigue reducir, en cierta medida, los errores grandes que tenía la línea base. 
Por lo tanto, el modelo presenta una primera mejora respecto a la línea base, pero su desempeño todavía es modesto. Hay outliers importantes y se indica heterocedasticidad o falta de linealidad.

# Conclusiones
La regresión lineal permite establecer un primer modelo para predecir Appliances.
Se compara su desempeño contra la línea base temporal.
Las métricas principales son MAE, RMSE y R².
El análisis de residuos permite identificar errores sistemáticos y dificultades del modelo.
El modelo puede presentar dificultades para representar los picos de consumo, por lo que existe margen de mejora.
# Posibles soluciones
Utilizar modelos capaces de capturar relaciones no lineales.

# Mejoras del modelo
Comparar varios algoritmos.
Ajustar hiperparámetros.
Utilizar validación temporal.
Analizar y tratar valores atípicos.
Evaluar transformaciones de variables.
Mejorar la representación de la temporalidad.
Comparar nuevamente los modelos mediante MAE, RMSE y R².
Revisar nuevamente los residuos después de cada mejora.
