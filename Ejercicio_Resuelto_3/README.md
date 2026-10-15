# Ejercicio resuelto 3: Loader (spinner) y barra de progreso

**Qué solicita:** un indicador de carga circular que gire sin fin y una barra de progreso que se llene y alterne de dirección, usando `animation-timing-function` y `animation-direction`.

**Cómo se resolvió:** el spinner usa `girar` (solo `to { rotate(360deg) }`) con `linear infinite`. La barra usa `llenar` (`scaleX(0)` → `scaleX(1)`) con `transform-origin: left center`, `ease-in-out infinite alternate`, evitando animar `width`.

**Cómo comprobar:** abrir `index.html`. El spinner gira a velocidad constante (probar `ease` para ver la diferencia) y la barra se llena y se vacía alternadamente. En Chrome/Edge: F12 → More tools → Animations, y reducir la velocidad al 10 %.

**Dependencias:** ninguna.
