• No hay una única arquitectura de un sistema.
• Hay distintas vistas de un sistema de software (paralelismo con ingeniería civil).
• Una vista consiste de elementos y relaciones entre ellos, y describe una estructura.
• Los elementos de una vista dependen de lo que la vista quiera destacar. Distintas vistas exponen distintas propiedades.
• Una vista que se enfoca en algún aspecto reduce la complejidad con la que debe
enfrentarse el lector.
• Muchos tipos de vistas fueron propuestos. La mayoría pertenece a alguno de estos tres tipos:
	Módulo
	Componentes y conectores
	Asignación de recursos

• Las distintas vistas están correlacionadas (¡todas representan al mismo sistema!)
Existen relaciones entre los elementos de una vista y los de otra; tal relación puede ser muy compleja.

#### Vista de módulos:
• Un sistema es una colección de unidades de código (ellas no representan entidades en ejecución) i.e., los elementos son módulos.
Ej.: Clases, paquetes, funciones, procedimientos, métodos, etcétera.
• La relación entre ellos está basada en el código.
Ej.: “parte de”, “usa a” o “depende de”, llamadas, generalización o especialización,
etcétera.

#### Vista de[[ componentes y conectores]]:

#### Vista de asignación de recursos:
• Se enfoca en cómo las unidades de SW se asignan a recursos como hw, sistemas
de archivos, gente, etcétera. i.e., especifica la relación entre los elementos del SW y las unidades de ejecución en el entorno.
• Exponen propiedades estructurales como qué proceso ejecuta en qué
procesador, qué archivo reside dónde, etcétera.

• Una descripción arquitectónica consiste de vistas de distintos tipos, cada una
mostrando una estructura diferente. Distintos sistemas necesitan distintos tipos de vistas dependiendo de las necesidades. Ej: 
	análisis de desempeño => C&C
	asignación de recursos => asignación de recursos
	planeamiento => módulos

![[Pasted image 20230905233218.png]]

•La vista de C&C es la que casi siempre se hace, y se ha transformado en la vista
principal.
Nos enfocaremos en C&C.
La vista de módulos se verá más adelante, en diseño de alto nivel (cuyo enfoque es
identificar módulos).