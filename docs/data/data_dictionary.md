# Data Dictionary

# Database Stars data

Los datos a usar para este proyecto consisten en un único conjunto en forma de archivo .csv, conformado por 240 filas y 7 columnas, representando 240 estrellas y 7 de sus características principales. Los datos fueron obtenidos de multiples observaciones astrofísicas y algunas cantidades fueron calculadas siguiendo leyes físicas como sigue:

	* 1. Para la luminosidad de la estrella fue usada la ley de Stefan-Boltzmann de la radiación de cuerpo negro.
	* 2. Para la temperatura superficial de la estrella se usó la ley de desplazamiento de Wien usando la longitud de onda.
	* 3. Fue usada la relación de la magnitud absoluta.
	* 4. El radio de la estrella fue calculado a través de paralaje.


## Table 1

Para mayor información de cada columna, revisar a continuación

| column | type | description |
| --- | --- | --- |
| Temperatura | int64 | Temperatura de la superficie de la estrella calculada con su longitud de onda asociada. Medida en Kelvin (K). |
| Luminosidad | float64 | Luminosidad de la estrella calculada con la ley de Stefan-Boltzmann. Adimensional al estar escalada con la luminosidad del sol (L/Lo). |
| Radio | float64 | Radio de la estrella calculado usando paralaje. Adimensional al estar calculado con el radio del sol (R/Ro). |
| Magnitud absoluta | float64 | Magnitud absoluta de la estrella. Medida en (Mv). |
| Tipo de estrella | int64 | Etiqueta a predecir por los modelos, toma valores de 0 a 5 indicando un tipo de estrella diferente: Enana marrón, enana roja, enana blanca, secuencia principal, supergigante e hipergigante. |
| Color de la estrella | object | Color de este objeto celeste. |
| Clase espectral | object | Clase espectral de cada estrella (O, B, A, F, G, K, M) |
