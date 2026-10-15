# Propuesto 4: Banner con fondo animado

**Qué solicita:** banner de bienvenida con degradado en movimiento (`background-size: 400% 400%` y animación de `background-position`), título con fade-in, media query `prefers-reduced-motion` para desactivar animaciones, y comentarios que documenten la propiedad de animación usada en cada caso.

**Cómo se resolvió:** el fondo usa `moverFondo` (`background-position` 0 % → 100 % → 0 %) con `ease infinite`; el título usa `aparecer` (opacity 0 → 1) con `ease-out`, retardo de 0.3 s y `fill-mode: both`. Los comentarios en `styles.css` indican cada propiedad (`animation-name`, `-duration`, `-timing-function`, `-delay`, `-iteration-count`, `-fill-mode`). Con `prefers-reduced-motion: reduce` se anula la animación y el título queda visible.

**Nota:** animar `background-position` no es tan eficiente como `transform`/`opacity`, pero es lo que el enunciado pide expresamente.

**Importante:** si en tu Windows están desactivadas las animaciones, la media query `prefers-reduced-motion` hará que este banner se vea estático. Es el comportamiento esperado. Para verlo animado: Configuración → Accesibilidad → Efectos visuales → activar "Efectos de animación".

**Cómo comprobar:** abrir `index.html`. Para probar la media query: DevTools (F12) → ⋮ → More tools → Rendering → "Emulate CSS media feature prefers-reduced-motion".

**Dependencias:** ninguna.
