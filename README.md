# Parseo - Lenguaje: Gestor de tareas  

## Objetivo  
Automatizar la gestión de una lista de tareas pendientes, pudiendo elegir quién la realiza y en qué orden, según prioridad  

## Alcance
- Crear tareas
- Modificar el estado de las tareas (pendiente, progreso, completada)
- Asignar responsable
- Listar tareas
- Asignar prioridad (alta, media, baja)

## Especificaciones léxicas
- tareaN, usuarioX, asignar, cambiarEstado, cambiarPrioridad, listar, crear, alta, media, baja, pendiente, progreso, completada

## Especificaciones sintácticas
- crear(tareaN)
- asignar(tareaN, usuarioX)
- cambiarEstado(tareaN, nuevoEstado)
- cambiarPrioridad(tareaN, nivel)
- listar()

## Especificaciones semánticas:
- crear(tareaN): genera una nueva tarea con el estado PENDIENTE, prioridad sin definir y responsable sin asignar; validarTarea: no debe haber tareas con el mismo nombre
- asignar(tareaN, usuarioX): asigna un responsable a la tarea, si ya tiene responsable lo reemplaza; validarQueExistaUsuario; validarQueExistaTarea
- cambiarEstado(tareaN, nuevoEstado): modifica el estado de la tarea; validarQueExistaTarea; validarEstado: debe ser pendiente, progreso, completada. No permite pasar de pendiente a completada directamente.
- cambiarPrioridad(tareaN, nivel): modifica la prioridad de la tarea; validarQueExistaTarea; validarPrioridad: debe ser alta, media o baja.
- listar(): muestra todas las tareas con nombre, estado, prioridad y responsable.
