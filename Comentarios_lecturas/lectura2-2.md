# Crítica de *BPR: Bayesian Personalized Ranking from Implicit Feedback*

En este *paper* los autores muestran un nuevo criterio de optimización (BPR-OPT) y algoritmo de aprendizaje genéricos para realizar recomendaciones de *rankings* personalizados con *feedback* implícito. Primero, parten con una breve contextualización del funcionamiento de los sistemas recomendadores del momento que son los filtros colaborativos adaptivos (kNN) y la factorización de matrices (MF) y mencionan cuáles son sus principales debilidades al momento de recomendar. Luego, presentan su método para resolver el problema del *ranking* personalizado mediante BPR-OPT. Este se basa en la formulación bayesiana para generar un criterio utilizando el *maximum posterior estimator* para cualquier modelo de recomendación. Después, presenta el algoritmo de aprendizaje *LearnBPR* que consiste en utilizar el descenso del gradiente estocástico con *bootstrapping*  (elegir muestran de forma aleatoria y con reposición). Una vez presentado este algoritmo, muestran como se puede implementar el BPR en los sistemas recomendadores más utilizados del momento, para luego mostrar los resultados de los experimentos realizados que comparan el desempeño de los algoritmos con y sin BPR. Por último, analizan estos resultados y concluyen que utilizar el criterio y el algoritmo de aprendizaje de BPR mejora considerablemente el desempeño sin importar el modelo utilizado.

Encuentro que fue bueno que presentaran  una contextualización del estado del arte que había en ese momento y las debilidades que tenían, ya que así generan un hilo conductor y le dan más importancia al método que iban a presentar más adelante.

Fue bueno que explicaran la notación que iban a utilizar para mostrar su método y las figuras del *paper* en general ayudaron a comprender mejor lo que querían explicar en cada momento.



Encontré interesante cómo utilizaran el AUC como analogía para entender mejor su algoritmo, aunque faltó explicar de forma breve lo que era AUC para los que no tenían ese conocimiento, para entender lo que querían explicar. Además, luego utilizan el AUC como medida de desempeño, que es fácil de ver y comprender, pero también podrían haber utilizado otra media para generar conclusiones más robustas.

Antes de realizar los experimentos con los distintos modelo de recomendación, hicieron una breve explicación de cada uno de ellos y cómo obtienen sus respectivos parámetros. Esto facilitó mucho más la comprensión del método propuesto y cómo se puede implementar a estos modelo.

Me gustó que utilizaran dos *datasets* en sus experimentos en vez de uno solo, porque así se puede ver el verdadero potencial que tiene este método para mejorar el aprendizaje de los sistemas recomendadores. También, la visualización de los resultados era simple y fácil de analizar para obtener propias conclusiones de los experimentos.

A modo general, encontré muy bueno cómo el formato de este *paper*. Gracias al modo de cómo explicaron cada elemento, el orden que siguieron y las figuras/ecuaciones que utilizaron en cada apartado, hicieron una grata lectura y comprensión del método que querían explicar. En cuánto al tema, encuentro muy interesante el enfoque que le dieron para mejorar el problema de la generación de *rankings* personalizados. En vez de afrontarlo mediante la propuesta de un nuevo modelo de recomendación, demostraron que cambiando el criterio y el algoritmo de aprendizaje se puede mejorar bastante el desempeño de un mismo modelo recomendador.

