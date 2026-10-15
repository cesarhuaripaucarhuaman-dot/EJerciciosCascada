# Ejercicio resuelto 2: Tarjetas con animación de entrada escalonada

**Qué solicita:** que tres tarjetas aparezcan al cargar la página con desvanecimiento y deslizamiento hacia arriba, una tras otra, usando `animation-delay` y `animation-fill-mode`.

**Cómo se resolvió:** las tarjetas parten con `opacity: 0`; la animación `entrada` (from/to) anima `opacity` y `transform: translateY()`. `forwards` mantiene el estado final y `:nth-child()` asigna retardos de 0.2 s, 0.5 s y 0.8 s.

**Cómo comprobar:** abrir `index.html` y recargar con Ctrl + F5. Para ver el efecto de `forwards`, quitarlo del atajo `animation`: las tarjetas vuelven a `opacity: 0` al terminar. También se puede probar `cubic-bezier(.68,-0.55,.27,1.55)` en lugar de `ease-out`.

**Dependencias:** ninguna.
