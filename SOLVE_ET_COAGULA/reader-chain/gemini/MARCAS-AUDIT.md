# Auditoría marcas — reader-chain Gemini (bloques 1–9)

Refactor jun 2026 · Fases 0–4. Fuentes: `index-reader.md`, `linea-aleph/cache/audit-talk.json`, `agentchain/composer/block-8.md`, `block-13.md`, `block-15.md`.

**Criterio de conteo:** emoji epistemológico seguido de `[` (marca activa) o fila de tabla `🟢 Validado` / `⚪ no validable`. No cuenta menciones explicativas en notas al pie.

## Baseline (antes)

| Bloque | 🟢 | 🟡 | 🔴 | ⚪ | Total | Combat / guerra (voz narradora) | ⚪ candidatos a upgrade |
|--------|----|----|----|----|-------|----------------------------------|-------------------------|
| 1 | 0 | 0 | 0 | 0 | 0 | — | — |
| 2 | 0 | 0 | 0 | 0 | 0 | «vandalizar» (spoiler sin marcas) | — |
| 3 | 3 | 4 | 4 | 0 | 11 | `INCIDENT REPORT`, `malicioso`, `Bunge_Violation` | — |
| 4 | 11 | 8 | 6 | 2 | 27 | `INCIDENTE`, `VIOLATION`, `FORCE-RESTORE` | línea 101 vestuario |
| 5 | 4 | 3 | 3 | 0 | 10 | `redPill`/`bluePill` (CSS UI), `force-restore` | — |
| 6 | 5 | 4 | 3 | 1 | 13 | `guerra arquitectónica`, `terreno hostil`, `choque` | línea 29 talk vacío |
| **Σ 1–6** | **23** | **19** | **16** | **3** | **61** | 12 términos / metáforas militar | 2 |

**Ratios baseline (bloques con marcas):**

| Bloque | 🟢 / total | 🔴 / total |
|--------|------------|------------|
| 3 | 27 % | 36 % |
| 4 | 41 % | 22 % |
| 5 | 40 % | 30 % |
| 6 | 38 % | 23 % |
| **4 + 6** | **40 %** (16/40) | **23 %** (9/40) |

## Post-refactor (después — Fase 1–2)

| Bloque | 🟢 | 🟡 | 🔴 | ⚪ | Total | Combat / guerra (narrador) |
|--------|----|----|----|----|-------|----------------------------|
| 1 | 0 | 0 | 0 | 0 | 0 | — |
| 2 | 0 | 0 | 0 | 0 | 0 | — (forcejeo editorial) |
| 3 | 5 | 8 | 1 | 1 | 15 | 0 (DevOps: merge conflict, linter, payload) |
| 4 | 15 | 12 | 3 | 3 | 33 | 0 (coreografía, corrección de compás, figura de cierre) |
| 5 | 5 | 8 | 2 | 1 | 16 | 0 (nota CSS ≠ marcas) |
| 6 | 8 | 8 | 2 | 2 | 20 | 0 (pista de etiqueta, partitura en repo) |
| **Σ 1–6** | **31** | **36** | **8** | **7** | **82** | **0** |

**Ratios post-refactor:**

| Bloque | 🟢 / total | 🔴 / total | Δ 🟢 | Δ 🔴 |
|--------|------------|------------|------|------|
| 3 | 33 % | 7 % | +6 pp | −29 pp |
| 4 | **45 %** | 9 % | **+4 pp** | −13 pp |
| 5 | 31 % | 13 % | −9 pp† | −17 pp |
| 6 | **40 %** | 10 % | +2 pp | −13 pp |
| **4 + 6** | **43 %** (23/53) | **9 %** (5/53) | **+3 pp** | **−14 pp** |

\* block-4: +4 oldids talk 🟢 en ELENCO/validación; ⚪ vestuario sustituido por tripartito estructural.  
† block-5: más 🟡 citando composer; 🔴 reducido a 1 glosa pastilla + mermaid.

**Mejora global Acto I:** 🟢 +35 % conteo (23→31); 🔴 −50 % (16→8). Bloque 4 cumple meta 15–25 % más 🟢 (41 %→45 %); bloque 4 cumple ≥30 % menos 🔴 (6→3).

## Upgrades epistemológicos aplicados

| Antes (⚪ obsoleto) | Después |
|---------------------|---------|
| block-4: «vestuario / ensayo fuera de wiki — DATO FALTANTE» | 🟢 UT Analiza/SC mismo día revert 12719652 (oldids 12719797, 12720101, 12720477, 12719917, 12720326); 🟢 sala = 0 rev. 2007; 🟡 Ignacio UT inexistente en 2007 |
| block-6: «pulsaciones no registradas en página de discusión» | Tabla tripartita: 🟢 UT (48 rev.); 🟢 sala vacío estructural; 🟡 Ignacio UT; ⚪ off-wiki |

## Checklist oldids talk citados (🟢)

Verificado en `network-engine/linea-aleph/cache/talk/snapshots/{oldid}.wikitext`:

12719797 · 12720101 · 12720477 · 12719917 · 12720326 · 12721439 · 12806744 · 12736728 · 12911274 · 12912735

## Acto II — bloques 7–9 (nuevos)

| Bloque | 🟢 | 🟡 | 🔴 | ⚪ | Total | Tema |
|--------|----|----|----|----|-------|------|
| 7 | 12 | 2 | 1 | 5 | 20 | Vestuario UT — upgrade ⚪ block-4 |
| 8 | 4 | 2 | 1 | 1 | 8 | Dual-rail artículo ↔ talk |
| 9 | 9 | 2 | 1 | 2 | 14 | Mensaje fantasma / probe sala |
| **Σ 7–9** | **25** | **6** | **3** | **8** | **42** | — |

| Bloque | 🟢 / total | 🔴 / total |
|--------|------------|------------|
| 7 | 60 % | 5 % |
| 8 | 50 % | 13 % |
| 9 | 64 % | 7 % |

## Fase 4 — Validación (2026-06-21)

### 1. Re-auditoría marcas (tabla definitiva Σ 1–9)

Criterio: emoji epistemológico seguido de `[` (§ arriba). Acto I = bloques 1–6 post-refactor; Acto II = 7–9.

| Alcance | 🟢 | 🟡 | 🔴 | ⚪ | Total |
|---------|----|----|----|----|-------|
| Baseline 1–6 | 23 | 19 | 16 | 3 | **61** |
| Post-refactor 1–6 | 31 | 36 | 8 | 7 | **82** |
| Acto II 7–9 | 25 | 6 | 3 | 8 | **42** |
| **Σ 1–9 (post-refactor)** | **56** | **42** | **11** | **15** | **124** |

| Métrica | Baseline 1–6 | Post 1–6 | Post 1–9 |
|---------|--------------|----------|----------|
| 🟢 | 23 | 31 (+35 %) | 56 |
| 🟡 | 19 | 36 | 42 |
| 🔴 | 16 | 8 (−50 %) | 11 |
| ⚪ | 3 | 7 | 15 |
| **Total marcas** | **61** | **82** | **124** |

Bloque 6 cumple meta ~15 % más 🟢; block-4 cumple ≥30 % menos 🔴 (6→3). Acto II mantiene 🔴 mínimo (3/42 = 7 %) — solo glosas performativas del lector.

### 2. Grep léxico militar

Patrón: `guerra|hostil|VIOLATION|INCIDENTE|malicioso` en `reader-chain/gemini/*.md` (excl. este archivo).

| Alcance | Resultado |
|---------|-----------|
| **Bloques 1–6** | **0 coincidencias** — voz narradora limpia |
| **Bloques 7–9** | 8 coincidencias; **todas admisibles**: ancla wiki `#Guerra_de_ediciones`, citas 🟢 entrecomilladas (`12720477`, `12806744`), metadatos de sección en tablas — **0 en voz narradora sin cita** |

Términos sustituidos en Acto I: `INCIDENTE` → `TURNO DE PISTA` / `deploy log`; `VIOLATION` → `corrección de compás`; `terreno hostil` → `pista de etiqueta exigente`; `guerra arquitectónica` → `partitura en el repo`.

### 3. Checklist oldids talk (🟢)

| Oldid | Snapshot | Bloque |
|-------|----------|--------|
| 12719797 | ✅ | 4, 7 |
| 12720101 | ✅ | 4, 7 |
| 12720477 | ✅ | 4, 7, 9 |
| 12719917 | ✅ | 7 |
| 12720326 | ✅ | 4 |
| 12721439 | ✅ | 9 |
| 12806744 | ✅ | 9 |
| 12736728 | ✅ | 7 |
| 12911274 | ✅ | 8 |
| 12912735 | ✅ | 8 |

Ruta: `network-engine/linea-aleph/cache/talk/snapshots/{oldid}.wikitext`.

### 4. Coherencia dual-voice (spot-check)

Revert Analiza [12719652](https://es.wikipedia.org/w/index.php?title=Pseudociencia&oldid=12719652): Gemini block-4/7 y [`composer/block-8.md`](../../agentchain/composer/block-8.md) coinciden en fecha, bytes (−108 874), summary «¿Vamos a dialogar o no?»; block-7 añade UT ±24 h sin contradecir crónica. Criterio block-11: no elegir ganador entre voces.

### 5. Checklist cierre refactor

- [x] Bloques 1–6 refactorizados; 7–9 creados
- [x] block-4 y block-6 sin ⚪ obsoleto sobre «¿hablaron?»
- [x] DevOps presente; léxico militar ausente en voz narradora (1–6)
- [x] `index-reader.md` § Gemini baile en pista + bloques 7–9
- [x] `composer/block-12.md` Story Board Gemini 1–9
- [x] `uichain/block-12-panel-estado.prompt.md` rama gemini hasta block-9
- [x] `uichain/ui-block-6-recap.md` disambiguation UI vs marcas
