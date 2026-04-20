# Parseo - Lenguaje: Gestión de tareas  

## Objetivo  
Automatizar la gestión de una lista de tareas pendientes, pudiendo elegir quién la realiza y en qué orden, según prioridad  

## Alcance
- Gestores: quiénes van a realizar la tarea
- Tareas: acción a realizar
- Estad: pendiente, en proceso o completada

## Especificaciones léxicas
- tarea, gestor, asignar, estado, prioridad

## Especificaciones sintácticas
- asignar(tarea, gestor)
- tarea nombreTarea(prioridad)

## Especificaciones semánticas:
- asignar(tarea, gestor): le asigna la acción que debe realizar al gestor
- prioridad: es un valor numérico del 1 al 10
