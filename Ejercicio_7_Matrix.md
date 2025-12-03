Ejercicio 7: Estrategia Matrix Avanzado

Preguntas

1. ¿Cuántas combinaciones se ejecutan?

- Se tienen 3 sistemas operativos: ubuntu-latest, windows-latest, macos-latest
- Se tienen 3 versiones de Node: 16, 18, 20
- Total de combinaciones base: 3 x 3 = 9
- Se excluye windows-latest con Node 16: 9 - 1 = 8
- Se incluye la combinación especial ubuntu-latest con Node 20 experimental: 8 + 1 = 9
- Total de combinaciones finales que se ejecutan: 9

2. ¿Cómo se ejecutan en paralelo?

- Cada combinación de la matriz se ejecuta como un job independiente.
- Los jobs se pueden correr al mismo tiempo, dependiendo de los runners disponibles.
- Cada job tiene su propio entorno aislado y ejecuta los pasos definidos.
- Se puede limitar el número de jobs en paralelo usando max-parallel, por ejemplo max-parallel: 5.

3. Límites de concurrencia en GitHub Actions

- Free: alrededor de 20 jobs concurrentes por repositorio.
- Pro/Enterprise: más jobs concurrentes según el plan.
- Jobs extra esperan en cola hasta que haya runner disponible.
- max-parallel permite controlar cuántos jobs de la matriz se ejecutan simultáneamente.
