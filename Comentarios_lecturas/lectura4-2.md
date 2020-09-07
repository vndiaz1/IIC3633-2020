# Crítica de la lectura 4-2: Document Clustering Based On Non-negative Matrix
Este *paper* creado el año 2003, los autores proponen una nueva forma de realizar *clustering* al corpus de documentos a través de una descomposición de matrices que tienen todos sus valores no negativos.

### Resumen

En un comienzo, se habla de la importancia que están teniendo los *clusters* de textos y de que los motores tradicionales de búsqueda que son basado en palabras claves son menos efectivos que una jerarquización mediante *clusters*.

Luego, se describen los dos tipos de métodos para hacer *clustering* que habían hasta el momento, que son el aglomerativo y particionado, y hablan sobre sus principales ventajas y desventajas.

Después, presentan se método propuesto que forma parte de *clustering* particionado, pero que tiene algunas características que lo hacen único y con buen desempeño. Estas son: primero, los ejes del espacio semántico que capturan los tópicos no son necesariamente ortogonales, y segundo, cada documento se descompone en una combinación de elementos aditivos, es decir, valores no negativos.

Una vez explicado la matemática del método, realizan una comparación con SVD, junto con experimentos en dos *datasets* que muestran los desempeños de cuatro modelos (dos del estado del arte vs dos propuestos por ellos) mediante dos métricas de desempeño.

Por último, concluyen con que las diferencias que tiene su método con respecto a los basado en SVD, permiten una fácil creación de *clusters*, lo que que se suma a un mejor rendimiento en *clustering* de documentos.

### Comentarios

Previo a comenzar la lectura de este *paper* sabía muy poco acerca de los métodos de *clustering* en documentos, por lo que me complicó en un principio la lectura. No obstante, los autores pudieron explicar muy bien y de forma sencilla lo que estaban proponiendo, lo que me permitió comprender bastante bien el contenido de este documento. Encuentro que el apartado de *Related works* fue fundamental para dar una introducción al tema y así tener un leve punto de comparación con el método propuesto.

En cuanto a este, encontré que su formulación es bastante intuitiva, lo que simplifica su comprensión, por lo que le doy mucho mérito a los autores por realizar un método con una base simple de entender en relación al problema que se quiere enfrentar.  También,  encontré muy elegante la derivación matemática, ya que plantearon el método de optimización de forma convencional utilizando Lagrange, lo que es muy simple, pero a la vez muy poderoso, debido a que les permitió demostrar convergencia en la actualización de parámetros y obtener un mínimo global con sólo normalizar los vectores.

También, me gustó la comparación gráfica que se hizo entre NMF y SVD, porque me ayudó a entender de forma muy fácil lo que querían explicar.

![](Assets\lectura4-2_comparacion.png)

Con la imagen anterior se puede ver claramente las diferencia que tienen los métodos de NMF y SVD al momento de hacer *clustering* mediante descomposición de matrices. En especial, el hecho de que NMF se evita el paso final de hacer *K-means* para segmentar los *clusters*, ya que cada clase tiene su propio eje.

Sobre lo experimentos, me pareció muy bueno el hecho de utilizar más de un *dataset*, dado que así se puede comparar de forma más robusta los métodos. Sin embargo, no me gustó la forma en que mostraron sus resultados:

![](Assets\lectura4-2_tabla.png)

El hecho de utilizar sólo tablas en vez de gráficos, me dificultó un poco más la interpretación de estos, ya que son muchos números con valores muy similares.

Para concluir, me gustó bastante este *paper*, porque explican un método que es simple de entender, pero muy poderoso a la vez, ya que su implementación no sólo se queda en *clustering* de documentos, si no que se puede utilizar para muchos otros tipos de datos.