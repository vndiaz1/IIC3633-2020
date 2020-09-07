# Crítica de la lectura 4-2: Content-Based Recommendation Systems
Este capítulo del libro *The Adaptive Web* escrito por Pazzani y Billsus trata sobre el funcionamiento general los sistemas recomendadores basado en contenido, hablando sobre sus principales características, métodos de aprendizaje, principales ventajas y desventajas, entre otros.

### Resumen

El capítulo comienza con una introducción que explica la utilidad que tiene estos tipos de sistemas al momento de hacer recomendaciones. Además, habla sobre la representación los ítems, que pueden ser datos estructurados, como de texto libre.

Luego, explica en qué consisten y cómo se forman los perfiles de usuarios para utilizarlos en los modelos recomendadores. En este apartado, los autores hablan que principalmente se utiliza el historial que tienen los usuarios, pero también se puede agregar la personalización de estos según sus gustos.

Después, explica que aprender estos perfiles de usuarios se puede modelar como un problema de clasificación, donde se utiliza el historial de estos para entrenar los modelos. Por esto, dicen que los algoritmos de clasificación son fundamentales para los *RecSys* basado en contenido, por lo explican los siguientes algoritmos tradicionales de clasificación:

- *Decision Trees and Rule Induction*
- *Nearest Neighbor Methods*
- *Relevance Feedback and Rocchio's Algorithm*
- *Linear Classifiers*
- *Probabilistic Methos and Naive Bayes*

Por último, hablan sobre los métodos que se están utilizando en ese momento y sobre las limitaciones y extensiones que tienen estos tipos de sistemas recomendadores.

### Comentarios

Quiero comenzar diciendo que me gustó la estructura de este artículo, ya que gracias al orden que utilizaron, me facilitó bastante la lectura. Además, el hecho de agregar ejemplos en cada apartado ayudó a aterrizar más y entender mejor el contenido que se estaba explicando.

En cuánto al contenido, encuentro que el hecho de que este *paper* se haya escrito el año 2007 lo hace estar un poco desactualizado si se lee el año 2020. Esto lo digo porque, como todos saben, en la década del 2010, toda el área de inteligencia artificial y *machine learning* tuvo un progreso gigantesco debido al aumento de capacidad de computo que tienen los computadores, lo que llevó a la utilización de millones e incluso billones de datos. Por esta gran evolución, los métodos clásicos de clasificación como algunos mostrados en este artículo ya no se utilizan para aprender modelos, ya que con tanta información disponible, las redes neuronales son una solución mucho mejor. Sin embargo, cuando se tienen pocos datos, estos métodos clásicos pueden llegar a tener un mejor desempeño que las NN.

También, encontré que este capítulo se centro mucho en la descripción de estos métodos de clasificación, pero faltó explicar más como añadirlos bien a los sistemas de recomendación, ya que es un apartado muy relevante para realizar recomendaciones correctas y no quedó muy claro esta implementación.

A modo general, este capítulo te permite conocer, de forma simple, los aspectos principales que requiere un sistema recomendador basado en contenido y cuáles son los métodos tradicionales que se utilizan para entrenarlos.

