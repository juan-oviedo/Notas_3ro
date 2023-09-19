• Dos tipos de componentes: clientes y servidores.
• Los clientes sólo se comunican con el servidor, pero no con otros clientes.
• La comunicación siempre es iniciada por el cliente quien le envía una solicitud al servidor y espera una respuesta de éste => la comunicación es usualmente asincrónica.
• Solo un tipo de conector: solicitud/respuesta (request/reply) - es asimétrico.
• Usualmente el cliente y el servidor residen en distintas máquinas.

Este estilo tiene en general la forma de una estructura multi-nivel.
El servidor también actúa como cliente.
Ej. clásico => 3 niveles:
	• Nivel de cliente: contiene a los clientes.
	• Nivel intermedio: contiene las reglas del servicio.
	• Nivel de base de datos: reside la información.