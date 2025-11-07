# Lenguajes-y-automatas Proyecto 3 Red de vuelos

Código Fuente y Documentación
Instrucciones de instalación

Para ejecutar el programa, primero debes instalar las dependencias:

pip install -r requirements.txt

Instrucciones para ejecutar

Para ejecutar el programa, solo necesitas usar el siguiente comando:

python run.py


El programa abrirá una interfaz gráfica donde podrás interactuar con la red de vuelos y ejecutar los algoritmos.

Funcionamiento del Código
1. Algoritmo Bellman-Ford

El algoritmo de Bellman-Ford se utiliza para encontrar el camino más corto desde un nodo de origen a todos los demás nodos en un grafo, permitiendo que haya pesos negativos en las aristas. El algoritmo funciona de la siguiente manera:

Relajación de aristas: Se itera sobre todas las aristas del grafo V-1 veces (donde V es el número de nodos), y se actualizan las distancias más cortas encontradas.

Detección de ciclos negativos: Después de realizar la relajación, se hace una última iteración para comprobar si alguna distancia puede seguir disminuyendo. Si es así, se detecta un ciclo negativo en el grafo.

2. Algoritmo Dijkstra

Dijkstra se utiliza para encontrar el camino más corto en un grafo, pero no maneja pesos negativos. Si se encuentra un peso negativo, Dijkstra no puede funcionar correctamente y lanzará un error.

3. Interfaz Gráfica (GUI)

La interfaz gráfica está construida usando Tkinter. Los componentes principales de la GUI incluyen:

Panel de Resultados: Muestra los resultados de los algoritmos (costos de ruta más corta, tiempos de ejecución).

Panel de Controles: Permite agregar aeropuertos (nodos), agregar vuelos (aristas), y ejecutar los algoritmos de Bellman-Ford y Dijkstra.

Visualización del Grafo: Usa matplotlib para dibujar el grafo de aeropuertos y vuelos.

4. Estructura del Grafo

El grafo de la red de vuelos es representado mediante dos estructuras:

Lista de adyacencia: Usada por el algoritmo de Dijkstra.

Lista de aristas: Usada por el algoritmo de Bellman-Ford.

Cada aeropuerto (nodo) está conectado por vuelos (aristas) que tienen un costo asociado, que puede ser negativo.

Ejemplo de Uso

Agregar un Aeropuerto:

Ingresa el nombre del aeropuerto en el campo correspondiente y haz clic en "Agregar Aeropuerto".

Agregar un Vuelo:

Ingresa el aeropuerto de origen, el de destino y el costo del vuelo (puede ser negativo para representar descuentos) y haz clic en "Agregar Vuelo".

Ejecutar Bellman-Ford:

Ingresa el aeropuerto de origen y haz clic en "Ejecutar Bellman-Ford" para calcular el camino más corto desde ese aeropuerto a todos los demás.

Si se detecta un ciclo negativo, aparecerá una advertencia.

Ejecutar Dijkstra:

Ingresa el aeropuerto de origen y haz clic en "Ejecutar Dijkstra" para calcular el camino más corto, pero ten en cuenta que Dijkstra fallará si hay pesos negativos.

Comparar los Algoritmos:

Haz clic en "Comparar Dijkstra vs Bellman-Ford" para ejecutar ambos algoritmos y comparar los resultados.

Análisis de Complejidad

Algoritmo Bellman-Ford:

Complejidad temporal: O(V * E), donde V es el número de vértices (aeropuertos) y E es el número de aristas (vuelos).

Complejidad espacial: O(V + E), debido a las estructuras de datos usadas para almacenar los nodos, aristas y distancias.

Algoritmo Dijkstra:

Complejidad temporal: O(E log V), utilizando una cola de prioridad.

Complejidad espacial: O(V + E), debido a las listas de adyacencia y las distancias almacenadas.

Resultados Esperados

Bellman-Ford: El algoritmo devuelve los caminos más cortos desde el nodo de origen hacia todos los demás nodos, y si se detecta un ciclo negativo, se muestra un mensaje de advertencia.

Dijkstra: El algoritmo devuelve los caminos más cortos, pero no funciona correctamente si el grafo tiene aristas con pesos negativos.

Comparación entre Dijkstra y Bellman-Ford

Dijkstra no maneja pesos negativos y lanzará un error si se encuentra con alguno.

Bellman-Ford, por otro lado, maneja correctamente los pesos negativos y detecta ciclos negativos.
