# Lab 4 WebSocket -- Project Report

## Description of Changes
Se añadió y habilitó el test `onChat` en `src/test/kotlin/websockets/ElizaServerTest.kt` para comprobar la funcionalidad de chat del servidor Eliza.

Cambios principales:
- Habilitación del test `onChat` (se eliminó `@Disabled` y se completó su implementación).
- Implementación de la lógica en el cliente de prueba para enviar el mensaje de prueba "I am feeling sad" cuando el servidor solicite información.
- Añadidos comentarios explicativos en el test para aclarar decisiones sobre condiciones de carrera y comprobaciones flexibles.

## Technical Decisions
- Decisiones de sincronización: los tests usan `CountDownLatch` para coordinar eventos asíncronos entre el cliente WebSocket y el hilo de pruebas.
- Cobertura de pruebas: se probaron tanto la apertura de la conexión (`onOpen`) como la interacción básica de chat (`onChat`) con mensajes reales enviados desde el cliente de prueba.
- Además se probó el correcto funcionamiento desde Postman.
## Learning Outcomes
- Practiqué la sincronización de hilos en pruebas asíncronas usando `CountDownLatch` y colecciones compartidas.
- Aprendí a diseñar aserciones robustas frente a respuestas no deterministas (usar contains / any / rangos en vez de assertEquals rígidos).

## AI Disclosure
### AI Tools Used
- GPT-5 mini.

### AI-Assisted Work
- Aproximadamente 10% del contenido fue generado con asistencia de AI y el resto (90%) fue cosecha propia. La he usado, como siempre, para mejorar la redacción.
### Original Work
- He hecho todo a mano poco a poco, han sido muy muy útiles los comentarios proporcionados por los profesores de la asignatura.
- He usado la IA para mejorar la redacción del informe, siempre escribo todo (así expreso mejor lo que quiero decir) y luego la IA me ayuda a pulir el texto.
