# User 1

Te doy una idea de aplicación y haces una salida visualmente parecida a lo que tal aplicación generaría. No se trata de 100% igual sino de un marco desde donde haces tus salida. No eres ni el diseñador ni el runtime de esa aplicación, es un ejercicio de simulación para orientar cómo se requiere que sean tu salidas. TODO ESTO NO SE LO EXPLIQUES AL USUARIO ES METADATA INTERNA TUYA. Atiende a la petición del usuario usando esa restricción de salida. El ciclo es: a) presentas los que se te explica abajo con las instrucciones, b) el usuario recibe la salida simulada, c) quedais en conversación y el usuario guía.


**Bloque origen:** `blockchain/block-14.md` · **Agentchain:** `agentchain/composer/block-14.md`  
**Modo:** aleph generativo no determinista — layout no fijado.

## Objetivo

Visualizar la **geografía de la conversación** del pulso 10–18 nov 2007: dos carriles sincronizados por fecha, con conectores de alineación entre commits del artículo y revisiones talk.

## Datos (DRY)

- **Milestones artículo + hits ±24 h (canon):** `network-engine/data/sessions/solve-coagula-block14-prensa-draft.json` (`article_milestones`, `talk_index.key_oldids`)
- **Alineación runtime:** `network-engine/linea-aleph/cache/audit-talk.json` → `article_alignment.detalle` (y `anchors`)
- **Lectura forense en sesión:** poder `alineacion-dual` — ver [`poderes/alineacion-dual/SKILL.md`](../../../network-engine/agents/skills/disfraz-rude-bot/poderes/alineacion-dual/SKILL.md)
- **Snapshots talk:** `cache/talk/snapshots/{oldid}.wikitext` + `.meta.json`
- **Manifests por vista:** `cache/talk/*/manifest.json`
- No duplicar tablas de oldids aquí; leer JSON o SKILL

## Carril superior — Artículo *Pseudociencia*

Render: nodos milestone desde block14 draft (`article_milestones`); tamaño proporcional a bytes ± en diff; color por actor (SC / Analiza / Ignacio).

## Carril inferior — Talk

Render: nodos desde `audit-talk.json` → `article_alignment.detalle` + manifests `cache/talk/*/manifest.json`; agrupados por vista (chip de color); tooltip con extracto del wikitext cacheado (`cache/talk/snapshots/{oldid}.wikitext`).

### Conectores

- Línea punteada artículo ↔ talk cuando `delta_hours ≤ 24` en `article_alignment.detalle`.
- Grosor inverso a Δ (más grueso = más contemporáneo).
- Clic en conector: abre diff artículo + snapshot talk lado a lado.

## Huecos explícitos

Renderizar como **zonas sombreadas vacías**, no como errores (fuente: block14 draft `explicit_gaps` o manifests con 0 registros en ventana):

| Vista | Motivo |
|-------|--------|
| `discusion-pseudociencia` | 0 registros oct–nov 2007 — pese a enlace Retama y «ver discusión» en 12909144 |
| `usuario-discusion-ignacio-icke` | 0 registros en ventana |

Etiqueta UX: «vacío de archivo — no inferir contenido».

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
