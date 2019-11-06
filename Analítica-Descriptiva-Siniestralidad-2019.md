# ANALITICA DESCRIPTIVA DE LAS MUERTES OCURRIDAS EN SINIESTROS VIALES EN EL MUNICIPIO DE MEDELLIN DE LOS AÑOS 2008 A 2019
#
#
>>>>>>>>>### Paolo Andrés Camacho Ramírez
>>>>>>>>>### William
>>>>>>>>>### Michael
>>>>>>>>>### Eduardo Santacruz Sanmartín
###
###
>>>>>### Estudiantes Curso Analitica Predictiva con Python
>>>>>### Convenio Universidad Nacional- Ruta N- Alcaldia de Medellin
#
### Noviembre 3 de 2019
#
#
## Resumen

Actualmente en el mpio de Medellín se generan gran cantidad de registros de información que se están acumulando, pero que no se alcanzan a analizar para la planeación y la toma de decisiones.

Uno de los puntos más importantes es la accidentalidad vehicular y la mortalidad que se presenta constantemente en la ciudad por la cantidad de medios de transporte que actualmente tiene la ciudad de Medellín.

Este trabajo busca generar el análisis de la información de la mortalidad que se presentan en los hechos vehiculares con el propósito de tener una herramienta que por lo menos cree herramientas para análisis y la toma de decisiones en la ciudad de Medellín.

En este trabajo utilizar la información de la accidentalidad vehicular en el municipio de Medellín para  años anteriores con el fin de pronosticar la frecuencia de accidentes agrupada según su tipo.

Utilizamos las herramientas descriptivas en phyton con este trabajo para crear una herramienta que sirva como base para analizar la problemática en la ciudad de Medellín.


## Tabla de Contenido
#
1.Introducción

En el diario transcurrir de la ciudad de Medellín, se están reportando grandes cantidades de novedades en la movilidad de la ciudad de Medellín, esto genera información y bases de datos públicas y privadas.

Todavía no se tienen herramientas definitivas para hacerle un seguimiento al 100% de las novedades que se presentan en la ciudad de Medellín.

Por lo anterior, un grupo de funcionarios de la alcaldía que recibieron las bases sobre analítica de datos en Phyton, tienen como objetivo generar una herramienta que sirva para visualizar las novedades sobre las víctimas fatales que surgen diariamente por accidentalidad de tránsito en la ciudad de Medellín.


>>1.1. Motivación

En analítica de datos predictiva se vieron técnicas estadísticas para pronóstico de la información, utilizando concepto de estadística descriptiva y probabilística.

El objetivo del trabajo es crear una herramienta descriptiva que sirva de base para la visualización de la información y que este sirva como base para comenzar a crear un sistema predictivo completo para el tema de mortalidad en la accidentalidad de tránsito.
Los entregables del trabajo son:

1.	Código de ejecución del modelo. 
2.	Reporte que contenga el entendimiento desarrollado en el trabajo-.
3.	Visualización de  los datos y la predicción del modelo


>>1.2. Metodología

## 2.Desarrollo

>## 2.1. Identificación del problema

Según la Organización Mundial de la Salud (OMS) en el mundo mueren 1,24 millones de personas al año por accidentes de tránsito y entre 40 y 50 millones de personas sufren lesiones a causa de estos eventos, lo cual ha aumentado la alerta frente al impacto global en la salud pública y productividad que conllevan los accidentes viales, al punto que ha sido declarado como una “Pandemia”, y representan la primera causa de muerte en la población juvenil de 15 a 29 años de edad y la tercera en la población de 30 a 40 años de edad. Asimismo, las tendencias actuales indican que, de no tomarse medidas urgentes, los incidentes de tránsito se convertirán en la quinta causa de muerte para 2030 (Organización Mundial de la Salud OMS, 2013).

En este sentido, en marzo de 2010, la resolución 64/255 de la Asamblea General de las Naciones Unidas proclamó el periodo 2011–2020 «Decenio de Acción para la Seguridad Vial» con el objetivo de estabilizar y, posteriormente, reducir las cifras previstas de víctimas mortales en accidentes de tránsito en todo el mundo, aumentando las actividades en los planos nacional, regional y mundial.

Siendo Colombia miembro de la ONU, se acogio a las directricez y politicas establecidas en el Decenio de Acción para la Seguridad Vial 2011–2020, para lo cual se expidio la respectiva normatividad que reglamentara la elaboracion de planes estrategicos de seguridad vial en el nivel nacional, departamental, municipal y empresarial; de otro lado se crearon Observatrios de seguridad vial en estos mismos niveles , encargados fundamentalmente de realizar seghuimiento a la evolucion de las metas trazadas endichos planes y adoptar estrategias que redunden en la reduccion de la lesiones y mortalidad en accidentes viales.

Tomando en cuenta la problematica enunciada, se plantea el desarrollo de este proyecto para la creacion de herramietas que permitan tener informacion para apoyar la toma de desciciones y la adopcion de estrategias de intervencion considerando la informacion de  grupos etareos afectados , georreferenciacion e identificacion donde zonas donde las muertes son recurrentes, detectar la incidencia de la alcoholemia, las muertes segun la garvedad, los rangos horarios con mayor numero de muertes, el dia de la semana el mes del año con el mayor numero de muertos

Dado el crecimiento que surgió en la ciudad de Medellín durante los últimos en los en la compra y venta del parque automotor y de la venta explosiva de motos en la ciudad, se han presentado dificultades de diversas formas, ya que las personas que consiguen su propia forma de vehículo no han tenido la suficiente experiencia en conducción y conocimiento en el manejo en las calles, lo cual ha generado que se presenten gran cantidad de sucesos y que sucedan muchos hechos catastróficos.

Con este trabajo se pretende crear una herramienta base para la ciudad con el fin de poder hacerle seguimiento a los hechos catastróficos y con esto poder comenzar a analizar que sucede realmente y de qué forma tomar decisiones para generar normas y controles que eviten estos sucesos en la ciudad de Medellín.

#
>## 2.2. Identificación de los datos

Para este proyecto se utilizó la base de datos que transcribe el contratisa UNE, quienes son los encargados de transcribir la información levantada por el guarda de transito en la vía, esta base de datos se viene diligenciando en formato excel desde el año 2008 al 18 de agosto de 2019, el libro de excel esta compuesto de doce hojas, una para cada año correspondiente.  link a los archivos de excel.

La estructura de la tabla en excel es la siguiente:

Orden	|Fecha Ocurrencia	|Hora Ocurrencia	|Fecha Levantamiento	|Spoa	|Expediente	|Clase	|Grupo	|Direccion Ocurrencia	|Municipio	|Lugar de Inspección	|Victima_Nombre	|Victima_Apellido	|Identificacion	|Sexo	|Años	|Condicion	|Vehículo Víctima o vehículo que atropella	|Placa	|Servicio	|Empresa	|Embriaguez 

Se realizo la respectiva anonimización de los datos de forma manual, en el archivo de excel, con el fin de poder publicarlo en este repositorio; se constituye a partir de este archivo un dataframe de pandas para realizar la respectiva preparación de los datos; procedimiento y codigo que se muestran mas adelante en el numeral 2.2.1.
#
#
>## 2.3. Descripción del conjunto de datos
El lenguaje de programación que se utilizara es Python, Para la limpieza de datos, los paquetes pandas, openpyxl, numpy y datetime; para el análisis de la información se utilizará los paquetes pandas;  para visualización se usan seaborn, folium; para geocodificación se usará el paquete geocoder y para estimar los modelos rpart y rpart.plot.
#
>>### 2.3.1. Limpieza y resumen de los datos
Se inicia leyendo los archivos de excel para crear un dataframe de pandas que concatene las hojas existentes del libro que contiene la base de datos, este arcivo se llama MUERTOS.xlsx. Luego de esto se crea un dataframe donde se renombran algunas columnas y se eliminan otras inecesaria para los fines de este proyecto, quedando la siguiente estructura de data frame

Index |Fecha Ocurrencia	|Hora Ocurrencia	|Edad Víctima	|Sexo	|Clase de Accidente	|Condición Víctima	|Vehículo Víctima o vehículo que atropella	|Dirección Ocurrencia	|Prueba Embriaguez|	Empresa Servicio Público	|Fecha Levantamiento	|Lugar de Inspección	|Servicio Publico o Particular	|Muertes	|Rango de Edades

A continuacion se realiza una limpieza sobre los 3305 registros existentes, rellenando los registros sin iniformacion  con null y unificando las categorias de cada campo.

2.Desarrollo

>>2.1. Identificación del problema

>>2.2. Identificación de los datos

>>2.3. Descripción de los datos

>>>2.3.1. Limpieza y resumen

>>>2.3.2. Análisis de los datos

>>>2.3.3. Tratamiento de datos atípicos

>>2.4. Modelación de los datos

>>2.5. Evaluación del modelo

>>2.6. Implementación del modelo

3.Conclusiones

4.Bibliografía
