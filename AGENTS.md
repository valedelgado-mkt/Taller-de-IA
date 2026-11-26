# AGENTS.md — [Nombre de la herramienta]

<!--
Instrucciones para el agente de IA. Reemplazá lo que está entre corchetes.
Podés generarlo a partir del brief con el prompt de prompts/generar-agents.md.
Mantenelo corto: instrucciones, no explicaciones. Nunca pongas claves ni datos personales.
-->

## Qué es este proyecto
[Una o dos frases. Ej.: CRM simple para una agencia: junta los contactos del formulario web en una planilla, los clasifica con IA y sugiere el próximo paso.]

Quien te pide cambios no programa: explicá cada paso en lenguaje simple y en español.

## Antes de empezar cada sesión
1. Leé `docs/brief.md` (qué hace la herramienta y para quién).
2. Leé `ROADMAP.md` (qué se está haciendo ahora).
3. Leé las últimas entradas de `changelog.md`.

Si `docs/brief.md` está vacío o incompleto, no construyas nada: ayudame a completarlo primero.
Si algo de lo que te pido contradice estos documentos, avisame antes de hacerlo.

## Stack
- Interfaz: [Ej.: Lovable]
- Automatización: [Ej.: n8n, corriendo en Docker en localhost:5678]
- IA: [Ej.: API de Claude]
- Datos: [Ej.: Google Sheets]
- Publicación: [Ej.: publicación de Lovable]

No agregues herramientas, librerías ni servicios nuevos sin preguntarme.

## Estructura del proyecto
- `docs/` — brief, interfaz, fuentes de datos y prompts
- `prompts/` — prompts recomendados para trabajar con IA
- `workflows/` — flujos de n8n exportados en JSON
- `ejercicios/` — prácticas del taller
- `ROADMAP.md` — qué va ahora, después y más adelante
- `changelog.md` — qué cambió y por qué

## Cómo trabajamos
- Antes de cambiar algo, contame tu plan en pocos pasos y esperá mi OK.
- Un cambio por vez. Después de cada cambio, decime cómo probarlo.
- Si algo falla, explicá la causa probable antes de intentar arreglarlo.
- Al terminar una tarea, actualizá `ROADMAP.md` y sumá una línea a `changelog.md`.
- Si surge una idea fuera de lo que estamos haciendo, anotala en `ROADMAP.md` en "Más adelante" y no la implementes.

## Cómo probar
- Una función está terminada cuando cumple su criterio de aceptación de `docs/brief.md`.
- Probá con datos de ejemplo antes de usar datos reales.
- Mostrame la evidencia (lo que se ve en pantalla, la fila creada, la respuesta del flujo), no solo "listo".

## Seguridad y datos
- Nunca escribas claves, tokens ni contraseñas en el código, en un prompt ni en un archivo que se suba a GitHub. Van en `.env`.
- `.env` está en `.gitignore` y no se sube nunca. Si necesitás una variable nueva, agregala con un valor vacío a `.env.example`.
- Antes de exportar un flujo de n8n a `workflows/`, verificá que no incluya credenciales.
- No uses datos personales reales en pruebas.
- Pedime confirmación antes de borrar archivos, datos o flujos.

## Qué no hacer
- [Copiá acá lo que el brief deja fuera de alcance. Ej.: no enviar mails automáticamente; siempre los revisa una persona.]
- [Ej.: no cambiar la estructura de la planilla sin avisar: hay columnas que usa el flujo.]

## Comandos y accesos útiles
- Abrir n8n: http://localhost:5678
- [Ej.: dónde está la planilla, cómo exportar un flujo, cómo publicar]
