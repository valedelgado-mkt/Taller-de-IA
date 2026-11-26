# Plantilla de proyecto — Taller de herramientas de IA para marketing digital

Una plantilla simple para construir herramientas con IA sin saber programar. Ordena el trabajo en tres documentos: **qué** vas a construir (brief), **cómo** tiene que trabajar el agente de IA (AGENTS.md) y **en qué orden** (ROADMAP.md).

La idea central: el agente lee la documentación antes de tocar nada. Si los documentos están vacíos, te ayuda a completarlos primero. Si están completos, arranca con todo el contexto cargado.

## Cómo empezar

1. Hacé clic en **Use this template** → **Create a new repository** y ponele el nombre de tu herramienta.
2. Completá `docs/brief.md`. Si te trabás, usá el prompt de `prompts/completar-brief.md` para que la IA te entreviste.
3. Generá tu `AGENTS.md` a partir del brief con el prompt de `prompts/generar-agents.md`.
4. Armá tu `ROADMAP.md` con las funciones del brief: qué va ahora, después y más adelante.
5. Copiá `.env.example` como `.env` y completá tus claves. `.env` nunca se sube a GitHub.
6. Empezá a construir de a una función por vez.

## Qué hay adentro

```
mi-herramienta/
├── AGENTS.md          # Instrucciones para el agente de IA: qué leer, stack, reglas, qué no tocar
├── CLAUDE.md          # Importa AGENTS.md (para quien usa Claude Code)
├── ROADMAP.md         # Qué va ahora, después y más adelante; se actualiza en cada sesión
├── README.md          # Este archivo; reemplazalo por la descripción de tu herramienta
├── changelog.md       # Qué cambió y por qué, una línea por cambio
├── .env.example       # Nombres de las claves, nunca los valores
├── .gitignore         # Archivos que no se suben (incluido .env)
├── docs/
│   ├── brief.md       # Qué problema resolvemos, para quién y qué tiene que hacer la herramienta
│   ├── interfaz.md    # Recorrido del usuario, pantallas y link a la maqueta
│   ├── fuentes.md     # De dónde salen los datos
│   └── prompts.md     # Prompts del paso con IA, con sus versiones
├── prompts/           # Prompts recomendados para trabajar con la IA
├── workflows/         # Flujos de n8n exportados en JSON (sin credenciales)
└── ejercicios/        # Lo que hagas en las clases del taller
```

## Cómo se trabaja

1. **Cada sesión empieza leyendo los documentos.** El agente lee el brief, el roadmap y el changelog antes de cambiar algo.
2. **Primero el plan, después el cambio.** El agente propone qué va a hacer y espera tu OK.
3. **Una función por vez.** Se construye, se prueba y recién después se pasa a la siguiente.
4. **Terminado es probado.** Una función está lista cuando cumple su criterio de aceptación del brief, con datos reales.
5. **Los documentos se actualizan en la misma sesión.** Si algo cambia, se anota en `ROADMAP.md` y `changelog.md`.
6. **Las ideas nuevas van al roadmap, no al código.** Lo que no entra ahora queda en "Más adelante".
7. **Las claves nunca se escriben en el código.** Van en `.env`, que no se sube.

## Brief, AGENTS.md y ROADMAP.md

| | Brief | AGENTS.md | ROADMAP.md |
| --- | --- | --- | --- |
| Responde | Qué y por qué | Cómo trabajar | En qué orden |
| Lo lee | Personas y el agente | El agente | Personas y el agente |
| Cambia | Cuando cambia el problema o el alcance | Cuando aparece una regla nueva | En cada sesión |

## Créditos

Versión simplificada e inspirada en [project-template](https://github.com/polmarza/project-template) de Pol Marzà, adaptada para el Taller de herramientas de IA para marketing digital de la Escuela Da Vinci. Sin tests automáticos, CI ni gestor de paquetes: lo justo para que alguien que no programa trabaje ordenado con un agente.

## Licencia

MIT © 2026 Flor Estévez. Podés usarla, adaptarla y compartirla libremente.
