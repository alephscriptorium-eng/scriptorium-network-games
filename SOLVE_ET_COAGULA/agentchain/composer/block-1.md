# User

@./GAMES/SOLVE_ET_COAGULA/index.md

El dispositivo linea es un navegador con cache. ¿Cuál es el estado actual?

En el registro de solve et coagula tengo el tramo de máxima acción. Quiero completar el registro con las entradas antes y después que entiendo serán menos, vemos cómo es y decidimos. El objetivo:

- Tener una snapshot antes de que el usuario SolveEtCoagula empiece.
- Tener una snapshot al final de que el usuario complete a intervención

Delta entre una y otra.


# Agent

**Composer · cabezal → celda 1.** Cinta leída. Navegador inspeccionado.

## Estado del dispositivo `linea-aleph`

| Capa | Estado | Detalle |
|------|--------|---------|
| **Núcleo** (677 registros) | ✅ materializado | `manifest.json`, `registros/`, 99 milestones |
| **Caché extremos** | ✅ fetch hecho | `11663303` y `12370021` en `cache/snapshots/` |
| **Índice** | ✅ | `INDICE.md` con tabla de extremos y hitos |
| **Delta extremo** | ⚠️ agregado, curación pendiente | `snapshots/delta-extremo.md` — `status: pending` |
| **Snapshot inicial** (r0677) | ❌ sin fetch | `11951034` — primera edición SC; `fetched: false` |
| **Viajes hipervinculados** | 🔲 bajo demanda | `cache/viajes/` según skill navegador |

El dispositivo funciona como navegador-caché: los cuerpos viven en `.wikitext`; markdown solo indexa y cura.

## Objetivo de la celda: extremos + delta

### Antes — `snapshots/previo/`

| Campo | Valor |
|-------|-------|
| oldid | **11663303** |
| fecha | 28 sep 2007 |
| usuario | **Dhidalgo** (no SolveCoagula) |
| bytes | **472** |
| caché | ✅ `cache/snapshots/11663303.wikitext` |

Cuerpo: miniesbozo Popper (~8 líneas). Sin registro en `linea.md`. Es el **antes** correcto.

### Después — `snapshots/final/`

| Campo | Valor |
|-------|-------|
| oldid | **12370021** |
| fecha | 07:39 27 oct 2007 |
| usuario | SolveCoagula |
| registro | `r0001` |
| bytes | **161 504** |
| caché | ✅ `cache/snapshots/12370021.wikitext` |

Cuerpo: artículo expandido (Historia, secciones ontología, Matrix, falsacionismo…). Es el **final del export `linea.md`**.

### Delta extremo (previo → final)

| Métrica | Valor |
|---------|-------|
| Δ bytes neto | **+161 032** (472 → 161 504) |
| Registros intermedios | **677** |
| Milestones curados | **99** (deltas individuales en `registros/`) |
| Diff WP | [oldid=11663303 → 12370021](https://es.wikipedia.org/w/index.php?title=Problema_de_la_demarcación&diff=12370021&oldid=11663303) |

El tramo previo es mínimo (stub); el núcleo es denso (677); los extremos ya están cacheados.

## Tercer extremo útil (no pedido, pero visible)

`snapshots/inicial/` — oldid **11951034**, 10 oct 2007, «Traducción completa del original en inglés», **16 056 bytes**. No es el «antes» (eso es previo/Dhidalgo); es el **arranque** de SolveCoagula: de 472 bytes a 16K en un salto. Sin fetch aún.
