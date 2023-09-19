• Esencial en el particionado del problema.
• Utilizado en todas las disciplinas de ingeniería.
• La abstracción de una componente describe el comportamiento externo sin dar
detalles internos de cómo se produce dicho comportamiento.

#### Abstracción de componentes existentes
• Representa a las componentes como cajas negras.
• Oculta detalle, provee comportamiento externo.
• Útil para comprender sistemas existentes => tiene un rol importante en  mantenimiento.
• Útil para determinar el diseño del sistema existente.

#### Abstracción durante el proceso de diseño
• Las componentes no existen.
• Para decidir como interactúan las componentes sólo el comportamiento
externo es relevante.
• Permite concentrarse en una componente a la vez.
• Permite considerar una componente sin preocuparse por las otras.
• Permite que el diseñador controle la complejidad.
• Permite una transición gradual de lo más abstracto a lo más concreto.
• Necesaria para solucionar las partes separadamente.
	
#### Dos mecanismos comunes de abstracción
• Abstracción funcional.
• Abstracción de datos.

#### Abstracción funcional
• Especifica el comportamiento funcional de un módulo.
• Los módulos se tratan como funciones de entrada/salida.
• La mayoría de los lenguajes proveen características para soportarla.
Ej.: procedimientos, funciones.
• Un módulo funcional puede especificarse usando pre y postcondiciones.
• Forma la base de las metodologías orientadas a funciones

#### Abstracción de datos
• Una entidad del mundo real provee servicios al entorno.
• Es el mismo caso para las entidades de datos: se esperan ciertas operaciones de un objeto de dato.
• Los detalles internos no son relevantes.
• La abstracción de datos provee esta visión:
• Los datos se tratan como objetos junto a sus operaciones.
• Las operaciones definidas para un objeto sólo pueden realizarse sobre este objeto.
• Desde fuera, los detalles internos del objetos permanecen ocultos y sólo sus
operaciones son visibles.
• Muchos lenguajes soportan abstracción de datos.
• Forma la base de las metodologías orientadas a objetos.