Una base de datos (BD) contiene información.
Aplicaciones de BD:
• Permiten navegar/consultar las informaciones
• Permiten alterar las informaciones

Esquema: se usa para describir la estructura de la BD.

Instancia: contenido actual de la BD en un momento del tiempo

Los datos (instancias) son almacenados en tablas.
Las columnas representan atributos (o propiedades) para los elementos de la tabla (tuplas).

Una consulta en una base de datos es una expresión que describe una
colección de datos deseada.
Para expresar consultas se usan lenguajes de consulta.
Para consultar los datos en modelo relacional es muy usado en la industria
el lenguaje de consultas SQL.

Para el modelo relacional existen lenguajes de consulta puros como álgebra
relacional, cálculo de tuplas, etc.
	o Son más sencillos y se concentran en menos aspectos.
	o En la materia veremos una variación más expresiva del álgebra relacional llamada álgebra de tuplas.
Veremos cómo el sistema gestor de BD procesa consultas para el modelo
relacional.
o Esta tarea se facilita si traducimos una consulta SQL al álgebra relacional – o álgebra
de tuplas - y luego la procesamos.

## Diseño de BD relacional
un mal diseño:
Almacenar toda la información en una sola tabla resulta en:
o Repetición de la información (llamado redundancia de datos)

Se modela una la base de datos de una organización como una
colección de entidades y relaciones.
• Entidad: objeto en organización distinguible de otros objetos. Descrito por
medio de atributos.
• Relación: asociación entre entidades.
• Representado diagramáticamente usado un diagrama de entidad-relación

Un buen diseño de entidad relación no contiene atributos
redundantes

### atributos vs relaciones
El CR supervisa es la forma correcta de representar esta situación porque
hace la conexión entre estudiante e instructor explícita en lugar de implícita
vía un atributo
Usar un CR que vincula los dos CE es la forma correcta de representar
esta situación porque hace la conexión entre los dos CE explícita, en
lugar de implícita vía atributos de la clave primaria de uno de los CE

### atributos en relaciones
usar los atributos de clave primaria de CEs
relacionados como atributos de CR

### relaciones de grado > 2
Si con los CR binarios puedo capturar los datos del CR de grado
2 y puedo expresar más restricciones de integridad que con
el CR de grado 2 entonces usar los CR binarios

### atributo multi-valorado compuesto vs entidad débil
Si el objeto contemplado tiene su complejidad e involucra varios atributos y
es de suma importancia para la organización, es poco conveniente tenerla
como un atributo de un CE fuerte
Por lo tanto, conviene modelarlo como un CE débiles.

Si los objetos siendo considerados están relacionados con entidades
de un CE fuerte que no es de identificación,
entonces es necesario modelar dichos objetos como CE débiles

### atributos vs entidades
Cuando el CE E tiene un solo objeto que tiene un solo valor (
conviene modelar al objeto como un atributo simple, sobre todo cuando
la estructura del objeto no va a cambiar en su organización y no forma
parte de los asuntos más importantes de la institución
La opción seleccionada es la más simple de representar

Cuando el CE E tiene cero o más objetos que tienen un solo valor ( se puede
modelar al objeto como un atributo multivalorado sobre todo cuando la estructura de esos objetos no va a cambiar en su organización y no forma parte de los asuntos más importantes de la institución
La opción seleccionada es la más simple de representar

Cuando el objeto tiene varios atributos y es poseído por una sola entidad del CE E
conviene modelar el objeto como CE
La razón es que “ser poseído por una sola entidad” no se puede representar usando un atributo

Cuando el objeto tiene varios atributos algunos de los cuales no son de clave
primaria del objeto y es poseído por varias entidades del CE E conviene modelar el
objeto como CE
La razón es que los atributos del objeto que no se usan para identificarlo generan
redundancia de información cosa que no pasa cuando el objeto se representa
como CE

### entidad vs relacion
Cuando el CR es uno varios o varios uno:
si hay atributos no de clave primaria en el CE del lado uno, entonces los atributos del CE del lado uno que no son de clave primaria dan lugar a redundancia de  información si se usa alternativa CE
Por lo que conviene usar la opción CR en lugar de CE

Si el CR es varios varios:
Si en al menos en un CE hay atributos que no son de clave primaria
Entonces los atributos del CE que no son de clave primaria dan lugar a redundancia de información si se usa la opción CE
Por lo que conviene usar CR en lugar de CE
## Sistema gestor de BD
Un sistema gestor de BD (SGBD) se compone de:
o Gestor de almacenamiento
o Procesamiento de consultas
o Gestor de transacciones

### Gestión del almacenamiento
Los datos deben ser organizados en archivos con estructuras apropiadas de
modo que su acceso, modificación y retorno sea eficiente.
• A nivel físico se explica cómo los registros de datos son almacenados en
archivos.
• Para acceso, modificación y almacenamiento eficiente a los datos se
pueden usar índices (unas estructuras de acceso especiales).
• A nivel lógico se describen los datos almacenados en la BD y las relaciones
entre ellos.
• El gestor de almacenamiento provee una interfaz para los datos a nivel
físico para ser usada por los programas de aplicación y consultas enviadas al
sistema. Se ocupa de: acceso al almacenamiento, organización en archivos
de los datos, indexado.

### Procesamiento de consultas
1. Parsing de la consulta y su traducción (p.ej. a algebra relacional)
2. Optimización:
• Encontrar la manera “más eficiente” (o plan) para obtener la información descrita
por la consulta.
3. Evaluación (siguiendo el plan optimizado)

• Una consulta se puede evaluar de maneras alternativas
• Expresiones equivalentes
• Diferentes algoritmos para cada operación
• La diferencia de costo entre una buena y una mala manera de
evaluar una consulta puede ser enorme.
• Es necesario estimar el costo de las operaciones.
• Depende de información estadística acerca de las relaciones que la BD
debe mantener.
• Hace falta estimar estadísticas para resultados intermedios para
computar el costo de expresiones complejas.

### Transacciones
• Preguntas importantes:
o ¿Qué pasa si falla el SGBD?
o ¿Qué pasa si más de un usuario actualiza concurrentemente los mismos datos?
• Una transacción es una colección de operaciones que realiza una función
lógica simple en una aplicación de BD
o Una transacción es una unidad de ejecución que accede y posiblemente actualiza
varios ítems de datos.

• La componente de manejo de transacciones asegura que BD
permanezca en un estado consistente (correcto) a pesar de fallas del
sistema (e.g. fallas de energía, caídas de SO) y fallas de transacciones.
• Problema: ¿Cómo hacer para que una transacción se ejecute
indivisiblemente?
• Solución: Aplicar atomicidad.
• Atomicidad significa o todas las operaciones de la transacción son reflejadas
en la BD o ninguna lo es.

• Asegurar la atomicidad es responsabilidad del SGBD, específicamente del gestor
de recuperaciones.
• En la ausencia de fallas todas las transacciones completan exitosamente y la
atomicidad se logra fácilmente.
• Debido a los varios tipos de falla una transacción puede no completarse
exitosamente.
• Para asegurar atomicidad, la falla de una transacción no debe tener efecto en el
estado de la base de datos.
• O sea, la BD debe restaurarse al estado en que estaba antes que la transacción
comenzara su ejecución.

• Planificaciones: secuencias que indican el orden cronológico en el cual las
instrucciones de transacciones concurrentes son ejecutadas.

• Cuando varias transacciones actualizan la BD concurrentemente, la
consistencia de los datos puede dejar de ser preservada, aun cuando cada
transacción individual es correcta.
o Se debe ejecutar una planificación adecuada que no genere problemas.
• Gestor de concurrencia de transacciones: controla la interacción entre
transacciones concurrentes para asegurar la consistencia de la BD.
• El gestor de transacciones consiste del gestor de recuperaciones y del
gestor de concurrencia de transacciones.



# traducción a tablas
Esquemas relacionales:

R = (A 1 , A 2 , …, A n ) es un esquema de relación

A 1 , A 2 , …, A n son atributos.

Dados conjuntos D 1 D 2 D n una relación r es un subconjunto de D 1 x D 2 x x D n
Las relaciones son conjuntos (el orden entre las tuplas no importa).
Se puede pensar una relación como una tabla con columnas para los
dominios D 1 , D 2 , …. D n respectivamente.
Un elemento t pertenece r es una tupla representado mediante una fila de la
tabla.

Notación nombres de relaciones comienzan con minúscula,
nombres de esquema comienzan con mayúscula

r (R) significa r es una relación con esquema de relación R
O sea, las columnas de r tienen como nombres los atributos de R

El conjunto de valores permitidos para cada atributo se llama dominio del atributo
Exigencia:
Los valores de los atributos se requiere que sean atómicos esto es, indivisibles
Esto se refiere al uso que se hace de los atributos
O sea que en las consultas o restricciones de integridad no me voy poner a dividir el valor de un atributo en partes
Esto va a simplificar la descripción de consultas o restricciones de integridad

•
Implicaciones de la exigencia anterior
En un esquema de relación no puedo tener atributos multivalorados
En un esquema de relación no puedo tener atributos compuestos
Aquí surge una diferencia importante con el diseño de entidad relación

Un esquema de una BD relacional es un conjunto de esquemas de
relación. R1 R n
Una base de datos relacional consiste de múltiples relaciones.
r 1( R 1 ),…, r n (R n)

Implicaciones
Primero definimos los conceptos del problema mediante esquemas de relación
Luego definimos los datos como tablas asociadas a esos esquemas
Luego podemos poblar las tablas, consultarlas y alterarlas

Propósito Ahora vamos a ver algunos tipos de restricciones de integridad
muy comunes cuando se trabaja con el modelo relacional

Mal diseño de DB relacional:
Almacenar toda la información en una sola relación resulta en
Repetición de la información
Necesidad de valores nulos

En ambos casos usar criterios de decisión que nos ayudarán a escoger
entre opciones de traducción o a mejorar una idea de traducción
Redundancia de información
Facilidad de comprensión
Facilidad para hacer consultas

# Reglas
## Entidades
### 1
Un CE fuerte que no involucra atributos compuestos ni atributos multi valorados se mapea a un esquema relacional con los mismos atributos
La clave primaria del CE se convierte en la clave primaria del esquema relacional

### 2
Un CE fuerte que no involucra
atributos/ subatributos multivalorados se mapea a un esquema relacional con los mismos atributos simples y los subatributos hoja de los atributos compuestos

### 3
un atributo multivalorado M simple de un CE E es representado por un esquema separado EM
EM tiene atributos correspondientes a la clave primaria de E y un atributo correspondiente al atributo multivalorado M
Todos los atributos de EM forman su clave primaria
Se pone una restricción de clave foránea desde EM que referencia a la clave primaria de E

### Decision
Los atributos derivados no son explícitamente representados en el modelo de datos relacional Se verá que si se los necesita una forma de computarlos es
por medio de consultas

## Relaciones
### 1
un CR varios varios es representado con un esquema con atributos para las claves primarias de los dos CE participantes y todos los atributos descriptivos del CR (que no son multivalorados
la clave primaria del esquema del CR es la unión de las claves primarias de los CEs que participan en el CR
Para cada CE que participa en el CR se crea restricción de clave foránea que referencia clave primaria de CE

### 2
un CR varios a uno o uno a varios que es total en el lado varios puede ser representado agregando atributos extra en el CE del lado varios, conteniendo la clave primaria del lado uno
La clave primaria del CR es la clave primaria del CE del lado varios
Se crea restricción de clave foránea de CR que referencia a clave primaria de
CE de lado varios

**no se porque se referencian las cardinalidades asi, pero como yo lo interpreto es que la clave foránea va en la entidad que es muchos, ya que sino tendria que guardar en el que es uno, la clave de todas las entidades con las que se relaciona**

Si la participación es parcial en el lado varios, aplicar la regla anterior puede resultar en valores nulos
Esto sucede cuando a una entidad del CE del lado varios no le corresponde ninguna entidad del CE del lado uno

### 3
Un CR uno a uno con participación total en ambos lados puede ser mapeado agregando al esquema resultante de traducir uno de los CE participantes los atributos de la clave primaria del otro CE
La clave primaria de cualquier CE puede ser elegida como la clave primaria del
CR 
Se crea restricción de clave foránea de esquema relacional asociado al CR que
referencia clave primaria de otro CE (el que no se tomo de base para hallar el
esquema asociado al CR)

### Entidad débil
un CE débiles se mapea a una tabla que incluye columnas para la clave primaria del CE identificador más los atributos (no multi-valorados) del CE débiles (achatando jerarquías de atributos compuestos si es necesario)
La clave primaria del CE debil es identificador más el discriminador del CE débil forman la clave primaria del esquema relacional de la traducción
Para atributos de esquema de CE débil que provienen de CE identificadora se agrega restricción de clave foránea desde esquema de CE débil a CE identificador
El CR identificador no se mapea

## generalización

### generalización que no esta relacionada con otras E
#### generalización no disjunta:
es decir cuando una entidad E, puede pertenecer a varias especificaciones a la vez
una persona puede ser un jugador y un desarrollador de un juego

Formar una tabla para el CE de nivel más alto (la generalización)
Formar una tabla para cada CE especialización que incluye la clave primaria del CE generalización y los atributos locales

obtener toda la información de CE de especialización requiere acceder a dos tablas, pero si guardamos en cada especificacion, todos los atributos de la generalizacion, podemos estar haciendo redundancia de datos si una instancia pertenece a 2 especificaciones

#### generalización disjunta, pero no total:
es decir cuando una entidad E, puede pertenecer a la entidad generalizadora sin pertenecer a las entidades especificas, pero no puede pertenecer a 2 entidades especificas ej:
si tengo una BD que modela que un vehiculo puede estar ser un auto, o un camion, pero se ingresa una moto a la BD, como no entra en ninguna especificacion se queda en la generalizacion

formar una tabla para cada CE especialización con los atributos locales y heredados del CE generalización

#### generalización disjunta y total:
es decir toda instancia de la generalización tiene que pertenecer a solo una especializacion

formar una tabla para cada CE especialización con los atributos locales y
heredados no formar tabla para la generalización

### Otra opción:
se puede ignorar las especificaciones, y formar solo la tabla de la generalizacion agregando algunos atributos que estaban en las especificaciones

**contras:**
si la generalización no es disjunta puedo tener datos redundantes
puedo tener campos como null, lo cual no es deseable




# Algebra de tablas
**operadores:**
- proyección(pi)
- selección (sigma)
- producto cartesiano (X)
- reunion (moño) solo hace X de tuplas que comparten un atributo, ej a.id = b.id
- definición local (let)
- concatenación (++) (se pone una tabla dsp de la otra)
- resta (\)
- intersección
- renombramiento (rho)
- remover duplicados (*v*)
- agregación y agrupamiento (upsilon): (agrup) (upsilon) (agreg)