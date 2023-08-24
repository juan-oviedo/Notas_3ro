**Enfoque tradicional:**
especificar cada función provista por el sistema.

**Casos de uso:**
captura el comportamiento del sistema como interacción de los
usuarios con el sistema.
• Se enfoca sólo en la especificación de la funcionalidad.
• Puede utilizarse también durante análisis.
• Puede usarse para especificar comportamiento de empresas u organizaciones.

**Nuestro foco**: solo software.
• Muy adecuado para sistemas interactivos.

## Conceptos básicos:
• Un caso de uso captura un contrato entre el usuario y el comportamiento del
sistema.
• La forma básica es textual. Existen notaciones gráficas (diagramas) como
soporte.
• Útil en la recolección de requerimientos dado que a los usuarios les agrada,
comprenden el formato, y reaccionan a éste fácilmente.

**Actor**: 
Una persona o un sistema que interactúa con el sistema propuesto para
alcanzar un objetivo.
+ j.: El usuario de un cajero automático (objetivo: obtener dinero); operador de ingreso de datos (objetivo: realizar transacciones).

Un actor es una entidad lógica => actores receptores y actores transmisores son
distintos (aún si es el mismo individuo).
Los actores pueden ser personas o sistemas.

**Actor primario**: 
El actor principal que inicia el caso de uso.
El caso de uso debe satisfacer su objetivo (AP es el interesado).
La ejecución real puede ser realizada por un sistema u otra persona en representación del actor primario.

**Escenario**: 
es un conjunto de acciones realizadas con el fin de alcanzar un objetivo
bajo determinadas condiciones.
Las acciones se especifican como un conjunto de pasos.
Un paso es una acción lógicamente completa realizada tanto por el actor como por
el sistema.
Es una interactuación entre el usuario y el sistema.
Generalmente se representan en secuencia, pero no necesariamente ésa es su implementación (ej.: podrían ocurrir en paralelo)

**Escenario exitoso principal**: 
cuando todo funciona normalmente y se alcanza el objetivo.

**Escenarios alternativos**: 
(de extensión/de excepción): cuando algo sale mal y el objetivo no puede ser alcanzado.

• Un caso de uso es una colección de muchos escenarios.
• Un escenario puede emplear otros casos de usos en un paso, es decir un sub objetivo del objetivo de un caso de uso puede realizarse en otro caso de uso.
• Los casos de uso pueden organizarse jerárquicamente
• Los casos de uso especifican funcionalidades describiendo la interacción entre actores y sistema.
• Se enfocan en el comportamiento externo.
• Los casos de uso son primariamente textuales
Los diagramas de casos de uso son suplementos de los casos de usos textuales.
Muestran casos de usos, actores y sus dependencias.
Sólo proveen una visión general.
**Los casos de usos no forman la SRS completa, sólo la parte funcional.**

![[Pasted image 20230823211646.png]]
![[Pasted image 20230823211707.png]]

* Los casos de uso se numeran para referencias posteriores
* El nombre del caso de uso especifica el objetivo del actor Primario
* El actor primario puede ser una persona o un sistema
* La precondición describe lo que el sistema debe asegurar antes de iniciar el caso de uso
* Las listas de excepciones no son exhaustivas
* Algunas de las acciones puede contener referencia a otros casos de usos
* La lista de acciones puede contener acciones que no son necesarias para el objetivo del actor primario. Sin embargo, Sin embargo, el sistema debe asegurar que el objetivo final, así como los otros objetivos puedan cumplirse

![[Pasted image 20230823212146.png]]

* Nivel 0 “resumen”
* El ámbito especifica el subsistema al cual se aplica el caso de uso
* También es posible especificar postcondiciones
### Elaboración de los Casos de uso

Los casos de uso proveen un medio adecuado para la discusión y el
brainstorming => también son apropiados para la recolección de requerimientos y el análisis del problema.
• Los casos de uso pueden elaborarse haciendo refinamientos paso a paso.
En este contexto se presentan varios niveles de abstracción. Cuatro de ellos
emergen naturalmente.

1. Actores y objetivos:
• Preparar una lista de actores y objetivos.
• Proveer un breve resumen del caso de uso.
• Esto define el ámbito del caso de uso.
• También se puede evaluar completitud.

2. Escenarios exitosos principales:
• Por cada caso de uso, expandir el escenario principal.
• Esto provee el comportamiento principal del sistema.
• Puede revisarse para asegurar que se satisface el interés de los participantes y
actores.

3. Condiciones de falla:
• Listar las posibles condiciones de falla para cada caso de uso.
• Por cada paso, identificar cómo y por qué puede fallar.
• Este paso descubre situaciones especiales.

4. Manipulación de fallas: (Quizás sea la parte más difícil.)
• Especificar el comportamiento del sistema para cada condición de falla.
• Al realizar esta etapa emergerán nuevas situaciones y actores.

Los cuatro niveles pueden dirigir el proceso de análisis comenzando desde lo más
abstracto y agregando más detalles a medida que se avanza.
• Los casos de uso se deben especificar al nivel de detalle que sea suficiente, no hay un criterio general para determinar cuál es el adecuado.
• Para escribir, utilizar reglas de buena escritura técnica:
	Usar gramática simple / oraciones simples.
	Especificar claramente todas las partes del caso de uso.
	Cuando sea necesario, combinar o dividir pasos.