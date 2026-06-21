# User 7

El vestuario ya tenía espejo: ¿hablaron en las páginas de usuario mientras la pista principal tenía el compás denso? Dame los logs de side-channel con marcas y oldids talk.

# Agent Reader

¡Hacklab! El bloque 4 cerró el baile en la **pista principal** (*Pseudociencia*). Pero el forcejeo no fue solo commits: el **vestuario** —las páginas de usuario (UT)— registró el diálogo que el diff del artículo no muestra.

Desplegando visor de **logs de side-channel** (`article_refs[]` en manifest talk)…

````carousel
<div align="center">
  <h2>🪞 EL VESTUARIO YA TENÍA ESPEJO</h2>
  <p><em>Fuente: talk-cache · `agentchain/composer/block-13.md`</em></p>
</div>

> **TESIS:** Noviembre 2007 **sí hubo conversación** —pero no en la sala del artículo— sino en UT Analiza y UT SolveCoagula.

🟢 [Dato Wiki · `cache/audit-talk.json`]: **80/80** cuerpos talk cacheados; ventana nov 2007: **48/48** (100 %).

| Vista talk | Revisiones oct–nov 2007 | Cuerpo en caché |
|------------|-------------------------|-----------------|
| [Discusión:Pseudociencia](https://es.wikipedia.org/wiki/Discusión:Pseudociencia) | **0** | vacío |
| [Usuario discusión:Analiza](https://es.wikipedia.org/wiki/Usuario_discusión:Analiza) | 46 | 100 % |
| [Usuario discusión:Ignacio_Icke](https://es.wikipedia.org/wiki/Usuario_discusión:Ignacio_Icke) | **0** | vacío |
| [Usuario discusión:SolveCoagula](https://es.wikipedia.org/wiki/Usuario_discusión:SolveCoagula) | 34 | 100 % |

<!-- slide -->
<div align="center">
  <h2>📅 PULSO 10 NOV — REVERT ANCHOR 12719652</h2>
</div>

🟢 [Dato Wiki · artículo]: [12719652](https://es.wikipedia.org/w/index.php?title=Pseudociencia&oldid=12719652) — Analiza, 19:18 UTC, −108 874 bytes, «¿Vamos a dialogar o no?».

🟢 [Dato Wiki · talk · oldid 12719797](https://es.wikipedia.org/w/index.php?title=Usuario_discusión:Analiza&oldid=12719797): Tercero advierte que eliminar >100 kb «sin argumentación racional» constituye vandalismo — **Δ ~0,1 h**.

🟢 [Dato Wiki · talk · oldid 12720101](https://es.wikipedia.org/w/index.php?title=Usuario_discusión:Analiza&oldid=12720101): SolveCoagula: «Reporto tu actitud por vandalismo a un bibliotecario» — **Δ ~0,5 h**.

🟢 [Dato Wiki · talk · oldid 12719917](https://es.wikipedia.org/w/index.php?title=Usuario_discusión:SolveCoagula&oldid=12719917): Analiza explica su reversión «temporal para consensuar» — **Δ ~0,1 h**.

🟢 [Dato Wiki · talk · oldid 12720477](https://es.wikipedia.org/w/index.php?title=Usuario_discusión:Analiza&oldid=12720477): Retama ofrece mediación, cita `Discusión:Pseudociencia#Guerra_de_ediciones` — **Δ ~1,2 h**.

🟡 [Inferencia Agentchain · `agentchain/composer/block-13.md`]: Quien pregunta «¿dialogar?» en el resumen del artículo deja su argumento desarrollado en la **UT del otro**, no en la sala común.

<!-- slide -->
<div align="center">
  <h2>📅 ENTRE PULSOS — NEGOCIACIÓN EN UT</h2>
</div>

🟢 [Dato Wiki · talk · oldid 12736728](https://es.wikipedia.org/w/index.php?title=Usuario_discusión:SolveCoagula&oldid=12736728): Retama advierte bloqueo si vuelve a acusar vandalismo (11 nov).

🟢 [Dato Wiki · talk]: Bloqueo 31 h a SolveCoagula (12 nov) — registro en UT, invisible en diff del artículo.

🟡 [Inferencia Agentchain · block-13]: PVN y «vandalismo» en el diff son etiquetas de una línea; en talk son argumentos con plantillas, citas de Sagan, tamaño de artículos.

⚪ [Blanco Explícito · estructural]: [Discusión:Pseudociencia](https://es.wikipedia.org/wiki/Discusión:Pseudociencia) = **0** revisiones 2007 (probe block-15).

⚪ [Blanco Explícito · ventana]: UT Ignacio_Icke sin actividad en el pulso (primera UT **2010**).

<!-- slide -->
<div align="center">
  <h2>✅ VALIDACIÓN VESTUARIO</h2>
</div>

| Afirmación | Estado |
|------------|--------|
| 48 cuerpos talk nov 2007 cacheados | 🟢 Validado |
| 15 alineaciones ±24 h con 12719652 / 12909144 | 🟢 Validado (`audit-talk.json`) |
| Diálogo UT mismo día revert Analiza | 🟢 Validado (oldids arriba) |
| Sala del artículo activa en 2007 | 🟢 Negativo (0 revisiones) |
| UT Ignacio en pulso | ⚪ Vacío estructural |
| Ensayo privado off-wiki | ⚪ No validable |

🔴 [Deducción del Lector]: El vestuario no contradice la pista: la **completa**. Quien solo lee commits ve forcejeo de bytes; quien abre UT ve forcejeo de palabras.
````

**Cierre del ⚪ obsoleto del bloque 4:** ya no preguntamos «¿hablaron?» — preguntamos **dónde**. Siguiente paso: dos carriles, un metrónomo (block-8).
