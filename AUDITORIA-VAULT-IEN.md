# Auditoría del vault IEN y comparación de agentes

Fecha de revisión: 2026-09-25.

## Conclusión

El agente nuevo es una base más confiable para preparar parciales y finales porque separa alcance, contenido y evidencia; usa ocho responsabilidades con dependencias; audita el borrador contra fuentes originales y evita prometer cobertura no comprobada. El agente anterior aporta una interfaz de uso diario mucho mejor adaptada a IEN: comandos naturales, materias, tags, plantillas, Dataview, investigación, crítica y seguimiento.

La solución adoptada es conservar el núcleo nuevo e incorporar las capacidades útiles del anterior como skills específicas. No se conservaron como obligaciones universales reglas como “dos ejemplos por concepto”, “un diagrama en cada nota”, “tres fuentes por claim” o puntajes de calidad generados por el propio modelo, porque aumentan el volumen sin demostrar precisión ni aprendizaje.

## Estructura observada

- 9 materias activas, de `01-Desarrollo-Web` a `09-Desarrollo-Aplicaciones-Moviles`.
- 105 notas académicas Markdown no vacías revisadas estadísticamente.
- 97 notas tienen frontmatter y tags; 82 incluyen `materia`, `tipo` y `fecha`.
- Se detectaron 347 wikilinks, 816 callouts, 221 bloques Mermaid, 318 bloques de respuestas desplegables y 434 tareas.
- Las notas más grandes superan 40–60 KB. El sistema debe favorecer índices y notas temáticas cuando una nueva síntesis vuelva difícil la navegación.
- La estructura no es uniforme: varias materias usan `Clases/Resumenes/Examenes`; Fundamentos de Ingeniería 2 se organiza por unidades y parciales; Aplicaciones Móviles agrega defensa y repaso final.
- Las carpetas globales `Flashcards`, `Quizzes`, `Mapas`, `Diario` y `Analisis-Critico` están vacías o casi vacías. La práctica real se guarda mayormente dentro de cada materia.

## Fortalezas de las notas

- Buen uso de frontmatter, tags, callouts, tablas, código y Mermaid.
- Materiales orientados al examen, con respuestas orales, ejercicios y solucionarios.
- Las materias con mayor desarrollo tienen índices, resúmenes completos y modelos de examen.
- Los apuntes técnicos incluyen ejemplos aplicados y comparaciones útiles.

## Problemas y oportunidades

- Ocho notas académicas carecen de frontmatter; otras quince no tienen las propiedades `materia`, `tipo` o `fecha` completas.
- Hay convenciones de nombres y rutas distintas. Deben respetarse por materia antes de intentar una migración global.
- El índice raíz y los dashboards quedaron desactualizados: el índice enumera hasta la materia 08 y el calendario principal conserva mayo de 2026.
- La documentación anterior describía un agente de seis skills; la migración actual dejó `AGENTS.md` y `.agents/skills` como única configuración activa de Codex.
- Algunas notas son monolíticas y mezclan resumen, práctica, flashcards y plan; conviene separar artefactos cuando eso facilite recuperar información sin mirar soluciones.
- La carpeta `03-Probabilidad-y-Estadistica` tiene cobertura muy escasa frente a otras materias.
- La calidad visual es alta, pero la presencia de muchos diagramas y callouts no demuestra por sí sola cobertura o corrección. El nuevo auditor prioriza evidencia y trazabilidad.

## Integración realizada

- Se añadió una política de escritura específica para IEN.
- Se incorporaron pensamiento crítico, investigación académica y seguimiento como skills mantenibles.
- El orquestador reconoce los comandos y frases naturales del agente anterior.
- Métodos de estudio ahora incluyen Pomodoro, Flowtime, Feynman, Cornell, SQ3R, blurting, recuperación activa, interleaving y práctica distribuida, seleccionados según la tarea.
- El flujo conserva mapas Mermaid/Canvas, Obsidian Markdown, Bases, Dataview y plantillas, pero evita imponerlos cuando no aportan.
- La auditoría ya no usa puntajes autoestimados: informa hallazgos verificables y pendientes.
- Se retiraron la carpeta y los archivos de configuración del sistema anterior. El vault queda operativo exclusivamente mediante Codex.
