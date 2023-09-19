• La estructura se decide durante el diseño.
• La implementación no debe cambiar la estructura.
• La estructura tiene efectos sobre el mantenimiento.
• La metodología de diseño estructurado (**SDM**) apunta a controlar la estructura.
• El objetivo de las metodologías de diseño (y en particular de la **SDM**) es proveer
pautas para auxiliar al diseñador en el proceso de diseño. No reduce al diseño a
una secuencia de pasos mecánicos.

• SDM ve al software como una función de transformación que convierte una
entrada dada en la salida esperada.

• El foco en el diseño estructurado es la función de transformación => SDM es una metodología orientada a funciones.
	• Utiliza abstracción funcional y descomposición funcional.

**Objetivo de la SDM:
• Especificar módulos de funciones y sus conexiones siguiendo una estructura
jerárquica con bajo acoplamiento y alta cohesión**.

• Los módulos con módulos subordinados no realizan mucha computación.
• La mayoría de la computación se realiza en los módulos subordinados.
• El módulo principal se encarga de la coordinación.
• Así sucesivamente hasta los módulos “atómicos”.
• La factorización es el proceso de descomponer un módulo de manera que el
grueso de la computación se realice en los módulos subordinados.
• Sistema completamente factorizado: el procesamiento real se realiza en los
módulos atómicos del nivel más bajo.
• SDM apunta a acercarse a la factorización completa.

**Pasos principales de esta metodología:**
1. Reformular el problema como un DFD.
2. Identificar las entradas y salidas más abstractas.
3. Realizar el primer nivel de factorización.
4. Factorizar los módulos de entrada, de salida, y transformadores.
5. Mejorar la estructura (heurísticas, análisis de transacciones).

#### Paso 1: Reformular el problema con DFDs
• El diseño estructurado comienza con un DFD que capture el flujo de datos del
sistema propuesto.
• DFD es una representación importante: provee una visión de alto nivel del
sistema.
• Enfatiza el flujo de datos a través del sistema.
• Ignora aspectos procedurales. (Aunque la notación es la misma, el propósito aquí es diferente de DFD en análisis de requerimientos).

• Identificar las entradas, salidas, fuentes, sumideros del sistema.
• Trabajar consistentemente desde la entrada hacia la salida o al revés.
• Si se complica => cambiar el sentido.
• Identificar los transformadores que convierten las entradas en salidas.
• No mostrar nunca lógica de control; si se comienza a pensar en término de loops/
condiciones: parar y recomenzar.
• Etiquetar cada flecha y burbuja. Identificar cuidadosamente las entradas y salidas de cada transformador.
• Hacer uso de + y *
• Ignorar las funciones menores al principio.
• En sistemas complejos realizar DFD de manera jerárquica.
• Dibujar DFDs alternativos antes de definirse por uno.

![[Pasted image 20230906230022.png]]
#### Paso 2: Identificar las entradas/salidas más abstractas
• Generalmente los sistemas realizan una función básica.
• Pero usualmente no se realiza sobre la entrada directamente.
• Primero la entrada debe convertirse en un formato adecuado.
• Similarmente las salidas producidas por los transformadores principales deben
transformarse a salidas físicas adecuadas.
• Se requieren varios transformadores para procesar las entradas y las salidas.
**Objetivo de este paso: 
separar tales transformadores de los que realizan las transformaciones reales.**

• **Entradas más abstractas** (**MAI**): elementos de datos en el DFD que están más
distantes de la entrada real, pero que aún puede considerarse como entrada.
• Podrían tener poca semejanza con la entrada real.
• En general son ítems de datos obtenidos luego de chequeo de errores, formateo,
validación de datos, conversión, etcétera.
• Para encontrarla:
	• Ir desde la entrada física en dirección de la salida hasta que los datos no puedan considerarse entrantes.
	• Ir lo más lejos posible sin perder la naturaleza entrante.
• Es dual para obtener las **salidas más abstractas** (**MAO**).

• Representa un juicio de valor, aunque usualmente la elección es bastante obvia.
• Las burbujas entre la MAI y la MAO corresponden a los transformadores centrales.
• Son los que realizan la transformación básica.
• Con las MAI y MAO, los transformadores centrales se concentran en la
transformación sin importar el formato/validación/… de las entradas y salidas.

• Visión del problema: cada sistema hace alguna E/S y algún procesamiento.
• En muchos sistemas el procesamiento de E/S forma una gran parte del código.
• Este enfoque separa las distintas funciones:
• Subsistema que realiza principalmente la entrada.
• Subsistema que realiza principalmente las transformaciones.
• Subsistema que realiza principalmente la presentación de la salida.

![[Pasted image 20230906230022.png]]
#### Paso 3: Realizar el primer nivel de factorización
Primer paso para obtener el diagrama de estructura.
• Especificar el módulo principal.
• Especificar un módulo de entrada subordinado por cada ítem de dato de la MAI.
• El propósito de estos módulos de entrada es enviar al módulo principal los ítems
de datos de la MAI.
• Especificar un módulo de salida subordinado por cada ítem de dato de la MAO.
• Especificar un módulo transformador subordinado por cada transformador
central.
• Las entradas y salidas de estos módulos transformadores están especificadas en el
DFD.


• El primer nivel de factorización es sencillo.
• El módulo principal es un módulo coordinador.
• Algunos módulos subordinados son responsables de entregar las entradas lógicas.
• Estas se pasan a los módulos transformadores para obtener las salidas lógicas.
• Estas salidas lógicas son consumidas por los módulos de salida.
• Divide el problema en tres problemas separados.
• Cada uno de los tres tipos distintos de módulos pueden diseñarse separadamente.
• Estos módulos son independientes.


imagen


Paso 4.1: Factorizar los módulos de entrada
El transformador que produce el dato de MAI se trata ahora como un transformador
central.
• Se repite el proceso del primer nivel de factorización considerando al módulo de
entrada como si fuera el módulo principal.
• Se crea un módulo subordinado por cada ítem de dato que llega a este nuevo
transformador central.
• Se crea un módulo subordinado para el nuevo transformador central.
• Usualmente no debería haber módulos de salida.
• Los nuevos módulos de entrada se factorizan de la misma manera hasta llegar a la
entrada física.

La factorización de la salida es simétrica.
• Módulos subordinados: un transformador y módulos de salida.
• Usualmente no debería haber módulos de entrada.


La factorización de los módulos de entrada y salida es simple si el DFD es detallado.
• No hay reglas para factorizar los módulos transformadores.
• Utilizar proceso de refinamiento top-down.
• Objetivo: determinar los subtransformadores que compuestos conforman el transformador.
• Repetir el proceso para los nuevos transformadores encontrados.
• Tratar al transformador como un nuevo problema en sí mismo.
• Graficar DFD.
• Luego repetir el proceso de factorización.
• Repetir hasta alcanzar los módulos atómicos.


imagen


Heurísticas de diseño
Los pasos anteriores no deberían seguirse ciegamente.
• La estructura obtenida podría modificarse si fuera necesario (si uno lo considera así).
• El objetivo, siempre, es lograr bajo acoplamiento y alta cohesión.
• Utilizar heurísticas de diseño para modificar el diseño inicial.
• Heurística de diseño: un conjunto de “rules of thumb” que generalmente son útiles.


• Tamaño del módulo: Indicador de la complejidad del módulo.
• Examinar cuidadosamente los módulos con muy poquitas líneas o con mas de
100 líneas.
• Cantidad de flechas de salida y cantidad de flechas de llegada:
• La primera no debería exceder las 5 o 6 flechas; la segunda debería maximizarse.
• Alcance del efecto de un módulo: los módulos afectados por una decisión en este
módulo.
• Alcance del control de un módulo: Todos los subordinados.
• “Rule of thumb”: Por cada módulo, el alcance del efecto debe ser un subconjunto
del de control.
• Idealmente una decisión solo debe tener efecto en los inmediatos subordinados.