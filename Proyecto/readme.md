# Especialización en Analítica y ciencia de datos
## Visualizacion:
---------------------------------------------------------------------------------
## Presentado por:

- Danilo Diaz Valencia

- Edwar Andres Hincapie

### FIFA 2020

## PROBLEMA 

Nuestro propósito es generar una aplicación analítica acerca de los jugadores de fútbol que tienen mejores cualidades deportivas y tienen gran proyección en su valorización en el mercado. También por que es necesario tomar conciencia de cuáles son aquellos parámetros claves que me brindarán las respuestas adecuadas a la situación planteada; es decir, a través de qué medidas puedo identificar cuál jugador será el más apto como atacante y si tiene potencial de valorizarse de manera que lo pueda vender mucho más caro versus el costo de la compra, de manera que asegure ganancias para el club.

### Caracterización del problema

- [miro](https://miro.com/app/board/o9J_l-x9y5g=/)

- Dado que el flujo de jugadores nuevos, lesiones, salidas de jugadores viejos e incremento en habilidades es alto, la base de datos debe actualizarse regularmente; en este caso puede tomarse cada temporada o anual, según la disposición de la base de datos.


### Proceso de diseño y la justificación del mismo

Para este proceso, se hace uso de la herramienta Power BI con el fin de generar las visualizaciones que se requieran y aprovechar la facilidad que brinda para obtener información dinámica de acuerdo a las gráficas y tablas que se encuentren relacionadas entre sí.

De esta forma, para dar inicio a las notas de cómo se llevó a cabo el planteamiento, nos cuestionamos sobre ¿Cómo escoger a un buen jugador, que además de brindarme resultados en los partidos, se valorice con el paso del tiempo?. Con esta pregunta lo primero que se define es que aquellos jugadores que ya están en los equipos de élite obviamente ya son conocidos por todos, su precio de compra es elevado, ellos ya no tienen tanta necesidad de ser vistos por otros clubes dado su fama y aunque puedan valorizarse un poco más, el porcentaje de valorización no incrementará mucho. 

### Características globales para seleccionar a un buen prospecto


Dada la premisa que se plantea líneas  atrás y sumándose al hecho de que la edad juega un papel muy importante  en cuánto al rendimiento físico y la probabilidad de descubrir a un jugador y valorizarlo, se plantea las primeras visualizaciones donde comparo la curva de valorización de los jugadores vs la edad y también como se comporta la capacidad física con la edad; luego en la misma visualización deseo conocer de estos comportamientos qué jugadores se encuentran mi campo de interés con el fin de hacer la preselección de aquellos más aptos.

Como resultado, se obtienen gráficas muy explícitas donde se observa una curva de crecimiento en la valorización y aptitudes físicas alcanzando un máximo a los 28 años y luego de dicha edad los valores decrecen, por lo que en mi criterio de negocio con el fin de obtener un margen de crecimiento a mi posible comprador en un futuro, estableceré que mis rangos de edades de interés se centrarán en jugadores entre los 15 y los 25 años. Es así que termina este análisis inicial con una tabla que toma los jugadores que se ajustan a mi selección de edad y los ordena por dos criterios; habilidades de juego (calificación de 1 a 5, siendo 5 el máximo puntaje) de mayor a menor y precio del jugador ordenado de menor a mayor, de manera que para la selección de los mejores jugadores sea muy claro que aquellos que aparecen en los primeros lugares son los de mayor interés.

<p align="center">
  <img src="img/VisualizaciónCaracterísticasGlobales.PNG?raw=true" alt="Sublime's custom image"/ width="1000">
</p>


### Características específicas para seleccionar un buen prospecto como atacante

Hasta el punto anterior, dejamos establecido como seleccionar al mejor prospecto sin importar su posición en el campo; esto nos puede ser útil cuando deseo renovar una plantilla o mis propósitos se basan netamente en el aprovechamiento de una buena inversión. Sin embargo, profundizando un poco más sobre el interés de cómo seleccionar a un muy buen atacante dado que son los que comercialmente tienen mayor peso en la industria, generamos otra visualización donde se abarcan las características particulares en este concepto.

Por lo tanto, tomamos como input el resultado que se obtiene del análisis anterior y es filtrar los jugadores por su edad entre los 15 y 25 años, luego se revisan varios gráficos donde se resalta la correlación encontrada entre la variable llamada attacking_finishing, attacking_volleys y attacking_heading_accuracy, del cual es fácil inferir que mientras mayor sea el valor de attacking_finishing, mayor capacidad tendrá en todas las demás variables para perfilar al jugador como excelente atacante. Con todo lo anterior y de manera similar a la visualización anterior, se genera una tabla dinámica que ordena a los jugadores con los criterios seleccionados y de acuerdo a su mejor puntaje en habilidades de juego y su precio de venta de menor a mayor valor.

Finalmente, entendiendo que si bien las visualizaciones guían al usuario para escoger al mejor jugador, también permite explorar diferentes escenarios donde pueda modificar la edad, nacionalidad y diferentes puntos en las correlaciones en el cual se pueda explorar de manera rápida las opciones disponibles.


<p align="center">
  <img src="img/VisualizaciónCaracterísticasEspecíficas.PNG?raw=true" alt="Sublime's custom image"/ width="1000">
</p>


## Pasos Ejecución Prototipo en Power BI

#### Dataset

```
Proyecto\Data\players_20 - players_20.csv

```

#### Power Bi

```
Proyecto\Dashboard\DashboardVisualización.pbix

```

1.	Ir a la pestaña campos ubicada al lado derecho de las visualizaciones
2.	Dar click a los tres puntos que indican más opciones
3.	Seleccionar editar consulta
4.	Se abre una nueva pestaña y al lado derecho hay una sección denominada “Pasos aplicados”
5.	Ubicar piñón al lado derecho de Source y en “Ruta de acceso de archivo” seleccionar la ruta que desee

<p align="center">
  <img src="img/cambioruta.png?raw=true" alt="Sublime's custom image"/ width="800">
</p>
