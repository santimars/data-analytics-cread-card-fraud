# data-analytics-cread-card-fraud
## Introducción

La deserción de clientes y el fraude en entidades financieras representan uno de los problemas más importantes dentro del sector bancario. Detectar patrones sospechosos o comportamientos anómalos permite a las instituciones financieras reducir pérdidas económicas y mejorar la seguridad de sus servicios.

En este proyecto se desarrolla un análisis utilizando técnicas de Machine Learning para identificar transacciones fraudulentas en tarjetas de crédito. Para ello se emplea un conjunto de datos que contiene múltiples variables relacionadas con las transacciones realizadas por los clientes.

El objetivo principal es comparar diferentes modelos de clasificación, analizar su desempeño mediante métricas estadísticas y seleccionar el modelo con mayor capacidad predictiva.

El análisis se desarrolla utilizando Python dentro de un entorno Jupyter Notebook, aplicando buenas prácticas de ciencia de datos como análisis exploratorio, preparación de datos, entrenamiento de modelos, ajuste de hiperparámetros y evaluación del rendimiento.

## Fuente de Datos

La fuente principal de datos utilizada en este proyecto corresponde al archivo:

**run-1621650847915-part-r-00000**

Este conjunto de datos contiene información sobre transacciones realizadas con tarjetas de crédito, incluyendo múltiples variables transformadas que permiten preservar la confidencialidad de los datos originales.

El dataset incluye variables numéricas que representan diferentes características de las transacciones, además de una variable objetivo que indica si la transacción corresponde a un fraude o a una operación legítima.

Las características principales del dataset son:

- Contiene múltiples variables numéricas transformadas.
- Incluye una variable de clasificación binaria (fraude / no fraude).
- Presenta un **alto desbalance de clases**, ya que las transacciones fraudulentas representan una pequeña proporción del total.

Este tipo de datasets es común en problemas de detección de fraude, donde la identificación correcta de la clase minoritaria es fundamental.

## Funciones Estadísticas

Para facilitar el análisis del dataset se utiliza el archivo:

**funciones_Estadisticas.py**

Este archivo contiene funciones auxiliares que permiten calcular diferentes métricas estadísticas y de evaluación utilizadas en modelos de Machine Learning.

Entre las funciones implementadas se encuentran:

- Cálculo de métricas de clasificación
- Generación de matrices de confusión
- Evaluación del desempeño de los modelos
- Cálculo de medidas estadísticas derivadas de la matriz de confusión

Estas funciones permiten automatizar el análisis de resultados y comparar el rendimiento entre diferentes algoritmos de clasificación.

## Análisis Exploratorio de Datos (EDA)

El análisis exploratorio de datos tiene como objetivo comprender las características principales del dataset antes de aplicar cualquier modelo de Machine Learning.

Durante esta etapa se analizan aspectos como:

- Distribución de las variables
- Estadísticas descriptivas
- Correlaciones entre variables
- Balance entre las clases del dataset

Este análisis permite identificar posibles problemas en los datos como valores atípicos, variables altamente correlacionadas o desbalance en las clases.

Las gráficas generadas permiten visualizar de forma clara el comportamiento de las variables y facilitan la interpretación del conjunto de datos.

## Preparación de los Datos

Antes de entrenar los modelos de Machine Learning es necesario realizar un proceso de preparación de los datos.

Esta etapa incluye diferentes técnicas de preprocesamiento que permiten mejorar el rendimiento de los modelos. Entre las principales técnicas utilizadas se encuentran:

### Escalado de variables

Algunas variables presentan rangos de valores muy diferentes, lo cual puede afectar el desempeño de ciertos algoritmos. Por esta razón se realiza un proceso de escalado para normalizar los datos y evitar que algunas variables tengan mayor peso que otras.

### Manejo del desbalance de clases

El dataset presenta un fuerte desbalance entre las transacciones fraudulentas y las no fraudulentas. Esto puede generar que los modelos aprendan principalmente la clase mayoritaria.

Para solucionar este problema se aplica la técnica de **Random Under-Sampling**, la cual consiste en reducir el número de muestras de la clase mayoritaria para equilibrar el dataset.

Este proceso permite mejorar la capacidad de los modelos para detectar correctamente los casos de fraude.

## Selección de Modelos de Machine Learning

Para este proyecto se seleccionaron diferentes algoritmos de clasificación con el objetivo de comparar su rendimiento en la detección de fraudes.

Entre los modelos utilizados se encuentran:

- Perceptrón Multicapa (Red Neuronal)
- Algoritmos clásicos de clasificación de Machine Learning
- Autoencoders para detección de anomalías

La selección de estos modelos permite analizar diferentes enfoques de aprendizaje supervisado y semi-supervisado aplicados al problema de detección de fraude.

## Entrenamiento del Modelo

Una vez preparados los datos, se procede al entrenamiento de los modelos de Machine Learning.

Para ello se divide el dataset en dos conjuntos:

- **Conjunto de entrenamiento**
- **Conjunto de prueba**

El modelo se entrena utilizando el conjunto de entrenamiento, mientras que el conjunto de prueba se utiliza para evaluar su capacidad de generalización sobre datos no vistos previamente.

Este proceso permite medir el desempeño real del modelo y evitar problemas de sobreajuste (overfitting).



## Evaluación del Modelo

Para evaluar el rendimiento de los modelos se utilizan diferentes métricas derivadas de la matriz de confusión.

Las principales métricas utilizadas son:

- **Accuracy:** porcentaje de predicciones correctas.
- **Precision:** capacidad del modelo para identificar correctamente los fraudes.
- **Recall:** proporción de fraudes detectados correctamente.
- **F1-Score:** medida que combina precisión y recall.

Debido al desbalance del dataset, métricas como **Precision y Recall** son más relevantes que el accuracy, ya que permiten evaluar mejor la capacidad del modelo para detectar fraudes.

## Ajuste de Hiperparámetros (Parameter Tuning)

El ajuste de hiperparámetros consiste en modificar los parámetros internos de los modelos de Machine Learning con el fin de mejorar su rendimiento.

Algunos de los parámetros que pueden ajustarse incluyen:

- Número de neuronas en redes neuronales
- Tasa de aprendizaje
- Número de capas
- Parámetros de regularización

El proceso de tuning permite optimizar el comportamiento del modelo y aumentar su capacidad de predicción sobre nuevos datos.

## Buenas Prácticas de Programación

Durante el desarrollo del proyecto se aplicaron buenas prácticas de programación, entre las cuales se incluyen:

- Organización clara del código
- Separación entre análisis, entrenamiento y evaluación
- Uso de funciones reutilizables
- Documentación mediante celdas Markdown

Estas prácticas facilitan la comprensión del código y permiten reproducir el análisis de manera más sencilla.

## Repositorio del Proyecto

El proyecto debe almacenarse en un repositorio de GitHub con el fin de mantener control de versiones y permitir la colaboración.

El repositorio incluye:

- Notebook del proyecto
- Archivo de funciones estadísticas
- Dataset utilizado
- Documentación del análisis

Esto permite que el proyecto sea reproducible y que otros investigadores o desarrolladores puedan revisar el trabajo realizado.

## Buenas Prácticas de Programación

Durante el desarrollo del proyecto se aplicaron buenas prácticas de programación, entre las cuales se incluyen:

- Organización clara del código
- Separación entre análisis, entrenamiento y evaluación
- Uso de funciones reutilizables
- Documentación mediante celdas Markdown

Estas prácticas facilitan la comprensión del código y permiten reproducir el análisis de manera más sencilla.

## Repositorio del Proyecto

El proyecto debe almacenarse en un repositorio de GitHub con el fin de mantener control de versiones y permitir la colaboración.

El repositorio incluye:

- Notebook del proyecto
- Archivo de funciones estadísticas
- Dataset utilizado
- Documentación del análisis

Esto permite que el proyecto sea reproducible y que otros investigadores o desarrolladores puedan revisar el trabajo realizado.
