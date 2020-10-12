# Crítica de la lectura 9-2: Carousel Personalization in Music Streaming Apps with Contextual Bandits 
Este *paper* actual, publicado este año, trata sobre una implementación que modela la personalización de carrusel como un problema contextual *multi-armed bandint* que utiliza un modelo en cascada y una semi-personalización vía *clustering* de usuarios.

### Resumen

En un comienzo, lo autores introducen la lectura explicando la importancia que se tiene hoy en día en las recomendaciones con el formato carrusel en las grandes plataformas de contenido. Resaltan que además de aprender a rankear, la personalización de carrusel necesita el *feedback* del usuario para adaptar y mejorar las recomendaciones vía estrategias de aprendizaje online.

Luego, se realiza una contextualización de los *contextual multi-armed bandit frameworks*, en especial para personalización de carruseles. Uno de los métodos para enfrentar este problema es usar la semi-personalización vía *clustering* de usuarios. También, otra forma para enfrentar este problema es utilizar los modelos de actualización en cascada (*cascade-based arm updae model*), para así poder capturar características de los carruseles implementados en el mundo real.

Después, se habla de las especificaciones de los experimentos que se realizaron. Para estos, se utilizó la aplicación de música vía *streaming* Deezer, como plataforma para probar sus recomendaciones de playlist. Los principales algoritmos que se evaluaron fueron los con probabilidad aleatoria, los con estrategia *upper confidence bound* (UCB) y los con la estrategia de sampleo de Thompson.

Se hicieron experimentos tanto de forma offline como online, donde el principal resultado fue el algoritmo **ts-seg** (estrategia de sampleo de Thompson) tuvo un desempeño mejor estadísticamente significante en comparación a los otros.

Finalmente, se concluye que el modelo propuesto beneficia la resolución de la tarea de recomendar playlist en formato carrusel, gracias a la integración del modelo en cascada y de la semi-personalización vía *clustering* de usuarios.

### Comentario

Quiero comenzar diciendo que me gustó este *paper* por el hecho de entregar una solución innovadora y eficaz para esta tarea desafiante de recomendar en plataformas de contenido vía carrusel, que se utilizan actualmente. Otra cosa que me gustó fue que hicieron la prueba de su modelo tanto de maneta offline como online, lo que lo hace más robusto y se puede obtener conclusiones más relevantes. Además, encontré bastante bueno que además de compartir la implementación de su modelo, también compartieron públicamente el gran dataset que utilizaron de las playlist en Deezer, ya que va a ayudar a las investigaciones futuras para este tipo de recomendaciones.

Por otro lado, algo que me hubiera gustado ver es un poco más del detalle de los modelos utilizados en esta implementación. Sentí que los explicaban de forma muy cualitativa, lo que hace que la interpretación de resultados se dificulte un poco más, dado que no se sabe cuáles son las reales diferencias entre los algoritmos.

En fin, encontré bastante interesante este *paper* dado que trata de resolver uno de los problemas de la actualidad que es bastante desafiante. Además, me gustó el hecho de que liberaran el dataset utilizado para futuros trabajos. Por otro lado, me hubiera gustado saber un poco más de los detalles de los algoritmos que implementaron y que tuvieron los mejores resultados.

