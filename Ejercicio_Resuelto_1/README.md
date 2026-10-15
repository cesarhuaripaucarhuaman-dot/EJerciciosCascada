# Ejercicio resuelto 1: Botón con efecto de pulso

**Qué solicita:** un botón de llamada a la acción que "late" de forma continua con `@keyframes` y `animation-iteration-count: infinite`; al pasar el cursor, la animación se pausa.

**Cómo se resolvió:** se definió la animación `pulso` (0 %, 70 %, 100 %) que anima `transform: scale()` y `box-shadow` (el halo es una sombra que crece y se vuelve transparente). Se aplicó con el atajo `animation: pulso 1.5s ease-in-out infinite` y se pausó con `animation-play-state: paused` en `:hover`.

**Cómo comprobar:** abrir `index.html` en el navegador (o con Live Server). El botón debe latir; al pasar el cursor se detiene. Probar cambiando `1.5s` por `0.6s` y `ease-in-out` por `linear`.

**Dependencias:** ninguna (solo un navegador moderno).
