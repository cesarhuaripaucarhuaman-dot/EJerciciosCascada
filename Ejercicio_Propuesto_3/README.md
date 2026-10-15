# Propuesto 3: Tres puntos de carga

**Qué solicita:** loader de tres puntos que aumentan y disminuyen su tamaño en secuencia ("ola"), con una sola `@keyframes` reutilizada con tres retardos distintos, repetición infinita y centrado en pantalla.

**Cómo se resolvió:** `@keyframes ola` (0 %/100 % pequeño, 50 % grande) anima `transform: scale()` y `opacity`. Los tres puntos comparten `animation: ola 1s ease-in-out infinite` y difieren en `animation-delay` (0 s, 0.15 s, 0.3 s). El centrado se logra con `display: grid; place-items: center` en `body`.

**Cómo comprobar:** abrir `index.html`; la ola de puntos debe repetirse sin fin.

**Dependencias:** ninguna.
