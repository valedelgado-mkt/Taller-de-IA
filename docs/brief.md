# Brief de producto — [Nombre de la herramienta]

<!--
Completalo antes de construir. Frases cortas alcanzan: el objetivo es pensar, no escribir lindo.
Si te trabás, usá prompts/completar-brief.md para que la IA te entreviste.
Los ejemplos (Ej.) son de un CRM simple para una agencia: reemplazalos por tu caso.
-->

## Ficha rápida

| Campo | Completar |
| --- | --- |
| Nombre de la herramienta | |
| Autor/a | |
| Fecha | |
| Versión del brief | 0.1 |
| Resumen en una frase | Ej.: un CRM que junta los contactos de la web en una planilla y sugiere el próximo paso con cada uno. |

## 1. Problema

Describí qué pasa hoy, no la solución. Si aparece el nombre de una herramienta, todavía estás describiendo la solución.

| Pregunta | Respuesta |
| --- | --- |
| ¿Qué pasa hoy? | Ej.: los contactos llegan por formulario, mail y WhatsApp, y se pierden. |
| ¿A quién le pasa? | Ej.: al equipo comercial de una agencia de 5 personas. |
| ¿Cada cuánto? | Ej.: entre 10 y 20 contactos por semana. |
| ¿Cuánto cuesta hoy? | Ej.: 3 horas por semana ordenando datos y al menos un cliente perdido por mes. |
| ¿Cómo se resuelve hoy? | Ej.: una planilla que cada uno completa a mano, cuando se acuerda. |

**Las tres preguntas antes de construir.** Si alguna da "no", conviene elegir otro problema o achicarlo.

- [ ] **¿Se repite?** Es una tarea frecuente que se hace siempre de la misma forma.
- [ ] **¿Están los datos?** La información existe, es accesible y está más o menos ordenada.
- [ ] **¿Se puede verificar?** Hay una forma rápida de saber si el resultado está bien.

## 2. Usuario

| Pregunta | Respuesta |
| --- | --- |
| ¿Quién la va a usar? | Ej.: la persona que atiende los contactos nuevos. |
| ¿En qué momento y desde dónde? | Ej.: a primera hora, desde la compu de la oficina. |
| ¿Qué sabe hacer? | Ej.: usa Sheets todos los días; no programa. |
| ¿Qué decisión la ayuda a tomar? | Ej.: a quién llamar primero y qué decirle. |

## 3. Objetivo y métrica de éxito

Una sola frase con un número. Sin métrica no hay forma de saber si la herramienta funciona.

- **Objetivo:** Ej.: que ningún contacto quede sin respuesta más de 24 horas.
- **Cómo lo medimos:** Ej.: tiempo entre que llega el contacto y el primer seguimiento.
- **Hoy:** Ej.: entre 2 y 5 días. **Meta:** Ej.: menos de 24 horas.

## 4. Qué hace la herramienta

Funciones como historias de usuario: *como [usuario], quiero [acción], para [beneficio]*. Cada una con un criterio de aceptación: la prueba concreta de que está lista. El MVP es solo lo imprescindible.

| # | Historia de usuario | Criterio de aceptación | Prioridad |
| --- | --- | --- | --- |
| F1 | Ej.: Como comercial, quiero cargar un contacto desde un formulario, para no copiarlo a mano. | Al enviar el formulario aparece una fila nueva en la planilla con nombre, mail, empresa y mensaje. | MVP |
| F2 | Ej.: Como comercial, quiero que cada contacto llegue clasificado, para saber a quién llamar primero. | Cada fila trae prioridad (alta, media o baja) e intención; en 10 casos de prueba coincide con mi criterio al menos 8 veces. | MVP |
| F3 | Ej.: Como comercial, quiero un borrador del primer mail, para responder más rápido. | Cada contacto trae un borrador de hasta 120 palabras en el tono de la agencia. | Después |
| F4 | | | |

## 5. Recorrido del usuario

Los pasos en orden, escritos a mano. Si no se pueden escribir, todavía no se pueden construir.

1. Ej.: el contacto completa el formulario en la web.
2. Ej.: la herramienta guarda los datos y los clasifica con IA.
3. Ej.: la comercial abre la planilla y ve los contactos ordenados por prioridad.
4. Ej.: abre el borrador sugerido, lo ajusta y lo envía.

## 6. Fuera de alcance

Lo que la herramienta **no** va a hacer en esta versión. Pasa directo a "Qué no hacer" en `AGENTS.md`.

- Ej.: no envía mails automáticamente; siempre los revisa una persona.
- Ej.: no se conecta con WhatsApp en la primera versión.

## 7. Datos

| Pregunta | Respuesta |
| --- | --- |
| ¿Qué entra? | Ej.: nombre, mail, empresa y mensaje de cada contacto. |
| ¿De dónde sale? | Ej.: formulario de la web. |
| ¿En qué formato? | Ej.: campos de texto; llega como JSON. |
| ¿Qué sale? | Ej.: una fila por contacto con prioridad, intención y borrador. |
| ¿Dónde se guarda? | Ej.: una planilla de Google Sheets. |
| ¿Hay datos personales o sensibles? | Ej.: sí, mails y teléfonos: no se pegan en prompts de prueba. |

## 8. El paso con IA

| Pregunta | Respuesta |
| --- | --- |
| ¿Qué tarea hace la IA? | Ej.: clasifica cada contacto y redacta un primer mail. |
| ¿Qué recibe? | Ej.: el mensaje del contacto y una guía de tono de la agencia. |
| ¿Qué devuelve y en qué formato? | Ej.: JSON con prioridad, intención y borrador. |
| ¿Cómo se verifica? | Ej.: una persona revisa cada borrador; 10 casos de prueba con respuesta conocida. |
| ¿Cuánto cuesta cada uso? | Ej.: estimar con 10 corridas de prueba y poner un límite de gasto. |

## 9. Stack y herramientas

Se completa en diálogo con la IA: a partir del brief, el asistente propone opciones con ventajas y desventajas, y vos elegís. Las de la tabla son muy usadas, pero no las únicas. Una vez elegido, copialo en `AGENTS.md`.

| Parte | Qué resuelve | Herramienta elegida | Otras opciones frecuentes |
| --- | --- | --- | --- |
| Interfaz | Lo que ve y usa la persona | Ej.: Lovable | Claude Design (maqueta), Bolt, Replit, HTML y CSS |
| Automatización | Los pasos que corren solos | Ej.: n8n | Apps Script, Make, Zapier |
| IA | Leer, clasificar, escribir | Ej.: API de Claude | API de OpenAI |
| Datos | Dónde se guarda la información | Ej.: Google Sheets | Supabase, Airtable |
| Publicación | Dónde vive y cómo se comparte | Ej.: publicación de Lovable | Netlify, Streamlit |

## 10. Riesgos y supuestos

| Riesgo o supuesto | Qué pasa si ocurre | Cómo lo cuidamos |
| --- | --- | --- |
| Ej.: la IA clasifica mal un contacto importante. | Se responde tarde. | Revisión humana diaria de los contactos marcados como "baja". |
| Ej.: la API no responde. | El contacto queda sin clasificar. | Se guarda igual, con la marca "pendiente". |
| Ej.: se filtra la API key. | Alguien la usa a nuestro costo. | La clave vive en `.env`; límite de gasto activo. |

## 11. Roadmap inicial

Pasalo a `ROADMAP.md`.

| Ahora (MVP) | Después | Más adelante |
| --- | --- | --- |
| F1: formulario y planilla | F3: borrador de mail | Conexión con WhatsApp |
| F2: clasificación con IA | Recordatorio de seguimiento | Reporte semanal |

## 12. Preguntas abiertas

- [ ] Ej.: ¿quién revisa los contactos cuando la comercial está de vacaciones?
- [ ] Ej.: ¿cuántos contactos por mes hay que soportar?
