# Baseline Model Report

## Analytic Approach
* What is target definition

En el modelo desarrollado se fijó una única variable objetivo, a saber la variable relacionada cone el tipo de la estrella. Dicha variable objetivo o de salida, se trata de un valor entero de 0 a 5, que como ya se ha discutido en documentos anteriores tiene como significado:

	* 0. Enana marrón.
	* 1. Enana roja.
	* 2. Enana blanca
	* 3. Secuencia principal.
	* 4. Supergigante.
	* 5. Hipergigante.

* What are inputs (description)

Para realizar una correcta predicción de la variable anteriormente discutida, se tuvo en cuenta la dependencia de la misma en características físicas de la estrella en cuestión. Es por esto que se escogieron las siguientes variables físicas disponibles en el conjunto de datos a estudiar:

	* Temperatura.
	* Luminosidad.
	* Radio.
	* Magnitud Absoluta.

* What kind of model was built?

Para obtener resultados de buena calidad para usarse y realizar posteriores predicciones, así como hacer una rápida implementación y entrenamiento del modelo, se usó un modelo clásico de árbol de desición. Las entradas de dicho modelo fueron las 4 características físicas ya mencionadas, y su salida es un número entero que indica el tipo de la estrella predicha.

## Model Description

* Models and Parameters

Como fue mencionado más atrás, se implementó un modelo de aprendizaje automático basado en árboles de decisión, al cual se le realizó una búsqueda de los mejores hiperparámetros para mejorar las predicciones obtenidas sobre un conjunto de validación. Los hiperparámetros trabajados fueron los siguientes:

	* Criterio de partición del árbol.
	* Profundidad del árbol.
  	
Del estudio de los mejores hiperparámetros para el conjunto de datos entrenado se obtuvo que los mejores resultados según el score del modelo en un conjunto de validación era usando el criterio "entropy" para particionar el árbol, y este debía tener una profundidad igual a 5.

A continuación se muestra una imagen del árbol de decisión obtenido con estos hiperparámetros:

![alt text](tree.png)

## Results (Model Performance)

* ROC/Lift charts, AUC, R^2, MAPE as appropriate

Para evaluar y probar la capacidad de predicción del modelo entrenado, se pasó a traves de un `classification report` para conocer su score en diferentes métricas para conjuntos de testeo. Estos fueron los resultados:

![alt text](report.png)

Así mismo, estos resultados se vieron gráficamente en una matriz de confusión para ver la capacidad de predicción en cada uno de los tipos de estrella:

![alt text](confusion.png)

## Model Understanding

* Variable Importance (significance)

* Insight Derived from the Model

## Conclusion and Discussions for Next Steps

* Conclusion on Feasibility Assessment of the Machine Learning Task

* Discussion on Overfitting (If Applicable)

* What other Features Can Be Generated from the Current Data

* What other Relevant Data Sources Are Available to Help the Modeling
