• Adecuado para sistemas que fundamentalmente realizan transformaciones
de datos.
• Un sistema que usa este estilo utiliza una red de transformadores para
realizar el resultado deseado.
• Tiene un sólo tipo de componente: filtro.
• Tiene un sólo tipo de conector: tubo.
• Un filtro realiza transformaciones y le pasa los datos a otro filtro a través de
un tubo.

#### Restricciones 1:
• Un filtro es una entidad independiente y asíncrona (se limita a consumir y producir datos).
• Un filtro no necesita saber la identidad de los filtros que envían o reciben los datos.
• Un tubo es un canal unidireccional que transporta un flujo de datos de un filtro a
otro.
• Un tubo sólo conecta 2 componentes.
• Los filtros deben hacer “buffering” y sincronización para asegurar el correcto
funcionamiento como productor y consumidor.
#### Restricciones 2:
• Cada filtro debe trabajar sin conocer la identidad de los filtros productores
o consumidores.
• Un tubo debe conectar un puerto de salida de un filtro a un puerto de
entrada de otro filtro.
• Un sistema puro de tubos y filtros usualmente requiere que cada filtro tenga
su propio hilo de control.