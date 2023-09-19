• Los elementos son entidades de ejecución denominados componentes, i.e., una componente es una unidad que tiene identidad dentro del sistema en ejecución. Ej.: objetos, procesos, .exe, .dll, etcétera.
• Los conectores proveen el medio de interacción entre las componentes.
Ej.: pipes, sockets, memoria compartida, protocolos, etcétera.

### Dos elementos principales: componentes y conectores.
• Componentes: son elementos computacionales o de almacenamiento de datos.
• Conectores: son mecanismos de interacción entre las componentes.
• Una vista C&C define las componentes y cómo se conectan entre ellas a través
de conectores, describe una estructura en ejecución del sistema: qué
componentes existen y cómo interactúan entre ellos en tiempo de ejecución.

#### Componentes
• Son unidades de cómputo o de almacenamiento de datos.
• Cada componente tiene un nombre que representa su rol y le provee una
identidad.
• Cada componente tiene un tipo. Los distintos tipos se representan con distintos símbolos.
• Las componentes utilizan interfaces o puertos para comunicarse con otras
componentes.

![[Pasted image 20230906190359.png]]

#### Conectores
• Describen el medio en el cual la interacción entre componentes toma lugar.
• Un conector puede proveerse por medio del entorno de ejecución.
Ej.: llamada a procedimiento/función.
• Sin embargo, los conectores pueden también ser mecanismos de interacción más
complejos, ej.: puertos TCP/IP, RPC, protocolos como HTTP, etcétera.
• Notar que estos mecanismos requieren una infraestructura de ejecución significativa + programación especial dentro de la componente para poder utilizarla. importante identificarlos/representarlos explícitamente.
• Los conectores no necesariamente son binarios (ej.: bus de broadcasting).
• Los conectores tienen:
	• Nombre, que identifican la naturaleza de la interacción
	• Tipo, que identifica el tipo de interacción (binaria o n-aria, unidireccional o bidireccional, etcétera).
	• Muchas veces los conectores representan protocolos => las componentes necesitan seguir algunas convenciones al usar el conector (ej.: TCP).
	• Los distintos tipos de conectores se representan con distintas notaciones.

![[Pasted image 20230906190934.png]]



### Estilos arquitectónicos para la vista de C&C

• Sistemas distintos tienen estructuras de C&C distintas.
• Algunas estructuras son generales y son útiles para una clase de problemas
=> estilos arquitectónicos.
• Un estilo arquitectónico define una familia de arquitecturas que satisface
las restricciones de ese estilo.
• Los estilos proveen ideas para crear arquitecturas de sistemas.
• Distintos estilos pueden combinarse para definir una nueva arquitectura.

#### [[Pipe and Filter]]
#### [[Estilo de datos compartidos]]

#### [[Estilo cliente-servidor]]

#### [[Estilo publish-subscribe]]
#### [[Estilo peer-to-peer]]
#### [[Estilo de procesos que se comunican]]



