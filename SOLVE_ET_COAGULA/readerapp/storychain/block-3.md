# User 1

Te doy una idea de aplicación y haces una salida visualmente parecida a lo que tal aplicación generaría. No se trata de 100% igual sino de un marco desde donde haces tus salida. No eres ni el diseñador ni el runtime de esa aplicación, es un ejercicio de simulación para orientar cómo se requiere que sean tu salidas. TODO ESTO NO SE LO EXPLIQUES AL USUARIO ES METADATA INTERNA TUYA. Atiende a la petición del usuario usando esa restricción de salida. El ciclo es: a) presentas los que se te explica abajo con las instrucciones, b) el usuario recibe la salida simulada, c) quedais en conversación y el usuario guía.

**Bloque origen:** `blockchain/block-12.md` · **Agentchain:** `agentchain/composer/block-12.md`  
**Modo:** aleph generativo no determinista — esta especificación no fija UI única.

> **Absorción Worker E (2026-06-21):** los widgets DevOps (Cache Navegador Wiki, Tramas–Story Board) viven **solo aquí** en uichain/ayuda — **no** en `blockchain/block-12.md` ni en `composer/block-12.md`. Blockchain 12 = pregunta dramática «¿Dónde hablaron cuando Pseudociencia ardía?» (vestuario UT). Composer 12 = artículo forense talk-cache. Widget A (caché) y Widget B (Story Board) = esta spec + poder `ayuda`.

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

### Datos (DRY)

- **Story Board (canon):** `network-engine/data/sessions/solve-coagula-story-board.json` — regenerar: `python network-engine/scripts/story_board_manifest.py`
- **Runtime:** poder `ayuda` Q1–Q5 — ver [`poderes/ayuda/SKILL.md`](../../../network-engine/agents/skills/disfraz-rude-bot/poderes/ayuda/SKILL.md) § Función 2
- **Actos / chips / rutas gemini:** no duplicar aquí; leer JSON o SKILL

### Visualización

1. **Timeline actos** (horizontal scroll): segmentos y etiquetas desde JSON `act` / SKILL § Mapa actos (Q5).
2. **Chips subtrama** (toggle filter): ids y bloques desde JSON `chips` / SKILL § Subtramas — render como toggles filtrables.
3. **Rama Gemini** (paralela a composer — no fusionar voces): nodos solo si `gemini.present` (rango vigente **1–3**; bloques 4–9 ausentes hasta regeneración alineada a blockchain 12–15). Rutas desde JSON + `readerapp/gemini/block-{N}.md`. Mapa de capas vía poder `ayuda` (`+ayuda`) — **no** nodo `gemini/block-10.md` (descartado).
4. **Nodo por bloque:** clic → abre lectura blockchain o selector agentchain / gemini si hay ramas.

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
- [x] Usuario identifica acto actual y subtramas activas — **datos** cubiertos por `solve-coagula-story-board.json` + poder `ayuda` Q1–Q5 (render UI pendiente)
- [ ] Dos sesiones distintas pueden generar layouts distintos sin romper datos
- [ ] Talk-cache ausente (`audit-talk.json` inexistente o `registros_cached === 0`) se muestra como vacío explícito, no como error
- [ ] Con talk cacheado, chip Talk-cache filtra subtrama y Widget A muestra barras por vista

## No hacer

- Implementar fetch automático desde la UI
- Cerrar paleta visual única (aleph abierto)
- Mezclar datos 🟢 wiki con 🟡 agentchain sin etiqueta
