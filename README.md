# Gestión Eficiente de Recursos Ferroviarios
Este repositorio contiene la implementación de algoritmos para resolver el problema de circulación de material rodante en sistemas ferroviarios, optimizando el uso de vagones para satisfacer la demanda de pasajeros. El objetivo principal es minimizar la cantidad de vagones necesarios, reduciendo así costos operativos y maximizando la eficiencia en la gestión de recursos.

## Descripción del Proyecto
El problema abordado en este trabajo se centra en la optimización de material rodante en un sistema ferroviario entre dos estaciones cabeceras. Utilizando técnicas de optimización de flujos en redes, este proyecto busca determinar el número mínimo de vagones necesarios para cubrir la demanda diaria de pasajeros, teniendo en cuenta restricciones como la capacidad de los vagones y la infraestructura disponible.

## Enfoque
Se modela el problema como un grafo dirigido donde los vértices representan eventos (partidas y llegadas de trenes) y las aristas representan los trayectos o traspasos de vagones entre trenes en las estaciones. El objetivo es aplicar un algoritmo de flujo mínimo con costo mínimo para determinar la circulación óptima del material rodante.

## Estructura del Proyecto
main.py: Contiene la implementación principal del modelo.
utils.py: Funciones auxiliares para cargar datos y construir el grafo.
data/: Carpeta con los archivos JSON que describen las instancias del problema (cronogramas, demanda y capacidad de vagones).
experiments/: Contiene los resultados de las pruebas realizadas sobre diferentes instancias.


## Instalación
Para ejecutar este proyecto, sigue los siguientes pasos:
Clona este repositorio
Instala las dependencias necesarias (se recomienda usar un entorno virtual):
pip install -r requirements.txt

Una vez que hayas clonado el repositorio y tengas las dependencias instaladas, puedes ejecutar el programa de la siguiente manera:


## Datos
Los datos utilizados en este proyecto están formateados en archivos JSON, que contienen:

Estaciones: Lista de estaciones cabeceras.
Servicios: Información sobre cada servicio, incluyendo horarios de salida y llegada, y la demanda de pasajeros.
Material rodante: Capacidad máxima de los vagones y restricciones de circulación.
Algoritmos
El modelo está basado en la implementación de un algoritmo de flujo de costo mínimo utilizando la librería networkx. Se resuelve el problema de optimización construyendo un grafo dirigido con las siguientes características:

Aristas de tren: Representan los trayectos entre estaciones, con límites inferiores y superiores de cantidad de vagones.
Aristas de traspaso: Permiten la reutilización de vagones entre servicios consecutivos en una misma estación.
Aristas de trasnoche: Conectan los eventos del último tren del día con los primeros del día siguiente.
Resultados
Los resultados de las optimizaciones se encuentran en la carpeta experiments/. Estos incluyen comparaciones entre el número de vagones requeridos sin optimización y los obtenidos después de aplicar el algoritmo, destacando los ahorros potenciales en recursos y costos.


## Referencias
Schrijver, A. (2008). Flows in Railway Optimization. Nieuw Archief voor Wiskunde.
