# Cuestionario: Sesión 09, Animaciones Web

**1. ¿Diferencia principal entre `transition` y una animación con `@keyframes`? Un caso de cada una.**
Una transición interpola entre solo dos estados (inicial y final) y necesita que algo cambie para dispararse (`:hover`, `:focus`, un cambio de clase). Una animación `@keyframes` define varios pasos intermedios y puede iniciar sola, repetirse, alternar y pausarse sin interacción.
- Transición: el cambio de color de un botón o enlace al pasar el cursor.
- `@keyframes`: un spinner de carga que gira indefinidamente o tarjetas que aparecen al cargar la página.

**2. ¿Para qué sirve `@keyframes` y qué diferencia hay entre `from/to` y porcentajes?**
`@keyframes` define el nombre de la animación y los fotogramas clave (los estilos en puntos concretos de la secuencia); luego se aplica con `animation-name`. `from/to` equivale a `0%`/`100%` y es práctico cuando hay solo dos pasos (ej.: `aparecer`). Con porcentajes se pueden definir tantos pasos intermedios como se necesiten (ej.: `rebote` con 0 %, 50 % y 100 %).

**3. ¿Qué hacen `animation-timing-function` y `animation-iteration-count`? Dos valores de cada una.**
- `animation-timing-function` define la curva de aceleración de la animación (cómo varía la velocidad). Valores: `ease-in-out`, `linear` (también `ease`, `steps(5)`, `cubic-bezier()`).
- `animation-iteration-count` define cuántas veces se repite la animación. Valores: `3`, `infinite`.

**4. ¿Qué efecto tiene `animation-fill-mode: forwards` y por qué es útil en animaciones de entrada?**
Hace que el elemento conserve los estilos del último fotograma al terminar la animación. En una animación de entrada (ej.: `opacity: 0` → `1`) evita que el elemento vuelva a su estado inicial (invisible) cuando acaba, de modo que permanece visible en su posición final.

**5. ¿Por qué animar `transform` y `opacity` en lugar de `width`, `height` o `top`? ¿Qué es `prefers-reduced-motion` y para qué sirve?**
`transform` y `opacity` el navegador las procesa en la GPU sin recalcular el diseño (layout) de la página, lo que da animaciones fluidas; animar `width`, `height`, `top` o `margin` obliga a recalcular el diseño en cada fotograma y perjudica el rendimiento.
`prefers-reduced-motion` es una media query que detecta si el usuario pidió reducir el movimiento en su sistema. Sirve para desactivar o reducir las animaciones (accesibilidad) por usuarios sensibles al movimiento, por ejemplo con `animation-duration: 0.01ms !important` o `animation: none`.
