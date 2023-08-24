Para poder estimar costos y tiempos y planear el proyecto se necesita “medir” el esfuerzo que
demandará.
• El esfuerzo del proyecto depende de muchos factores.
• El tamaño es el principal factor (validado por muchos experimentos y datos de análisis).
• Al principio el tamaño sólo puede ser estimado.
• Conseguir buenos estimadores es muy difícil.
• Una métrica es importante sólo si es útil para el seguimiento o control de costos, calendario
o calidad.
• Se necesita una unidad de tamaño que se pueda computar a partir de los requerimientos:
¿Tamaño de la SRS? => dependen mucho del autor

Punto función
•Es una métrica como las LOC.
•Se determina sólo con la SRS.
•Define el tamaño en términos de la “funcionalidad”.
Tipo de funciones:
Entradas externas
Salidas externas
Archivos lógicos internos
Archivos de interfaz externa
Transacciones externas

Tipo de salida
que deja el
sistema

Tipo de entrada (dato/
control) externa a la
aplicación



Input/output
inmediatos
(queries)

Archivos pasados/
compartidos entre
aplicaciones

Grupo lógico de dato/
control de información
generado/usado/
manipulado

![[Pasted image 20230823200928.png]]

Contar cada tipo de función diferenciando según sea compleja, promedio o simple.
• Cij denota la cantidad de funciones tipo “i” con complejidad “j”.
• Punto función no ajustado (UFP):

![[Pasted image 20230823200949.png]]



Ajustar el UFP de acuerdo a la complejidad del entorno.
Se evalúa según las siguientes características:
1. comunicación de datos
2. procesamiento distribuido
3. objetivos de desempeño
4. carga en la configuración de operación
5. tasa de transacción
6. ingreso de datos online
7. eficiencia del usuario final
8. actualización online
9. complejidad del procesamiento lógico
10. reusabilidad
11. facilidad para la instalación
12. facilidad para la operación
13. múltiples sitios
14. intención de facilitar cambios
• Factor de ajuste de complejidad (CAF):
• Puntos función = CAF * UFP

1 punto función =
• 125 LOC en C
• 50 LOC en C++ o
Java

Cada uno de estos ítems debe
evaluarse como:   categoria -- pi
no presente 0
influencia insignificante 1
influencia moderada 2
influencia promedio 3
influencia significativa 4
influencia fuerte 5

![[Pasted image 20230823201121.png]]


Métricas de calidad
La calidad de la SRS tiene impacto directo en los costos del proyecto.
=> se necesitan buenas métricas de calidad para evaluar la calidad de la SRS.
• Métricas de calidad directa: evalúan la calidad del documento estimando el
valor de los atributos de calidad de la SRS.
• Métricas de calidad indirecta: evalúan la efectividad de las métricas del
control de calidad usadas en el proceso en la fase de requerimientos.
Ej.: Número de errores encontrados.
Frecuencia de cambios de requerimientos. Importantísimo:
El proceso debe estar
bajo control
estadístico