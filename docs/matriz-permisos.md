# Matriz de permisos

Completa esta matriz antes de habilitar acciones de un agente. Una accion no declarada debe considerarse prohibida hasta consultar.

| Accion | Estado | Alcance o justificacion |
|---|---|---|
| Leer archivos del proyecto | Permitida | Lectura de plantillas para auditoria y contexto. |
| Buscar rutas y simbolos | Permitida | Glob y busqueda para verificar estructura real. |
| Editar archivos previstos | Pendiente | Solo README.md y docs/ de proceso, bajo confirmacion. |
| Ejecutar scripts documentados | Prohibida | Aun no hay proyectos del motor ni scripts. Git queda autorizado como herramienta documentada para reconciliar y publicar el estado actual. |
| Instalar dependencias | Prohibida | No se instalara nada sin autorizacion. |
| Usar red | Prohibida | No corresponde. |
| Publicar o subir cambios | Permitida | Solo el push del estado autorizado al remoto `ItalianoBruno/PlantillaAgente_PIAPC`. Autorizado por el estudiante el 2026-09-09. |
| Acceder a secretos o credenciales | Prohibida | No corresponde al trabajo. |

## Condiciones de detencion

- Detener y consultar si se detecta un proyecto del motor no declarado, cambios ajenos a la plantilla, o si la consigna modifica el alcance de la auditoria.
- Detener y consultar si una edicion o validacion falla sin causa comprendida.
