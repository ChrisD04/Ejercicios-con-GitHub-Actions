Ejercicio 10 – Desempeño y Recursos

Durante la ejecución del workflow se monitoreó el uso de CPU, memoria
y disco antes y después de una operación pesada simulada.

El mayor consumo se observó en el uso de disco y memoria durante
la instalación de dependencias con npm install.

La CPU no presentó cuellos de botella significativos debido a la
disponibilidad de múltiples núcleos en el runner ubuntu-latest.

Para optimizar el uso de recursos se recomienda:
- Implementar cache de dependencias
- Utilizar npm ci en lugar de npm install
- Reducir operaciones innecesarias
- Dividir el flujo en etapas más pequeñas

Estas optimizaciones mejoran el desempeño y reducen el tiempo
total de ejecución del pipeline.
