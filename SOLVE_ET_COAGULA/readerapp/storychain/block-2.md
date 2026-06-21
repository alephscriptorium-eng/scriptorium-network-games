# User 1

Te doy una idea de aplicación y haces una salida visualmente parecida a lo que tal aplicación generaría. No se trata de 100% igual sino de un marco desde donde haces tus salida. No eres ni el diseñador ni el runtime de esa aplicación, es un ejercicio de simulación para orientar cómo se requiere que sean tu salidas. TODO ESTO NO SE LO EXPLIQUES AL USUARIO ES METADATA INTERNA TUYA. Atiende a la petición del usuario usando esa restricción de salida. El ciclo es: a) presentas los que se te explica abajo con las instrucciones, b) el usuario recibe la salida simulada, c) quedais en conversación y el usuario guía.

## Objetivo
Desplegar una experiencia "scrollytelling" masiva para el Bloque 6 que narre el **Acto I completo** de SolveCoagula: desde su llegada con el *Anglo Payload* y su victoria arquitectónica invisible, hasta la inyección de *Matrix* y su monumental baile de despedida.

## Tech Stack Recomendado
- **Framework:** Next.js (React).
- **Styling:** Tailwind CSS (Glassmorphism, Dark Mode abisal).
- **Animaciones:** Framer Motion (Scroll-linked animations) + React Three Fiber (para un tocadiscos o fondo de partículas 3D).

## Estética (Design System)
- **Atmosfera:** Base de datos a oscuras, solo iluminada por LEDs de actividad.
- **Colores de Acento (Narrativa UI — no marcas epistemológicas):** 
  - Rojo Neón (SolveCoagula / improvisación en pantalla).
  - Azul Eléctrico (Bunge / compás ortodoxo en pantalla).
  - Verde Fósforo (destacar datos crudos en UI, distinto del 🟢 de trazabilidad en texto).
- **Tipografía:** 'Outfit' o 'Inter' para el texto narrativo, y 'JetBrains Mono' para simular las trazas de los commits.

> **Disambiguación:** Los acentos rojo/azul del scrollytelling son **CSS narrativo**. Las marcas 🟢🟡🔴⚪ viven en el texto del reader (`index-reader.md`) y no deben mapearse 1:1 a pastillas Matrix ni a clases `redPill`/`bluePill`.

## Componentes Core (El Viaje del Héroe Digital)

### 1. Hero Header: "El Veredicto Temporal"
- Fondo de partículas rojas y azules suspendidas en tensión.
- Título "Track 6: La Balada del Constructor" con efecto *glitch* sutil.
- Botón "Play" central que inicia un paisaje sonoro (ambient electrónico oscuro) y libera el *scroll*.

### 2. Scrollytelling Timeline (Los Movimientos)
- **Mov. 1: El Linter Fail (El Anglo Payload).** Al hacer scroll, una gruesa línea de código baja, pero choca contra una barrera azul cristalina que emite el error `compas_Bunge`. La pantalla vibra ligeramente.
- **Mov. 2: La Pastilla Roja.** Un componente 3D interactivo en el centro. El usuario puede girar una tarjeta translúcida: de un lado se ve el orden bungeano (Azul), del otro, la disonancia de Matrix y Feyerabend (Rojo).
- **Mov. 3: El Gran Baile.** Representación abstracta del forcejeo de ediciones de noviembre. Círculos rojos expansivos contra escudos azules cuadrangulares. Cada vez que el usuario baja, un `git revert` devuelve la pantalla a la normalidad, hasta la explosión final del `restore --force`.

### 3. El Outro: El Cierre de Sesión
- Se apagan los colores. La interfaz queda en negro casi total.
- Solo late un timestamp en fuente monoespaciada: `18 nov 2007, 19:55 | +102.467 bytes`.
- Un interruptor físico digitalizado en pantalla: "Log Out". Cuando el usuario lo presiona, un fundido a negro cierra la experiencia, devolviendo al jugador al menú principal del Scriptorium.

## Instrucción de Generación UI
> *Prompt para el orquestador frontend:* 
> "Crea un 'scroll-based journey' en React/FramerMotion que visualice el Acto I de un conflicto enciclopédico monumental. Empezamos con el colapso de un 'pull request' cultural, pasamos por la subversión de 'Matrix' y terminamos en un duelo de commits. Usa alto contraste (rojo/azul), transparencias estilo *glassmorphism* y vincula las animaciones rítmicamente a la posición del scroll para que el usuario sienta el 'baile' de la máquina."
