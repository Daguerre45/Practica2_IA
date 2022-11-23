# PRÁCTICA DE BÚSQUEDA HEURÍSTICA SIN ADVERSARIOS

## Como ejecutarlo
1. Deberá descargarse el repositorio poniendo en un terminal el cual tenga la opcion de git
```shell
git clone 
```
2. Una vez clonado deberá ejecutar lo siguiente para comprobar que funciona
```shell
ant run_main
```
el resultado esperado debería ser el siguiente
```shell
run_main:
     [java] [[ 1(0) ] -> [ 3(0) ] = 9
     [java] , [ 3(0) ] -> [ 6(0) ] = 2
     [java] , [ 6(0) ] -> [ 8(0) ] = 14
     [java] ]

BUILD SUCCESSFUL
```
## Preguntas
#### 1. ¿Qué variable representa la lista ABIERTA?
##### la variable que representa la lista abierta es "openSet"
#### 2. ¿Qué variable representa la función g?
##### la variable que representa la lista abierta es "gScore"
#### 3. ¿Qué variable representa la función f?
##### la variable que representa la lista abierta es "fScore"
#### 4. ¿Qué método habría que modificar para que la heurística representara la distancia aérea entre vértices?
##### El método que habría que modificar sería dentro de AStar.java heuristicCostEstimate().
#### 5. ¿Realiza este método reevaluación de nudos cuando se encuentra una nueva ruta a un determinado vértice? Justifique la respuesta
##### La clase Astar.java contiene un método que realiza dicha revaluación de nudos en esta parte del código.  
``` java
 public int compare(Vertex<T> o1, Vertex<T> o2) {
                if (fScore.get(o1) < fScore.get(o2))
                    return -1;
                if (fScore.get(o2) < fScore.get(o1))
                    return 1;
                return 0;
            }
```
##### Lo que hace este método es comparar los vértices devolviendo el valor inferior



### Autor

- <span style="color:grey">**@Daguerre45 -> Alberto Daguerre Torres**</span>
