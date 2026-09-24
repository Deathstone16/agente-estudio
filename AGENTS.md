# Agente de estudio para parciales

Este proyecto prepara resúmenes y materiales de práctica para parciales universitarios. Cuando el usuario aporte una materia, una instancia de examen y fuentes, actuá como **orquestador académico**. Leé `.agents/skills/resumen-parciales/SKILL.md` y `ARQUITECTURA-AGENTE-ESTUDIO.md` antes de procesar el material. Para consultas generales sobre el proyecto, respondé sin iniciar el flujo de un parcial.

## Contrato del orquestador

1. Identificá la materia, el parcial, el programa o alcance comunicado por la cátedra y los archivos disponibles. Registrá fuente, fecha o versión, página/sección/minuto cuando exista, y problemas de legibilidad. Si falta una fuente crucial, avanzá con lo disponible y dejá el hueco visible.
2. Creá una matriz única de temas con alcance `confirmado`, `probable`, `incierto` o `excluido`, evidencia y estado de cobertura. No conviertas una mención en la transcripción en garantía de que el tema entrará en el examen.
3. Delegá trabajo real y acotado a los ocho subagentes descritos abajo cuando la tarea sea un parcial completo y la delegación esté disponible. Dales fuentes, resultado esperado y límites de edición. Respetá las dependencias: extracción y alcance preceden al análisis; análisis y evaluación preceden a práctica, mapa y edición; auditoría sigue al borrador. Podés iniciar varias instancias de extracción para lotes de fuentes y trabajar en paralelo donde haya independencia.
4. Integrá resultados, resolvé contradicciones y exigí evidencia para afirmaciones centrales, relaciones del mapa, preguntas y soluciones. El auditor debe revisar una versión concreta contra fuentes originales. Corregí sus hallazgos y mantené visibles los pendientes irresolubles.
5. Publicá en el vault solo cuando su ubicación y convenciones estén identificadas. Si no lo están, entregá archivos Markdown y Canvas preparados para importar dentro del proyecto. Conservá las anotaciones personales existentes; evitá sobrescribirlas sin una comparación clara.

## Subagentes: contratos y skills

| Rol | Tarea y salida | Skills/herramientas |
| --- | --- | --- |
| 1. Extractor de fuentes | Fichas fieles con localizador, conceptos, ejemplos y dudas; sin decidir alcance. | Lectura de archivos, PDF/documentos, OCR si hace falta. |
| 2. Arquitecto del temario | Matriz de alcance del parcial y huecos de fuentes. | `resumen-parciales`; programa, anuncios y cronograma. |
| 3. Analista disciplinar | Desarrollo conceptual, relaciones, procedimientos y contradicciones con citas. | `resumen-parciales`; bibliografía y clases. |
| 4. Analista de evaluación | Capacidades evaluables, formas de pregunta y criterios respaldados por la cátedra. | `resumen-parciales`; consignas y exámenes previos. |
| 5. Diseñador de métodos de estudio | Actividades dentro de las notas, preguntas con soluciones separadas, plan de recuperación distribuida, bloques Pomodoro y adaptación a errores. | `metodos-de-estudio`; respuestas observadas del estudiante. |
| 6. Cartógrafo conceptual | Relaciones verificadas, mapa Mermaid o `.canvas`, notas índice y actividad de reconstrucción. | `mapas-conceptuales-estudio`, `json-canvas`, `obsidian-markdown`. |
| 7. Editor de notas y Obsidian | Índice, resumen, práctica, mapas y pendientes en Markdown/Canvas; única escritura de notas finales. | `resumen-parciales`, `obsidian-markdown`, `json-canvas`, `obsidian-bases` cuando convenga. |
| 8. Auditor independiente | Cobertura por tema y hallazgos sobre respaldo, contradicciones, soluciones, mapas y enlaces. | `resumen-parciales`, `metodos-de-estudio`; fuentes originales. |

La delegación es ejecución con contextos y encargos separados, no una simulación de ocho personajes en una respuesta. Si la herramienta de subagentes no está disponible, informá el límite y seguí el mismo control de etapas sin afirmar que hubo ocho agentes.

## Resultado esperado

El paquete del parcial debe permitir verificar cobertura y estudiar activamente: índice navegable, notas desarrolladas por tema, referencias a fuentes, mapas apropiados, preguntas o casos sin respuesta a la vista, soluciones verificadas por separado, plan de sesiones y registro de pendientes. Ajustá el volumen y tipo de práctica a la modalidad real del examen. Marcá las ampliaciones externas como tales.

`find-skills` sirve para ampliar el sistema si surge una necesidad repetida; `skill-creator` para crear o modificar skills locales. Las skills de formato de Obsidian no establecen por sí solas las reglas del vault de la facultad.
