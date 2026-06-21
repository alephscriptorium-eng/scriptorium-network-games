# uichain — Block 12: Panel de estado juego (index-reader)

**Bloque origen:** `blockchain/block-12.md` · **Agentchain:** `agentchain/composer/block-12.md`  
**Modo:** aleph generativo no determinista — esta especificación no fija UI única.

## Objetivo

Vista de apertura del index-reader: dos widgets lado a lado (o apilados en móvil) que orientan al lector antes de elegir itinerario blockchain o agentchain.

## Widget A — Cache Navegador Wiki

### Datos

- `network-engine/linea-aleph/cache/audit-block10.json` (artículos: demarcación / pseudociencia)
- `network-engine/linea-aleph/cache/audit-talk.json` (corpus talk paralelo; ver `agentchain/composer/block-12.md`)
- `network-engine/linea-aleph/manifest.json` (demarcación)
- `network-engine/linea-aleph/pseudociencia/manifest.json`
- `network-engine/linea-aleph/talk/*/manifest.json` (4 vistas: sala + 3 UT)
- Cola activa: `scripts/fetch-priority-*.json`, `scripts/fetch-priority-talk-block13.json` si existen

### Visualización

1. **Doble barra** por artículo (demarcación / pseudociencia):
   - Registros con cuerpo (%)
   - Milestones con cuerpo (%) — siempre 100 % en estado actual
2. **Barra talk** (si `audit-talk.json` existe): `registros_cached` / `registros` y `registros_pct` por vista; opcional `ventana_nov_2007`, `article_alignment` (cruce ±24 h con reverts artículo). Snapshot 2026-06-21: global **80/80** (100 %); UT Analiza **46/46** (100 % vista); UT SolveCoagula **34/34**; `discusion-pseudociencia` e `ignacio-icke` vacío explícito.
3. **Delta panel:** lista de oldids en `missing` de la oleada activa (artículo y/o talk); botón «copiar comando fetch» (`--corpus talk` cuando aplique; no ejecutar automáticamente).
4. **Heatmap calendario** oct–nov 2007: intensidad = ediciones/día en manifest; resaltar 16 oct (Matrix), 10–18 nov (fricción).
5. **Zonas sensibles sin enlace** (predicción): satélites thin en `INDICE2.md` con `body_cached: false`; sección «explicación científica» demarcación (registros 11–15 oct sin body).

### Reglas UX

- Si `missing.length > 0`: banner «vacío explícito» en bloques que dependan de esos oldids — no inventar wikitext.
- No scrape `/wiki/`; solo citar oldids cacheados o marcar fetch pendiente.

## Widget B — Tramas–Story Board

### Datos

- Metadatos `blockchain/block-{0..12}.md` (título user prompt, acto)
- Presencia `agentchain/composer/block-N.md` y `reader-chain/gemini/block-N.md`

### Visualización

1. **Timeline cinco actos** (horizontal scroll):
   - Constitución 0–4
   - Radiografía 5–7
   - Fricción 8
   - Profundización 9–10
   - Meta-lectura 11–12
2. **Chips subtrama** (toggle filter): Matrix · Noviembre/Analiza · Dual reader · Talk-cache
3. **Nodo por bloque:** clic → abre lectura blockchain o selector agentchain si hay ramas.

### Reglas UX

- Chip «Talk-cache»: **disabled** si falta `audit-talk.json` o la suma de `registros_cached` por vista es 0; **enabled** cuando `audit-talk.json` reporta `registros_cached > 0` (al menos un cuerpo talk offline). Coherente con corpus paralelo en `agentchain/composer/block-12.md`; vacío explícito por vista sigue siendo dato válido (bloque 13).
- No fusionar composer y gemini en una sola voz; mostrar ramas paralelas.

## DevOps (fase tramitación)

| Paso | Acción |
|------|--------|
| 1 | Crear rama `uichain/block-12-panel` en network-engine site build o SPA local del juego |
| 2 | Endpoint estático: leer audit JSON vía fetch relativo a `linea-aleph/cache/` |
| 3 | Sin backend obligatorio — JSON estático + markdown index-reader |
| 4 | Tests: render con audit-block7 fixture; heatmap con manifest subset |

## Criterios de aceptación

- [ ] Usuario ve % caché y % milestones sin abrir terminal
- [ ] Usuario identifica acto actual y subtramas activas
- [ ] Dos sesiones distintas pueden generar layouts distintos sin romper datos
- [ ] Talk-cache ausente (`audit-talk.json` inexistente o `registros_cached === 0`) se muestra como vacío explícito, no como error
- [ ] Con talk cacheado, chip Talk-cache filtra subtrama y Widget A muestra barras por vista

## No hacer

- Implementar fetch automático desde la UI
- Cerrar paleta visual única (aleph abierto)
- Mezclar datos 🟢 wiki con 🟡 agentchain sin etiqueta
