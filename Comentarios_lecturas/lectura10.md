# Crítica de la lectura: Deep Learning based Recommender System: A Survey and New Perspectives - Parte 1

Este artículo trata sobre cómo el *deep learning* se está utilizando en los sistemas recomendadores. Los autores hicieron una recopilación de varios *papers* sobre el tema y hace un resumen de las técnicas más llamativas que se han implementado hasta el momento y concluyen con el trabajo futuro que se puede hacer en esta área.

## Resumen

Para comenzar, se hace una breve introducción sobre los aspectos que diferencian esta compilación de *papers* de *deep learning* en sistemas recomendadores con los que se han publicado anteriormente, señalando en especial que este contiene un resumen más profundo de los detalles de los esfuerzos y problemas que tiene esta área. Además, indican las fuentes de donde obtuvieron estos artículos, que son principalmente de las conferencias de alto perfil (eg. SIGIR, NIPS, RecSys, entre otros).

Luego, se hace una explicación general sobre las técnicas utilizadas en los sistemas recomendadores y en *deep learning*. También, se explica el por qué se utiliza DL en los sistemas recomendadores. La respuesta que dan a esto, se puede resumir en las siguientes cuatro ventajas: transformación no lineal, aprendizaje de representación, modelamiento secuencial y flexibilidad.

Después, se comienza a hablar sobre el estado del arte de los sistemas recomendadores basados en *deep learning*. Estos se pueden separar en dos grandes categorías, en recomendaciones con *Neural Building Blocks* y en recomendaciones con modelos híbridos profundos. Dentro de la primera categoría, los modelos que se utilizan son:

- **Multilayer Perceptron (MLP)**
- **Autoencoder (AE)**
- **Convolutional Neural Network (CNN)**
- Recurrent Neural Network
- Restricted Boltzmann Machine (RBM)
- Neural Autoregressive Distribution Estimation (NADE)
- Adversarial Networks (AN)
- Attentional Models (AM)

Los modelos que están en **negrita** son los que se va a resumir y comentar en esta parte de la crítica.

### *Multilayer Perceptron based Recommendation*

Este tipo de red, es concisa pero efectiva al momento de aproximar cualquier función medible, lo que la a hecho ser la base de muchas otras técnicas más avanzadas.

Primero, se ha utilizado como la extensión neuronal de los métodos tradicionales de recomendación. Los métodos destacados son: Neural Network Matrix Factorization (NNMF), Neural Collaborative Filtering (NCF) y Deep Factorization Machine (DeepFM). Con estos se ha llegado a tener mejores resultados empíricos que con los métodos tradicionales.

Segundo, se utilizan para aprender representaciones de *features* dado a su facilidad y alta eficiencia, aunque no con tanta expresividad como los autoencoders, CNNs y RNNs.

Tercero, se han utilizado para crear *Deep Structured Semantic Models*, que han sido extensamente utilizados en el área de recuperación de información y para recomendación top-n.

### *Autoencoder based Recommendation*

Los autoencoders han demostrado ser útiles para aplicaciones de filtro colaborativo, ya que permiten tener un buen desempeño en dos secciones de este método de recomendación: aprender la representación de *features* de los usuarios/ítems, y rellenar los espacios vacíos de la matriz de interacciones.

Existen varias implementaciones de filtros colaborativos que utilizan los autoencoders. Algunos de los más importantes son: AutoRec, CFN, CDAE (*Collaborative Denoising Auto-Encoder*), Multi-DAE, entre otros.

En el área de *machine learning* los autoencoders se conocen como una herramiento muy poderosa para aprender repreentaciones de *features*, por lo que se han implementado varios métodos de recomendación estos últimos años que incorporan esta técnica. Los principales algoritmos de esta área son: *Collaborative Deep Learning* (CDL), *Collaborative Deep Ranking* (CDR) que se especializa en recomendaciones top-n, AutoSVD++ y HRCD, que es un modelo colaborativo híbrido.

### *Convolutional Neural Networks based Recommendation*

Las redes convolucionales son muy potentes para procesar datos no estructurados, como lo son el audio y las imágenes. Por esto, los modelos de recomendación que se basan en CNNs, las utilizan para la extracción de características. Para la extracción de *features* en imágenes, existen métodos bastantes conocidos como son VPOI (*visual content enhanced POI*) y VBPR (*visual Bayesian personalized ranking*). Para las extracción de características en textos, existe DeepCoNN, que utiliza dos CNNs para modelar los comportamientos de los usuarios y los ítems de reseñas escritas. También, para el audio y el video, existen un par de métodos que permiten extraer estas características que ayudan a solucionar el problem de *cold start*.

Otro lado que se utilizan las redes convolucionales, aunque en menor proporción, es en el área de filtro colaborativo (e.g ConNCF) y en la recomendación con grafos (se utiliza para datos no Euclidianos).

El resto de los modelos que utilizan *deep learning* en sistemas recomendadores y las conclusiones de este artículo se van a resumir en la crítica de la próxima semana. 

## Comentario

Primero que todo, encuentro muy buenos y útiles estos tipos de artículos (i.e *survey*), ya que permiten entrar a una área de investigación de forma fácil,por el hecho de que te dan un contexto general sobre el tema, tanto del desarrollo pasado, como el estado del arte. Además, este artículo se me hizo fácil su comprensión, gracias a su buena estructura organización y vocabulario. Algo que me gustó en particular, es que dado la gran cantidad de referencias que tiene este artículo, los autores supieron bien como utilizarlas dentro del texto, como por ejemplo, las tablas de resumen de todas las referencias de los algoritmos separadas según el tipo de método utilizado.

En cuanto al tema, encuentro que era inevitable que *deep learning* no entrara como recurso fundamental en los sistemas recomendadores. Esto lo digo porque estos sistemas se basan en entrenamientos con dataset para aprender algún tipo de estructura, lo que casi por definición es lo que hace una red neuronal. Otra de las ventajas que tiene DL es la flexibilidad y la variedad de modelos que existen. Basta con ver el punteo del resumen, en donde se indicaron 8 áreas distintas de DL, donde en cada una de ellas existen múltiples algoritmos que pueden solucionar un mismo problema, pero con otro enfoque. A pesar de que esto se considera como una ventaja, se puede considerar como una desventaja, ya que el hecho de existir tantas posibilidades, puede confundir al momento de elegir un método para enfrentar un problema.

Como conclusión, aLgo que la mayoría estamos de acuerdo, es que la incorporación de DL ha mejorado sustancialmente algunas áreas de los sistemas recomendadores, como lo es la exactitud y la extracción de *features*. Sin embargo, hay otros aspectos en donde los métodos más tradicionales siguen siendo mejor o similar a los de *deep learning*, como es el bias, el *fairness*, entre otros.
