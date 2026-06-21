# Cadena gemini — reader-chain

Narrativa paralela del **index-reader**: cómo se cuenta el juego al visitante del libro vivo. No opera la blockchain; persiste actos de lectura en `block-{N}.md`.

## Convenciones de archivo

| Campo | Regla |
|-------|-------|
| `# User {N}` | `N` = número del archivo (`block-N.md`) |
| `# Agent Reader` | Respuesta gemini persistente (artefacto de cadena) |
| Cabecera traje | Primera línea tras `# Agent Reader` — ver [`disfraz-rude-bot/SKILL.md`](../../../../network-engine/agents/skills/disfraz-rude-bot/SKILL.md) § Cabecera |
| Plantilla | [`reader-gemini-block.hot.md`](../../../../network-engine/agents/skills/disfraz-rude-bot/templates/reader-gemini-block.hot.md) |

## Paridad con blockchain

**No es copia 1:1.** `gemini/block-N.md` no repite literalmente `blockchain/block-N.md`. El número de archivo marca el **orden del viaje reader**, no la pregunta ledger del mismo índice.

| gemini N | Acto reader | Blockchain relacionada | Notas |
|----------|-------------|------------------------|-------|
| 1 | Onboarding traje | 0–1 | UI + comandos; no duplicar [`index-reader.md`](../../index-reader.md) entero |
| 2 | Demo `+ayuda` | todos (Q1–Q5) | Mapa capas + Story Board; canon runtime en poder `ayuda` |
| 3 | Épica anglo / Bunge | 5–6 (radiografía) | Requiere 🟢 oldids oct 2007 antes de glosa DevOps |
| 4 | Protocolo REIC / manual de campo | 4 | Molde periodístico; 🟢 = archivo público MediaWiki |
| 5+ | *pendiente* | 5 … 15 | Perfil SC, radiografía, cierre |

## Mínimos epistemológicos por bloque

| N | 🟢 obligatorio antes de narrar | CTA sugerido |
|---|--------------------------------|--------------|
| 1 | ninguno (onboarding) | `+ayuda` o gemini 2 |
| 2 | leer `solve-coagula-story-board.json` o SKILL ayuda | gemini 3 o `blockchain/block-0.md` |
| 3 | oldids **11663303** (previo), **12370021** (cierre oct SC) o ⚪+fetch | `blockchain/block-4.md` (REIC) |
| 4 | archivo público contribuciones MediaWiki (🟢 procedural) | `blockchain/block-5.md` (perfil SC) |

## Roadmap gemini 4+

| gemini | Tema reader | Ancla blockchain |
|--------|-------------|------------------|
| 4 | Protocolo REIC / manual de campo | 4 | ✓ vigente |
| 5 | Perfil SolveCoagula | 5 |
| 6–7 | Catedral demarcación · pseudociencia política | 6–7 |
| 8 | Clímax noviembre (eco narrativo) | 8 |
| 9–10 | Flashback Matrix · genealogía | 9–10 |
| 11–15 | Cierre (contrato · vestuario · dual · fantasma · epílogo) | 11–15 |

Actualizar `gemini_range` en [`story_board_manifest.py`](../../../../network-engine/scripts/story_board_manifest.py) solo cuando existan archivos en disco.

## Lint

```bash
python network-engine/scripts/lint_gemini_chain.py
```
