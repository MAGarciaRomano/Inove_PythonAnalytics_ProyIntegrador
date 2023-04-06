## Inove_PythonAnalytics_ProyIntegrador
# Proyecto Integrador. Predictor de resultados en partidos de Campeonatos Mundiales.
## Autor: Martín A. García Romano
### Curso Python Analytics (2022)
#### Objetivo del Proyecto Integrador
(Basado en el proyecto de un clasificador para predecir la selección nacional ganadora de un partido de fútbol).
Se realizó un clasificador para predecir el resultado posible (local, empate o visita) de un partido de fútbol entre dos selecciones nacionales de fútbol.
#### Recolección de datos
Se toma como fuente para su dataset un archivo de producción propia con los resultados de todos los partidos disputados en los Campeonatos Mundiales de 
Fútbol de la FIFA, incluyendo el disputado en Qatar en 2022.
#### Preparación del dataset
Del dataset original se conservan sólo tres columnas: la de la selección que hace las veces de local, la de la selección que hace las veces de visitante y 
la columna que refleja el resultado final del partido (local, empate o visitante), ya sea que se haya definido en el tiempo reglamentario, en tiempo 
suplementario o por penales.
#### Codificación.
El proyecto toma dataset obtenido y lo transforma a través de cada una de las siguientes tres codificaciones:
- Label Encoder.
- One Hot Encoder.
- Binary Encoder.
#### Clasificador
Con cada codificación se elabora un clasificador con Random Forest Classifier para el que previamente se determinan parámetros óptimos de n_estimators y 
max_depth.
#### Métricas
Para cada modelo aplican las siguientes métricas:
- accuracy_score
- confusion_matrix
- f1_score
#### Utilización del modelo
Se hace una sola utilización del modelo clasificador con la codificación Label Encoder.
En la misma se pueden introducir por teclado la selección local, la selección visitante y obtener la predicción del resultado.
No se hace una verificación sobe el texto introducido en cada caso.
#### Respaldo de dataframes y exportación de codificaciones y modelos.
- Se respaldan los dataframes sobre los que trabaja cada modelo en formato csv.
- Se exporta la codificación en Label Encoder.
- Se exportan los tres modelos según las codificaciones realizadas.
### Resultados
El accuracy (exactitud) de cada uno de los tres modelos supera holgadamente al modelo base que se crea previamente.
El accuracy de los tres modelos supera el 50% tal cual se establece en el objetivo del proyecto propuesto por Inove, pero lo hace por un margen muy 
estrecho, ubicándose en un rango que va entre el 53% y el 55%.
A lo largo de varias pruebas la mayor exactitud se obtuvo con el modelo que utilizó la codificación One Hot Encoder. Luego le sigue el modelo en el que 
se codificó mediante Binary Encoder y el peor resultado se obtuvo en el modelo que trabajó con Label Encoder. Sin embarog, en varios de los ensayos, los
modelos con Binary Encoder y Label Encoder obtuvieron la misma exactitud.



