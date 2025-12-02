Ejercicio 2: Almacenamiento en caché de dependencias

1. ¿Cuánto tiempo se ahorra con el caché?

El uso de caché reduce significativamente el tiempo de ejecución del pipeline. 
En la práctica:
- Primer run (sin caché): la instalación de dependencias puede tardar entre 1 y 3 minutos en proyectos pequeños.
- Runs siguientes (con caché): la restauración e instalación mínima dura entre 10 y 30 segundos.
- Porcentaje de ahorro aproximado: entre 50% y 90%, dependiendo del tamaño del proyecto.

2. ¿Qué pasa si cambias el package.json?

Al modificar el archivo package.json y, por ende, el package-lock.json:
- El hash de la clave del caché cambia.
- El pipeline no reutiliza la caché anterior (cache miss).
- Se realiza una nueva instalación de dependencias.
- GitHub Actions guarda una nueva caché con la nueva clave, asegurando consistencia en las dependencias.

3. ¿Cómo se relaciona esto con sistemas de archivos en el SO?
- La caché se guarda en el sistema de archivos del runner (disco temporal del job).
- Evita descargas repetidas de red y reduce operaciones de I/O.
- La eficiencia del cache depende de las características del sistema de archivos: latencia, throughput y espacio disponible.
- En resumen, el cache complementa la gestión de archivos del sistema operativo para optimizar rendimiento y tiempos de ejecución.
