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
| X_train.csv | [Stars.csv](link/to/dataset1/report) | [data_exploring.ipynb](https://github.com/cagutierrezgu/tdsp_template/blob/aa9bda826f1b09c181274744cc697ffd9b036ff9/scripts/data_loading.ipynb) | [X_train.csv Report](data_summary.md)|
| X_test.csv | [Stars.csv](link/to/dataset2/report) |[data_exploring.ipynb](https://github.com/cagutierrezgu/tdsp_template/blob/aa9bda826f1b09c181274744cc697ffd9b036ff9/scripts/data_loading.ipynb) | [X_test.csv Report](data_summary.md)|
| y_train.csv | [Stars.csv](link/to/dataset2/report) |[data_exploring.ipynb](https://github.com/cagutierrezgu/tdsp_template/blob/aa9bda826f1b09c181274744cc697ffd9b036ff9/scripts/data_loading.ipynb) | [y_train.csv Report](data_summary.md)|
| y_test.csv | [Stars.csv](link/to/dataset2/report) |[data_exploring.ipynb](https://github.com/cagutierrezgu/tdsp_template/blob/aa9bda826f1b09c181274744cc697ffd9b036ff9/scripts/data_loading.ipynb) | [y_test.csv Report](data_summary.md)|

* X_train, X_test, y_train and y_test summary. <Provide brief summary of the processed data, such as why you want to process data in this way. More detailed information about the processed data should be in the Processed Data1 Report.>

## Feature Sets

| Feature Set Name | Input Dataset(s)   | Feature Engineering Tools/Scripts | Link to Report |
| ---:| ---: | ---: | ---: | 
| Feature Set 1 | [Dataset1](link/to/dataset1/report), [Processed Dataset2](link/to/dataset2/report) | [R_Script2.R](link/to/R/script/file/in/Code) | [Feature Set1 Report](link/to/report1)|
| Feature Set 2 | [Processed Dataset2](link/to/dataset2/report) |[SQL_Script2.sql](link/to/sql/script/file/in/Code) | [Feature Set2 Report](link/to/report2)|

* Feature Set1 summary. <Provide detailed description of the feature set, such as the meaning of each feature. More detailed information about the feature set should be in the Feature Set1 Report.>
* Feature Set2 summary. <Provide detailed description of the feature set, such as the meaning of each feature. More detailed information about the feature set should be in the Feature Set2 Report.> 
