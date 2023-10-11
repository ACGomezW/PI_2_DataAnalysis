# PROYECTO INDIVIDUAL N° 2
Data Science- Soy Henry

## Accidentes Aereos

![AdobeStock_618340412](https://github.com/ACGomezW/PI_2_DataAnalysis/assets/135540204/6ab1898d-6f21-4d1b-81b9-08ff4d37441a)


### Contexto

Este proyecto se centra en el análisis de accidentes aereos, con el objetivo de comprender mejor tendencias y patrones relacionados con los accidentes de aviación. 
En el rol de Data Analytics se utilizarán los datos para obtener información significativa que ayude a la toma de decisiones y resolución de problemas.

Los accidentes de aviones han sido un tema de gran importancia en la industria de la aviación; y su análisis es esencial para identificar las posibles causas de los accidentes, mejorar la seguridad y la prevención de futuros accidentes, evaluar las medidas de seguridad y regulaciones existentes.

### Dataset

El dataset original posee información acerca de vuelos que han sufrido accidentes en todo el mundo desde el año 1908 hasta 2021. El mismo cuenta con 5008 filas (cada fila es un registro de accidente aéreo) y 18 columnas (atributos de los accidentes).

### Procesos

## **E.T.L.** *(Extract, Transform and Load)*

Se cargó el archivo formato csv, para trabajar con Python, realizando una primera inspección de algunas columnas, se eliminan posibles registros duplicados y se realizan las transformaciones necesarias para la identificación de registros nulos. Se imputan valores faltantes con el objetivo de no perder información relevante. También se llevó a cabo la transformación de tipo de dato para un correcto análisis y se normalizaron columnas categoricas que tenian información muy importante, pero con datos poco estructurados, se categorizaron y clasificaron para una mejor comprensión de los datos. 
Se crearon 'Nubes de palabras' para una aproximación a las causas de los accidentes y con el fin de identificar patrones comunes en la información. Posteriormente se detectaron 'outliers' (datos atípicos) y se analizó caso por caso su posible imputación o eliminación del archivo. Finalmente se eliminaron columnas innecesarias para el análisis.

## **E.D.A.** *(Exploratory Data Analysis)*

En el análisis exploratorio se realizaron varias métricas con el fin de establecer relaciones entre las variables y comprender mejor su relación, para tener un mejor 'conocimiento de negocio'. Para las variables numéricas se realizaron gráficos de dispersión, matriz de correlación de variables, observación de medidas de tendencia central. Para las categóricas se realizaron gráficos de barras, barras apliladas, circulares, y con el Procesamiento de Lenguaje Natural también se realizó 'Nube de Palabras' para el estudio de tendencias. 


Una vez realizados estos dos procesos se guarda el archivo 'limpio' en un nuevo archivo llamado 'vuelos' formato 'csv'.

## ** Visualización**

Se cargó el nuevo archivo a PowerBi, donde a traves de Power Query se realizaron transformaciones de modo tal que el archivo original quede dividido en tablas, resultando la tabla de hechos 'vuelo' y tres tablas de dimensiones 'operador', 'tipo_modelo' y 'pais'. Además se creó la tabla 'Calendario' y se efectuaron distintos cálculos de medidas para determinar patrones o tendencias mediante gráficos interactivos. 

