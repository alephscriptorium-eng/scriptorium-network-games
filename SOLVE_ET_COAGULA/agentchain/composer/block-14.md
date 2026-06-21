# User

Crea un artículo de prensa que...

... visualiza el hallazgo del bloque 13: la conversación de noviembre 2007 no vivió en Discusión:Pseudociencia sino en páginas de usuario. Propón en uichain una línea de tiempo dual (carril artículo + carril talk) para el pulso 10–18 nov, con enlaces de alineación article_refs.

Opcional: borrador de sesión publicable en network-engine prensa que indexe los oldids talk clave sin duplicar el corpus.

# Agent

**Composer · celda 14.**

## Artículo de prensa (consolidado)

### El mapa que faltaba: dónde hablaron cuando el artículo ardía

El bloque anterior demostró que en noviembre de 2007 **sí hubo conversación** sobre [Pseudociencia](https://es.wikipedia.org/wiki/Pseudociencia), pero no donde el manual de Wikipedia sugiere buscarla. Este bloque convierte ese hallazgo en **geografía legible**: un mapa de cuatro ventanas —artículo, sala del artículo, bandejas de usuario— y dos pulsos sincronizados entre el **10** y el **18 de noviembre**.

No se repite la crónica entera del pulso. Se responde una pregunta de diseño editorial: *si el lector abre solo el diff del artículo o solo la sala de discusión, ¿qué parte del diálogo se pierde?*

---

### Cuatro geografías, un solo conflicto

Wikipedia no guarda la conversación en un solo sitio. Para el pulso de noviembre de 2007 conviene dibujar **cuatro parcelas**:

| Geografía | Qué registra en nov 2007 | Estado en el pulso |
|-----------|--------------------------|-------------------|
| **[Pseudociencia](https://es.wikipedia.org/wiki/Pseudociencia)** (artículo) | Commits: reverts, restauraciones, ±108 000 bytes | **Activo** —108 revisiones en el mes |
| **[Discusión:Pseudociencia](https://es.wikipedia.org/wiki/Discusión:Pseudociencia)** (sala) | Hilos del artículo | **Vacía** en la ventana oct–nov estudiada |
| **[Usuario discusión:Analiza](https://es.wikipedia.org/wiki/Usuario_discusi%C3%B3n:Analiza)** | Bandeja del revertidor del 10 nov | **Activa** —mensajes minutos después de [12719652](https://es.wikipedia.org/w/index.php?title=Pseudociencia&oldid=12719652) |
| **[Usuario discusión:SolveCoagula](https://es.wikipedia.org/wiki/Usuario_discusi%C3%B3n:SolveCoagula)** | Bandeja del constructor del volcado | **Activa** —réplicas cruzadas y seguimiento del 18 nov |
| **[Usuario discusión:Ignacio Icke](https://es.wikipedia.org/wiki/Usuario_discusi%C3%B3n:Ignacio_Icke)** | Bandeja del revertidor del 18 nov | **Sin actividad** en la ventana |

Quince revisiones de la capa *talk* caen dentro de **±24 horas** de los dos reverts ancla del artículo —[12719652](https://es.wikipedia.org/w/index.php?title=Pseudociencia&oldid=12719652) y [12909144](https://es.wikipedia.org/w/index.php?title=Pseudociencia&oldid=12909144)—. **Ninguna** pertenece a la sala del artículo. Todas viven en las páginas de Analiza o SolveCoagula.

Esa asimetría es el hallazgo del bloque 13 hecho visible: el archivo conversacional **no coincide** con el archivo canónico que el resumen de edición invoca.

---

### Dos carriles, dos pulsos (10–18 noviembre de 2007)

Imaginemos una línea de tiempo con **dos carriles sincronizados por fecha**:

**Carril superior — el artículo.** Cuatro hitos marcan el pulso:

1. **10 nov, 19:18 UTC** — Analiza revierte el volcado en [12719652](https://es.wikipedia.org/w/index.php?title=Pseudociencia&oldid=12719652): «¿Vamos a dialogar o no?»
2. **10 nov, 19:45 UTC** — SolveCoagula restaura en [12720368](https://es.wikipedia.org/w/index.php?title=Pseudociencia&oldid=12720368).
3. **18 nov, 18:55 UTC** — Ignacio_Icke revierte en [12909144](https://es.wikipedia.org/w/index.php?title=Pseudociencia&oldid=12909144): «versión consensuada **(ver discusión)**».
4. **18 nov, 19:55 UTC** — SolveCoagula restaura de nuevo en [12910974](https://es.wikipedia.org/w/index.php?title=Pseudociencia&oldid=12910974).

**Carril inferior — la conversación.** Los nodos no siguen la misma cadena lineal; se **alinean** con los reverts por proximidad temporal:

**Pulso del 10 de noviembre** (ancla [12719652](https://es.wikipedia.org/w/index.php?title=Pseudociencia&oldid=12719652)):

- **Δ 0,1 h** — SolveCoagula abre «Vandalismo en Pseudociencia» en la UT de Analiza ([12719797](https://es.wikipedia.org/w/index.php?title=Usuario_discusi%C3%B3n:Analiza&oldid=12719797)).
- **Δ 0,1–0,5 h** — Réplicas cruzadas: Analiza en la UT de SolveCoagula ([12719917](https://es.wikipedia.org/w/index.php?title=Usuario_discusi%C3%B3n:SolveCoagula&oldid=12719917), [12720326](https://es.wikipedia.org/w/index.php?title=Usuario_discusi%C3%B3n:SolveCoagula&oldid=12720326)); escalada de SolveCoagula en la UT de Analiza ([12720101](https://es.wikipedia.org/w/index.php?title=Usuario_discusi%C3%B3n:Analiza&oldid=12720101)).
- **Δ 0,5–1,2 h** — Retama declara «guerra de ediciones» y ofrece mediación en ambas UT ([12720477](https://es.wikipedia.org/w/index.php?title=Usuario_discusi%C3%B3n:Analiza&oldid=12720477), [12721439](https://es.wikipedia.org/w/index.php?title=Usuario_discusi%C3%B3n:SolveCoagula&oldid=12721439)), citando un mensaje en [Discusión:Pseudociencia](https://es.wikipedia.org/wiki/Discusión:Pseudociencia) que **no aparece** en el archivo de la ventana.

**Pulso del 18 de noviembre** (ancla [12909144](https://es.wikipedia.org/w/index.php?title=Pseudociencia&oldid=12909144)):

- **Δ 1,2–2,0 h** — Seguimiento en la UT de SolveCoagula ([12911274](https://es.wikipedia.org/w/index.php?title=Usuario_discusi%C3%B3n:SolveCoagula&oldid=12911274), [12912735](https://es.wikipedia.org/w/index.php?title=Usuario_discusi%C3%B3n:SolveCoagula&oldid=12912735)): Retama, Chabacano y la disputa sobre vandalismo frente a [PVN](https://es.wikipedia.org/wiki/Wikipedia:PVN).
- **Silencio** en la UT de Ignacio_Icke y en la sala del artículo pese al «ver discusión» del resumen de edición.

Entre ambos pulsos hay **ocho días** sin hito artículo en el mapa, pero el carril talk conserva colas alineadas (±24 h) que muestran que la negociación **no se cerró** el 10 de noviembre.

---

### Huecos que no deben colapsarse

Un mapa honesto marca también lo que **no** está:

1. **Sala vacía.** [Discusión:Pseudociencia](https://es.wikipedia.org/wiki/Discusión:Pseudociencia) no registra actividad recuperable en oct–nov 2007, aunque Retama afirma haber escrito allí y aunque Ignacio_Icke remite al lector a «discusión».
2. **UT de Ignacio_Icke muda.** Quien firma el revert consensual del 18 de noviembre no deja mensaje en su bandeja en la ventana estudiada.
3. **Desfase semántico.** «Dialogar» (Analiza), «vandalismo» (SolveCoagula), «consenso en discusión» (Ignacio_Icke) son tres gramáticas distintas; ninguna converge en un hilo único visible en la sala.

Colapsar esos huecos en silencio sería falsear la geografía. La visualización debe mostrarlos como **franjas etiquetadas**, no como ausencia de datos.

---

### Por qué hace falta verlo en dos carriles

Leer solo el historial del artículo produce una película de bytes: alguien borra, alguien restaura, alguien cita normas en el resumen. Leer solo la sala produce **vacío** para este pulso. Leer las UT exige **saltar de namespace en namespace** sin un índice que alinee fechas.

Una línea de tiempo dual —artículo arriba, talk abajo, conectores por Δ en horas— no resuelve el conflicto de 2007, pero **reparte las fuentes** como lo hace un periodista con dos agendas paralelas: la del hecho editorial y la del diálogo que lo acompaña o lo contradice.

El lector index-reader gana tres cosas:

- **Trazabilidad:** cada conector enlaza un oldid de artículo con uno o varios oldids talk verificables en Wikipedia.
- **Honestidad:** los huecos de sala e Ignacio UT permanecen visibles.
- **No determinismo:** el layout puede variar entre sesiones; los datos y enlaces no.

---

### Cierre index-reader

Este bloque no añade bytes nuevos al archivo. **Visualiza** lo que el bloque 13 ya demostró: la conversación de noviembre de 2007 vivió en páginas de usuario, no en la sala del artículo.

**Hecho de archivo:** 48 ediciones talk con cuerpo en la ventana nov 2007; 15 alineadas en ±24 h con [12719652](https://es.wikipedia.org/w/index.php?title=Pseudociencia&oldid=12719652) y [12909144](https://es.wikipedia.org/w/index.php?title=Pseudociencia&oldid=12909144); cuatro milestones artículo en el rango 10–18 nov.

**Propuesta de interfaz:** línea de tiempo dual 10–18 nov 2007 (especificación en sección siguiente).

**Vacíos no rellenados:** cuerpo del mensaje de Retama en la sala; actividad UT de Ignacio_Icke; hilos completos pre-2008 de la UT de Analiza fuera de la ventana nov.

---

## uichain — línea de tiempo dual (referencia)

Especificación completa: [`uichain/block-14-timeline-dual.prompt.md`](../../uichain/block-14-timeline-dual.prompt.md)

Resumen operativo para implementación:

| Elemento | Fuente | Notas |
|----------|--------|-------|
| Eje temporal | 10–18 nov 2007 UTC | Zoom opcional días 10 y 18 |
| Carril artículo | Milestones 12719652 → 12720368 → *(pausa 8 d)* → 12909144 → 12910974 | Desde block-8 / manifest artículo |
| Carril talk | 15 aristas `article_alignment` | audit-talk: vista, talk_oldid, article_oldid, delta_hours |
| Huecos | `discusion-pseudociencia`, `usuario-discusion-ignacio-icke` | `vacío_explícito` — franjas etiquetadas |
| Conectores | Δ ≤ 24 h | Etiqueta Δ; hover resalta pares |
| Layout | Aleph abierto | Scroll, swimlanes o curvas; datos fijos |

Criterios de aceptación y DevOps: ver prompt uichain. **No implementar UI en este bloque** — solo dejar la especificación cableada al hallazgo de prensa.

Borrador de sesión publicable (índice de oldids, sin corpus duplicado): `network-engine/data/sessions/solve-coagula-block14-prensa-draft.json` + `.md`.
