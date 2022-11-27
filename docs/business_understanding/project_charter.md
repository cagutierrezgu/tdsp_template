# Project Charter

## Business background

* Who is the client, what business domain the client is in.

Juan Sebastián Lara Ramírez, Magíster en ingeniería de sistemas y computación de la Universidad Nacional de Colombia y Juan Sebastián Malagón Torres, egresado del programa de bioingeniería de la universidad el bosque.
Así mismo, cualquier profesor, investigador o estudiante que desde la academia desee realizar clasificación de estrellas basado en mediciones observacionales de sus características.

* What business problems are we trying to address?

El objetivo del proyecto es determinar qué tipo de estrella se está estudiando a partir de las características más importantes de esta, así como encontrar posibles relaciones ocultas entre dichas características que aporten nuevos conocimientos en la astrofísica estelar.

## Scope
* What data science solutions are we trying to build?

El problema a solucionar requiere construir un modelo de clasificación, ya que existen un número finito de clases o etiquetas a predecir.

* What will we do?

Con una debida exploración y procesamiento de los datos dispuestos se escogerá la mejor opción que retorne los mejores resultados según las métricas evaluadas, entre los modelos de aprendizaje automático clásicos y los que usan redes neuronales artificiales.

* How is it going to be consumed by the customer?

A pesar de que quien solicita el modelo no es del área del mercado, es decir, no se trata de mejorar ventas o atraer clientes para una empresa, el modelo pretende ser usado para mejorar la detección y clasificación de estrellas. De esta manera, la herramienta de machine learning le permite al investigador ahorrar grandes tiempos descubriendo el tipo de estrella observado, para así dedicarlo en otras preguntas para su proyecto de investigación.

## Personnel
* Who are on this project:
	* Creador del modelo:
		* Carlos Esteban Gutierrez Guarnizo
	* Client:
		* Juan Sebastián Lara Ramírez
		* Juan Sebastián Malagón Torres
		* Comunidad científica
	
## Metrics
* What are the qualitative objectives? (e.g. reduce user churn)
	* Construir un modelo de decisión que prediga el tipo de estrella estudiada a partir de sus propiedades observacionales.
	* Verificar que las estrellas siguen una gráfica determinada basado en su tamaño, temperatura y otras características, a saber, el diagrama de Hertzsprung-Russell.
* What is a quantifiable metric  (e.g. reduce the fraction of users with 4-week inactivity)

	* Reducir el tiempo que los investigadores tardan realizando tareas de clasificación de estrellas u objetos astrofísicos de características similares de manera inmediata.

* Quantify what improvement in the values of the metrics are useful for the customer scenario (e.g. reduce the  fraction of users with 4-week inactivity by 20%) 

Lograr alrededor de un 90% de capacidad de predicción para cada uno de los tipos de estrellas.

* What is the baseline (current) value of the metric? (e.g. current fraction of users with 4-week inactivity = 60%)

No existen valores de referencia actuales, las etiquetas de los datos dispuestos han sido impuestas por personas y se asumen como correctas. Por otro lado, el tiempo que se tarda en clasificar una persona un conjunto de datos observacionales puede ser de varias horas, incluso días, pero un modelo de aprendizaje automático podría hacerlo en pocos minutos.

* How will we measure the metric? (e.g. A/B test on a specified subset for a specified period; or comparison of performance after implementation to baseline)

Debido a que no se dispone de valores de referencia anteriores, se usará la métrica de accuracy para determinar el porcentaje de aciertos en las clasificaciones de las estrellas, y queda a juicio del investigador si lo considera como una buena herramienta para su uso académico.

## Plan
* Phases (milestones), timeline, short description of what we'll do in each phase.
	* Entendimiento del negocio: Con esto se busca comprender el tipo de datos que se dispone y de dónde provienen, así mismo puntualizar el trabajo a realizar y fijar los elementos a optimizar y/o a resolver mediante herramientas de ciencia de datos. Duración máxima: 1 semana.
	* Carga de datos, exploración y procesamiento de los mismos: Se descargarán los datos desde la web y se cargarán Google Colab, lugar donde se harán tareas de reconocimiento de los datos, búsqueda de valores faltantes, correlaciones entre ellos y análisis gráficos que den información adicional antes de entrenar cualquier modelo. Duración máxima: 2 semanas.
	* Modelación y evaluación: Los modelos de aprendizaje automático se entrenarán en esta sección, donde se buscará la mejor herramienta para obtener los mejores resultados, ya sea un entrenamiento supervisado o no supervisado, así como la escogencia de la librería de sklearn o de tensorflow. Dichos modelos serán evaluados dándole mayor relevancia a los resultados del accuracy según los intereses del consumidor. Duración máxima: 2 semanas.
	* Despliegue: Luego de obtener el modelo más adecuado para realizar las predicciones deseadas, se buscará la mejor opción para su posterior uso para la comunidad académica, que logre ahorrar tiempos a la hora de querer saber el tipo de una estrella según sus características y que sea fácil y rápido de usar. Duración máxima: 1 semana.

## Architecture
* Data
  * What data do we expect? Raw data in the customer data sources (e.g. on-prem files, SQL, on-prem Hadoop etc.)

Los datos serán extraídos de la página web de Kaggle, donde se encuentra un archivo .csv con mediciones realizadas observacionalmente (datos en bruto).

* Data movement from on-prem to Azure using ADF or other data movement tools (Azcopy, EventHub etc.) to move either

Como ya se ha mencionado, los datos a usar se encuentran en Kaggle, de allí se descargarán manualmente como archivo .zip a una máquina local, para posteriormente cargarlos a un notebook de colab, donde el archivo es descomprimido y posteriormente manipulado en Python haciendo uso de la librería de Pandas y otras herramientas.

* What tools and data storage/analytics resources will be used in the solution e.g.,

En primer lugar, se utilizará Google Colaboratory para manipular los datos y construir los modelos a implementar, cuyo sistema operativo y su versión son 'Linux-5.10.133+-x86_64-with-Ubuntu-18.04-bionic', es decir, un dispositivo con dichas características podría ejecutar el modelo. Sin embargo, no se usarán comando exclusivos de linux para tener un mayor alcance de otros dispositivos con características diferentes. Además, se hará uso de librerías como Numpy, Pandas, Matplotlib, Seaborn, Sklearn y Tensorflow para el desarrollo de modelos. 

* How will the score or operationalized web service(s) (RRS and/or BES) be consumed in the business workflow of the customer? If applicable, write down pseudo code for the APIs of the web service calls.
  * How will the customer use the model results to make decisions
  * Data movement pipeline in production
  * Make a 1 slide diagram showing the end to end data flow and decision architecture
    * If there is a substantial change in the customer's business workflow, make a before/after diagram showing the data flow.

## Communication
* How will we keep in touch? Weekly meetings?

Se realizan 3 sesiones semanales con los clientes inmediatos, con el fin de mejorar las técnicas usadas y obtener mejores resultados según las métricas para evaluar los modelos.

* Who are the contact persons on both sides?

De una de las partes, Carlos Gutierrez, el creador de los modelos a implementar y quien posee conocimientos en el tema a desarrollar. Del otro lado, Juan Sebastián Lara y Juan Sebastián Malagón.
