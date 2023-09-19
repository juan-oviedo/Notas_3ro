Propósito básico: proveer una evaluación cuantitativa del diseño (así el producto
final puede mejorarse).
• El tamaño es siempre una métrica: luego del diseño se puede estimar mejor.
Ej.: Cantidad de módulos + tamaño estimado de c/u.
• La complejidad es otra métrica de interés.


Métricas
Métricas de red
Se enfoca en la estructura del diagrama de estructuras; se considera un buen
diagrama a aquel en el cual cada módulo tiene sólo un módulo invocador (reduce
acoplamiento).
• Cuanto más se desvíe de esta forma de árbol, más impuro es el diagrama:
• Impureza del grafo = n - e - 1
• Impureza = 0 => árbol
• A medida que este valor se hace más negativo, se incrementa la impureza.
Esta métrica no tiene en
cuenta el uso común de
rutinas (ej.: bibliotecas)
n = nodos del grafo
e = aristas del grafo


Métricas de estabilidad
La estabilidad trata de capturar el impacto de los cambios en el diseño.
• Cuanto mayor estabilidad, mejor.
• Estabilidad de un módulo: la cantidad de suposiciones por otros módulos sobre
éste.
• Depende de la interfaz del módulo y del uso de datos globales.
• Se conocen luego del diseño.


Métricas de red: parte de la hipóstesis que si la impuridad del grafo se incrementa
=> el acomplamiento se incrementa.
• Pero: el acoplamiento también se incrementa con la complejidad de la interfaz.
• Las métricas de flujo de información tienen en cuenta:
• la complejidad intra-módulo, que se estima con el tamaño del módulo en
LOC.
• la complejidad inter-módulo que se estima con
• inflow: flujo de información entrante al módulo.
• outflow: flujo de información saliente del módulo.
• La complejidad del diseño del módulo C se define como
• DC = tamaño * (inflow * outflow)2
Métricas
Métricas de flujo de información
(inflow * outflow)
representa el total de
combinaciones de
entradas y salidas
Su cuadrado representa la
importancia de la interconexión
entre módulos con respecto a la
complejidad interna (i.e., el
tamaño)

La métrica anterior define la complejidad sólo en la cantidad de información que
fluye hacia adentro y hacia fuera y el tamaño del módulo.
• Ya vimos en la métrica de red que también es importante la cantidad de módulos
desde y hacia donde fluye la info.
• En base a esto, el impacto del tamaño del módulo empieza a resultar considerarse
insignificante.
• En base a esto, la complejidad del diseño del módulo C se puede definir como:
DC = fan_in * fan_out + inflow * outflow
donde fan_in representa la cantidad de módulos que llaman al módulo C, y
fan_out los llamados por C.


Ahora: ¿cómo utilizamos esta métrica?
• Se usa el promedio de la complejidad de los módulos y su desviación estándar para
identificar los módulos complejos y los propenso a error
• Propenso a error si
DC > complej_media + desv_std
• Complejo si
complej_media < DC < complej_media + desv_std
• Normal en caso contrario.
Notar que esta evaluación se
realiza chequeando contra
datos del mismo sistema y no
contra datos históricos




