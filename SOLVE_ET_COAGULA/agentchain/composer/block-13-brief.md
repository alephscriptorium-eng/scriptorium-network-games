# Block 13 — brief (pre-prensa)

**Generado:** 2026-06-21 · **Fuente:** Wave A + Wave B + Wave C talk-cache + `cache/audit-talk.json`

> No es el bloque 13 completo. Solo inventario de datos para decidir la hipótesis *solo commits* vs *commits + sala*.

## Conteos noviembre 2007

| Corpus | Revisiones en nov 2007 | Con cuerpo cacheado |
|--------|------------------------|---------------------|
| **Talk** (4 vistas, ventana oct–nov filtrada) | 48 | **48** (100 %) |
| **Artículo** *Pseudociencia* (`pseudociencia/manifest.json`) | 108 | **46** (42.6 %) |

Wave A talk: **39** fetches nuevos + **6** skipped (ya en caché) + **0** fallos.

Wave B talk (`talk-block13-waveB`): manifest **9** entradas (2 wave B, 7 wave C); fetch_batch wave B → **0** nuevos + **2** skipped (`exists`) + **0** fallos.

Wave C talk (`talk-block13-waveC`): **7** oldids Analiza pre-2008 → **7** fetched + **0** fallos. Audit post-Wave C: **46/46** (100 %) UT Analiza total vista.

## Vacío explícito por vista (oct–nov 2007)

| Vista | Registros ventana | Cuerpos (post-Wave C) | Nota |
|-------|-------------------|----------------------|------|
| `discusion-pseudociencia` | **0** | 0 | Sala artículo sin actividad en ventana — pese a «ver discusión» en oldid 12909144 |
| `usuario-discusion-analiza` | 46 | **46** (100 % total vista; 100 % nov) | Actividad UT; alineación ±24 h con revert 12719652 |
| `usuario-discusion-ignacio-icke` | **0** | 0 | Sin edits UT en ventana |
| `usuario-discusion-solvecoagula` | 34 | **34** (100 %) | SC conversó en su propia UT, no en sala |

## Alineación talk ↔ reverts artículo (±24 h)

Anclas blockchain: **12719652** (revert Analiza), **12909144** (revert Ignacio_Icke, «ver discusión»).

- **15 hits** `article_refs` en manifests talk (detalle en `audit-talk.json` → `article_alignment.detalle`)
- Conversación contemporánea a reverts: **UT Analiza** (oldids 12719797–12720477 ↔ 12719652) y **UT SolveCoagula** (12719917–12721439 ↔ 12719652; 12911274–12912735 ↔ 12909144)
- **Ningún** hit en `Discusión:Pseudociencia` (vista vacía)

## Hipótesis bloque 13 (decidible con A1)

1. **Solo commits (parcial):** el pulso nov 2007 en *Pseudociencia* es legible casi enteramente en NS0 (artículo). La sala `Discusión:Pseudociencia` no registra debate en oct–nov 2007.
2. **Commits + conversación, pero fuera de sala:** la fricción **sí** dejó huella talk en **páginas de usuario** (Analiza, SolveCoagula), alineada en horas con los reverts — no en la sala del artículo.
3. **Ignacio_Icke:** sin actividad UT en ventana; su revert 12909144 cita «discusión» que **no** aparece en `Discusión:Pseudociencia` ni en su UT oct–nov 2007.

**Conclusión provisional para agentchain:** bloque 13 no es binario «hablaron / no hablaron» — es **dónde** hablaron (UT vs sala) y **qué** oldids leer antes de redactar.

## Próximo paso (fuera de este brief)

- Redactar `agentchain/composer/block-13.md` (prensa exportable) — **hecho**
- ~~Wave C talk~~ — **cerrada** (`cache/talk/viajes/talk-block13-waveC.json`)
- Enganche block-14: timeline dual artículo + talk — **hecho**
- Block 15: probe sala + Ignacio fuera de ventana oct–nov (`talk-sala-probe`)
