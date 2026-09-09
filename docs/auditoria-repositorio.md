# Auditoria del repositorio

## Objetivo

Registrar hechos verificables sobre la estructura, arquitectura y validacion del proyecto antes de proponer cambios.

## Rutas y simbolos relevantes

| Ruta o simbolo | Rol observado | Evidencia |
|---|---|---|
| `README.md` | Datos del proyecto y guia de uso de la plantilla. | Lectura directa del archivo. |
| `GDD.md` | Plantilla de GDD simplificado; todos los campos en `[PENDIENTE]`. | Lectura directa; busqueda de `[PENDIENTE]`. |
| `AGENTS.md` | Reglas de trabajo del agente sobre la plantilla. | Lectura directa del archivo. |
| `docs/README.md` | Orden de trabajo de los artefactos de proceso (8 documentos). | Lectura directa. |
| `docs/auditoria-repositorio.md` | Presente documento de hechos de la auditoria. | Lectura directa. |
| `docs/matriz-permisos.md` | Matriz de acciones permitidas/prohibidas del agente. | Lectura directa. |
| `docs/especificacion.md`, `docs/plan.md`, `docs/registro-intervencion.md`, `docs/evidencia-pruebas.md`, `docs/informe-final.md` | Plantillas de proceso sin completar. | Lectura directa. |
| `.gitignore` | Reglas genericas (`.env`, `.DS_Store`); sin reglas de Godot. | Lectura directa. |
| `project.godot`, `*.tscn`, `*.gd`, `*.cs` | No existen en el repositorio. | Glob y busqueda de archivos. |

## Flujo observado

No hay aun un proyecto creado en Godot: no existen `project.godot` ni escenas ni scripts del motor. En consecuencia no hay flujo de entrada de acciones, capas de juego ni comportamiento observable para auditar. El unico flujo existente es el documental de la plantilla (docs -> GDD -> especificacion -> plan -> evidencia -> informe). Godot no se detecto en el PATH del sistema (`godot`/`godot4` no encontrados).

## Pruebas y comandos disponibles

| Comando o prueba | Que verifica | Resultado inicial |
|---|---|---|
| `godot --version` / `godot4 --version` | Disponibilidad del binario de Godot en el PATH. | No encontrado (`Get-Command` sin resultados). |
| `git -C . rev-parse --is-inside-work-tree` | Si la carpeta es un repositorio git. | No es un repositorio git (exit 128). |
| Busqueda de archivos por patron | Presencia de artefactos del motor Godot. | Ninguno encontrado. |

## Hechos, supuestos y preguntas abiertas

- Hechos comprobados: el repositorio contiene solo la plantilla PIAPC (README, GDD, AGENTS, docs/ y .gitignore); todos los campos de datos estan en `[PENDIENTE]`; no hay proyecto del motor; no se detecta Godot en el PATH; la carpeta no es un repositorio git.
- Supuestos por verificar: la version concreta de Godot sera una 4.x; el nombre del proyecto y el problema de diseno los define la consigna; el binario de Godot se instalara o ubicara fuera del PATH estandar.
- Preguntas para consultar: nombre del proyecto; problema/consigna de diseno a resolver; version exacta de Godot (ej. 4.3, 4.4); si la catedra define el tipo o genero de juego; desde que version habra que registrar evidencia.
