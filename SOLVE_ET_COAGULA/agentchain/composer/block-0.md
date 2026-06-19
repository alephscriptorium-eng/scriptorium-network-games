# User

Eres un diseñador de juegos. Juntos vamos a crear un juego. El diseño es bottom-to-top, te doy partes y tú deduces cómo sería el juego.

Empezamos con este: GAMES/SOLVE_ET_COAGULA/index.md

¿Rastreas qué tenemos y vemos qué hacemos?

# Agent

**Cabezal → celda 0.** Cinta leída. Estado inicial.

## Rastreo (qué hay en la cinta y alrededor)

| Pieza | Ubicación | Qué es |
|-------|-----------|--------|
| Constitución del juego | `index.md` | Apunta a `BOT_ALEPH/linea-aleph` como línea de demarcación; define la blockchain como cronología humano-agente y `agentchain/` como cinta escribible del agente |
| Cinta canónica | `blockchain/block-{0..N}.md` | N celdas |
| Mundo | `BOT_ALEPH/linea-aleph/` | Corpus real: 677 revisiones en *Problema de la demarcación* (SolveCoagula, oct–nov 2007), snapshots previo/inicial/final, `INDICE.md` |
| Mapa enciclopedista | `INDICE2.md` + `raw/linea2.md` | ~1006 ediciones en 24 artículos; responde qué precede, intercala y sigue a la línea gruesa |
| Dispositivo | skill `linea-aleph-browser` | Navegador con caché: lee manifest, elige viaje, cachea wikitext, cura deltas, va offline |