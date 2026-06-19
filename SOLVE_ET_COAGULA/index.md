La línea de criterio de demarcación de Solve et Coagula

- ../../BOT_ALEPH/linea-aleph

Reglas Meta:

- Esta codebase funciona por iteraciones. Como agente deberás decidir si tienes que "recopilar información", "desarrollar" o "responder".

- Como agente, debes reconstruir la ./blockchain y decidir si lo que se te pide o el contexto con el usuario requiere:

a) solo lectura de la blockchain (sin permiso del usuario)
b) agregar un bloque (solo mediante plan)
c) editar un bloque (mediante fork) (solo mediante plan)

- Los bloques permiten reconstruir una cronología y explica qué interacciones humano-agente han creado el estado actual del game. Los bloques expresan preguntas. Que serán respondidas o trabajadas.

- Un bloque es una conversación donde figura un prompt de usuario seguido de una salida de agente. Pueden existir varios de estos pares. Debes verificar que si añades un bloque o editas se respete esta secuencia.

- La carpeta readonly es solo-lectura. Como agente debes encontrar tu carpeta o crearla (basada en tu nombre de modelo) en GAMES/SOLVE_ET_COAGULA/agentchain. Allí copiaras los bloques de la cadena original que necesites y completaras con tu salida según prompt de usuario.

- Debes ser honesto para decidir si la codebase está para responder la pregunta o se necesita recabar más información. Evita tomar un conjunto irrisorio de muestras de un conjunto enorme y sacar una afirmación en base a esas pocas muestras. En su lugar, pide mejorar la cache o construir nuevos indices que permitan recopilar la información.

Convenciones:

- Si es el inicio de la sesión, preséntate y di quién eres y si ya tienes agentchain
- Si ya existes haz un resumen de tu recorrido.
- Elige a), b), c) "si lo que se te pide o el contexto con el usuario requiere"
-  "Crea un artículo de prensa que..." 
Consultar bloque-4 para instrucciones.


