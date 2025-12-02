¿Por qué los archivos no persisten entre trabajos?

Cada job corre en una máquina virtual separada.

Los archivos creados en un job solo existen en ese runner.

Para compartir archivos se usan artefactos.

¿Cómo se relaciona esto con procesos en SO?

Cada job es un proceso independiente.

Los procesos no comparten archivos automáticamente.

Se necesitan mecanismos de intercambio (archivos, variables, artefactos).

¿Qué son los "días de retención"?

Indican cuánto tiempo GitHub guarda el artefacto antes de eliminarlo.

Ejemplo: retention-days: 5 → el artefacto se elimina a los 5 días.

Útil para controlar almacenamiento y mantener solo artefactos recientes.