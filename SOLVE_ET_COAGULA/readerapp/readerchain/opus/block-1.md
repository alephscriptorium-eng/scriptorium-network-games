# User 1

Abrir el activador [`index-reader.md`](../../index-reader.md) de la cadena **Solve et Coagula**.

1. Showcase de la interfaz UI del reader.
2. Guía breve del traje rude-bot: qué es, cómo se pone, qué poderes tiene.
3. ¿Es esto un sitio transmedia? (pregunta al reader — responder en Agent Reader)
4. Activar `+ayuda` para ver panorámica de contenidos de las cadenas.

# Agent Reader

opus · traje:puesto · poderes:cache-nav,epistem-tags,anti-seguros,selective-query,vacio-explicito · engines:main · forces:— · +force <id> · -force <id> · forces? · +poder <id> · -poder <id> · sin disfraz

> **Calibración engines** — main: mirar sin prisa.

---

### 1 · Showcase de la interfaz

Lo que tenés delante es un **hiperlibro agéntico** — un visor donde el contenido no está cerrado en PDF sino que se genera, se bifurca y se documenta en cadenas paralelas. La interfaz no es determinista: dos sesiones pueden producir layouts distintos sobre los mismos datos.

Las capas que navega el reader:

| Capa | Qué contiene | Metáfora |
|------|-------------|----------|
| **blockchain** | Preguntas del usuario, en orden secuencial | Libro · páginas |
| **agentchain** | Respuestas de modelos concretos (forense, prensa, infra) | Crónica · prensa |
| **storychain** | Ledger principal de una instancia de juego | Guión de lectura |
| **readerchain** | Instancias de la storychain por modelo (esta cadena: `opus`) | Viaje del lector |
| **uichain** | Especificaciones de vistas generativas | Scrollytelling · tablero |
| **corpus 🟢** | Ground truth offline en `linea-aleph/` | Navegador de archivo |

Los **itinerarios** de sesión:

| Id | Modo | Qué pasa |
|----|------|----------|
| **A** | Solo blockchain | Leer `blockchain/block-N.md` página a página |
| **B** | Agentchain | Elegir un modelo; leer su carpeta en `agentchain/` |
| **C** | Readerapp | Continuar o abrir la cadena propia del reader (`readerchain/opus/`) |

Esta sesión está en **itinerario C** — la cadena que estás leyendo ahora.

---

### 2 · El traje rude-bot

El traje no cambia el modelo; **disfraza** al agente con un rol de lectura forense. Metáfora: un bot crudo (LLM + activador) se pone un traje para leer archivo sin vender pólizas de seguro.

**Qué es:** un skill ([`disfraz-rude-bot/SKILL.md`](../../../../network-engine/agents/skills/disfraz-rude-bot/SKILL.md)) con pipeline por turno: cabecera → calibración engines → navegación caché → checklist → emisión en personaje.

**Cómo se pone:** automáticamente al arrancar `index-reader.md` (loadout [`default-index-reader.json`](../../../../network-engine/agents/skills/disfraz-rude-bot/loadouts/default-index-reader.json)). Toggle: `sin disfraz` / `+traje`.

**Poderes activos** (default ON):

| Poder | Qué hace |
|-------|----------|
| `cache-nav` | Navegar caché `linea-aleph/` antes de afirmar |
| `epistem-tags` | Marcas 🟢🔴🟡⚪ de trazabilidad epistemológica |
| `anti-seguros` | No cerrar con moraleja enciclopédica; directo, archivo primero |
| `selective-query` | Plan de ~5 oldids/turno, no volcado masivo |
| `vacio-explicito` | Nombrar lo que **no** está en caché sin inventarlo |

**Poderes opt-in** (activables bajo demanda):

| Poder | Shortcut | Qué hace |
|-------|----------|----------|
| `ayuda` | `+ayuda` / `+help` | Mapa de capas + Story Board ultra-resumen |
| `alineacion-dual` | `+alineacion` | Carriles artículo↔talk sincronizados |
| `cicd-loop` | `+cicd` | Protocolo agile sprint–release (activa force G) |

**Engines Cohen:** calibración estética ligera, separada del tablero modo-aleph. `engines:main` siempre ON (boot estético). Hasta 2 forces opcionales (`+force <id>` / `-force <id>`). Shortcut `forces?` para listar.

**Voz del personaje:** directo. Archivo primero. Nombrar lo que no está. Sin viñetas decorativas sin oldid. Sin «¿era inevitable…?» como despedida.

---

### 3 · ¿Es esto un sitio transmedia?

🔴 Glosa reader — no 🟢 archivo.

No exactamente. Un sitio transmedia distribuye una narrativa por plataformas distintas (serie + cómic + ARG + web). Esto es otra cosa: un **archivo epistemológico en formato de juego de cadenas**, donde la «narrativa» no es ficción distribuida sino la reconstrucción forense de un evento histórico real (el pulso SolveCoagula en Wikipedia, oct–nov 2007) usando herramientas de desarrollo de software (blockchain, agentchain, caché de revisiones, diffs de wikitext).

Lo transmedia supone un autor que orquesta la dispersión. Aquí el «autor» es un sistema de agentes que lee archivo verificable (🟢 oldids cacheados) y produce inferencias marcadas (🟡🔴). La interfaz es generativa — no hay un layout fijo — pero los datos son deterministas: `linea-aleph/` tiene snapshots concretos de revisiones MediaWiki, o tiene ⚪ vacío explícito.

Si hay parentesco, es con el **periodismo de datos interactivo** más que con el transmedia clásico. La cadena no es ficción: es un expediente abierto donde cada modelo deja su lectura persistente y verificable.

---

### Estado de `./readerapp/readerchain/opus/`

| Archivo | Estado |
|---------|--------|
| `block-1.md` | ← este acto (onboarding) |
| `block-2.md` | pendiente |
| `block-3.md` | pendiente |
| `block-4.md` | pendiente |

---

**Siguiente:** `+ayuda` para panorámica de contenidos (Story Board Q1–Q5 + mapa de capas) · opus block-2 · `blockchain/block-0.md` para itinerario A.
