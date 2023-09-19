• Los sistemas procedurales tradicionales separan datos de procedimientos;
modela a ambos separadamente.
• Orientación a objetos: ve a los datos y a las funciones juntas (abstracción de
datos como base).
• El propósito del diseño OO es el de definir las clases del sistema a construir y las
relaciones entre éstas.


Análisis OO y diseño OO
• Las técnicas OO pueden utilizarse tanto para el análisis del requerimiento como
para el diseño.
• Los métodos y notaciones son similares.
• Pero: AOO modela el problema y DOO modela la solución.
• Existen métodos que combinan análisis y diseño (ADOO).
• ADOO sostiene que la representación creada por el AOO generalmente se
subsume en la representación del dominio de la solución creada por el DOO.


imagen


Análisis OO y diseño OO
• En este sentido la línea entre AOO y DOO no está definida del todo.
• Sin embargo, se diferencian en el tipo de objetos que manipulan:
• Los objetos del AOO representan un concepto del problema => objetos
semánticos.
• Además de los objetos semánticos, el DOO producen otros tipos de objetos:
• objetos de interfaces,
• objetos de aplicaciones, y
• objetos de utilidad.
• Además, el DOO hace mayor incapié en el comportamiento dinámico del sistema.
Se encargan de la
interfaz con el usuario
Especifican los mecanismos
de control para la solución
propuesta
Son los necesarios para soportar los
servicios de los objetos semánticos
(ej.: pilas, árboles, diccionarios, etc.)


Conceptos de la orientación a objetos
Clases y objetos
• La propiedad básica de los objetos es el encapsulado:
• Encapsula datos e información (i.e. el estado) y provee interfaces para accederlos y
modificarlos.
• Brinda abstracción y ocultado de información.
• Los objetos tienen estado persistente:
• Las funciones y procesos no retienen el estado.
• Un objeto sabe de su pasado y mantiene el estado.
• Los objetos tienen identidad: cada objeto puede ser identificado y tratado como una
entidad distinta.
• El comportamiento del objeto queda definido conjuntamente por los servicios y el
estado:
• La respuesta de un objeto depende del estado en que se encuentra.



• Una clase es una plantilla del cual se crean los objetos; define la estructura y los
servicios.
• Una clase tiene:
• una interfaz que define cuales partes de un objeto pueden accederse desde el exterior,
• un cuerpo que implementa las operaciones,
• variables de instancias para retener el estado del objeto.
• Las operaciones de una clase pueden ser:
• públicas: accesibles del exterior,
• privadas: accesibles sólo desde dentro de la clase,
• protegidas: accesibles desde dentro de la clase y desde sus subclases.
• Existen operaciones constructoras y destructoras.
Los objetos y las clases son
diferentes: las clases definen un
tipo, los objetos son sus
instancias


Relaciones entre objetos
• Si un objeto está vinculado durante un tiempo con otro hay una asociación entre
ellos.
• Un objeto interactúa con otro enviándole un mensaje solicitando un servicio.
Tras la recepción del mensaje, el objeto receptor invoca al método que
implementa tal servicio.
• Si un objeto es parte de otra clase hay una agregación (Relación derivada de una
asociación). En general es una colección. Sus ciclos de vida no están relacionado.
Es una relación unidireccional.
• Si un objeto está compuesto por otros se dice que hay una composición. El ciclo
de vida de ámbos objetos están muy relacionados.


Herencia y polimorfismo
• La herencia es un concepto único en OO.
• La herencia es una relación entre clases que permite la definición e
implementación de una clase basada en la definición de una clase existente.
• Cuando una clase Y hereda de una clase X, Y toma implícitamente todos
los atributos y operaciones de X.
• Y se denomina la subclase o clase derivada.
• X se denomina la superclase o clase base.
• La subclase Y tiene un parte derivada (heredada de X) y una parte
incremental (nueva).
• La parte incremental es la única que necesita definirse en Y.
• La herencia crea una relación “es-un”: un objeto de clase Y también es un
objeto de clase X.



• Herencia estricta: una subclase toma todas las características de su superclase.
• Sólo agrega características para especializarla.
• Herencia no estricta: la subclase redefine alguna de las características.
• La herencia estricta representa limpiamente la relación “es-un” y tiene muchos
menos efectos colaterales.
Es suficiente con mantener el invariante de clase y las pre/post-condiciones en las
interfaces (métodos).



• La herencia induce polimorfismo: un objeto puede ser de distintos tipos
(pertenecer a distintas clases).Un objeto de tipo Y es también un objeto de tipo
X (si Y es subclase de X).
• Un objeto tiene un tipo estático y un tipo dinámico.
• Vinculación dinámica (dynamic binding) de operaciones: el código asociado
con una operación se conoce sólo durante la ejecución.




Conceptos de diseño
• Durante el diseño la actividad clave es la especificación de clases del sistema a
construir.
• La corrección del diseño es fundamental.
• Pero el diseño también debe ser “bueno”: eficiente, modificable, estable, etc.
• El diseño se puede evaluar usando:
• Acoplamiento
• Cohesión
• Principio abierto-cerrado


Acoplamiento
El acoplamiento es un concepto inter-modular, captura la fuerza de interconexión
entre módulos.
Objetivo: bajo acoplamiento.
Tres tipos de acoplamiento:
• Acoplamiento por interacción
• Acoplamiento de componentes
• Acoplamiento de herencia


Acoplamiento por interacción:
• Ocurre debido a métodos de una clase que invocan a métodos de otra clase.
• Es similar al acoplamiento que se produce en diseño orientado a funciones.
• Mayor acoplamiento si:
• Los métodos acceden partes internas de otros métodos,
• los métodos manipulan directamente variables de otras clases,
• la información se pasa a través de variables temporales.
• Menor acoplamiento si los métodos se comunican directamente a través de los
parámetros:
• Con el menor número de parámetros posible,
• pasando la menor cantidad de información posible,
• pasando sólo datos (y no control).


Acoplamiento de componentes:
• Ocurre cuando una clase A tiene variables de otra clase C, en particular,
si A tiene variables de instancia de tipo C,
si A tiene parámetros de tipo C, o
si A tiene un método con variables locales de tipo C.
• Cuando A está acoplado con C, también está acoplado con todas sus subclases.
• Menor acoplamiento si las variables de clase C en A son, o bien atributos, o bien
parámetros en un método, i.e. son visibles.


Acoplamiento de herencia:
• Dos clases están acopladas si una es subclase de otra.
• Peor forma de acoplamiento si las subclases modifican la signatura de un método
o eliminan un método.
• También es malo si, a pesar de mantener la signatura de un método se modifica el
comportamiento de éste (debería preservar la pre/postcondición para que no sea
malo).
• Menor acoplamiento si la subclase sólo agrega variables de instancia y métodos
pero no modifica los existentes en la superclase.


Cohesión
La cohesión es un concepto intra-modular; captura cuán relacionado están los
elementos de un módulo.
Objetivo: alta cohesión.
Tres tipos de cohesión:
• Cohesión de método
• Cohesión de clase
• Cohesión de la herencia

Cohesión de método:
• ¿Por qué los elementos están juntos en el mismo método?
(Similar a la cohesión en diseño orientado a funciones).
• La cohesión es mayor si cada método implementa una única función claramente
definida con todos sus elementos contribuyendo a implementar esta función.
• Se debería poder describir con una oración simple que es lo que el método hace


Cohesión de clase:
• ¿Por qué distintos atributos y métodos están en la misma clase?
• Una clase debería representar un único concepto con todos sus elementos
contribuyendo a este concepto.
• Si una clase encapsula múltiples conceptos, la clase pierde cohesión.
• Un síntoma de múltiples conceptos se produce cuando los métodos se pueden
separar en diversos grupos, cada grupo accediendo a distintos subconjuntos de
atributos.


Cohesión de la herencia:
• ¿Por qué distintas clases están juntas en la misma jerarquía?
• Hay dos razones para definir subclases:
• Generalización-Especialización
• Reuso
• La cohesión es más alta si la jerarquía se produce como consecuencia de la
generalización-especialización.


Principio abierto-cerrado
“Las entidades de software deben ser abiertas para extenderlas y cerradas para
modificarlas”
B. Meyer
• El comportamiento puede extenderse para adaptar el sistema a nuevos
requerimientos, pero el código existente no debería modificarse.
i.e.: permitir agregar código pero no modificar el existente.
• Minimiza el riesgo de “dañar” la funcionalidad existente al ingresar cambios (lo
cual es una consideración muy importante al modificar código).
• Además es positivo para los programadores ya que ellos prefieren escribir código
nuevo en lugar de cambiar el existente.


Conceptos de diseño
Principio abierto-cerrado
• En OO este principio es satisfecho si se usa apropiadamente la herencia y el
polimorfismo.
• La herencia permite crear una nueva (sub)clase para extender el comportamiento
sin modificar la clase original.
Ej.: Un objeto cliente que interactúa con un objeto impresora:
Client llama
directamente a los
métodos de
Printer1
¿Qué ocurre si se
permite otra clase de
impresora?
Si se permite otra clase de
impresora se necesita crear otra
clase “Printer2”.
Pero además se debe modificar
al cliente para que la
pueda usar


Alternativamente:
• Definir Printer1 como subclase de una clase
Printer más general.
• Client accede sólo a Printer.
• Para modificar este caso, sólo es necesario
agregar Printer2 como suclase de Printer.
• Client no necesita ser modificado.


Principio de sustitución de Liskov:
Un programa que utiliza un objeto O con clase C debería permanecer
inalterado si O se reemplaza por cualquier objeto de una subclase de C.
• Si las jerarquías de un programa siguen este principio, entonces el programa
responde al principio abierto-cerrado.


Una metodología de diseño
• El punto de partida del diseño OO es el modelo obtenido durante el análisis OO.
• Usando este modelo se debe producir un modelo detallado final.
• La metodología OMT (Object Modeling Technique) involucra los siguientes pasos:
1. Producir el diagrama de clases.
2. Producir el modelo dinámico y usarlo para definir operaciones de las clases.
3. Producir el modelo funcional y usarlo para definir operaciones de las clases.
4. Identificar las clases internas y sus operaciones.
5. Optimizar y empaquetar. Es básicamente el
diagrama obtenido en
análisis



2. Producir el modelo dinámico
• El diagrama de clases es una estructura estática.
• El modelo dinámico apunta a especificar cómo cambia el estado de los distintos
objetos cuando ocurre un evento.
• Evento: desde el punto de vista de un objeto, es una solicitud de operación.
• Escenario: secuencia de eventos que ocurre en una ejecución particular del
sistema (recordar casos de uso).
• Los escenarios permiten identificar los eventos que realizan los objetos, i.e., los
servicios de los objetos.


• Comenzar por los escenarios iniciados por eventos externos.
• Primero modelar los escenarios exitosos, luego los escenarios excepcionales.
• Los distintos escenarios juntos permiten caracterizar el comportamiento
completo del sistema.
utilizar diagramas de interacción (secuencia/colaboración) o diagramas de estado
(ver Sección 8.1.3).


ejemplo

• Una vez modelados los escenarios se reconocerán eventos de los distintos objetos
(i.e. operaciones).
• Esta información se utilizará para expandir el diagrama de clases.
• En general, para cada evento en el diagrama de secuencia habrá una operación en
el objeto sobre el cual el evento es invocado.
• Por lo tanto, los diagramas de secuencias nos permiten refinar nuestra visión de
un objeto y agregar las operaciones necesarias que pueden no haber sido
identificadas previamente.
Ej.: “placeOrder” y “getBill” para el objeto “Order”




3. Producir el modelo funcional
• El modelo funcional describe las operaciones que toman lugar en el sistema.
• Especifica cómo computar los valores de salida a partir de los valores de la
entrada.
• No considera los aspectos de control, usar DFD.
• En OO las operaciones se realizan sobre objetos.
• Los transformadores del DFD representan esas operaciones.
Deben aparecer en alguna clase como una sola operación, o como múltiples
operaciones en varias clases.



4. Definir las clases y operaciones internas
• Hasta ahora las clases provienen del dominio del problema.
• Sin embargo, el diseño final debe ser un plano de la implementación =>
considerar cuestiones de implementación (incluyendo algoritmos y
optimización).
• Evaluar críticamente cada clase para ver si es necesaria en su forma actual (puede
que algunas clases innecesarias para la implementación se descarten.)
• Considerar luego las implementaciones de las operaciones de cada clase.
• Puede que necesiten operaciones de más bajo nivel sobre clases auxiliares más
simples (ej. árboles, diccionarios).
• Estas clases se denominan clases contenedoras.




5. Optimizar
• Agregar asociaciones redundantes,
con el fin de optimizar acceso a datos.
• Guardar atributos derivados,
con el fin de evitar cálculos complejos repetidos,
asegurar consistencia.
• Usar tipos genéricos,
permite reusabilidad de código.
Ej.: lista de ... , BTree de ...
• Ajustar la herencia,
considerar subir en la jerarquía las operaciones comunes,
considerar la generación de clases abstractas por sobre otras clases,
mejora reusabilidad.
Además de estos aspectos, se
deben aplicar los principios
generales (acoplamiento,
cohesión, y abierto-cerrado)
con el fin de mejorar la
calidad del diseño


Métricas
WMC
Métodos pesados por clases (WMC)
• La complejidad de la clase depende de la cantidad de métodos en la misma y
su complejidad.
• Sean M1 ... Mn los métodos de la clase C en consideración.
• Sea C(Mi) la complejidad del método i (ej.: la longitud estimada, complejidad
de la interfaz, complejidad del flujo de datos, etcétera).
• Luego: WMC = Σ C(Mi)
• Si WMC es alto => la clase es más propensa a errores.




Métricas
DIT
Profundidad del árbol de herencia (DIT)
• Una clase muy por debajo en la jerarquía de clases puede heredar muchos
métodos.
=> dificulta la predicción de su comportamiento.
• DIT de C es la profundidad desde la raíz.
• Es la longitud del camino de la raíz a la clase C.
• Si herencia múltiple => camino más largo.
• Significativo en detección de clases propensas a errores:
> DIT => > probabilidad de error en esa clase.



Métricas
NOC
Cantidad de hijos (NOC)
• Cantidad de subclases inmediatas de C.
• Da una idea del reuso:
> NOC => > reuso
• También da la idea de la influencia directa de la clase C sobre otros elementos
de diseño:
> influencia => > importancia en la corrección del diseño de esta clase.


Métricas
CBC
Acoplamiento entre clases (CBC)
Cantidad de clases a las cuales esta clase está acoplada.
• Dos clases están acopladas si los métodos de una usan métodos o atributos de
la otra.
• Usualmente se puede determinar fácilmente desde el código aunque existen
formas indirectas de acoplamiento que no se pueden determinar
estáticamente.
• < acoplamiento de una clase =>
> independencia de la clase => más fácilmente modificable.
• > CBC => > probabilidad de error en esa clase.



Métricas
RFC
Respuesta para una clase (RFC)
• CBC de C captura el número de clases a la cual C está acoplada.
• Sin embargo no captura la fuerza de las conexiones.
• RFC captura el grado de conexión de los métodos de una clase con otras clases.
• RFC de una clase C es la cantidad de métodos que pueden ser invocados como
respuesta de un mensaje recibido por un objeto de la clase C.
• Es decir, la cantidad de todos los métodos de C más los métodos de otras clases
que reciben un mensaje de un método de C.
• Es probable que sea más difícil testear clases con RFC más alto.
• Muy significativo en la predicción de clases propensas a errores.
