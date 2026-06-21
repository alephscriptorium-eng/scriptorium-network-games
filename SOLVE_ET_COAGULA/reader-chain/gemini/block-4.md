# User 4

Acabamos de ver el choque anglo/Bunge. Antes de nombrar protagonistas: ¿cómo radiografiamos a un enciclopedista sin jerga de codebase? Enséñame el protocolo REIC como manual de campo para el hacklab — y el molde «El usuario X es (o fue) un enciclopedista que…».

# Agent Reader

Gemini 3.1 Pro (High) · traje:puesto · poderes:cache-nav,epistem-tags,anti-seguros,selective-query,vacio-explicito,ayuda · engines:main · forces:— · +force <id> · -force <id> · forces? · +poder <id> · -poder <id> · sin disfraz

> **Calibración engines** — main: mirar sin prisa.

🟢 [Dato Wiki / Ground Truth]: El historial de ediciones de MediaWiki —contribuciones por usuario, fecha, delta de bytes, resumen de edición— es **archivo público** (API y páginas de contribuciones). REIC no necesita acceso privilegiado: solo leer lo que ya está publicado.

🟡 [Inferencia Agentchain · `agentchain/composer/block-4.md`]: El protocolo **REIC** ordena la radiografía en cuatro ejes medibles:

| Eje | Pregunta de campo | Señal en el repo |
|-----|-------------------|------------------|
| **R — Ritmo** | ¿Pulso o hormiga? | Ventana activa; ediciones/día; concentración temporal |
| **E — Estrategia** | ¿Construye, traduce o revierte? | Ratio adición/eliminación; tamaño medio del diff |
| **I — Interacción** | ¿Solitario o forcejeo? | Reverts mutuos; guerras breves; tono en resúmenes |
| **C — Corpus** | ¿Dónde opera? | Nº de artículos; dominancia en pocos títulos; «véase también» |

🔴 [Deducción del Lector / Generativo]: En términos hacklab: REIC es el **scanner** antes del *profiling*. No etiqueta «bueno/malo»; describe *cómo* alguien empuja el grafo enciclopédico. La salida exportable es una sola frase-molde:

> *«El usuario **X** es (o fue) un enciclopedista que…»*

…seguida de una etiqueta compuesta (ningún arquetipo es puro: constructor + traductor + vigilante pueden coexistir).

### Tres preguntas que REIC responde sin jerga interna

1. **¿Abrió una vía cerrada?** → **C** + **E** (artículo antes/después; primer volcado masivo).
2. **¿Solo corrige o reescribe?** → **E** (micro-edits vs bloques; secciones nuevas).
3. **¿Enlaza mundos?** → **C** (satélites, traducción, puentes temáticos).

⚪ [Blanco Explícito]: REIC no asigna intención psicológica — solo trayectoria observable. La interpretación filosófica va en 🟡 agentchain, no en el molde.

---
**Siguiente:** [`blockchain/block-5.md`](../../blockchain/block-5.md) — aplicar REIC al caso **SolveCoagula** («El usuario SolveCoagula es un enciclopedista que…»).
