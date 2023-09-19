Dos módulos son independientes si cada uno puede funcionar completamente sin la presencia del otro.
• La independencia entre módulos es deseable:
	• Los módulos se pueden modificar separadamente.
	• Se pueden implementar y testear independientemente.
	• El costo de programación decrece.
	• En un sistema no existe la independencia entre todos los módulos.
	• Los módulos deben cooperar entre sí.
	• Cuanto más conexiones hay entre dos módulos, más dependientes son uno del otro, i.e. se requiere más conocimiento de un módulo para comprender el otro módulo.
• El acoplamiento captura la noción de dependencia.

**Objetivo: los módulos deben estar tan débilmente acoplados como sea posible.**
• Cuando sea posible => módulos independientes.
• El nivel de acoplamiento se define a nivel de diseño arquitectónico y de alto nivel.
• No puede reducirse durante la implementación.
• El acoplamiento es un concepto inter-modular.

**Factores más importantes que influyen en el acoplamiento:**
• Tipo de conexiones entre módulos
	Ej.: ¿Utilizo sólo las interfaces especificadas o también uso datos compartidos?
• Complejidad de las interfaces.
	Ej.: ¿Estoy pasando sólo los parámetros necesarios?
• Tipo de flujo de información entre módulos.
	Ej.: ¿Estoy pasando parámetros de control (ej.: flag)?

El acoplamiento entre módulos queda definido por la “fuerza de conexión” entre
dichos módulos.
• En general: cuanto más necesitamos conocer de un módulo A para comprender un módulo B, mayor es la conexión de A a B.
• Los módulos fuertemente acoplados están unidos por fuertes conexiones.
• Los módulos débilmente acoplados están débilmente conectados.

**La complejidad y oscuridad de las interfaces de un módulo, i.e. el tipo de conexión incrementan el acoplamiento.**
• Minimizar la cantidad de interfaces por módulo.
• Minimizar la complejidad de cada interfaz.

• El acoplamiento disminuye si:
	• Sólo las entradas definidas en un módulo son utilizadas por otros.
	• La información se pasa exclusivamente a través de parámetros.

• El acoplamiento se incrementa si:
	• Se utilizan interfaces indirectas y oscuras.
	• Se usan directamente operaciones y atributos internos al módulo.
	• Se utilizan variables compartidas.

El acoplamiento se incrementa con la complejidad de cada interfaz,
	ej.: cantidad y complejidad de los parámetros.
• Usualmente se usa más de lo necesario,
	ej.: pasar un registro completo cuando sólo un campo es necesario.
• Cierto nivel de complejidad en las interfaces es necesario para soportar la
comunicación requerida con el módulo. => Encontrar balance.
• Mantener las interfaces de los módulos lo más simple que sea posible.

El acoplamiento depende del tipo del flujo de información.
• Dos tipos de información: control o dato.

• Transferencia de información de control:
	• Las acciones de los módulos dependen de la información.
	• Hace que los módulos sean más difíciles de comprender.

• Transferencia de información de datos:
	• Los módulos se pueden ver simplemente como funciones de entrada/salida.

• Bajo acoplamiento: las interfaces sólo contienen comunicación de datos.
• Alto acoplamiento: las interfaces contienen comunicación de información híbrida
(datos+control).

![[Pasted image 20230906202808.png]]
