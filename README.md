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
  El Dashboard consta de cuatro páginas mas la portada. 
  En la primera página *'General'* se graficaron los principales indicadores de siniestros por pais, por año, y también por hora, junto con la tabla que muestra los paises con mayores índices de accidentes. Se aplicaron filtros para un mejor control del usuario de acuerdo a sus necesidades y preferencias.
  ![General](https://github.com/ACGomezW/PI_2_DataAnalysis/assets/135540204/c8765349-45e9-49c1-9638-55d6486fbe85)  
  
  La segunda página *'fatalidades'* muestra los índices de las víctimas de accidentes, asi también las variaciones de cifras de fallecimientos de acuerdo a los tipos de operadores y modelos.
  ![fatalidades](https://github.com/ACGomezW/PI_2_DataAnalysis/assets/135540204/fc5000d8-d1c8-4997-a9eb-27555c838448)  
  
  La tercer página *'operadores y modelos'* muestra la variaciones de los accidentes de acuerdo al tipo de operador, al tipo de modelo o al modelo en sí mismo. 
![OperadorsyModelos](https://github.com/ACGomezW/PI_2_DataAnalysis/assets/135540204/2af1b625-51bf-4a6b-a32a-2dc7272d032f)  

  la cuarta página *'Claves'* muestra indicadores de acuerdo a objetivos propuestos: 
  * El primer indicador muestra el índice de mortalidad en tripulantes de aeronaves diferenciando las últimas dos décadas. El objetivo propuesto es reducir en un 10% ese índice en la última década respecto de la anterior. Este objetivo no se pudo cumplir ya que en la última década el índice de mortalidad en la tripulación fue mayor que en la anterior.
  * El segundo indicador muestra el índice de supervivencia en general de los ocupantes de aeronaves a lo largo del tiempo. El objetivo propuesto es aumentar en un 5% ese índice respecto del año anterior. Este objetivo no se cumplió dado que en el último año el índice de supervivencia fue menor que el anterior.

    Aquí se anexan gráficos descriptivos del análisis realizado. 
![claves](https://github.com/ACGomezW/PI_2_DataAnalysis/assets/135540204/c2714674-3924-4161-8494-db3356ac6c9a)

### Conclusiones

A lo largo del tiempo los accidentes aéreos han variado en su cantidad, viendo tendencias marcadas, por ejemplo en la década del 20' donde el avión comienza a aumentar su comercialización. Se observa un marcado aumento en la década del 40' interpretando que coincidentemente se produce la Segunda Guerra Mundial y la posterior Guerra de Vietnam que pudo ser uno de los motivos de tal incremento.
Asimismo se nota una baja de esa tendencia posteriormente a la década del 80' en adelante, quizas por los avances tecnológicos y computarizados que mejoraron la seguridad de los aparatos. Respecto de la hora declarada de los accidentes, se puede evaluar que la mayoría se han producido en horas del día. 
El país con mayor indice de accidentes es Estados Unidos, teniendo ese solo país mas del 30% del total de accidentes, asumiendo que se trata del pais con mayor tráfico aéreo, y la diversidad de operadores y flotas. Asimismo si se observa el gráfico de mapa se puede observar que una gran cantidad de accidentes se han producido en regiones montañosas, considerando que ese es un factor importante a la hora de evaluar causas.
Respecto de las fatalidades ocurridads en los accidentes se puede observar que si bien es lógico que entre las víctimas haya un mayor porcentaje de pasajeros frente a la tripulación, a principios de siglo esa tendencia no era tan marcada, asumiendo que la causa se da por el tipo de aeronave, haciendo que a medida que los aviones comerciales se expandieran, esa brecha se agrandara. Por eso mismo se observa una gran tendencia de accidentes de aviones frente a otras aeronaves y del tipo comercial frente a otros tipos de operadores.   
La tasa de mortalidad es en promedio de mas del 70%, se puede observar que si bien ha bajado la cantidad de accidentes, esa tasa ha permanecido casi uniforme a lo largo del tiempo. 
Es de gran importancia que si bien los avances tecnológicos han contribuído a la marcada baja en accidentes, se pueda seguir avanando con los estudios correspondientes para que la tasa de mortalidad tenga una tendencia alcista. 






