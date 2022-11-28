# Data and Feature Definitions

This document provides a central hub for the raw data sources, the processed/transformed data, and feature sets. More details of each dataset is provided in the data summary report. 

For each data, an individual report describing the data schema, the meaning of each data field, and other information that is helpful for understanding the data is provided. If the dataset is the output of processing/transforming/feature engineering existing data set(s), the names of the input data sets, and the links to scripts that are used to conduct the operation are also provided. 

For each dataset, the links to the sample datasets in the _**Data**_ directory are also provided. 

_**For ease of modifying this report, placeholder links are included in this page, for example a link to dataset 1, but they are just placeholders pointing to a non-existent page. These should be modified to point to the actual location.**_

## Raw Data Sources

| Dataset Name | Original Location   | Destination Location  | Data Movement Tools / Scripts | Link to Report |
| ---:| ---: | ---: | ---: | -----: |
| Stars.csv | Los datos se descargan de la página web [Kaggle](https://www.kaggle.com/datasets/deepu1109/star-dataset) en la ruta "/c/Users/hurom/Jupyter/MLDS/MLDS6" | Se trabajará en Google Colab, así que se sube el conjunto de datos original de Drive bajo la ruta "/content/drive/MyDrive/Project/Data/stars.csv" | No fue usado el cliente de Kaggle, ya que el dataset es del orden de KB. | [Dataset 1 Report](docs/data/data_dictionary.md)|

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
| Processed Dataset 1 | [Dataset1](link/to/dataset1/report), [Dataset2](link/to/dataset2/report) | [Python_Script1.py](link/to/python/script/file/in/Code) | [Processed Dataset 1 Report](link/to/report1)|
| Processed Dataset 2 | [Dataset2](link/to/dataset2/report) |[script2.R](link/to/R/script/file/in/Code) | [Processed Dataset 2 Report](link/to/report2)|
* Processed Data1 summary. <Provide brief summary of the processed data, such as why you want to process data in this way. More detailed information about the processed data should be in the Processed Data1 Report.>
* Processed Data2 summary. <Provide brief summary of the processed data, such as why you want to process data in this way. More detailed information about the processed data should be in the Processed Data2 Report.> 

## Feature Sets

| Feature Set Name | Input Dataset(s)   | Feature Engineering Tools/Scripts | Link to Report |
| ---:| ---: | ---: | ---: | 
| Feature Set 1 | [Dataset1](link/to/dataset1/report), [Processed Dataset2](link/to/dataset2/report) | [R_Script2.R](link/to/R/script/file/in/Code) | [Feature Set1 Report](link/to/report1)|
| Feature Set 2 | [Processed Dataset2](link/to/dataset2/report) |[SQL_Script2.sql](link/to/sql/script/file/in/Code) | [Feature Set2 Report](link/to/report2)|

* Feature Set1 summary. <Provide detailed description of the feature set, such as the meaning of each feature. More detailed information about the feature set should be in the Feature Set1 Report.>
* Feature Set2 summary. <Provide detailed description of the feature set, such as the meaning of each feature. More detailed information about the feature set should be in the Feature Set2 Report.> 
