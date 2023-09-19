Un sistema es una jerarquía de componentes.
• Dos enfoques para diseñar tal jerarquía:
• Top-down:
	• comienza en la componente de más alto nivel (la más abstracta);
	• prosigue construyendo las componentes de niveles más bajos descendiendo
	en la jerarquía.
• Bottom-up:
	• comienza por las componentes de más bajo nivel en la jerarquía (las más
	simples)
	• prosigue hacia los niveles más altos hasta construir la componente más alta.

Enfoque top-down:
	• El diseño comienza con la especificación del sistema.
	• Define el módulo que implementará la especificación.
	• Especifica los módulos subordinados.
	• Luego, iterativamente, trata cada uno de estos módulos especificados cómo el nuevo problema.
	• El refinamiento procede hasta alcanzar un nivel donde el diseño pueda ser implementado directamente.
pros:
	• En cada paso existe una clara imagen del diseño.
	• Enfoque más natural para manipular problemas complejos.
	• La mayoría de las metodologías de diseño se basan en este enfoque.
contra:
	• La factibilidad es desconocida hasta el final.
	• Top-down o bottom-up puros no son prácticos.
• En general se utiliza una combinación de ambos.