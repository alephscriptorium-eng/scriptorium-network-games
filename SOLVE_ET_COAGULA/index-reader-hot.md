# index-reader — estado de sesión

Activador: [`index-reader.md`](index-reader.md). **Leer al inicio** de cada turno; **reescribir** al cambiar itinerario, posición o readerapp.

```
modelo: opus
itinerario: C-readerapp
posicion: readerapp/storychain/block-2.md
reader_chain: ./readerapp/readerchain/opus
sesion_iniciada: true
ultimo_turno: 2026-06-21
```

Traje: [`reader-traje.hot.md`](reader-traje.hot.md) · engines: [`engines-active.json`](../../network-engine/aleph-context/engines-active.json)

## Turno

1. Sincronizar hot files (este archivo + traje + `engines-active.json`).
2. Si `traje:puesto` — pipeline completo en [`disfraz-rude-bot/SKILL.md`](../../network-engine/agents/skills/disfraz-rude-bot/SKILL.md) (cabecera → calibración → caché → checklist → emitir).
3. Actualizar `posicion`, `itinerario`, `reader_chain` y `ultimo_turno` al cerrar.
