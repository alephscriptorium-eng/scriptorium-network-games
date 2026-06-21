# User 3

RESULTADOS DEL BLOQUE ANTERIOR: block-3.md

Épica anglo / Bunge — blockchain bloques 5-6 (radiografía). ¿Qué construyó SolveCoagula en Demarcación antes del campo de batalla?

# Agent Reader

**composer** · traje:puesto · poderes:cache-nav,epistem-tags,anti-seguros,selective-query,vacio-explicito,ayuda · engines:main · forces:—

Plan hecho y **ejecutado** — el bloqueo queda cerrado.

---

## Plan (5 fases)

Documento: `network-engine/linea-aleph/crosswiki/PLAN-paridad-traduccion.md`

| Fase | Qué | Estado |
|------|-----|--------|
| **0** | Identificar oldid enwiki al traducir | ✓ **161154035** (29 sep 2007 — sin edits en enwiki hasta el 10 oct) |
| **1** | Fetch fuente inglesa | ✓ `cache/crosswiki/en/snapshots/161154035.wikitext` |
| **2** | es traducción ya cacheada | ✓ `11951034` |
| **3** | Reporte paridad | ✓ `crosswiki/reports/demarcation-en-es-oct2007-parity.json` |
| **4** | Tabla inaugural | ✓ `crosswiki/matrix-inaugural-en-es.json` |

Ancla del par: `crosswiki/anchors/demarcation-en-es-oct2007.json`

---

## Veredicto 🟢

**PARIDAD_ESTRUCTURAL** — la traducción es refleja la arquitectura del artículo inglés en oct 2007.

| | en 161154035 | es 11951034 |
|---|-------------|-------------|
| **Bytes** | 13.973 | 16.056 (+traducción, interwikis) |
| **Secciones ==** | 8 | 8 |
| **Línea** | `PLURALIST` | `PLURALIST` |

Mapeo confirmado: Historia, Positivismo, Falsacionismo, Kuhn, Feyerabend, Demarcación contemporánea, Referencias. Detalle menor: enwiki tiene `Science and religion part ways` como `==`; en eswiki pasa a `===` bajo Historia (`Separación entre ciencia y religión`) — relevado de sección, no contenido ausente.

---

## Infra añadida (para siguientes pares)

- `fetch_snapshot.py --lang en --corpus crosswiki` (ruta `cache/crosswiki/{lang}/`)
- `scripts/compare_translation_pair.py --anchor crosswiki/anchors/...json`

---

## Tabla inaugural (rellena)

| Lang | Tema | oldid | Línea | Evidencia |
|------|------|-------|-------|-----------|
| **en** | demarcación · fuente oct 2007 | 161154035 | PLURALIST | 🟢 crosswiki/en |
| **es** | demarcación · previo | 11663303 | POPPER-ONLY | 🟢 |
| **es** | demarcación · traducción | 11951034 | PLURALIST | 🟢 · paridad ✓ |
| **es** | demarcación · SC cierre | 12763920 | PLURALIST+ | 🟢 |

---

**Pendiente fuera de este plan:** pseudociencia `11597663` (meta sin wikitext en disco) · revert `11951164` (manifest sí, cuerpo no).

¿Siguiente par en la máquina B: **pseudociencia en↔es** con el mismo patrón anchor→fetch→parity?