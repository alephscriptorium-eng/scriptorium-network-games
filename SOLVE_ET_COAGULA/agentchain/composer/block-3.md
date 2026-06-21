# User

¿Qué satélites merecen su propia línea?

# Agent

**Composer · cabezal → celda 3.** Cinta leída. Clusters de `manifest2.json` / `INDICE2.md` cruzados.

## Respuesta: solo Pseudociencia merece línea gruesa

| Tier | Artículo | Edits | ¿Línea propia? |
|------|----------|-------|----------------|
| thick | Demarcación | 713 | Ya existe (`raw/linea.md`) |
| thick_candidate | **Pseudociencia** | 169 | **Sí** — único candidato |
| medium | Método científico (40), Filosofía de la ciencia (25) | 65 | No — solo índice |
| thin | 20 artículos | 1–12 c/u | No — solo índice |

**Conclusión:** una sola línea gruesa nueva. El resto permanece en `INDICE2` como mapa enciclopedista.

Pseudociencia concentra el 58 % de las ediciones fuera de demarcación (169/293). Método científico y Filosofía de la ciencia no alcanzan densidad de corpus propio; la cola fina (20 artículos) no justifica líneas separadas.

## Decisión de implementación

Materializar la segunda línea gruesa vía **historial completo del artículo** (API MediaWiki), no solo las 169 contribuciones de usuario en `linea2`:

| Motivo | Detalle |
|--------|---------|
| Paridad con linea1 | `raw/linea.md` incluye **todos** los editores en la ventana, no solo SolveCoagula |
| Ventana anclada | Desde **previo** (parent de primera edit SC, oldid `11597663`) hasta última edit SC (`12910974`) |
| Sub-corpus aislado | `BOT_ALEPH/linea-aleph/pseudociencia/` — sin colisión con `registros/` de demarcación |

Pipeline ejecutado:

```bash
cd BOT_ALEPH/linea-aleph
python3 scripts/fetch_article_history.py --title Pseudociencia --corpus-dir pseudociencia
python3 segment_linea.py --corpus-dir pseudociencia --title Pseudociencia --corpus-id linea-pseudociencia --expand milestones
```

## Sub-corpus generado

| Artefacto | Ruta |
|-----------|------|
| Historial crudo | [`pseudociencia/raw/linea.md`](../../../BOT_ALEPH/linea-aleph/pseudociencia/raw/linea.md) |
| Backup API | `pseudociencia/raw/linea.json` |
| Manifest + registros | [`pseudociencia/manifest.json`](../../../BOT_ALEPH/linea-aleph/pseudociencia/manifest.json) |
| Índice | [`pseudociencia/INDICE.md`](../../../BOT_ALEPH/linea-aleph/pseudociencia/INDICE.md) |
| Delta extremo | `pseudociencia/snapshots/delta-extremo.md` (`status: pending`) |

Cross-ref: registros con `in_linea2: true` cuando el oldid coincide con contribuciones Pseudociencia en `manifest2.json`. `INDICE2` actualizado: Pseudociencia pasa de `thick_candidate` a **thick** implementada.

## Diagrama

```
linea1 (demarcación)          linea2 (usuario NS0)
     │                              │
     │                              ├── thick → demarcación
     │                              ├── thick → Pseudociencia  ← celda 3
     │                              └── medium/thin → solo índice
     │
     └── pseudociencia/  (historial artículo, ventana SC)
```

## Movimiento siguiente (opcional)

1. **Curar** `pseudociencia/snapshots/delta-extremo.md` (previo → final).
2. **Fetch** snapshots extremos si `fetched: false`.
3. **Viajes hipervinculados** desde milestones Pseudociencia hacia demarcación / método científico.
