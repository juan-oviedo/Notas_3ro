Un DFD es una representación gráfica el flujo de datos a través del sistema.
• Ve al sistema como una transformación de entradas en salidas.
• La transformación se realiza a través de “transformadores/procesos”.
• El DFD captura la manera en que ocurre la transformación de la entrada en
la salida a medida que los datos se mueven a través de los transformadores.
• No se limita al software.

Es un gráfico lógico del plan de trabajo que se ejecutará para la solución de un
determinado problema.

![[Pasted image 20230823191839.png]]

* Las burbujas se conectan con flechas sobre las cuales se identifican los datos que fluyen (sustantivos)
* Los transformadores se representan con círculos/burbujas con un nombre (representativo-verbo)
* Los rectángulos representan una fuente o un sumidero y es generador/consumidor de datos (usualmente fuera del sistema).
* Los archivos externos se muestran como una línea recta etiquetada (almacén de datos
* Las conexiones entre burbujas y rectángulos define la interfaz entre el sistema y el mundo exterior
* La necesidad de múltiples flujos de datos se representa con * (significa ‘and’), es decir no se puede completar la tareas sin esos datos
* Similarmente, existe una relación de ‘or’ que se representa con +
* Todos los procesos y flechas deben tener nombre.
* Los procesos deben representar transformadores; las flechas deben representar algunos datos

### Funcionamiento DFD
* Se enfoca en qué hacen los transformadores, no en cómo lo hacen. Usualmente se muestran sólo las entradas/salidas más significativas y se ignoran las de menor importancia (como por ej. mensajes de error).
* En general, NO hay loops, razonamiento condicional.
* Un DFD NO es un diagrama de control, no debería existir diseño ni pensamiento algorítmico.

### **Cómo dibujar el DFD de un sistema:**
• Identificar las entradas, salidas, fuentes, sumideros del sistema.
• Trabajar consistentemente desde la entrada hacia la salida.
• Si se complica => cambiar el sentido (de la salida a la entrada).
• Avanzar identificando los transformadores de más alto nivel para capturar la transformación completa.
• Cuando los transformadores de alto nivel están definidos, refinar cada uno con transformaciones más detalladas.
• No mostrar nunca lógica de control, si se comienza a pensar en término de loops/condiciones: parar y recomenzar.
• Etiquetar cada flecha y burbuja. Identificar cuidadosamente las entradas y salidas de cada transformador.
• Hacer uso de + y *
• Intentar dibujar grafos de flujo de datos alternativos antes de definirse por uno.

### **DFD en niveles:**
• El DFD de un sistema puede resultar muy grande => organizar jerárquicamente.
• Comenzar con un DFD de nivel superior abstracto conteniendo pocas burbujas.
• Luego dibujar un DFD por cada burbuja.
• Al “explotar” una burbuja, preservar la E/S original con el fin de preservar  consistencia.
• Para obtener el DFD en niveles se realiza un proceso de refinamiento top-down. Esto permite modelar sistemas grandes y complejos

### **El diccionario de datos:**
• Las flechas del DFD están etiquetadas con ítems de datos.
• El diccionario de datos define con mayor precisión los datos en un DFD.
• Muestra la estructura de los datos; la estructura se hace más visible a medida que
se van “explotando” (refinando) las burbujas.
• Se puede usar expresiones regulares para representar la estructura de datos.

![[Pasted image 20230823192942.png]]

### **Errores comunes al graficar DFD:**
• Flujos de datos sin etiquetar.
• Flujos de datos omitidos (necesarios para un proceso).
• Flujos de datos irrelevantes (dibujado pero no usado por el proceso).
• Consistencia no preservada por el refinamiento.
• Procesos omitidos.
• Inclusión de información de control.