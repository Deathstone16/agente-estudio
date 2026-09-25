---
name: escritura-vault-ien
description: Crear o actualizar notas académicas dentro del vault Obsidian IEN respetando su estructura real, frontmatter, tags, wikilinks, plantillas y contenido existente. Usar antes de cualquier escritura en C:\Users\Bruno\Desktop\IEN; no usar para vaults ajenos.
---

# Escritura en el vault IEN

El vault está en `C:\Users\Bruno\Desktop\IEN`. Esta skill define dónde y cómo escribir; las skills académicas determinan el contenido.

## Antes de escribir

1. Identificá la materia por su carpeta real. Actualmente existen `01-Desarrollo-Web` a `09-Desarrollo-Aplicaciones-Moviles`.
2. Inspeccioná `Índice-Materia.md`, las notas recientes del mismo tipo y las carpetas de la materia. No supongas que todas usan la misma estructura.
3. Buscá una nota que ya cumpla el objetivo. Actualizala cuando sea más claro que crear un duplicado.
4. Preservá texto personal, respuestas, marcas y convenciones locales. Para una reescritura amplia, prepará primero una versión separada o un diff revisable.
5. Verificá el estado Git. No mezcles archivos ajenos ni modifiques `.obsidian`, `.git`, `.opencode` o carpetas de herramientas salvo que la tarea lo requiera.

## Ubicación

- En materias `01` a `05`, `07` y `08`, preferí sus carpetas existentes `Clases`, `Resumenes`, `Examenes`, `Docs` o `Trabajos-Practicos`.
- En `06-Fundamentos-Ingenieria-2`, respetá la organización por `Unidad-*` y `Parcial-*` observada.
- En `09-Desarrollo-Aplicaciones-Moviles`, respetá `Clases`, `Resumenes`, `Examenes`, `Defensa_*` y `Repaso Final` según el propósito.
- Las carpetas globales `Flashcards`, `Quizzes`, `Mapas`, `Diario` y `Analisis-Critico` están disponibles, pero no son la convención dominante. Usalas solo cuando el usuario pida un recurso global o cuando el índice existente ya apunte allí.
- No crees una jerarquía nueva para uniformar el vault durante una tarea académica normal.

## Nombre y frontmatter

Usá nombres descriptivos consistentes con la carpeta. Conservá los nombres existentes al actualizar. Para notas nuevas fechadas, preferí `YYYY-MM-DD-Titulo.md`; para materiales estables por unidad o parcial, seguí el patrón local.

Frontmatter mínimo para una nota académica nueva:

```yaml
---
materia: "09-Desarrollo-Aplicaciones-Moviles"
tipo: resumen
fecha: YYYY-MM-DD
unidad: ""
tags:
  - estado/en-progreso
  - tipo/resumen
  - tema/desarrollo-aplicaciones-moviles
---
```

- `materia` debe coincidir con la carpeta.
- `tipo` y `tipo/...` deben describir el mismo artefacto.
- Usá `estado/en-progreso`, `estado/completado` o `estado/para-revisar` según evidencia real. No marques como completado un borrador con fuentes faltantes.
- Agregá `unidad/...` y `concepto/...` solo cuando tengan un valor concreto. No dejes tags vacíos.
- `subagente` es opcional; no hace falta atribuir cada nota al sistema.
- Para seguimiento pueden agregarse `parcial`, `estado_estudio`, `proximo_repaso`, `ultimo_repaso` y `resultado_repaso`.

## Estilo y enlaces

- Escribí en español y conservá términos técnicos en inglés cuando correspondan.
- Usá callouts para información que realmente necesita énfasis; no conviertas cada párrafo en un bloque visual.
- Creá wikilinks únicamente a archivos existentes o a notas que se creen en la misma operación.
- Preferí rutas explícitas en wikilinks cuando haya nombres duplicados.
- Mermaid, Canvas, tablas y código deben ayudar a explicar o practicar. Verificá sintaxis y relaciones antes de publicar.
- Las respuestas de quizzes, simulacros y actividades deben quedar separadas u ocultas para permitir recuperación activa.
- Cuando una nota supere una longitud difícil de navegar, proponé dividirla en notas temáticas enlazadas desde un índice o MOC.

## Índices, dashboards y plugins

El vault usa Dataview, Templater, Excalidraw, Kanban, Calendar, Obsidian Git, PDF++ y otros plugins. No dependas de un plugin cuando Markdown común resuelva el objetivo.

- Actualizá `Índice-Materia.md` al crear un artefacto central si el índice mantiene enlaces manuales.
- No inventes estadísticas, metas, fechas o estados para dashboards.
- Verificá que las consultas Dataview usen propiedades presentes en las notas.
- No reescribas calendarios históricos como si fueran actuales; generá una sección o nota correspondiente al período vigente.

## Entrega segura

Después de escribir, informá archivos creados y modificados, pendientes y cualquier nota que no se tocó por ambigüedad. No hagas commit ni push salvo pedido del usuario. La documentación Git del vault está en `GIT-WORKFLOW.md` cuando la instalación Codex está activa.
