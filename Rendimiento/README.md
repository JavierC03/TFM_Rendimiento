# Rendimiento

Esta carpeta contiene los datos y el notebook usados para comparar el coste de simulación entre Gazebo y O3DE.

## Contenido

- `Metricas.ipynb`: notebook principal de carga, limpieza, análisis y visualización.
- `Gazebo/`: resultados y CSV de ejecuciones de Gazebo usadas para pruebas con las métricas.
- `Gazebo_2/`: resultados y CSV asociados a las ejecuciones de Gazebo.
- `O3DE/`: resultados y CSV asociados a las ejecuciones de O3DE.

Cada subcarpeta incluye ficheros de texto con los resultados brutos y una carpeta `CSV/` con los datos estructurados usados por el notebook.

## Objetivo

El propósito del análisis es comparar el coste de ejecución de ambos simuladores en un escenario equivalente, observando principalmente:

- uso de CPU del proceso,
- uso de memoria,
- carga general del sistema,
- variabilidad del comportamiento durante la simulación.

## Cómo usarlo

1. Abrir `Metricas.ipynb` en Jupyter o en VS Code.
2. Ejecutar las celdas de arriba a abajo.
3. Verificar que las rutas de `ruta_gazebo` y `ruta_o3de` apuntan a las carpetas correctas.

## Dependencias

El notebook utiliza, como mínimo:

- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`

## Interpretación rápida

- Si un simulador muestra menos uso medio de CPU, su coste computacional es menor.
- Si un simulador muestra menos uso de memoria, su huella en RAM es menor.
- Si el boxplot es más alto o más disperso, el comportamiento es más variable.

## Nota

Los resultados dependen del escenario ejecutado, del hardware y de la configuración del entorno. Por tanto, deben interpretarse como una comparación experimental de estas ejecuciones concretas.