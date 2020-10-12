# Crítica de la lectura 9-1: Multi-Armed Recommender System Bandit Ensembles 
En este reciente *paper* presentado en la RecSys'19, los autores españoles Cañamares, Redondo  y Castells presentan un ensamble de sistema recomendador que lo describen como *Multi-armed Bandit Ensemble*.

### Resumen

Se ha comprobado empíricamente que las recomendaciones más efectivas se dan cuando se utilizan sistemas que combinan diferentes tipo de algoritmos. Estos se conocen como sistemas híbridos, pero cada uno tiene su forma especial de combinar los algoritmos. La mayoría de estos trabajos consideran escenarios simples donde los datos son estáticos, ya que se tienen los ítems con que se miden las métricas finales. Por esto, en este trabajo se van a ensamblar algoritmos que van a ser dinámicamente ajustados y actualizados según un proceso cíclico, donde los usuarios reaccionan a las recomendaciones realizadas por estos y generar una mejor efectividad del sistema.

El modelo propuesto es utilizar un *multi-armed bandit approach* para realizar ensambles de sistemas recomendadores. Este consiste en: **contexto**, el usuario objetivo al que se le va a recomendar, **brazos**,  que son los algoritmos recomendadores que se combinan en el ensamble, la **recompenza**, que es 1 si el usuario esta conforme o 0 en otro caso y la **actualización** de los brazos por cada recomendación individual. Lo importante de este método es que la selección del algoritmo recomendador en cada etapa depende del desempeño que tuvo en el último ciclo que fue seleccionado.

El experimento realizado se hizo con el dataset de Movielens y los algoritmos de ensambles probados fueron **e-greedy bandit** y **Thompson sampling bandit**. Estos se compararon con los algoritmos independientes de *most popular*, *user-based kNN* y *matrix factorization* y mediante la métrica de recall acumulativa.

El resultado principal fue que ambos sistemas de ensambles tuvieron mejores resultados que los algoritmos independientes, pero entre ellos fue muy pequeña la diferencia de desempeño.

Se concluyó que el ensamble recomendador propuesto tuvo un resultado empíricamente efectivo y tiene la ventaja adicional de que tiene bajo costo computacional.

### Comentario

A pesar de que este *paper* era breve (4 páginas), presenta un gran aporte al área por el hecho de proponer un nuevo sistema recomendador generado por ensamble que obtiene un mejor rendimiento que los algoritmos básicos de forma independiente.

Encontré que estaba bien estructurado el documento y ocupaban un vocabulario sencillo que permitía tener una fácil lectura. Además, las figuras con los gráficos permitían analizar de forma más rápida y sencilla  los resultados obtenidos del experimento. Lo que me hubiera gustado ver es que se probara con datasets de otras áreas, ya que así se podría ver si es lo suficientemente robusto y comprobar si es efectivamente mejor que los otros algoritmos. 

Yo opino que los ensambles de algoritmos es una herramienta muy poderosa, y que pueden generar buenos resultados, sin embargo, no se ven comúnmente en los sistemas actuales.  Además, en particular me gustó la forma en que el modelo presentado genera las recomendaciones. Encuentro que es bastante intuitivo que se vaya eligiendo sólo un algoritmo por cada recomendación y que la elección dependa del desempeño de la última vez que se seleccionó. Esto, como lo dijeron los autores, permite generar un algoritmo más eficiente en términos computacionales, ya que sólo se corre un algoritmo por iteración y no varios que luego se combinan de cierta forma, como lo hacen otros sistemas híbridos. 

Una de las novedades que se presentaba en este *paper* era que utilizaban el *feedback* de los usuarios después de entregar las recomendaciones para mejorar el rendimiento. Sin embargo, este proceso puede ser bastante complejo y se demora bastante tiempo para realizar los experimentos.

A modo de conclusión, quiero decir que encontré bastante novedosa el sistema de recomendación basado en ensambles que se presentó, aunque me siento que faltaron más pruebas para ver el real beneficio que puede generar al área de RecSys.

