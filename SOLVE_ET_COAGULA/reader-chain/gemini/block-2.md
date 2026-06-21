# User 2

¿Ahora tengo un bot convertido en rude-bot porque tiene un traje? ¿Esto es un sitio transmedia? Activar el modo ayuda para ver panorámica summary de contenidos de las cadenas

# Agent Reader

Gemini 3.1 Pro (High) · traje:puesto · poderes:cache-nav,epistem-tags,anti-seguros,selective-query,vacio-explicito,ayuda · engines:main · forces:— · +force <id> · -force <id> · forces? · +poder <id> · -poder <id> · sin disfraz

> **Calibración engines** — main: mirar sin prisa.

🔴 [Deducción del Lector / Generativo]: El traje **rude-bot** es calibración operativa: Trazabilidad Epistemológica Estricta, no decoración transmedia. Con `+ayuda` activo, el mapa de capas y el Story Board siguen el canon del poder [`ayuda`](../../../../network-engine/agents/skills/disfraz-rude-bot/poderes/ayuda/SKILL.md) y [`solve-coagula-story-board.json`](../../../../network-engine/data/sessions/solve-coagula-story-board.json).

> **Ayuda capas**

### Contraste de capas

| Dimensión | **blockchain** | **agentchain** | **gemini** | **uichain** |
|-----------|----------------|----------------|------------|-------------|
| **Rol** | Fundación secuencial | Inferencia y análisis | Narrativa y enrutamiento | Interfaz generativa |
| **Unidad** | Bloque = pregunta usuario | Bloque = respuesta del modelo | Bloque = acto de lectura | `.prompt.md` / plan DevOps |
| **Metáfora** | Libro · páginas | Crónica forense · prensa | Baile en pista · compás DevOps | Scrollytelling · tablero · timeline |
| **Marca dominante** | Pregunta canónica (no 🟢 wiki) | 🟡 fuente de inferencia | 🟡 cita + 🔴 glosa mínima | Especificación (no verdad) |
| **Mutabilidad** | Solo vía plan (añadir/fork) | Carpeta por modelo (`composer/`) | Cadena paralela del reader | Aleph abierto; sin UI fija |

```mermaid
flowchart TB
  GT["linea-aleph<br/>snapshots · talk · registros"]
  BC["blockchain<br/>preguntas"]
  AC["agentchain/composer<br/>respuestas"]
  GEM["reader-chain/gemini<br/>divulgación"]
  UI["uichain<br/>planes UI"]
  IR["index-reader"]

  GT --> IR
  BC --> AC
  BC --> GEM
  AC --> GEM
  AC --> UI
  BC --> UI
  GEM --> UI
  IR --> BC & AC & GEM & UI
```

---

### Ultra-resumen Story Board

| N | Acto | Ultra-resumen (blockchain) | composer | gemini | uichain | chips |
|---|------|----------------------------|----------|--------|---------|-------|
| 0 | constitucion | ¿Qué juego es este si la fuente es un usuario real de 2007? | ✓ | ⚪ | ⚪ | — |
| 1 | constitucion | ¿Cuánto archivo tenemos del pulso SolveCoagula? | ✓ | ✓ | ⚪ | — |
| 2 | constitucion | ¿Qué otros artículos orbitan al protagonista? | ✓ | ✓ | ⚪ | — |
| 3 | constitucion | ¿Qué satélites merecen su propia línea? | ✓ | ✓ | ⚪ | — |
| 4 | constitucion | ¿Cómo radiografiamos a un enciclopedista sin jerga interna? | ✓ | ⚪ | ⚪ | — |
| 5 | radiografia | ¿Quién es SolveCoagula como enciclopedista? | ✓ | ⚪ | ⚪ | — |
| 6 | radiografia | ¿Qué construyó en Demarcación antes del campo de batalla? | ✓ | ⚪ | ui-block-6-recap | — |
| 7 | radiografia | ¿Por qué Pseudociencia es el escenario inevitable? | ✓ | ⚪ | ⚪ | — |
| 8 | friccion | ¿Qué pasó en Pseudociencia entre el 10 y el 18 de noviembre de 2007? | ✓ | ⚪ | ⚪ | noviembre_analiza |
| 9 | profundizacion | ¿Qué hizo el 16 de octubre con Matrix que prefiguró noviembre? | ✓ | ⚪ | ⚪ | matrix |
| 10 | profundizacion | ¿Cómo vibra Matrix entre Demarcación y Pseudociencia? | ✓ | ⚪ | ⚪ | matrix |
| 11 | cierre | ¿Cómo leemos once capítulos sin confundir archivo con interpretación? | ✓ | ⚪ | ⚪ | — |
| 12 | cierre | ¿Dónde hablaron cuando Pseudociencia ardía? | ✓ | ⚪ | block-12-panel-estado | talk_cache |
| 13 | cierre | ¿Qué se pierde si solo abres el diff del artículo? | ✓ | ⚪ | ⚪ | dual_reader · talk_cache |
| 14 | cierre | ¿Existió la sala que Retama e Ignacio citaron? | ✓ | ⚪ | block-14-timeline-dual | dual_reader · talk_cache |
| 15 | cierre | ¿Qué quedó de SolveCoagula tras el último commit? | ✓ | ⚪ | ⚪ | epilogo |

*Gemini 4+ pendiente — temas 11–15 cubiertos en `agentchain/composer` hasta regenerar reader.*

---
**Siguiente:** [`reader-chain/gemini/block-3.md`](block-3.md) (épica anglo) o `blockchain/block-0.md`.
