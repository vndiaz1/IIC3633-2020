# Crítica de la lectura: Deep Learning based Recommender System: A Survey and New Perspectives - Parte 2

## Resumen

Los modelos que se nombraron y explicaron en esta segunda parte del artículo son:

### Recurrent Neural Networks based Recommendation

Las RNNs son muy buenas para procesar datos secuenciales. Por esta razón, han sido la opción natural para lidiar con problemas temporalmente dinámicos como lo es trabajar con textos y audios. Este tipo de red se han utilizado de tres maneras diferentes para elaborar sistemas recomendadores:

- **Session-based Recommendation without User Identifier**: generalmente, los usuarios no se identifican cuando entran a una aplicación o sitio web. Aunque gracias a los *cookies*, los sistemas pueden tener disponible las preferencias de corto plazo del usuario. Uno de los modelos de recomendación basado en sesión más conocido es **GRU4REC**. Este modelo, mediante RNNs básicas, predice lo que el usuario va a comprar basado en su historial de clicks.
- **Sequential Recommendation with User Identifier**: en este tipo de casos sí se conoce el identificador del usuario al que se le quiere recomendar. Un modelo a destacar es el **Recurrent Recommender Network (RRN)**, que es un modelo recomendador no paramétrico construido con RNNs. Este es capaz de modelar la evolución temporal de los ítems y de los cambios de las preferencias del usuario en el tiempo.
- **Feature Representation Learning with RNNs**: las RNNs se ha demostrado que son una opción viable como herramienta de representación para información con patrones secuenciales. Principalmente, los modelos de esta área utilizan GRUs para codificar la información en un modelo de factores latentes para secuencias de textos y para el historial de navegación.

### Restricted Boltzmann Machine based Recommendation

Este fue el primer modelo de recomendación que fue construido en base a redes neuronales. Este tiene algunas desventajas como estar limitado a valores binarios y no ser manejable, ya que sus parámetros son aprendidos mediante el algoritmo *Contrastive Divergence (CD)*. Hay modelos que utilizan las RBM para hacer filtros colaborativos como lo son **RBM-CF** basado en usuario y en ítems, y el **hybrid RBM-CF**.

### Neural Attention based Recommendation

Este tipo de modelos se basa en generar un mecanismo capaz de filtrar las características no informativas (inútiles) de los inputs y reducir los efectos de los datos ruidosos. Generalmente se utilizan junto con MLP, CNNs o RNNS, aunque de igual manera puede desempeñar tareas de forma independiente. Los modelos de atención aprenden a poner atención en la entrada según puntajes de atención. Estos puntajes son la base de este tipo de modelo y se clasifican en dos: en *vanilla attention* y en *co-attention*. 

### Neural AutoRegressive based Recommendation

Este modelo es la alternativa deseable para reemplazar las RBM, ya que es un estimador de distribución manejable. Un algoritmo que utiliza este modelo es el **CF-NADE**, el que modela una distribución de *ratings* de usuarios.

### Deep Reinforcement Learning for Recommendation

Estos modelos, a diferencia de los otros que son estáticos, permiten hacer recomendaciones más personalizadas a través de feedback positivo y negativo de forma secuencial del usuario. Esto trae ventajas como: tener cambios dinámicos del nuevo contenido y de las preferencias del usuario, incorporar patrones de los usuarios e incrementar la diversidad de las recomendaciones.

### Adversarial Network based Recommendation

**IRGAN** es el primer modelo que aplica GANs en el área de recuperación de información. También, hay otros algoritmos que utilizan GANs que han obtenido buenos resultados, por lo que en un futuro van a poder ayudar a mejorar significativamente el rendimiento.

### Deep Hybrid Models for Recommendation

Gracias a la buena flexibilidad que tienen las redes neuronales profundas, se han podido crear bloques neuronales que al integrar varios modelos, permiten generar modelos muchos más poderosos y expresivos. Las combinaciones que se han probado más efectivas en el campo de aplicación son: *CNNs and Autoencoder*, *CNNs and RNNs*, *RNNs and Autoencoder* y *RNNs with DRL*. 

### Futuras direcciones de investigación y problemas abiertos

A pesar de la gran cantidad de trabajos con fundación sólida en los sistemas recomendadores profundos, siguen habiendo varias direcciones de investigación y problemas abiertos en esta área. Algunas de estas son:

- Joint Representation Learning from User and Item Content Information
- Explainable Recommendation with Deep Learning
- Going Deeper for Recommendation
- Machine Reasoning for Recommendation
- Cross Domain Recommendation with Deep Neural Networks
- Deep Multi-Task Learning for Recommendation
- Scalability of Deep Neural Networks for Recommendation
- The Field Needs Better, More Unified and Harder Evaluation

Con estas opiniones finales, termina este artículo de investigación del estado del arte de los sistemas recomendadores con *deep learning*.

## Comentario

Primero que todo, los autores pudieron hacer un muy buen resumen de cada tipo de modelo de *deep learning* que se han creado para crear sistemas recomendadores e indicando los nombres de los modelos más relevantes del área. Sin embargo, se me hizo difícil la lectura en algunos tramos cuando explican la parte matemática de los modelos. El hecho de que lo explicaran en párrafos en vez de ecuaciones en punteo dificultó la comprensión de estos.

Pude darme cuenta la gran variedad de modelos que existen para generar sistemas recomendadores con *deep learning*, lo que hace bueno y malo al momento de enfrentar un problema de recomendación. Por un lado, la gran variedad de modelos te permite explorar varias soluciones y tener la posibilidad de elegir la mejor según los requerimientos del problema a resolver. Por otro lado, esta gran diversidad te hace más difícil la elección de un modelo y te puede confundir al momento de realizar la elección.

Lo que más me llamó la atención de esta parte del *paper* son los problemas actuales que hay que solucionar en área de sistemas recomendadores. En especial, estoy de acuerdo con el tema de estandarizar el tema de la prueba de algoritmos, ya que hoy en día cada investigador utiliza el dataset, las métricas, los *baseline* que quiere, lo que dificulta la comparación de métodos para tener una discusión objetiva entre estos.

Otro tema importante con estos sistemas, es que a pesar de que se dicen que son "inteligentes", en verdad aprenden un modelo que le pasa un humano con una función objetivo, lo que no incluye el hecho de discriminar contenido que puede ser perjudicial para el usuario.

Finalmente, quiero concluir que la llegada de *deep learning* a los sistemas recomendadores ayudó a mejorar bastante los modelos actuales, pero hay mucho camino por delante y hay varios problemas por resolver.
