# Propuesto 1: Logo con rebote

**Qué solicita:** un círculo/ícono que rebote verticalmente sin fin, con `@keyframes` de al menos tres porcentajes (0 %, 50 %, 100 %), `ease-in-out` y `alternate`, más una sombra en el suelo que se reduzca cuando el objeto está arriba.

**Cómo se resolvió:** `rebote` (0 %, 50 %, 100 %) mueve el círculo con `translateY` y lo aplasta ligeramente al tocar el suelo. `sombra` usa los mismos tiempos y anima `scale` y `opacity` (más pequeña y clara arriba). Ambas usan `0.9s ease-in-out infinite alternate`. Solo se animan `transform` y `opacity`.

**Cómo comprobar:** abrir `index.html`; la sombra debe achicarse mientras el círculo sube.

**Dependencias:** ninguna.
