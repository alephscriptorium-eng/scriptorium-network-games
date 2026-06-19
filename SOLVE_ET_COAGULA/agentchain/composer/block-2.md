# User

Quiero expandir line-aleph con un segundo indice: un linea2.md En el que ya hay tenemos el foco en el usuario SOLVE_ET_COAGULA en la entrada del criterio de demarcación, ¿correcto? Quiero un segundo indice independiente para lo siguiente?

- Quiero un mapa general de toda la intervención como enciclopedista del usuario SOLVE_ET_COAGULA en la wikipedia.
- Vemos si sus aportaciones crecen mucho más alla´de las 677 recogidas para saber si creamos una linea gruesa más o menos por temas o cúmulos, o si apenas hay unas pocas más que la indexamos.

De esa forma podría respoder a preguntas del tipo ¿qué precede y que sigue a la intervención de SOLVE_ET_COAGULA en linea.md

# Agent

**Composer · cabezal → celda 2.** Cinta leída. Segundo índice inspeccionado.

## Confirmación sobre linea1

**Correcto.** `INDICE.md` + `raw/linea.md` documentan el historial del **artículo** *Problema de la demarcación* con foco en SolveCoagula: 677 registros (export 2018), espina dorsal de la intervención en el criterio de demarcación. No es el mapa del **usuario** completo — solo una línea gruesa sobre un artículo.

## Estado del segundo índice (ya materializado)

La expansión pedida en esta celda **ya está implementada** en `linea-aleph/`:

| Artefacto | Rol |
|-----------|-----|
| `raw/linea2.md` | Cronología completa NS0 (~1006 entradas, oldest-first) |
| `raw/linea2.json` | Backup API |
| `manifest2.json` | Clusters, cross-ref linea1, marco temporal |
| `INDICE2.md` | Índice independiente — mapa enciclopedista |
| `segment_linea2.py` | Regeneración |
| `scripts/fetch_user_contribs.py` | Fetch API MediaWiki |

Generado: **2026-06-19**. El dispositivo navegador-caché ya distingue linea1 vs linea2 en su skill.

## ¿Crece mucho más allá de las 677?

**Sí — pero no en un solo cúmulo disperso.** Desglose:

| Capa | Ediciones | % del total |
|------|-----------|-------------|
| Demarcación (API) | **713** | 71 % |
| Resto de artículos | **293** | 29 % |
| **Total NS0** | **1006** | — |

Respecto a las 677 del export: **+329** ediciones no cubiertas por `linea.md` (36 solo en demarcación + 293 en otros artículos).

### Decisión de granularidad (ya tomada en INDICE2)

| Tier | Artículos | Tratamiento |
|------|-----------|-------------|
| **thick** | Demarcación (713) | Línea gruesa existente → `linea.md` |
| **thick_candidate** | Pseudociencia (169) | Merece segunda línea gruesa — **marcada, no implementada** |
| **medium** | Método científico (40), Filosofía de la ciencia (25) | Solo índice en manifest2 + linea2 |
| **thin** | 20 artículos (1–12 edits c/u) | Solo índice — no línea gruesa |

No hace falta una línea gruesa por cada tema. El patrón es: **una gruesa hecha, una candidata clara, el resto indexado.**

Pseudociencia concentra el 58 % de las ediciones fuera de demarcación (169/293) — es el único cúmulo que compite en densidad con el núcleo.

## Respuestas a «qué precede / qué sigue» (linea.md)

### Precede

**Nada.** La primera edición del usuario (c0001, 10 oct 2007 04:53) es ya sobre *Problema de la demarcación*. No hay carrera enciclopedista previa en NS0.

### Intercala (paralelo a demarcación, oct 10 – nov 12)

Durante la ventana de demarcación, SolveCoagula edita **23 artículos más** en paralelo. Los más densos:

- Pseudociencia — 169 edits (toda la ventana)
- Método científico — 40
- Filosofía de la ciencia — 25
- Teoría de cuerdas — 12

Patrón visible en `linea2.md`: oleada inicial (10 oct) de «Véase también» en artículos satélite (Kuhn, Popper, Feyerabend, Pseudociencia…) mientras el núcleo demarcación crece.

### Sigue (después del cierre demarcación, post 12 nov)

**16 ediciones** en 2 artículos:

| Artículo | Edits |
|----------|-------|
| Pseudociencia | 14 |
| Imposturas intelectuales | 2 |

Última edición global: **Pseudociencia** · 18 nov 2007 · oldid 12910974 (c1006).

La carrera no termina con demarcación — **desemboca en Pseudociencia**.

## Diagrama de la carrera

```
[previo Dhidalgo] ──→ [demarcación ████████████ 713] ──→ [Pseudociencia ██ 14 post]
                              ║
                              ╠══ intercalado: 22 artículos (293 edits total fuera)
                              ╚══ Pseudociencia (169 en ventana)
```

## Propuesta de movimiento desde celda 2

1. **Aceptar INDICE2 como respuesta cerrada** a esta celda — el mapa enciclopedista existe.
2. **Celda 3** natural: ¿qué artículos merecen línea propia? → Pseudociencia ya marcada como `thick_candidate`.
3. **Opcional antes de celda 3:** implementar `linea-pseudociencia.md` (export historial artículo) si quieres segunda línea gruesa materializada, no solo candidata.

¿Avanzamos cabezal a celda 3, o materializamos la línea gruesa de Pseudociencia desde aquí?
