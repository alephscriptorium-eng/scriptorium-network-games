# User

Crea un artículo de prensa que...

... se basa en un agente de tipo [index-reader.md](../index-reader.md). En este caso, para ver cómo desde esta blockchain y el modo  [index.md](../index.md) mejoramos el feature [uichain](../uichain/) sin cerrarlo, dejándolo como aleph generativo no determinista.

Panel de estado juego:
- Widget Cache Navegador Wiki: visión sobre todo del delta entre lo cacheado y lo que faltaría por bajar; más predicción de zonas de la wikipedia que son calientes y sensibles de explorar aunque aún no se tengan concretos enalces.
- Widget Tramas-Story Board: visión general de las hilos y subtramas que contiene la blockchain.

Pregunta, ¿el protagonista y el resto de enciclopedistas compartieron git, pero también se guardaron las conversaciones entre ellos? ¿Tenemos posibilidad de reconstruir e integrar en caché y asociar a linea-aleph? Habría que crear el contenedor y dejar preparado para que se vayan descargando a demanda como la cache normal?

# Agent

**Composer · celda 12.**

## Artículo de prensa (consolidado)

### El tablero de lectura: ver el archivo antes de abrir el capítulo

El bloque anterior cerró un acto: ya no se preguntaba solo qué hizo SolveCoagula en la [Wikipedia en español](https://es.wikipedia.org/), sino **cómo leer** once capítulos de indagación sin confundir archivo con interpretación. Este bloque da un paso más: convertir esa meta-lectura en **panel de estado** —un tablero que el lector index-reader pueda abrir al entrar en sesión, como quien mira el mapa antes de elegir itinerario.

No es un cierre de interfaz. Es una propuesta de **uichain** abierta: cada sesión puede rediseñar el tablero; el aleph sigue siendo generativo y no determinista. Lo que se fija aquí no es la pantalla definitiva, sino **qué información** merece estar visible cuando alguien entra al juego Solve et Coagula.

---

### Widget Cache Navegador Wiki: cuánto archivo tenemos y dónde arde

Imaginemos un indicador que responda de un vistazo: *¿cuánto del histórico editorial ya podemos leer sin conexión, y qué falta?*

En el caso SolveCoagula, la respuesta es asimétrica. Sobre el [Problema de la demarcación](https://es.wikipedia.org/wiki/Problema_de_la_demarcación), el archivo completo del pulso suma **seiscientas setenta y siete** revisiones registradas; el cuerpo literal de apenas **una de cada tres** está disponible offline —unas **duzentas siete** con texto completo—, pero **todos los hitos ancla** del arco (el esbozo previo, la primera edición de SolveCoagula, el cierre de noviembre, la versión actual) sí están guardados. Sobre [Pseudociencia](https://es.wikipedia.org/wiki/Pseudociencia), el patrón se repite: **doscientas veintitrés** revisiones en ventana, **setenta y ocho** con cuerpo cacheado —algo más de un tercio—, y **ciento por ciento** de los milestones del pulso de noviembre.

Sobre el corpus **talk** (discusiones de usuario NS3), el tablero añade una tercera familia de barras según `audit-talk.json` (2026-06-21): **ochenta** cuerpos offline en **ochenta** revisiones de ventana (**100 %** global); la ventana nov 2007 está al **100 %** de cuerpos en las UT cacheadas. Dos vistas siguen en vacío explícito: [Discusión:Pseudociencia](https://es.wikipedia.org/wiki/Discusión:Pseudociencia) y `Usuario discusión:Ignacio_Icke` —justo la sala que Ignacio_Icke invoca al revertir—.

El widget no sería solo una barra de progreso. Mostraría el **delta**: qué revisiones faltan por bajar, agrupadas por oleada de prioridad —primero los padres de un diff caliente, luego el relleno intermedio—. Y marcaría **zonas calientes** aunque aún no tengan enlace concreto en el índice: la franja del **16 de octubre de 2007**, donde aparece por primera vez el módulo Matrix; el tramo **10–18 de noviembre**, donde Analiza e Ignacio_Icke revierten volcados masivos; los artículos satélite de filosofía de la ciencia que SolveCoagula tocó una sola vez con un «véase también». Son territorios sensibles para la narrativa aunque el mapa aún no los haya cableado todos.

El lector no necesita saber cómo se llama el script que baja cada revisión. Necesita saber si puede **afirmar** algo sobre un oldid concreto o debe marcar vacío explícito hasta el próximo viaje de caché.

---

### Widget Tramas–Story Board: el guion detrás de las preguntas

El segundo widget no resume Wikipedia: resume la **blockchain** —la secuencia de preguntas humano-agente que construyó el juego.

Cinco actos, doce bloques:

1. **Constitución** (0–4): diseño del juego, corpus archivado, protocolo para radiografiar enciclopedistas y escribir prensa exportable.
2. **Radiografía** (5–7): quién fue SolveCoagula, qué decía la enciclopedia antes y después, demarcación como taller y pseudociencia como campo de aplicación.
3. **Fricción** (8): noviembre de 2007, volcados y reversiones, Analiza e Ignacio_Icke frente al constructor.
4. **Profundización** (9–10): anatomía del módulo Matrix y su genealogía entre demarcación y pseudociencia.
5. **Meta-lectura** (11–12): index-reader, uichain, tablero de estado; de qué pasó a cómo se lee y qué falta en el archivo.

Subtramas visibles en el tablero: la balada transmedia de la cadena Gemini frente a la crónica forense del compositor; el hilo Matrix como artefacto móvil; la tensión ortodoxia bungeana / heterodoxia demarcatoria; **Talk-cache** (chip activo: `registros_cached > 0` en `audit-talk.json`; bloque 13 profundiza en UT). Ramas Gemini presentes en bloques 1–6; composer cubre 0–12. El widget permitiría saltar de un hilo a un bloque sin leer la cadena entera —como un storyboard de serie— manteniendo visible en qué acto estamos.

---

### Compartieron el mismo repositorio, pero ¿guardaron las conversaciones?

La pregunta apunta a una distinción que Wikipedia hace explícita y que el juego hasta ahora solo ha explorado por una mitad.

**Sí compartieron un «git» editorial.** El historial público de cada artículo es una cadena de commits: autor, fecha, bytes añadidos o retirados, resumen de edición. SolveCoagula, Analiza e Ignacio_Icke dejaron huella en el mismo repositorio —[Pseudociencia](https://es.wikipedia.org/wiki/Pseudociencia)— con oldids verificables. Los resúmenes de edición son legibles en el diff: Analiza invoca la [política de punto de vista neutral](https://es.wikipedia.org/wiki/Wikipedia:PVN); SolveCoagula califica una reversión ajena de «vandalismo en curso»; Ignacio_Icke revierte a «versión consensuada» y añade **«ver discusión»** en [12909144](https://es.wikipedia.org/w/index.php?title=Pseudociencia&oldid=12909144).

Eso último es la pista: **las conversaciones no viven en el mismo namespace que los artículos.** En Wikipedia, el debate editorial paralelo se guarda en las **páginas de discusión** —por ejemplo, [Discusión:Pseudociencia](https://es.wikipedia.org/wiki/Discusión:Pseudociencia)— y, en su caso, en páginas de discusión de usuario. Son otro archivo público, con su propio historial de revisiones, enlazable pero separado del volcado de ediciones del artículo.

**¿Se pueden reconstruir e integrar?** Sí, con la misma política que el resto del corpus: API de MediaWiki (`w/api.php`), nunca scrape del HTML; snapshots por `oldid`; descarga a demanda en viajes, no volcado ciego. **¿Lo tenemos hoy?** Parcialmente. El contenedor `linea-aleph/cache/talk/` está operativo; oleadas block-13 poblaron las UT de **Analiza** (46/46 cuerpos, 100 %) y **SolveCoagula** (34/34, 100 %), con **quince** cruces talk↔artículo en ±24 h respecto a los reverts [12719652](https://es.wikipedia.org/w/index.php?title=Pseudociencia&oldid=12719652) y [12909144](https://es.wikipedia.org/w/index.php?title=Pseudociencia&oldid=12909144). La **sala de artículo** y la UT de **Ignacio_Icke** siguen sin cuerpo offline —vacío estructural (0 registros en ventana), no pendiente de fetch.

Integrar la capa talk no cambia los hechos del diff del artículo: cambia **qué podemos afirmar** sobre negociación previa al revert, argumentos fuera del wikitext del artículo, y si el «consenso» citado en la reversión dejó rastro textual recuperable. En UT Analiza/SolveCoagula ya es afirmable; en `Discusión:Pseudociencia` aún no.

---

### Aleph abierto: el tablero no cierra el juego

Mejorar uichain con este panel de estado no fija una UI canónica. Cada sesión del index-reader puede proponer otro layout —más denso en caché, más narrativo en tramas, minimalista para lectura página a página—. El tablero es **invitación a elegir viaje**: bajar la discusión que falta, seguir la cadena Gemini, o abrir el bloque 8 en crónica 5W.

SolveCoagula sigue siendo el hilo conductor, pero el objeto del bloque 12 es la **infraestructura de lectura**: ver de un golpe qué archivo tenemos, qué historia contamos, y qué conversaciones aún no hemos bajado del sótano de la enciclopedia.

---

## Panel de estado — especificación uichain

Tramitado en [`uichain/block-12-panel-estado.prompt.md`](../uichain/block-12-panel-estado.prompt.md). Resumen operativo:

| Widget | Fuente de datos (🟢 ground truth) | Render mínimo |
|--------|-----------------------------------|---------------|
| **Cache Navegador Wiki** | `linea-aleph/cache/audit-block10.json`; `linea-aleph/cache/audit-talk.json`; `manifest.json` + `pseudociencia/manifest.json`; `talk/*/manifest.json` (4 vistas); colas `scripts/fetch-priority-*.json`, `fetch-priority-talk-block13.json` (+ waveB si existe) | Barras artículo (demarcación / pseudociencia: registros % vs milestones %); barras talk por vista; `missing` oleada activa; heatmap oct–nov 2007; `article_alignment` ±24 h; satélites thin en `INDICE2.md` |
| **Tramas–Story Board** | `blockchain/block-{0..12}.md`; presencia `agentchain/composer/block-N.md`; `reader-chain/gemini/block-N.md` (1–6) | Cinco actos; chips Matrix · Noviembre/Analiza · Dual reader · **Talk-cache** (enabled si `audit-talk.totals.registros_cached > 0`); enlace a bloque |

Comportamiento aleph: el prompt uichain no prescribe CSS ni framework; cada generación puede variar disposición manteniendo los dos widgets y la política «no bloquear lectura si falta caché — mostrar vacío explícito». **No usar este bloque como única fuente numérica** — leer los audit JSON en cada sesión.

### Índice operativo index-reader (snapshot 2026-06-21)

| Métrica | Artículos (`audit-block10.json`) | Talk (`audit-talk.json`) |
|---------|----------------------------------|--------------------------|
| Demarcación registros / cuerpo | 677 / 207 (30,6 %) | — |
| Pseudociencia registros / cuerpo | 223 / 78 (35,0 %) | — |
| Milestones artículo | 100 % ambos | — |
| Talk global | — | 80 / 80 (100 %) |
| UT Analiza | — | 46 / 46 (100 %); milestones 100 % |
| UT SolveCoagula | — | 34 / 34 (100 %) |
| UT Ignacio_Icke | — | vacío explícito |
| Discusión:Pseudociencia | — | vacío explícito |
| Ventana nov 2007 (talk cacheado) | — | 48 / 48 cuerpos (100 %) |
| Cruce talk↔reverts artículo | — | 15 hits (`12719652`, `12909144`) |

Rutas relativas desde repo: `network-engine/linea-aleph/cache/`. Regenerar: `python scripts/audit_cache.py` (artículo) y `python scripts/audit_cache.py --corpus talk`.

---

## Contenedor talk-cache — linea-aleph

Respuesta a la pregunta del bloque: **sí, contenedor creado; población parcial por oleada block-13.**

### Capas Wikipedia y estado caché

| Capa | Namespace | Ejemplo | En caché actual |
|------|-----------|---------|-----------------|
| Ediciones artículo | NS0 | `Pseudociencia` | Sí (parcial ~35 % cuerpos) |
| Resumen de edición | meta en revisión | «ver discusión» | Sí (en meta/registro) |
| Página de discusión artículo | NS1 (`Discusión:`) | `Discusión:Pseudociencia` | **Vacío explícito** (0 registros 2007; probe `talk-sala-probe`) |
| Discusión de usuario Analiza | NS3 | `Usuario discusión:Analiza` | **Sí** (46/46 cuerpos) |
| Discusión de usuario SolveCoagula | NS3 | `Usuario discusión:SolveCoagula` | **Sí** (34/34) |
| Discusión de usuario Ignacio_Icke | NS3 | `Usuario discusión:Ignacio_Icke` | **Vacío explícito** |

### Árbol (`cache/talk/` — operativo)

```
linea-aleph/cache/talk/
  snapshots/{oldid}.wikitext
  snapshots/{oldid}.meta.json   # corpus: talk, namespace, linked_article
  anchors/
    discusion-pseudociencia.json
    usuario-discusion-analiza.json
    usuario-discusion-ignacio-icke.json
    usuario-discusion-solvecoagula.json
  viajes/                       # log fetch talk (CACHE_RUNBOOK)
```

Índices editoriales por vista: `linea-aleph/talk/{slug}/manifest.json`, `raw/linea.md`, `INDICE.md`. Auditoría agregada: `cache/audit-talk.json`.

### Integración con registros artículo

- Campo opcional `talk_refs[]` en `pseudociencia/registros/*/registro.md` cuando existan oldids talk contemporáneos.
- Milestone [12909144](https://es.wikipedia.org/w/index.php?title=Pseudociencia&oldid=12909144): `summary_cites_talk: true` → prioridad P1 en `discusion-pseudociencia` (ventana 10–18 nov 2007).
- Fetch: `fetch_snapshot.py --corpus talk --title "…" --oldid {N}` (misma política `mw_client.py`).

### Política de descarga

Oleada A = anclas blockchain (reverts 12719652, 12909144) — **ejecutada** en UT Analiza/SolveCoagula. Oleada B = historial talk nov 2007 paginado (`fetch-priority-talk-block13-waveB.json`). Oleada C (manifest) = 7 oldids Analiza pre-2008 — **cerrada** (`viajes/talk-block13-waveC.json`, 46/46). En block-12, «Oleada C sala» nombraba `Discusión:Pseudociencia` + UT Ignacio_Icke: vacío estructural (0 registros oct–nov 2007), distinto del manifest Wave C. Sin fetch masivo fuera de cola priorizada.

| Oleada | Viaje / manifest | Alcance | Estado |
|--------|------------------|---------|--------|
| A | block-13 wave A | anclas ±24 h reverts | ejecutada |
| B | `talk-block13-waveB` | nov 2007 paginado | ejecutada |
| C | `talk-block13-waveC` | 7 Analiza pre-2008 | **cerrada** (46/46) |
| C sala (block-12) | — | `Discusión:Pseudociencia` + UT Ignacio_Icke | vacío estructural |

**Vacío explícito vigente:** contenido textual de `Discusión:Pseudociencia` y UT Ignacio_Icke; afirmaciones sobre la sala citada en el revert 12909144 siguen limitadas a resúmenes de edición del artículo.

---

**Composer · celda 12 · panel estado + talk-cache · actualizado 2026-06-21.**
