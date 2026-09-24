# Agente de estudio para parciales

Proyecto de instrucciones y skills para preparar resúmenes de parciales universitarios a partir del programa, bibliografía, apuntes y transcripciones de clase. El flujo controla la cobertura del temario, conserva referencias a las fuentes y agrega práctica de estudio y mapas para Obsidian.

## Cómo está organizado

- [`AGENTS.md`](AGENTS.md): instrucciones del orquestador y contratos de ocho subagentes.
- [`ARQUITECTURA-AGENTE-ESTUDIO.md`](ARQUITECTURA-AGENTE-ESTUDIO.md): diseño completo, dependencias entre roles, herramientas y criterios de aceptación.
- [`.agents/skills/`](.agents/skills/): skills locales e instaladas para resúmenes, métodos de estudio, mapas conceptuales y formatos de Obsidian.
- [`skills-lock.json`](skills-lock.json): origen y versión de las skills instaladas mediante Skills CLI.

## Uso

Abrí esta carpeta como proyecto en un entorno compatible con `AGENTS.md`, skills y delegación de subagentes. Indicá la materia y el parcial, y proporcioná el programa, las instrucciones de alcance, el material de estudio y las transcripciones disponibles. La ubicación y las convenciones de tu vault de Obsidian se definen antes de escribir allí; mientras tanto, los materiales pueden prepararse en este proyecto.

Las skills establecen procedimientos y formatos. La ejecución multiagente depende de que el entorno permita crear subagentes con encargos separados. Los archivos de este repositorio no incluyen aún un examen real ni materiales de una materia.

## Skills de terceros

`find-skills` procede de [vercel-labs/skills](https://github.com/vercel-labs/skills). `obsidian-markdown`, `json-canvas` y `obsidian-bases` proceden de [kepano/obsidian-skills](https://github.com/kepano/obsidian-skills). Sus licencias MIT se conservan en [`third_party/`](third_party/). `skill-creator` conserva su propio `license.txt` dentro de su carpeta.
