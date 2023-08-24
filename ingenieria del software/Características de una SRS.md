Para satisfaces las metas básicas, un SRS debe tener las siguientes características: 

**Corrección**:
Cada requerimiento representa precisamente alguna característica deseada por el cliente en el sistema final.

**Completitud**:
Todas las características deseadas por el cliente están descriptas.
La característica más difícil de lograr (para conseguirla uno debe detectar las ausencias en la especificación).
Corrección y completitud están fuertemente relacionadas.

**No ambigua:**
Si para cada requerimiento existe un solo significado.
Si es ambigua los errores se colarán fácilmente. La no ambigüedad es esencial para verificabilidad. Como la verificación es usualmente hecha a través de revisiones, la SRS debe ser comprensible (al menos por el desarrollador, el usuario y el cliente). Particular atención si se usa lenguaje natural.
Los lenguajes formales ayudan a “desambiguar”.

**Consistente**:
Ningún requerimiento contradice a otro.
Ej.: conflictos lógicos, temporales, de dependencias.

**Verificable**:
Si existe para cada requerimiento algún proceso efectivo que puede asegurar que el software final satisface el requerimiento.

**Rastreable**:
Se debe poder determinar el origen de cada requerimiento y cómo éste se relaciona a los elementos del software.
Hacia adelante: dado un requerimiento se debe poder detectar en qué elementos de diseño o código tiene impacto.
Hacia atrás: dado un elemento de diseño o código se debe poder rastrear que requerimientos está atendiendo.

**Modificable**:
Si la estructura y estilo de la SRS es tal que permite incorporar cambios fácilmente
preservando completitud y consistencia.
La redundancia es un gran estorbo para modificabilidad (puede resultar en inconsistencia).

**Ordenada en aspectos de importancia y estabilidad**:
Los requerimientos pueden ser críticos, importantes pero no críticos, deseables pero no importantes.
Algunos requerimientos son esenciales y difícilmente cambien con el tiempo. Otros son propensos a cambiar => Se necesita definir un orden de prioridades en la construcción para reducir riesgos debido a cambios de requerimientos.