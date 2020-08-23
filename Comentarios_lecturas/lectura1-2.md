# Crítica lectura 1-2: Blog FunkSVD

Este blog explica la idea principal de un sistema recomendador de películas basado en la factorización de matrices mediante SVD y *machine learning*.  En un comienzo, el autor explica de qué se trataba el *Netflix prize* y los principales desafíos que tenía (un gran cantidad de películas y usuarios, y un porcentaje muy menor de *ratings*). Para solucionar esto, propone utilizar un modelo basado en SVD ( *singular value decomposition*) que utilice menos parámetros que los 8.5 billones de elementos de la matriz de *ratings*. Este consiste básicamente en descomponer la gran matriz en submatrices que aproximen con el menor error posible a esta. De esta forma, se utilizan bastante menos parámetros en el modelo sin perder información importante ni empeorar tanto el desempeño. Luego, explica el funcionamiento de este modelo y sus principales suposiciones que lo hacen posible realizar y funcionar de buena manera. Estas suposiciones implican el cómo inferir los *ratings* de las películas y los parámetros de los usuarios que tengan pocas valoraciones. Por último, muestra el entrenamiento de este modelo mediante *machine learning* y cómo fue cambiando hiperparámetros y funciones dentro de este, para evitar el *over fitting*  y así tener un mejor desempeño.

La forma de explicar el SVD con el ejemplo de que cada usuario y película tenga un único vector de características pero con distintos valores, ayudó mucho al entendimiento de este método y a la posterior explicación de su funcionamiento. Es interesante cómo le dio un significado a un método de álgebra lineal que es complicado de entender e implementarlo en un problema de recomendación.

Me gustó cómo solucionó el problema de obtener los promedios de las películas que tenían pocas valoraciones y la forma de explicarlo me pareció fácil de seguir.

Cómo comentario del formato del artículo, el hecho de estar escrito en un blog y mostrar las ecuaciones  y/o códigos cómo texto puro, hizo más difícil la comprensión de lo que quería explicar en cada apartado. Los gráficos utilizados, a pesar de que muestran los resultados obtenidos, no lo hacen de forma tan clara, ya que cuesta entenderlos (faltan los ejes). Algunos párrafos eran muy densos y con muchos números que dificultaban el seguimiento de lo que quería explicar, hubiese sido mejor una figura o una ecuación.

A modo general, me pareció muy interesante la forma de cómo explicó el método basado en SVD y cómo realizó su entrenamiento,  aunque el hecho de que este escrito en un blog hizo más difícil la lectura, lo que dificultó la comprensión del modelo. Aun así, se pudo entender la idea principal que quería transmitir el autor.



