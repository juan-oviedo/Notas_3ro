Ventajas del modelo orientado a objetos:
• Más fácil de construir y de mantener.
• La transición del análisis orientado a objetos al diseño orientado a objetos
parece ser más simple.
• El análisis orientado a objetos es más resistente/adaptable a cambios porque
los objetos son más estables que las funciones.

El sistema es visto como un conjunto de objetos interactuando entre sí (o con
el usuario) a través de servicios que cada objeto provee.

### Objetivo:
• Identificar los objetos (de hecho, las clases) en el dominio del problema.
• Definir las clases identificando cuál es la información del estado que ésta
encapsula (i.e. los atributos).
• Identificar las relaciones entre los objetos de las distintas clases, ya sea en la
jerarquía o a través de llamadas a métodos.
#### El sistema consta de objetos.
• Cada objeto tiene atributos que juntos definen al objeto. Definen el estado del
objeto.
• Los objetos de tipos similares se agrupan en clases (de objetos).
• Un objeto provee servicios o realiza operaciones.
• Estos servicios son los únicos medios que permiten ver o modificar el estado de
un objeto.
• Los servicios se acceden a través de mensajes que se envían a los objetos.

![[Pasted image 20230823194242.png]]

* Diagrama de clase: representa gráficamente la estructura del problema
* Clase: conformada por nombre, atributos, y servicios
* Asociación: representa una relación entre objetos de distintas clases (lineas que unen 2 clases)
* Estructura de agregación: modela la relación “está conformado por” (rombo en una relación)
* Estructura de generalización-especialización: utilizado para representar herencia de objetos (triangulo en una relación)
* La presencia de este círculo negro indica la multiplicidad de la relación


### Los pasos más significativos para realizar el análisis orientado a objetos son:
#### Identificar objetos y clases.
* Observar el espacio del problema
* Obtener breve resumen 
* Identificar sustantivos 
* Aislar candidatos como potenciales objetos del sistema 
* Posteriormente podrían descartarse
#### Identificar estructuras.
* Considerar clases previamente identificadas 
* Considerar si alguna generaliza/especializa a otra (¡que sea significativa!) 
* Considerar si algún objeto es parte de otro para definir agregación
#### Identificar atributos.
* Los atributos representan las características que definen los objetos 
* Considerarlos cuidadosamente dentro del dominio del problema
- No agregar atributos innecesarios 
- Ubicarlos apropiadamente en la jerarquía de clases
#### Identificar asociaciones.
* Una asociación captura la relación entre	instancias de varias clases Usualmente se derivan directamente del dominio del	problema 
* Pueden tener sus propios atributos (no forzar estos atributos en los
	objetos)
#### Definir servicios
* Los servicios proveen el elemento activo en el modelado OO
* Para identificar los servicios, definir los estados del sistema y por cada estado listar los eventos externos y respuestas requeridas 
* Asociar estas actividades con las clases