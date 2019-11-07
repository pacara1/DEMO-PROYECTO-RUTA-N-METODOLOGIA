# ANALITICA DESCRIPTIVA DE LAS MUERTES OCURRIDAS EN SINIESTROS VIALES EN EL MUNICIPIO DE MEDELLIN DE LOS AÑOS 2008 A 2019
#
#
>>>>>>>>>### Paolo Andrés Camacho Ramírez
>>>>>>>>>### Michael Gómez Lopera
>>>>>>>>>### Eduardo Santacruz
>>>>>>>>>### William Zapata
###
###
>>>>>### Estudiantes Curso Analitica Predictiva con Python
>>>>>### Convenio Universidad Nacional- Ruta N- Alcaldia de Medellin
#
### Noviembre 3 de 2019
#
#
## Resumen
#

## Tabla de Contenido
#
1.Introducción

>>1.1. Motivación

>>1.2. Metodología

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
#
#
#
## 1.Introducción

>## 1.1. Motivación
Según los lineamientos contenidos en el Decenio de Acción para la Seguridad Vial de la OMS, el mejoramiento de las condiciones de seguridad vial se debe trabajar a través de 5 ejes fundamentales: Fortalecimiento Institucional, Comportamiento Humano, Vehículos Seguros, Infraestructura Segura y Atención a Víctimas. El Municipio de Medellín, demostrando un alto nivel de compromiso en el trabajo por la seguridad vial, adoptó en el año 2014 el Plan de Movilidad Segura 2014-2020, el cuál mediante el diseño y definición de múltiples estrategias a través de sus 5 componentes, tiene como objetivo la reducción de víctimas fatales en incidentes de tránsito en un 25% para el año 2020. 

Gracias al trabajo interdisciplinar y a las diversas estrategias ejecutadas por la Secretaría de Movilidad, Medellín se ha convertido en un referente nacional en seguridad vial, obteniendo por parte de la Agencia Nacional de Seguridad Vial en el 2018 el reconocimiento como la ciudad capital con mayor reducción de fallecidos en hechos viales.

Una de las estrategias fundamentales comprende el análisis detallado de la información registrada en los Informes Policiales de Accidentes de Tránsito para los casos de mortalidad, de modo que permitan identificar patrones o tendencias que faciliten el desarrollo de estrategias que permitan continuar disminuyendo la ocurrencia de eventos fatales.

Para este fin se hace necesario el uso e implementación de herramientas analíticas avanzadas para procesar grandes volúmenes de información, correlación bases de datos y generar análisis multivariados que brinden nuevas perspectivas sobre como atacar el problema de seguridad vial en Medellín. 
#
#
>## 1.2. Motivación
Durante el curso de Analítica de Datos Predictiva fue posible conocer técnicas estadísticas que facilitaban el cálculo de pronósticos de tomando la información de incidentes viales en la ciudad, utilizando tanto estadística descriptiva como probabilística.
Mediante la aplicación de estas técnicas se pretende crear una herramienta descriptiva que sirva de base para la visualización de la información y permita realizar análisis correlacionando múltiples variables y que posibiliten la creación de un sistema predictivo sobre los casos de mortalidad en incidentes viales.
A continuación se indican los principales productos de este trabajo:
1. Código de ejecución del modelo.
2. Reporte que contenga el entendimiento desarrollado en el trabajo.
3. Visualización de los datos y la predicción del modelo
#
## 2.Desarrollo

>## 2.1. Identificación del problema
Según la Organización Mundial de la Salud (OMS) en el mundo mueren 1,24 millones de personas al año por accidentes de tránsito y entre 40 y 50 millones de personas sufren lesiones a causa de estos eventos, lo cual ha aumentado la alerta frente al impacto global en la salud pública y productividad que conllevan los accidentes viales, al punto que ha sido declarado como una “Pandemia”, y representan la primera causa de muerte en la población juvenil de 15 a 29 años de edad y la tercera en la población de 30 a 40 años de edad. Asimismo, las tendencias actuales indican que, de no tomarse medidas urgentes, los incidentes de tránsito se convertirán en la quinta causa de muerte para 2030 (Organización Mundial de la Salud OMS, 2013).

En este sentido, en marzo de 2010, la resolución 64/255 de la Asamblea General de las Naciones Unidas proclamó el periodo 2011–2020 «Decenio de Acción para la Seguridad Vial» con el objetivo de estabilizar y, posteriormente, reducir las cifras previstas de víctimas mortales en accidentes de tránsito en todo el mundo, aumentando las actividades en los planos nacional, regional y mundial.

Siendo Colombia miembro de la ONU, se acogio a las directricez y politicas establecidas en el Decenio de Acción para la Seguridad Vial 2011–2020, para lo cual se expidio la respectiva normatividad que reglamentara la elaboracion de planes estrategicos de seguridad vial en el nivel nacional, departamental, municipal y empresarial; de otro lado se crearon Observatrios de seguridad vial en estos mismos niveles , encargados fundamentalmente de realizar seghuimiento a la evolucion de las metas trazadas endichos planes y adoptar estrategias que redunden en la reduccion de la lesiones y mortalidad en accidentes viales.

Tomando en cuenta la problematica enunciada, se plantea el desarrollo de este proyecto para la creacion de herramietas que permitan tener informacion para apoyar la toma de desciciones y la adopcion de estrategias de intervencion considerando la informacion de  grupos etareos afectados , georreferenciacion e identificacion donde zonas donde las muertes son recurrentes, detectar la incidencia de la alcoholemia, las muertes segun la garvedad, los rangos horarios con mayor numero de muertes, el dia de la semana el mes del año con el mayor numero de muertos
#
#
>## 2.2. Identificación de los datos
Para este proyecto se utilizó la base de datos enaviada por el consorcio contratista SIMM, el cual es el encargados de transcribir la información levantada por los Agentes de Tránsito con funciones de Policía Judicial en la vía, esta base de datos se viene diligenciando en formato excel desde el año 2008 al 18 de agosto de 2019, el libro de excel esta compuesto de doce hojas, una para cada año correspondiente.  link a los archivos de excel.

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
