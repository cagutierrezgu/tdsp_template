# Data and Feature Definitions

A continuación se presenta la extracción de datos realizada y la manipulación de dichos archivos:

## Raw Data Sources

| Dataset Name | Original Location   | Destination Location  | Data Movement Tools / Scripts | Link to Report |
| ---:| ---: | ---: | ---: | -----: |
| Stars.csv | Los datos se descargan de la página web [Kaggle](https://www.kaggle.com/datasets/deepu1109/star-dataset) en la ruta "/c/Users/hurom/Jupyter/MLDS/MLDS6" | Se trabajará en Google Colab, así que se sube el conjunto de datos original de Drive bajo la ruta "/content/drive/MyDrive/Proyectos/MLDS6/Raw data/stars.csv" | No fue usado el cliente de Kaggle, ya que el dataset es del orden de KB. | [Dataset 1 Report](data_dictionary.md)|

* Stars.csv summary. Este es un conjunto de datos tipo tabla, con 240 estrellas y 7 características para cada una de estas, las cuales son:
	* Temperatura superficial de la estrella (K).
	* Luminosidad escalada a la luminosidad del sol (L/Lo).
	* Radio de la estrella escalado al radio del sol (R/Ro).
	* Magnitud absoluta (Mv).
	* Tipo de estrella (etiqueta de 0 a 5).
	* Color de la estrella (variable discreta).
	* Clase espectral.

## Processed Data
| Processed Dataset Name | Input Dataset(s)   | Data Processing Tools/Scripts | Link to Report |
| ---:| ---: | ---: | ---: | 
| X_train.csv | [Stars.csv](data_dictionary.md) | [data_exploring.ipynb](https://github.com/cagutierrezgu/tdsp_template/blob/aa9bda826f1b09c181274744cc697ffd9b036ff9/scripts/Notebooks/data_exploring.ipynb) | [X_train.csv Report](data_summary.ipynb)|
| X_test.csv | [Stars.csv](data_dictionary.md) |[data_exploring.ipynb](https://github.com/cagutierrezgu/tdsp_template/blob/aa9bda826f1b09c181274744cc697ffd9b036ff9/scripts/Notebooks/data_exploring.ipynb) | [X_test.csv Report](data_summary.ipynb)|
| y_train.csv | [Stars.csv](data_dictionary.md) |[data_exploring.ipynb](https://github.com/cagutierrezgu/tdsp_template/blob/aa9bda826f1b09c181274744cc697ffd9b036ff9/scripts/Notebooks/data_exploring.ipynb) | [y_train.csv Report](data_summary.ipynb)|
| y_test.csv | [Stars.csv](data_dictionary.md) |[data_exploring.ipynb](https://github.com/cagutierrezgu/tdsp_template/blob/aa9bda826f1b09c181274744cc697ffd9b036ff9/scripts/Notebooks/data_exploring.ipynb) | [y_test.csv Report](data_summary.ipynb)|

* X_train, X_test, y_train and y_test summary. No hubo imputación ni eliminación de datos como consecuencia de datos faltantes, ya que no los había. En lugar de esto, se corrigieron los colores de las estrellas porque habían mismos colores escritos de maneras diferentes. Además, se usó la técnica de 'one hot encoding' para las variables categóricas 'Star color' y 'Spectral class' para ser consideradas en los modelos de aprendizaje posteriores de igual manera que las variables numéricas originales. Por último, los datos fueron separados en características y variable objetivo, así como en conjuntos de entrenamiento y prueba.
