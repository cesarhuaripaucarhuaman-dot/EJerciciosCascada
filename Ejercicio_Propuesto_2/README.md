# Propuesto 2: Menú con efecto de entrada

**Qué solicita:** barra de navegación con cinco enlaces que se deslicen desde la izquierda de forma escalonada (`animation-delay` creciente), mantengan su posición final (`forwards` o `both`) y tengan una transición de color al pasar el cursor.

**Cómo se resolvió:** `@keyframes deslizar` anima `opacity` y `translateX(-60px → 0)`. Cada enlace tiene un retardo mayor (0.1 s a 0.7 s) con `:nth-child()`. Se usó `animation-fill-mode: both`. La transición de color/fondo se aplica con `transition` en `:hover` (y `:focus-visible`).

**Cómo comprobar:** abrir `index.html` y recargar (Ctrl + F5); los enlaces entran uno tras otro. Pasar el cursor para ver el cambio de color.

**Dependencias:** ninguna.
