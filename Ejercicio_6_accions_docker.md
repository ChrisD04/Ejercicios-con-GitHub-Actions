Ejercicio 6: Acciones de Docker en GitHub Actions

Preguntas

1. ¿Cómo se relacionan los contenedores con procesos en el SO?

- Un contenedor es un proceso aislado dentro del sistema operativo.
- Docker utiliza namespaces y cgroups del kernel de Linux para aislar procesos:
  - Namespaces: aíslan procesos, red, sistema de archivos, PID, etc.
  - Cgroups: limitan recursos (CPU, memoria, I/O) que puede usar el contenedor.
- Cada contenedor se ejecuta como un proceso normal en el SO host, pero con un entorno virtualizado.

Ejemplo: Al ejecutar docker run, el contenedor aparece como un proceso en el host (ps aux | grep docker).

2. ¿Qué recursos del SO usa Docker?

Docker utiliza los recursos del sistema operativo host de la siguiente manera:

- CPU: para ejecutar los procesos dentro del contenedor.
- Memoria RAM: para los procesos y aplicaciones que corren dentro.
- Almacenamiento: espacio en disco para imágenes, capas y volúmenes.
- Red: interfaces virtuales para comunicación entre contenedores y con el host.
- I/O: acceso a archivos según permisos y volúmenes montados.

Nota: Docker comparte el kernel del host, por lo que no virtualiza un SO completo como una máquina virtual, lo que lo hace más eficiente.

3. Ventajas de testear en contenedores

- Aislamiento total: cada contenedor tiene su propio entorno, evitando conflictos con dependencias del host.
- Consistencia: el mismo contenedor puede ejecutarse en local, CI/CD y producción sin cambios.
- Reproducibilidad: cada build genera un contenedor limpio, sin residuos de ejecuciones anteriores.
- Escalabilidad: permite ejecutar múltiples contenedores en paralelo para tests masivos.
- Portabilidad: los contenedores funcionan igual en cualquier sistema con Docker instalado.
