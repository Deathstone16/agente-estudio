---
name: mapas-conceptuales-estudio
description: Diseñar mapas conceptuales verificables para estudiar parciales y representarlos en Obsidian como Mermaid, JSON Canvas o notas índice. Usar cuando el temario exige relacionar conceptos, autores, procesos o causas, o el usuario pide mapas de estudio.
---

# Mapas conceptuales para estudiar

Un mapa útil representa relaciones que el estudiante debe poder explicar. Diseñalo a partir de la matriz del parcial y fuentes verificadas, junto con el analista disciplinar. No conviertas automáticamente cada título o palabra repetida en un nodo.

## Construcción

1. Definí la pregunta que el mapa ayuda a responder y el conjunto de temas incluidos en el parcial.
2. Elegí conceptos suficientes para representar la explicación sin saturar la vista. Agrupá cuando los detalles puedan quedar en notas enlazadas.
3. Etiquetá las conexiones con verbos o relaciones precisas: «causa», «requiere», «se diferencia de», «es ejemplo de», «ocurre antes de». Una flecha sin significado suele ser insuficiente.
4. Revisá cada relación contra las fuentes. Marcá disputas o incertidumbre en vez de dibujar una conexión falsa. Incluí referencias en notas enlazadas o leyenda si el mapa no permite citarlas cómodamente.
5. Pedí al estudiante reconstruir una parte del mapa o explicar sus enlaces sin mirar; aportá luego el mapa completo como retroalimentación.

## Forma en Obsidian

- **Mermaid en Markdown** para un diagrama compacto que acompaña una explicación. Usá `obsidian-markdown` para la sintaxis y comprobá que el diagrama se represente.
- **JSON Canvas `.canvas`** para un mapa amplio, editable y navegable entre notas. Usá `json-canvas` para el esquema, IDs, posiciones, enlaces y validación estructural. Las referencias a archivos deben apuntar a notas existentes del vault.
- **Nota índice o MOC** para navegación por unidades, autores y prácticas. Es una lista curada de enlaces, no un sustituto del mapa de relaciones.
- **Tabla** cuando la tarea principal es comparar atributos entre teorías, autores o categorías; un mapa espacial no siempre mejora esa comparación.

Entregá al editor el objetivo del mapa, conceptos, relaciones etiquetadas, fuentes, formato elegido y actividad de recuperación. El auditor revisará que todos los enlaces y relaciones importantes sean correctos antes de publicar.

## Fuentes

- [Obsidian: diagramas Mermaid](https://obsidian.md/help/advanced-syntax).
- [Obsidian: Canvas y formato JSON Canvas](https://obsidian.md/help/plugins/canvas).
- [Metaanálisis de mapas conceptuales](https://pubmed.ncbi.nlm.nih.gov/38163243/).
