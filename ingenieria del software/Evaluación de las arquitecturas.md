• La arquitectura tiene impacto sobre los atributos no funcionales tales como modificabilidad, desempeño, confiabilidad, portabilidad, etcétera.
• Tanto como las elecciones de diseño y codificación => se deben evaluar estas propiedades en la arquitectura propuesta.
• ¿Cómo hacerlo?
	Una posibilidad => técnicas formales (redes de colas, model checkers, lenguajes de specificación, etcétera.)
	Otra posibilidad => metodologías rigurosas.

### El método de análisis ATAM
Architecture Trade-off Analysis Method
Analiza las propiedades y las concesiones entre ellas.
### Recolectar escenarios
• Los escenarios describen las interacciones del sistema.
• Elegir los escenarios de interés para el análisis.
• Incluir escenarios excepcionales sólo si son importantes.
#### Recolectar requerimientos y/o restricciones
• Definir lo que se espera del sistema en tales escenarios.
• Deben especificar los niveles deseados para los atributos de interés  (preferiblemente cuantificados.)
#### Describir las vistas arquitectónicas
• Las vistas del sistema que serán evaluadas son recolectadas.
• Distintas vistas pueden ser necesarias para distintos análisis.
#### Análisis específicos a cada atributo
• Se analizan las vistas bajo distintos escenarios separadamente para cada atributo de interés distinto.
• Esto determina los niveles que la arquitectura puede proveer en cada atributo.
• Se comparan con los requeridos.
• Esto forma la base para la elección entre una arquitectura u otra o la modificación de la arquitectura propuesta.
• Puede utilizarse cualquier técnica o modelado.
#### Identificar puntos sensitivos y de compromisos 
• Análisis de sensibilidad: cuál es el impacto que tiene un elemento sobre
un atributo de calidad. Los elementos de mayor impacto son los puntos de sensibilidad.
• Análisis de compromiso:
Los puntos de compromiso son los elementos que son puntos de
sensibilidad para varios atributos.

### leer del libro el ejemplo