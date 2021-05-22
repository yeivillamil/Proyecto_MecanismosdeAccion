# Proyecto_MecanismosdeAccion

A continuaci�n ser� presentada una breve descripci�n de los diferentes notebooks:

Para la ejecuci�n de cada uno de los notebooks, es importante descargar de manera previa el conjunto de datos en la siguiente URL: https://www.kaggle.com/c/lish-moa/data. Debido a su tama�o, no fue posible dejarlo en una carpeta espec�fica dentro del repositorio. Este debe estar en un entorno local, donde vaya a ser guardado el repo.

Cada uno de los notebooks, contiene informaci�n de la forma de ejecuci�n.

## 1.) 01-Moa_AnalisisExploratorio**

En el an�lisis exploratorio son descritas las variables, ingenier�a de caracteristicas, distribuciones y conteo de prote�nas (mecanismos de acci�n) para el problema en desarollo.

## 2.) 02-PrimeraIteracion**

Para la primera iteracion, fueron tomadas dos prot�inas de las 206 totales. Una con mayor y otra con menor activaci�n respectivamente, y fueron probados de manera inicial tres diferentes tipo de modelos de machine learning para clasificaci�n: modelo de Bayes multinomial, regresi�n log�stica y clasificador de vecinos cercanos. La ejecuci�n se debe realizar en orden, ejecutando celda a celda

## 3.) 1_ETAPA_ONEVsREST**

Para la ejecuci�n de la primera etapa, donde son probados cuatro modelos de clasificaci�n en un proceso OneVsrest, es importante considerar la ejecuci�n de manera ordenada para entender el problema:
* El archivo 03 consta de la primera experimentaci�n y mostrar� los resultados del primer proceso de esta etapa. Es necesaria la instalaci�n de las librer�as `scikit-multilearn` y `XGBoost` para su total ejecuci�n, esta se debe realizar celda a celda.
* El archivo 04 consta de un procedimiento similar al paso anterior, sin embargo, ser�n creados datos sint�ticos a trav�s del m�todo `SMOTE`. El m�dulo que debe ser instalado para el uso de esta librer�a es `imblearn` y el notebook debe ser ejecutado celda a celda.
* El archivo 05 contiene la ejecuci�n de solo de los modelos de m�quina de soporte y XGBoost usando GPU, la cual fue realizada a trav�s de la plataforma Kaggle. Es importante que se tenga una cuenta all� o en su defecto que se tenga una m�quina con GPU. Dentro de kaggle, en profile-->code podr�n construir notebook y all� debe ser activada la GPU. Para la ejecuci�n es importante la instalaci�n del m�dulo de m�quina de soporte encontrado en la siguiente URL `https://docs.rapids.ai/api/cuml/stable/`. La ejecuci�n debe ser realizada celda a celda.
* El archivo 06 contiene el procedimiento presentado anteriormente para los modelos de m�quina de soporte y XGBoost, sin embargo, ser� usado `SMOTE` como punto adicional. Su ejecuci�n se debe realizar, celda a celda.

## 4.) 2_ETAPA_MULTILABEL**

Para esta etapa fueron usando dos diferentes modelos para abordar el problema multietiqueta. Estos dos fueron: Random Forest y redes neuronales. Para el caso de las redes, fueron usados de dos diferentes librer�as; scikit-learn y tensorflow.
* El archivo 07 contiene la ejecuci�n del modelo random forest y redes neuronales (usando la librer�a de scikit-learn). Es importante que sean instaladas las librer�as mencionadas en los pasos anteriores y esta debe ser realizada celda a celda.
* El archivo 08 contiene la informaci�n para la ejecuci�n de redes neuronales usando las librer�as de tensorflow, as� que se hace necesaria la instalaci�n de este m�dulo `pip install tensorflow`. La ejecuci�n se realizar� celda a celda.

## 5.) 3_ETAPA_DEEPLEARNING**

Para la �ltima etapa de la experimentaci�n, fueron usadas arquitecturas sof�sticas a trav�s de redes neuronales con autoencoder y denoising autoenconders.
* El archivo 09 contiene la informaci�n para la ejecuci�n de las arquitecturas de redes neuronales usando denoising autoencoder (ruido blanco). Es importante la instalaci�n de m�dulo de `tensorflow` y el complemento `tensorflow-addons`. La ejecuci�n debe ser realizda celda a celda.
* El archivo 10 contiene la informaci�n para le ejecuci�n de autoencoder pero usando los datos originales. Ya con la instalaci�n de los m�dulos del paso anterior, solo debe ser ejecutado el notebook celda a celda.