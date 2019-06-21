En esta práctica tendremos que recorrer un circuito mediante subobjetivos y sorteando los obstáculos mediante fuerzas virtuales VFF. Esas fuerzas son tres, las actractivas que son generadas por los subobjetivos, las repulsivas que son generadas por los obstáculos y la total que es la suma de ambas.

**1. Percepción**

En esta práctica no se van a usar filtros de imagen como en las anteriores, no hacen falta. Se van a usar los datos proporcionados por el sensor láser.

**2. Algoritmo**

El primer paso es sacar la coordenadas de los subobjetivos y a medida que vayamos superandolos, los marcaremos como superados.
A continuación sacamos la posición (coordenadas) de nuestro robot, las cuales convertiremos a relativas ya que nos la devuelven en absolutas.

El siguiente paso es calcular el angulo y la fuerza atractiva de cada subobjetivo mediante funciones matemáticas.
Haciendo uso de las funciones del API y los datos que nos proporciona el sensor, sacamos la distancia y el angulo a los obstáculos, y de nuevo con las matemáticas y lo anterior, podemos sacar la localización del obstáculo y con ella el vector repulsión.

Hago más pequeño el ángulo para que sea más brusco, calculo el vector total. Cuanto más cerca del obstáculo, mayor es el vector de repulsión. Tenemos la varible promedio, que se corregira en funcion de las posiciones de mi coche y de los obstáculos.

Haciendo casos, con Fr, Ft, Fa y el angulo ordeno movimiento robot.

