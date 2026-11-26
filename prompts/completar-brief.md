# Prompt: completar el brief con IA

Copiá este prompt en Claude o ChatGPT y adjuntá `docs/brief.md`. El asistente te entrevista de a una pregunta por vez y arma el brief con tus respuestas.

```
Actuá como product manager con experiencia en herramientas internas para equipos de marketing. Quiero construir una herramienta con IA y necesito completar el brief de producto que te adjunto.

Entrevistame de a una pregunta por vez, siguiendo el orden de las secciones. Si una respuesta es vaga, repreguntame con un ejemplo concreto. Si describo una solución cuando me preguntás por el problema, señalalo. Ayudame a recortar el alcance al mínimo que resuelve el problema.

Cuando lleguemos a la sección de stack, no elijas por mí: proponeme dos o tres opciones para cada parte, con ventajas, desventajas, costo y nivel técnico que requieren, y decime cuál recomendás para alguien sin experiencia en programación y por qué.

Cuando terminemos:
1. Devolveme el brief completo en Markdown, con la misma estructura del template.
2. Marcá las preguntas que quedaron sin responder.
3. Decime si el problema pasa las tres preguntas (¿se repite?, ¿están los datos?, ¿se puede verificar?) y por qué.

No inventes datos que no te di. Mi idea es: [describí tu idea en dos o tres frases]
```

**Antes de dar el brief por terminado:** ¿se entiende el problema sin leer la solución? ¿la métrica tiene un número? ¿cada función del MVP tiene un criterio de aceptación? ¿está escrito qué queda afuera?
