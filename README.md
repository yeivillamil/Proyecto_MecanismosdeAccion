# Proyecto_MecanismosdeAccion

A continuación será presentada una breve descripción de los diferentes notebooks:

Para la ejecución de cada uno de los notebooks, es importante descargar de manera previa el conjunto de datos en la siguiente URL: https://www.kaggle.com/c/lish-moa/data. Debido a su tamaño, no fue posible dejarlo en una carpeta específica dentro del repositorio. Este debe estar en un entorno local, donde vaya a ser guardado el repo.

Cada uno de los notebooks, contiene información de la forma de ejecución.

## 1.) 01-Moa_AnalisisExploratorio**

En el análisis exploratorio son descritas las variables, ingeniería de caracteristicas, distribuciones y conteo de proteínas (mecanismos de acción) para el problema en desarollo.

## 2.) 02-PrimeraIteracion**

Para la primera iteracion, fueron tomadas dos protéinas de las 206 totales. Una con mayor y otra con menor activación respectivamente, y fueron probados de manera inicial tres diferentes tipo de modelos de machine learning para clasificación: modelo de Bayes multinomial, regresión logística y clasificador de vecinos cercanos. La ejecución se debe realizar en orden, ejecutando celda a celda

## 3.) 1_ETAPA_ONEVsREST**

Para la ejecución de la primera etapa, donde son probados cuatro modelos de clasificación en un proceso OneVsrest, es importante considerar la ejecución de manera ordenada para entender el problema:
* El archivo 03 consta de la primera experimentación y mostrará los resultados del primer proceso de esta etapa. Es necesaria la instalación de las librerías `scikit-multilearn` y `XGBoost` para su total ejecución, esta se debe realizar celda a celda.
* El archivo 04 consta de un procedimiento similar al paso anterior, sin embargo, serán creados datos sintéticos a través del método `SMOTE`. El módulo que debe ser instalado para el uso de esta librería es `imblearn` y el notebook debe ser ejecutado celda a celda.
* El archivo 05 contiene la ejecución de solo de los modelos de máquina de soporte y XGBoost usando GPU, la cual fue realizada a través de la plataforma Kaggle. Es importante que se tenga una cuenta allí o en su defecto que se tenga una máquina con GPU. Dentro de kaggle, en profile-->code podrán construir notebook y allí debe ser activada la GPU. Para la ejecución es importante la instalación del módulo de máquina de soporte encontrado en la siguiente URL `https://docs.rapids.ai/api/cuml/stable/`. La ejecución debe ser realizada celda a celda.
* El archivo 06 contiene el procedimiento presentado anteriormente para los modelos de máquina de soporte y XGBoost, sin embargo, será usado `SMOTE` como punto adicional. Su ejecución se debe realizar, celda a celda.

## 4.) 2_ETAPA_MULTILABEL**

Para esta etapa fueron usando dos diferentes modelos para abordar el problema multietiqueta. Estos dos fueron: Random Forest y redes neuronales. Para el caso de las redes, fueron usados de dos diferentes librerías; scikit-learn y tensorflow.
* El archivo 07 contiene la ejecución del modelo random forest y redes neuronales (usando la librería de scikit-learn). Es importante que sean instaladas las librerías mencionadas en los pasos anteriores y esta debe ser realizada celda a celda.
* El archivo 08 contiene la información para la ejecución de redes neuronales usando las librerías de tensorflow, así que se hace necesaria la instalación de este módulo `pip install tensorflow`. La ejecución se realizará celda a celda.

## 5.) 3_ETAPA_DEEPLEARNING**

Para la última etapa de la experimentación, fueron usadas arquitecturas sofísticas a través de redes neuronales con autoencoder y denoising autoenconders.
* El archivo 09 contiene la información para la ejecución de las arquitecturas de redes neuronales usando denoising autoencoder (ruido blanco). Es importante la instalación de módulo de `tensorflow` y el complemento `tensorflow-addons`. La ejecución debe ser realizda celda a celda.
* El archivo 10 contiene la información para le ejecución de autoencoder pero usando los datos originales. Ya con la instalación de los módulos del paso anterior, solo debe ser ejecutado el notebook celda a celda.