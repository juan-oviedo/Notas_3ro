El acoplamiento caracteriza el vínculo inter-modular.
• Se reduce minimizando las relaciones entre los elementos de los distintos
módulos. Otra forma de lograr un efecto similar es maximizando las relaciones entre los elementos del mismo módulo.
• La cohesión considera esta relación.
**La cohesión caracteriza el vínculo intra-modular.**

• Con la cohesión intentamos capturar cuan cercanamente están relacionados
los elementos de un módulo entre sí.
**Buscamos: menor acoplamiento y mayor cohesión.**

La cohesión de un módulo representa cuán fuertemente vinculados están los
elementos de un módulo.
• Da una idea de si los distintos elementos de un módulo tienen características
comunes.

**Objetivo: Alta cohesión.**
• La cohesión y el acoplamiento están correlacionados.
• Usualmente, a mayor cohesión de los módulos, menor acoplamiento entre los
módulos.
• Pero la correlación no es perfecta.

**Hay varios niveles de cohesión:**
• Casual:
	La relación entre los elementos del módulo no tiene significado. Ej.: (1) El programa es “modularizado” cortándolo en pedazos. (2) Un módulo es creado para evitar código repetido
	
• Lógica
	Existe alguna relación lógica entre los elementos del módulo; los elementos realizan funciones dentro de la misma clase lógica. Ej.: Un módulo que realiza todas las entradas. => Necesito flags para indicar que tipo de registro quiero imprimir
	
• Temporal
	Parecido a cohesión lógica pero los elementos están relacionados en el tiempo y se ejecutan juntos. Ej.: inicialización, clean-up, finalización. Mayor cohesión que lógica
	
• Procedural
	Contiene elementos que pertenecen a una misma unidad procedural. Ej.: un ciclo o secuencia de decisiones. Usualmente corta a través de bloques funcionales: tiene un trozo de función o parte de muchas funciones

• Comunicacional
	Tiene elementos que están relacionados por una referencia al mismo dato, i.e. los elementos están juntos porque operan sobre el mismo dato. Ej.: (1) “print and punch” (2) Pedir los datos de una cuenta personal y devolver todos los datos del registro
	
• Secuencial
	Los elementos están juntos porque la salida de uno corresponde la entrada del otro. Puede contener varias funciones o parte de una. Ej.: Quiero pintar el Fiat 600 de verde: (1) limpiar la chapa, (2) reparar defectos, (3) lijar (4) pintar. => Podría haber una segunda mano. Es relativamente buena cohesión y relativamente fácil de mantener, pero difícil de reusar
	
• Funcional
	Es la más fuerte de todas las cohesiones: Todos los elementos del módulo están relacionados para llevar a cabo una sola función. Ej.: (1) calcular el seno de un ángulo; (2) ordenar un arreglo; (3) calcular el salario neto; (4) reservar un asiento en el avión

**¿Cómo determinar la cohesión de un módulo?**
• Describir el propósito del módulo con una oración.
• Realizar el siguiente test:
	• Si la oración es compuesta, tiene comas o más de un verbo => el módulo está probablemente realizando más de una función. Probablemente tenga cohesión secuencial o comunicacional.
	• Si la oración contiene palabras relacionadas al tiempo (ej.: primero, luego, cuando, después) => probablemente el módulo tenga cohesión secuencial o temporal.
	• Si el predicado no contiene un único objeto específico a continuación del verbo (como es el caso de “editar los datos”) => probablemente tenga cohesión lógica.
	• Palabras como inicializar/limpiar/... implican cohesión temporal.
	• Los módulos funcionalmente cohesivos siempre pueden describirse con una oración simple.