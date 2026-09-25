# Superagente de estudio para el vault IEN

Sistema multiagente para preparar clases, parciales, finales y materias libres a partir del programa, bibliografía, apuntes, exámenes previos y transcripciones. Combina el control de alcance y evidencia del agente nuevo con los comandos, métodos, seguimiento y convenciones de Obsidian del agente anterior de IEN.

## Cómo está organizado

- [`AGENTS.md`](AGENTS.md): instrucciones del orquestador, lenguaje natural y contratos de ocho subagentes.
- [`ARQUITECTURA-AGENTE-ESTUDIO.md`](ARQUITECTURA-AGENTE-ESTUDIO.md): diseño completo, dependencias entre roles, herramientas y criterios de aceptación.
- [`AUDITORIA-VAULT-IEN.md`](AUDITORIA-VAULT-IEN.md): comparación de ambos agentes y análisis cuantitativo de la estructura real del vault.
- [`.agents/skills/`](.agents/skills/): skills para resúmenes, métodos, mapas, investigación, pensamiento crítico, seguimiento y escritura segura en IEN.
- [`skills-lock.json`](skills-lock.json): origen y versión de las skills instaladas mediante Skills CLI.

El vault conserva además sus carpetas por materia, `Plantillas`, `Dashboard`, `Diario`, `Mapas`, `Quizzes` y los plugins de Obsidian ya configurados. La estructura de cada materia se respeta tal como existe; el agente no fuerza una migración global.

## Uso

La instalación activa vive en `C:\Users\Bruno\Desktop\IEN`. Abrí ese vault como proyecto en Codex y pedí la tarea en lenguaje natural, por ejemplo: “preparame el segundo parcial de Testing”, “hoy cursé Base de Datos 2” o “haceme un repaso de Aplicaciones Móviles”. El agente inspeccionará primero la estructura y las notas existentes de la materia.

No se utiliza OpenCode. La configuración activa es:

```text
IEN/
├── AGENTS.md
├── .agents/skills/
├── ARQUITECTURA-AGENTE-ESTUDIO.md
├── AUDITORIA-VAULT-IEN.md
└── skills-lock.json
```

Las skills establecen procedimientos y formatos. La ejecución multiagente depende de que el entorno permita crear subagentes con encargos separados. Si no está disponible, el orquestador conserva las etapas y controles sin simular agentes inexistentes.

## Capacidades incorporadas

- Resúmenes con matriz de alcance y cobertura verificable.
- Investigación académica y análisis crítico diferenciados de la voz de la cátedra.
- Recuperación activa, práctica distribuida, Feynman, Cornell, SQ3R, blurting, interleaving, Pomodoro y Flowtime.
- Quizzes, flashcards, simulacros, mapas Mermaid/Canvas, MOC y práctica con respuestas separadas.
- Diario, registro de errores, próximos repasos y dashboards basados en datos observados.
- Política específica para las nueve materias y las estructuras heterogéneas del vault IEN.

## Skills de terceros

`find-skills` procede de [vercel-labs/skills](https://github.com/vercel-labs/skills). `obsidian-markdown`, `json-canvas` y `obsidian-bases` proceden de [kepano/obsidian-skills](https://github.com/kepano/obsidian-skills). Sus licencias MIT se conservan en [`third_party/`](third_party/). `skill-creator` conserva su propio `license.txt` dentro de su carpeta.
