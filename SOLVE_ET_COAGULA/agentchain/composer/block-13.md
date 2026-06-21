# User

¿Qué se pierde si solo abres el diff del artículo?

# Agent

**Composer · celda 13.**

## Artículo de prensa

### Dos carriles, un conflicto

Si el lector abre solo el historial de [Pseudociencia](https://es.wikipedia.org/wiki/Pseudociencia) entre el 10 y el 18 de noviembre de 2007, ve una película de bytes: alguien borra ~108 000, alguien restaura, alguien cita PVN o «versión consensuada». Si abre solo [Discusión:Pseudociencia](https://es.wikipedia.org/wiki/Discusión:Pseudociencia), ve **vacío** en la ventana. Si no salta a las UT de Analiza y SolveCoagula, **pierde el diálogo** que acompañó los reverts.

### Carril artículo (milestones)

| Fecha (UTC) | oldid | Evento |
|-------------|-------|--------|
| 10 nov 19:18 | [12719652](https://es.wikipedia.org/w/index.php?title=Pseudociencia&oldid=12719652) | Revert Analiza |
| 10 nov 19:45 | [12720368](https://es.wikipedia.org/w/index.php?title=Pseudociencia&oldid=12720368) | Restauración SolveCoagula |
| 18 nov 18:55 | [12909144](https://es.wikipedia.org/w/index.php?title=Pseudociencia&oldid=12909144) | Revert Ignacio_Icke («ver discusión») |
| 18 nov 19:55 | [12910974](https://es.wikipedia.org/w/index.php?title=Pseudociencia&oldid=12910974) | Restauración final SolveCoagula |

### Carril talk — alineación ±24 h (`article_refs`)

| Δ (h) | talk_oldid | Vista | article_oldid |
|-------|------------|-------|---------------|
| 0,1 | [12719797](https://es.wikipedia.org/w/index.php?title=Usuario_discusión:Analiza&oldid=12719797) | UT Analiza | 12719652 |
| 0,1–0,5 | [12720101](https://es.wikipedia.org/w/index.php?title=Usuario_discusión:Analiza&oldid=12720101) | UT Analiza | 12719652 |
| 0,3 | [12719917](https://es.wikipedia.org/w/index.php?title=Usuario_discusión:SolveCoagula&oldid=12719917) | UT SolveCoagula | 12719652 |
| 0,5–1,2 | [12720477](https://es.wikipedia.org/w/index.php?title=Usuario_discusión:Analiza&oldid=12720477) | UT Analiza | 12719652 |
| 1,2–2,0 | [12911274](https://es.wikipedia.org/w/index.php?title=Usuario_discusión:SolveCoagula&oldid=12911274) | UT SolveCoagula | 12909144 |

**Quince** aristas talk↔artículo en ±24 h; **ninguna** en la sala del artículo. Fuente: `audit-talk.json` → `article_alignment`.

### Qué se pierde

- **Tono:** en el diff, «vandalismo» es una etiqueta; en talk, un argumento desarrollado.
- **Geografía:** Analiza pregunta «¿vamos a dialogar?» en el resumen del artículo y explica en la UT del otro.
- **Mediación:** Retama interviene en UT citando una sala que no registra actividad.

Especificación visual dual-rail: [`uichain/block-14-timeline-dual.prompt.md`](../../uichain/block-14-timeline-dual.prompt.md).
