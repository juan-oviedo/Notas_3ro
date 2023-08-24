¿Qué debe contener una SRS?
• Tener lineamientos sobre qué se debe especificar en una SRS ayudará a
conseguir completitud.

Una SRS debe especificar requerimientos sobre:
• **Funcionalidad**.
• **Desempeño** (performance).
• **Restricciones de diseño.**
• **Interfaces externas.**

### Requerimientos de funcionalidad:
• Es el “corazón” del documento de SRS; conforma la mayor parte de la especificación.
• Especifica toda la funcionalidad que el sistema debe proveer.
• Especifica qué salidas se deben producir para cada entrada dada y las relaciones entre ellas.
• Describe todas las operaciones que el sistema debe realizar.
• Describe las entradas válidas y las verificaciones de validez de la entrada y salida.
• Describe el comportamiento del sistema en caso de entradas inválidas, errores de
cálculo u otras situaciones anormales (o en el caso de situaciones normales pero con imposibilidad de operar, ej. avión fully booked).
### Requerimientos de desempeño:
• Todas las restricciones en el desempeño del sistema de software.
• Requerimientos Dinámicos (especifican restricciones sobre la ejecución):
	Tiempo de respuesta.
	Tiempo esperado de terminación de una operación dada.
	Tasa de transferencia o rendimiento.
	Cantidad de operaciones realizadas por unidad de tiempo.
	En general se especifican los rangos aceptables de los distintos parámetros (en casos normales y	extremos).
	
• Requerimientos Estáticos o de capacidad (no imponen restricción en la ejecución):
	Cantidad de terminales admitidas.
	Cantidad de usuarios admitidos simultáneamente.
	Cantidad de archivos a procesar y sus tamaños.
	
• Todos los requisitos se especifican en términos medibles => verificable.

### Restricciones de diseño:
Existen factores en el entorno del cliente que pueden restringir las elecciones
de diseño. Por ejemplo:
• Ajustarse a estándares y compatibilidad con otros sistemas, limitaciones de
hardware y otros recursos.
• Requerimientos de confiabilidad, tolerancia a falla, o respaldo, seguridad

### Requerimientos de interfaces externas:
• Todas las interacciones del software con gente, hardware, y otros software
deben especificarse claramente.
• La interfaz con el usuario debe recibir atención adecuada. Crear un manual preliminar indicando los comandos del usuario, los formatos de las pantallas, etcétera.
• Estos requerimientos también deben ser precisos para asegurar
verificabilidad (evitar cosas como “la interfaz debe ser amigable”).

## Lenguajes de especificación
Los lenguajes de especificación deben facilitar escribir SRS con las características deseadas (modificabilidad, no ambigüedad, etcétera).
• A la vez deben ser fáciles de aprender.
• Los lenguajes formales son precisos y carecen de ambigüedad pero no son muy fáciles de aprender.
• Usualmente se utiliza el lenguaje natural apoyado por documentos estructurados
(estandarizados) para reducir imprecisiones y ambigüedades.
• La mayor ventaja del lenguaje natural es que tanto el cliente como los desarrolladores lo comprenden, pero es ambiguo...
• Las notaciones formales se utilizan en propiedades específicas del sistema o en sistemas críticos

Ej.: expresiones regulares para especificar formatos de E/S, autómatas (o álgebras de proceso) para especificar protocolos.
Otros: notación Z, método B, Alloy, redes de Petri, etcétera. Usualmente herramientas que los soportan