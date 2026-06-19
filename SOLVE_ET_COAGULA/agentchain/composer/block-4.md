# User

Cada enciclopedista es un mundo. Además hay enciclopedistas enquistados que forman la élite de libreros oficial y oficiosa haciendo que la experiencia del enciclopedista sea una aventura a veces de edición en solitario en un desierto otras verdaderos pulsos con la ortodoxia o singulares y peculiares tensiones heterodoxas. Afortunadamente, wikipedia mantiene el histórico y dado un usuario podemos ver si es un usuario tranquilo de ora et labora que como hormiguita ha ido participando en a construcción de la gran ontología enciclopédica, si ha sido un traductor (se dice que traductore traditore), si ha sido un vigilante de un orden canónico. Al final, en la visión podemos escribir cosas como. Dependiendo de qué devuelva el histórico veremos a un enciclopedista silencioso colando bloques de datos en los artículos, o en su extremo, a un censor que no ha puesto una línea en un artículo y se mantuvo como un "revertidor". Podremos ver qué le interesa al enciclopedista y cuál fue su relación con el corpus. Ejemplos de algunas preguntas genéricas: ¿quiso abrir una vía cerrada? ¿quiso corregir algo? ¿quiso enlazar con otras wikipedias?

NOTA: Generaliza y abstrae mi párrafo anterior. Entiende cual es mi user intention y diseña un protocolo científico para radiografiar usuarios. No cierres el foco a lo literal de mis instrucciones.

Eres un periodista que no va a dar por sentado que quien lee conoce esta codebase ni el vocabulario interno para indexar y montar el corpus. Crea un artículo para "El usuario <nombre de usuario> es (o fue) un enciclopedista que..."

# Agent

**Composer · cabezal → celda 4 ** Protocolo.

---

# Radiografía del enciclopedista: un protocolo a partir del historial de ediciones

Wikipedia no guarda solo artículos: guarda **quién** los tocó, **cuándo**, **cuánto** cambió cada vez y, a menudo, **por qué** (el resumen de edición). Eso permite tratar a cada cuenta no como un nombre en una lista, sino como una **trayectoria** — comparable a la de un investigador que deja huella en un archivo.

La intención detrás de preguntar «qué tipo de enciclopedista fue X» no es etiquetar por deporte. Es **inferir relación con el conocimiento compartido**: si alguien construye en silencio, traduce, vigila un canon, abre caminos cerrados o solo deshace el trabajo ajeno. El historial público de MediaWiki es la radiografía.

## Protocolo REIC (Ritmo · Estrategia · Interacción · Corpus)

Cuatro ejes, medibles sin acceso privilegiado — solo la API de contribuciones y, cuando hace falta, el historial del artículo:

| Eje | Qué mide | Indicadores |
|-----|----------|-------------|
| **R — Ritmo** | Cómo distribuye el trabajo en el tiempo | Duración activa; ediciones/día; concentración vs dispersión vitalicia |
| **E — Estrategia** | Qué tipo de acto editorial predomina | Ratio adición/eliminación; tamaño medio del cambio; traducción; ampliación de secciones; reversiones |
| **I — Interacción** | Relación con otros editores | Solitario vs pulso; guerras de edición; reverts mutuos; comentarios en resúmenes |
| **C — Corpus** | Dónde y sobre qué temas opera | Nº de artículos; dominancia en pocos títulos; coherencia temática; enlaces internos («véase también») |

**Preguntas genéricas** (no cerradas) se derivan de los ejes:

- ¿Abrió una vía cerrada? → **C** (artículo antes/después del usuario) + **E** (primeras ediciones masivas, traducción).
- ¿Quiso corregir o reescribir? → **E** (micro-edits vs bloques; secciones nuevas).
- ¿Quiso enlazar mundos? → **C** (dispersión temática; secciones de enlaces; traducción interwiki implícita).

**Salida del protocolo:** un párrafo de síntesis bajo la plantilla *«El usuario X es (o fue) un enciclopedista que…»*, más una etiqueta compuesta (ningún arquetipo puro en la práctica).

