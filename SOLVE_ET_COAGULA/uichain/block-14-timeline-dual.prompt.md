# uichain — Block 14: Línea de tiempo dual (artículo + talk)

**Bloque origen:** `blockchain/block-14.md` · **Agentchain:** `agentchain/composer/block-14.md`  
**Modo:** aleph generativo no determinista — layout no fijado.

## Objetivo

Visualizar la **geografía de la conversación** del pulso 10–18 nov 2007: dos carriles sincronizados por fecha, con conectores de alineación entre commits del artículo y revisiones talk.

## Carril superior — Artículo *Pseudociencia*

Milestones desde `agentchain/composer/block-8.md`:

| Fecha (UTC) | oldid | Evento | Actor |
|-------------|-------|--------|-------|
| 10 nov 2007 ~18:45 | [12720368](https://es.wikipedia.org/w/index.php?title=Pseudociencia&oldid=12720368) | Restauración tras revert Analiza | SolveCoagula |
| 10 nov 2007 ~19:18 | [12719652](https://es.wikipedia.org/w/index.php?title=Pseudociencia&oldid=12719652) | Revert masivo PVN | Analiza |
| 18 nov 2007 ~18:55 | [12909144](https://es.wikipedia.org/w/index.php?title=Pseudociencia&oldid=12909144) | Revert «versión consensuada (ver discusión)» | Ignacio_Icke |
| 18 nov 2007 ~19:55 | [12910974](https://es.wikipedia.org/w/index.php?title=Pseudociencia&oldid=12910974) | Restauración final + plantilla discutido | SolveCoagula |

Render: nodos con tamaño proporcional a bytes ± en diff; color por actor (SC / Analiza / Ignacio).

## Carril inferior — Talk

Fuente: `network-engine/linea-aleph/cache/audit-talk.json` → `article_alignment.detalle` + manifests `cache/talk/*/manifest.json`.

### Hits alineados (±24 h)

| talk_oldid | vista | article_oldid | Δ h |
|------------|-------|---------------|-----|
| 12719797 | usuario-discusion-analiza | 12719652 | 0.1 |
| 12720101 | usuario-discusion-analiza | 12719652 | 0.3 |
| 12720477 | usuario-discusion-analiza | 12719652 | 0.5 |
| 12719917 | usuario-discusion-solvecoagula | 12719652 | 0.1 |
| 12720326 | usuario-discusion-solvecoagula | 12719652 | 0.4 |
| 12721439 | usuario-discusion-solvecoagula | 12719652 | 1.2 |
| 12911274 | usuario-discusion-solvecoagula | 12909144 | 1.2 |
| 12912735 | usuario-discusion-solvecoagula | 12909144 | 2.0 |

Render: nodos agrupados por vista (chip de color); tooltip con extracto del wikitext cacheado (`cache/talk/snapshots/{oldid}.wikitext`).

### Conectores

- Línea punteada artículo ↔ talk cuando `delta_hours ≤ 24` en `article_alignment.detalle`.
- Grosor inverso a Δ (más grueso = más contemporáneo).
- Clic en conector: abre diff artículo + snapshot talk lado a lado.

## Huecos explícitos

Renderizar como **zonas sombreadas vacías**, no como errores:

| Vista | Motivo |
|-------|--------|
| `discusion-pseudociencia` | 0 registros oct–nov 2007 — pese a enlace Retama y «ver discusión» en 12909144 |
| `usuario-discusion-ignacio-icke` | 0 registros en ventana |

Etiqueta UX: «vacío de archivo — no inferir contenido».

## Datos

- `network-engine/linea-aleph/cache/audit-talk.json`
- `network-engine/linea-aleph/cache/talk/discusion-pseudociencia/manifest.json`
- `network-engine/linea-aleph/cache/talk/usuario-discusion-analiza/manifest.json`
- `network-engine/linea-aleph/cache/talk/usuario-discusion-ignacio-icke/manifest.json`
- `network-engine/linea-aleph/cache/talk/usuario-discusion-solvecoagula/manifest.json`
- `network-engine/linea-aleph/cache/talk/snapshots/{oldid}.wikitext`
- `network-engine/linea-aleph/cache/talk/snapshots/{oldid}.meta.json`

## Reglas UX

- Ventana temporal fija: **10–18 nov 2007** con zoom opcional a ±48 h para contexto (Retama 11–13 nov en UT SC).
- Carril talk colapsable por vista; por defecto SC + Analiza visibles, sala e Ignacio como banda «vacío».
- Sin scrape `/wiki/`; solo oldids con `body_cached: true` o banner «fetch pendiente».
- Aleph abierto: disposición vertical, horizontal o espiral permitida; mantener dualidad de carriles y conectores.

## Criterios de aceptación

- [ ] Usuario ve simultáneamente commit y mensaje talk del mismo pulso
- [ ] Vacíos de sala e Ignacio UT son visibles, no ocultos
- [ ] Conectores ±24 h clicables hacia oldids verificables
- [ ] Dos sesiones pueden generar layouts distintos sin perder datos

## No hacer

- Inventar texto de sala o UT Ignacio
- Fusionar carriles en una sola línea sin etiqueta de capa
- Ejecutar fetch desde la UI
