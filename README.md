# PROYECTO INDIVIDUAL N° 2
Data Science- Soy Henry

## Accidentes Aereos

![AdobeStock_618340412](https://github.com/ACGomezW/PI_2_DataAnalysis/assets/135540204/6ab1898d-6f21-4d1b-81b9-08ff4d37441a)


### Contexto

Este proyecto se centra en el análisis de accidentes aéreos, con el objetivo de comprender mejor tendencias y patrones relacionados con los accidentes de aviación. 
En el rol de Data Analytics se utilizarán los datos para obtener información significativa que ayude a la toma de decisiones y resolución de problemas.

Los accidentes aéreos sean aviones, helicópteros o dirigibles han sido un tema de gran importancia en la industria de la aviación; y su análisis es esencial para identificar las posibles causas de los accidentes, mejorar la seguridad y la prevención de futuros accidentes, evaluar esas medidas y regulaciones existentes.

### Dataset

El dataset original posee información acerca de vuelos que han sufrido accidentes en todo el mundo desde el año 1908 hasta 2021. El mismo cuenta con 5008 filas (cada fila es un registro de accidente aéreo) y 18 columnas (atributos de los accidentes).

### Procesos

## **E.T.L.** *(Extract, Transform and Load)*

  Se cargó el archivo formato csv, para trabajar con Python, realizando una primera inspección de algunas columnas, se eliminan posibles registros duplicados y se realizan las transformaciones necesarias para la identificación de registros nulos que no se registraban como tal, sino que tenían un '?' en su lugar. Se imputan valores faltantes en las columnas numéricas de las víctimas de los siniestros, con el objetivo de no perder información relevante. 
  También se llevó a cabo la transformación de tipo de dato para un correcto análisis y se normalizaron y clasificaron columnas categóricas que tenían información muy importante, pero con datos poco estructurados, para una mejor comprensión.  
  * Se categorizaron las columnas que describían la ubicación (dejando el nombre del país).
  * Se categorizó también la columna 'operador', ya que con un gráfico de 'nube de palabras' se observó que los operadores eran militares, privados y una gran proporción eran empresas comerciales.
  * Con la columna de 'modelo' se agregó una columna que clasifica su tipo en aviones, helicópteros o dirigibles, aún asi se deja la columna 'modelo' pues se consider útil para el análisis.
  
  Se crearon 'Nubes de palabras' para una aproximación a las causas de los accidentes y con el fin de identificar patrones comunes en la información.  
  Posteriormente se detectaron 'outliers' (datos atípicos) mediante gráficos y funciones visualizando y analizando caso por caso su posible imputación o eliminación del archivo.  
  Finalmente se eliminaron columnas innecesarias para el análisis.

## **E.D.A.** *(Exploratory Data Analysis)*

En el análisis exploratorio se realizaron varias métricas con el fin de establecer relaciones entre las variables y comprender mejor su relación, para tener un mejor 'conocimiento de negocio':
* Para las variables numéricas se realizaron gráficos de dispersión, para observar relaciones entre sí.
* Se graficó una matriz de correlación de las variables con el cual se identificaron las que son extremadamente dependientes de aquellas que no lo son.
* Se observaron las medidas de tendencia central para un mejor escenario de los datos.

* Para las variables categóricas se realizaron gráficos de barras, barras apliladas, circulares con los que se observaron cantidades en el agrupamiento, las fuertes tendencias de algunas variables en particular (de operador o de modelo).
* Con el Procesamiento de Lenguaje Natural también se realizó 'Nube de Palabras' para el estudio de la columna que describe el resúmen de los datos, a fin de identificar patrones en común que pudieran dilucidar causas de los siniestros.

  Una vez realizados estos dos procesos se guarda el archivo 'limpio' en un nuevo archivo llamado 'vuelos' formato 'csv'.

## **Visualización**

  Se cargó el nuevo archivo 'vuelos' con formato csv a PowerBi, donde a traves de Power Query se realizaron transformaciones de modo tal que el archivo original quede dividido en tablas, resultando la tabla de hechos 'vuelo' y tres tablas de dimensiones 'operador', 'tipo_modelo' y 'pais', agregando las columnas de identificación para cada una y vinculando ese dato a la tabla de hechos para crear un Diagrama de Entidad Relación que fuera concordante para el análisis.  
  Además se creó la tabla 'Calendario' con sus cálculos por año, mes, trimestre para la interpretación de datos.  
  Se efectuaron distintos cálculos de medidas para determinar patrones o tendencias mediante gráficos interactivos. 
  El Dashboard consta de 

