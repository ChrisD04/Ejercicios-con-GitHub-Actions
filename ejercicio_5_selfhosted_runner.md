# Ejercicio 5: Runner autohospedado

**Nombre:** Corredores Autoalojados (Self-Hosted Runners)

**Objetivo:** Entender la diferencia entre runners de GitHub y propios.



 Descripción

Un **runner** es una máquina (virtual o física) que ejecuta los jobs de GitHub Actions.  
- **Runners alojados en GitHub:** proporcionados por GitHub, se configuran automáticamente.  
- **Runners autohospedados:** se instalan en tu propio hardware o servidor, con control total sobre recursos y personalización.



 Comparación de recursos

| Aspecto              | Alojado en GitHub       | Autoalojado             |
|----------------------|------------------------|-------------------------|
| Configuración        | Automático             | Manual                  |
| Mantenimiento        | GitHub                 | Tú                       |
| Costo                | Incluido / limitado    | Hardware propio          |
| Seguridad            | Aislado                | Tu responsabilidad       |
| Personalización      | Limitada               | Total                    |
| Recursos             | Fijos                  | Configurables            |


 Casos de uso típicos de runners autohospedados

- Repositorios privados que requieren acceso a recursos internos  
- Workflows que necesitan software específico preinstalado  
- Proyectos que requieren más CPU, RAM o almacenamiento de lo que ofrece GitHub  
- Integración con sistemas locales o bases de datos internas


 Respuestas a las preguntas

1. ¿Cuándo usarías un corredor autohospedado? 
   - Cuando necesitas más recursos que los runners de GitHub o acceso a entornos internos.  
   - Para ejecutar jobs que requieren software específico o licencias locales.  
   - Si quieres control total sobre personalización y mantenimiento del entorno.

2. ¿Qué consideraciones de SO son importantes? 
   - Sistema operativo compatible con GitHub Runner  
   - Actualizaciones de seguridad y parches  
   - Gestión de dependencias y librerías necesarias para los workflows

3. ¿Cómo afecta la seguridad del SO?
   - El runner autohospedado ejecuta código de GitHub Actions en tu máquina  
   - Riesgo de exponer tu red, archivos o credenciales si no está correctamente aislado  
   - Necesario aplicar buenas prácticas de seguridad: usuarios limitados, firewalls, permisos adecuados
