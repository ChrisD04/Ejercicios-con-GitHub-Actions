Ejercicio 3: Variables de Entorno y Secretos

1. ¿Por qué son importantes las variables de entorno en SO?
-----------------------------------------------------------
- Permiten configurar parámetros del sistema o aplicaciones sin modificar el código.
- Facilitan portabilidad y manejo de distintos entornos (desarrollo, pruebas, producción).
- Ejemplo: NODE_ENV=production indica que la app debe ejecutarse en modo producción.

2. ¿Cómo se pasan variables entre procesos?
-------------------------------------------
- Cuando un proceso se inicia, hereda las variables de entorno del proceso padre.
- En GitHub Actions, se pueden pasar usa
