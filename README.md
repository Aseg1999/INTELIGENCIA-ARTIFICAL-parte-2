# Proyecto inteligencia artificial , A* heuristica y teoria de juegos

## Descripcion

Este proyecto muestra tres conceptos importantes de inteligencia artificial , el algoritmo A* , la heuristica y la teoria de juegos. Todos los ejemplos estan hechos en python y se ejecutan en google colab. Cada ejemplo se presenta de forma visual , paso a paso y de forma lenta para poder entender como funcionan las decisiones del algoritmo o de los jugadores.

## Algoritmo A*

### Que es

El algoritmo A* es un algoritmo de busqueda que se usa para encontrar el camino mas corto entre dos puntos dentro de un mapa o grafo. Es muy utilizado en inteligencia artificial , videojuegos , robots y sistemas de navegacion.

### Para que sirve

Sirve para encontrar la mejor ruta posible entre un punto inicial y un objetivo , evitando obstaculos y explorando los caminos que parecen mas prometedores.

### Como funciona

El algoritmo combina dos valores.
g(n) , que representa el costo real desde el inicio hasta el nodo actual.
h(n) , que es una estimacion de la distancia hasta la meta usando una heuristica.

La suma de estos valores da el costo total.

f(n) = g(n) + h(n)

El algoritmo siempre elige explorar el nodo con el menor valor de f(n).

### Codigo

En el proyecto se implementa un mapa tipo videojuego donde un personaje debe encontrar el camino hasta una meta evitando obstaculos. El recorrido se muestra paso a paso para entender como el algoritmo explora el mapa.

## Heuristica

### Que es

Una heuristica es una tecnica que permite estimar rapidamente cual opcion puede ser mejor sin analizar todas las posibilidades completas.

### Para que sirve

Sirve para acelerar la busqueda de soluciones , permitiendo tomar decisiones rapidas basadas en estimaciones.

### Como funciona

La heuristica calcula una distancia estimada entre dos posiciones. En los ejemplos se usa la distancia manhattan , que suma la diferencia de filas y columnas entre dos posiciones del mapa.

### Ejemplos en python

Ejemplo 1 , un jugador debe decidir cual de dos tesoros esta mas cerca usando una estimacion de distancia.

Ejemplo 2 , un enemigo persigue a un jugador evaluando cual movimiento lo acerca mas a su objetivo.

Los ejemplos se muestran visualmente en un mapa con emojis para facilitar la comprension.

## Teoria de juegos

### Que es

La teoria de juegos estudia como toman decisiones diferentes participantes cuando el resultado depende de las decisiones de todos.

### Para que sirve

Sirve para analizar estrategias en situaciones de competencia o cooperacion , donde cada jugador intenta maximizar su beneficio.

### Como funciona

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

## Conclusion

Este proyecto permite entender de forma visual como funcionan diferentes tecnicas de inteligencia artificial. Se muestra como los algoritmos pueden tomar decisiones usando busqueda , estimaciones heuristicas y estrategias entre diferentes agentes.

