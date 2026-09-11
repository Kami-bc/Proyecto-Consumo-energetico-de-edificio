## Autores
- Caroline Valentina García Pereira.
- Karol Michelle Benavides Castillo.
- Kevin Duque Delgado.
- Brenk Sneider Bohorquez Vargas.

## Fecha de entrega
11 de Septiembre del 2026.

## Estructura del proyecto

```text
Proyecto-Consumo-energetico-de-edificio/
│
├── .gitignore
├── README.md
├── Requerimientos/
├── bitacora_ia/
├── energydata_complete.csv
└── requirements.txt

# Proyecto - Consumo energético de edificio
Modelo de regresión temporal para predecir el consumo energético de electrodomésticos en función de factores ambientales, climáticos y temporales.

# Objetivo
Desarrollar un modelo de regresión que sea capaz de estimar el consumo energético de un edificio de acuerdo a las condiciones externas.

# variable objetivo
Consumo energético

El proyecto se desarrollará mediante las siguientes etapas:

1. Carga y diagnóstico de los datos.
2. Limpieza y preparación de los datos.
3. Análisis exploratorio de datos (EDA).
4. Ingeniería y selección de características.
5. División de los datos en entrenamiento y prueba.
6. Construcción de una línea base.
7. Entrenamiento de modelos de regresión.
8. Evaluación mediante métricas.
9. Análisis de errores y residuos.
10. Comparación de resultados.

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
