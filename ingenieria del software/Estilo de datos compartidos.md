• Dos tipos de componentes: repositorio de datos y usuarios de datos.
• Repositorio de datos: provee almacenamiento permanente confiable.
• Usuarios de datos: acceden a los datos en el repositorio, realizan cálculos, y
ponen los resultados otra vez en el repositorio.
• La comunicación entre los usuarios de los datos sólo se hace a través del
repositorio.
• En este estilo sólo hay un tipo de conector: lectura/escritura.
Pero las funcionalidades prestadas pueden ser distintas: simples lecturas/ escrituras a transacciones complejas
#### Dos variantes principales:
• Estilo pizarra:
	Cuando se agregan/modifican datos en el repositorio, se informa a todos los usuarios. i.e.: la fuente de datos compartidos es una entidad activa.
	
• Estilo repositorio:
	El repositorio es pasivo. Ej.: sistemas orientados a base de datos; sistemas de web; entornos de programación; etc.