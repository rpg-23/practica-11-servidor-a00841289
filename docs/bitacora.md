Ejercicio 0
1.- Cada prueba registra a sus personas con un sufijo al azar (ana.f07ea4b1). ¿Qué pasaría si todas usaran ana?
Después de la primera 'ana', todas las demás pruebas fallarían porque ya existe un registro 'ana'.

2.- Las pruebas corren contra el PostgreSQL de verdad, no contra una base falsa. ¿Qué se gana? ¿Qué se pierde?
Se gana que se prueba la respuesta verdadera del servidor.

Ejercicio B4
Las cuatro pruebas mandan los envíos uno después del otro. ¿Qué parte de crear no ejecuta ninguna? ¿Cómo escribirías una prueba que sí la ejecute?
No se ejecuta la parte que corre cuando dos avisos duplicados se envían al mismo tiempo. Habría que hacer una prueba con threads distintos que puedan enviar la petición en el mismo momento.

Ejercicio D2
Escojan tres requisitos de su backlog: uno de seguridad, uno funcional y uno que hoy no puedan demostrar. Escriban su fila completa, con el estado honesto.

ID: SEG-01
Requisito: Una familia solo puede modificar sus propias inscripciones.
Criterio de aceptación: Dada una familia con sesión, cuando intenta modificar la inscripción de otra familia, entonces el servidor rechaza la operación y los datos de la inscripción permanecen iguales.
Resultado: Sin probar.
Estado: Pendiente: falta demostrar el rechazo y comprobar que la inscripción no se modifica.
Prueba o evidencia: Ninguna todavía.
ID: HU-01
Requisito: Al liberarse un lugar, se asigna a la primera familia de la lista de espera.
Criterio de aceptación: Dada una actividad con cupo lleno y dos familias en espera, cuando se libera un lugar, entonces la primera familia según el orden establecido queda inscrita, la segunda permanece en espera y no se supera el cupo.
Resultado: Sin evidencia revisada.
Estado: Pendiente de demostrar: la funcionalidad se implementó, pero falta incorporar evidencia que compruebe el criterio completo.
Prueba o evidencia: Pendiente de incorporar la prueba o el registro de comprobación manual.
ID: RNF-01
Requisito: Las solicitudes simultáneas no exceden el cupo de una actividad.
Criterio de aceptación: Dada una actividad con un solo lugar disponible, cuando dos familias solicitan inscribirse simultáneamente, entonces exactamente una obtiene el lugar, la otra recibe el resultado definido para cupo lleno y el total de inscritos no supera la capacidad.
Resultado: Sin probar.
Estado: Pendiente: las pruebas con solicitudes sucesivas no demuestran el comportamiento ante solicitudes simultáneas.
Prueba o evidencia: Ninguna todavía.