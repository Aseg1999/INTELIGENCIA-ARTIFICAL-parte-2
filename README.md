# Proyecto inteligencia artificial , A*, heuristica y teoria de juegos

## Descripcion

Este proyecto muestra tres conceptos importantes de inteligencia artificial , el algoritmo A* , la heuristica y la teoria de juegos.

Todos los ejemplos estan hechos en python y se ejecutan en google colab. Cada ejemplo se presenta de forma visual , paso a paso y de forma lenta para poder entender como funcionan las decisiones del algoritmo o de los jugadores.

## Algoritmo A*

### Que es?

El algoritmo A* es un algoritmo de busqueda que se usa para encontrar el camino mas corto entre dos puntos dentro de un mapa o grafo. Es muy utilizado en inteligencia artificial , videojuegos , robots y sistemas de navegacion.

### Para que sirve?

Sirve para encontrar la mejor ruta posible entre un punto inicial y un objetivo , evitando obstaculos y explorando los caminos que parecen mas prometedores.

### Como funciona?

El algoritmo combina dos valores.
g(n) , que representa el costo real desde el inicio hasta el nodo actual.
h(n) , que es una estimacion de la distancia hasta la meta usando una heuristica.

La suma de estos valores da el costo total.

f(n) = g(n) + h(n)

El algoritmo siempre elige explorar el nodo con el menor valor de f(n).

### Codigo

En el proyecto se implementa un mapa tipo videojuego donde un personaje debe encontrar el camino hasta una meta evitando obstaculos. El recorrido se muestra paso a paso para entender como el algoritmo explora el mapa.

## Heuristica

### Que es?

Una heuristica es una tecnica que permite estimar rapidamente cual opcion puede ser mejor sin analizar todas las posibilidades completas.

### Para que sirve?

Sirve para acelerar la busqueda de soluciones , permitiendo tomar decisiones rapidas basadas en estimaciones.

### Como funciona?

La heuristica calcula una distancia estimada entre dos posiciones. En los ejemplos se usa la distancia manhattan , que suma la diferencia de filas y columnas entre dos posiciones del mapa.

### Ejemplos en python

Ejemplo 1 , un jugador debe decidir cual de dos tesoros esta mas cerca usando una estimacion de distancia.

Ejemplo 2 , un enemigo persigue a un jugador evaluando cual movimiento lo acerca mas a su objetivo.

Los ejemplos se muestran visualmente en un mapa con emojis para facilitar la comprension.

## Teoria de juegos

### Que es?

La teoria de juegos estudia como toman decisiones diferentes participantes cuando el resultado depende de las decisiones de todos.

### Para que sirve?

Sirve para analizar estrategias en situaciones de competencia o cooperacion , donde cada jugador intenta maximizar su beneficio.

### Como funciona?

Cada jugador elige una estrategia , y el resultado final depende de la combinacion de estrategias de todos los participantes.

### Ejemplos en python

Ejemplo 1 , dos jugadores deciden atacar o defender en un combate.

Ejemplo 2 , dos equipos compiten por recursos en un mapa.

Ejemplo 3 , dos jugadores deben decidir si cooperan o traicionan al repartir un botin.

Cada escenario muestra visualmente el resultado de las diferentes decisiones.

## Estructura del proyecto

El repositorio contiene varios notebooks de python con cada ejemplo.

* A* busqueda de camino en mapa tipo videojuego
* Heuristica ejemplo 1 , elegir tesoro mas cercano
* Heuristica ejemplo 2 , enemigo persigue jugador
* Teoria de juegos ejemplo 1 , atacar o defender
* Teoria de juegos ejemplo 2 , competir por recursos
* Teoria de juegos ejemplo 3 , cooperar o traicionar

Todos los ejemplos se ejecutan en google colab.

## Funcionamiento detallado de los codigos

Codigo 1 , algoritmo A*.
Este codigo implementa una busqueda informada sobre una cuadricula que representa un mapa de videojuego. El agente inicia en una posicion P y busca alcanzar la meta M evitando obstaculos. En cada iteracion el algoritmo mantiene una cola de prioridad donde los nodos se ordenan por el valor f(n). Este valor se calcula como f(n) = g(n) + h(n) , donde g(n) es el costo real acumulado desde el inicio hasta el nodo actual y h(n) es una estimacion heuristica de la distancia restante hasta la meta. La heuristica usada es la distancia manhattan , adecuada para movimientos en cuatro direcciones sobre una grilla. El algoritmo explora primero los nodos con menor f(n) , marcando nodos visitados y expandiendo vecinos validos. Cuando la meta es encontrada , se reconstruye el camino siguiendo los padres registrados durante la busqueda. El mapa se muestra paso a paso para visualizar la expansion del espacio de estados y el recorrido final.

Codigo 2 , heuristica ejemplo del tesoro.
Este ejemplo ilustra el uso de una heuristica para tomar una decision rapida entre dos objetivos posibles. El jugador se encuentra en una posicion fija del mapa y existen dos tesoros en diferentes coordenadas. En lugar de calcular rutas completas hacia ambos objetivos , el programa estima la distancia de cada tesoro usando la distancia manhattan. Esta estimacion se obtiene sumando la diferencia absoluta entre filas y columnas de las posiciones. El resultado de ambas estimaciones se compara y se selecciona el tesoro con menor distancia heuristica. El ejemplo demuestra como las heuristicas reducen el costo computacional al evitar explorar todas las rutas posibles.

Codigo 3 , heuristica ejemplo enemigo persigue jugador.
En este escenario un enemigo intenta alcanzar la posicion de un jugador dentro de una cuadricula. El enemigo evalua posibles movimientos en cuatro direcciones , derecha , izquierda , arriba y abajo. Para cada movimiento potencial se calcula una estimacion heuristica de la distancia restante hasta el jugador. El movimiento que produce la menor distancia heuristica es elegido como la siguiente accion. Este proceso se repite paso a paso hasta que el enemigo alcanza al jugador. El ejemplo demuestra como un agente puede tomar decisiones locales basadas en heuristicas para aproximarse a un objetivo.

Codigo 4 , teoria de juegos combate estrategico.
Este codigo representa una interaccion estrategica entre dos jugadores que deben elegir entre atacar o defender. Cada combinacion de estrategias produce un resultado diferente sobre la vida de los jugadores. Si ambos atacan , ambos reciben daño significativo. Si uno ataca y el otro se defiende , el defensor reduce el daño recibido. Si ambos se defienden , no se produce daño. Este modelo muestra una situacion donde el resultado no depende de un solo participante sino de la combinacion de decisiones de ambos , lo cual es el principio fundamental de la teoria de juegos.

Codigo 5 , teoria de juegos competencia por recursos.
En este ejemplo dos equipos compiten por recursos dentro de un mapa. Cada equipo puede elegir entre recoger recursos o atacar al rival. Si ambos equipos recogen recursos , ambos obtienen beneficios similares. Si un equipo decide atacar mientras el otro recoge recursos , el atacante obtiene ventaja estrategica. Si ambos atacan , se genera conflicto y el beneficio para ambos es menor. El modelo demuestra como las decisiones estrategicas afectan la distribucion de beneficios en situaciones competitivas.

Codigo 6 , teoria de juegos cooperar o traicionar.
Este escenario representa una situacion clasica similar al dilema del prisionero. Dos jugadores deben decidir si cooperan para repartir un botin o si traicionan al otro para quedarse con una mayor parte. Si ambos cooperan , el botin se reparte equitativamente. Si uno coopera y el otro traiciona , el traidor obtiene la mayor recompensa. Si ambos traicionan , la confianza se rompe y ambos reciben una ganancia menor. Este ejemplo muestra como la teoria de juegos analiza decisiones estrategicas donde la mejor opcion individual puede no ser la mejor para ambos jugadores.


## Conclusion

Este proyecto permite entender de forma visual como funcionan diferentes tecnicas de inteligencia artificial. Se muestra como los algoritmos pueden tomar decisiones usando busqueda , estimaciones heuristicas y estrategias entre diferentes agentes.

