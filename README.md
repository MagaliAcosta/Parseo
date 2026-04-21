# Parseo - Lenguaje: Gestor de tareas  

## Objetivo  
Orientado a la representación de rutinas y acciones cotidianas 

## Alcance
#### Permite
- Definir rutinas principales
- Declarar y asignar variables simples
- Ejecutar acciones simbólicas
- Mostrar información en pantalla
- Utilizar estructuras condicionales
#### Limitaciones
- No maneja estructuras de datos coplejas
- No posee POO
- No tiene manejo avanzadod de tipos

## Especificaciones léxicas
#### Palabras reservadas 
- rutina, inicio, fin, hacer, mostrar, si, sino, definir, como, accion
#### Identificadores
- Secuencia de letras y números
- Deben comenzar con una letra en minúscula
#### Constantes
- Números enteros
- Strings
- Booleanos
#### Operadores
> ==, !=, <, >, <=, >=
#### Símbolos especiales
> { } ( ) ;

## Especificaciones sintácticas
#### General
Todo programa debe comenzar con la palabra ``rutina``, seguida de un nombre y contener un bloque de ``inicio`` y ``fin``
  Ejemplo
  ```
  rutina nombreRutina inicio
      instrucciones
  fin
  ```
#### Sentencias
Un programa está compuesto por una secuencia de sentencias. Cada sentencia representa una acción o instrucción.  
Las sentencias pueden ser:
- asignaciones
- acciones
- condicionales
  #### Asignación de variables
  Se utiliza la palabra ``definir``, seguida del nombre de la variable, la palabra ``como`` y un valor.  
  Ejemplo
  ```
    definir x como 5;
    definir dia como "lunes";
  ```
  ##### Acciones
  Se pueden definir acciones propias dentro del programa utilizando la palabra ``accion``, seguida de un nombre y un bloque de instrucciones
  - Creación
    ```
      accion nombreAccion {
          sentencia | sentencias
      }
    ```
  - Uso: Las acciones se ejecutan mediante la palabra ``hacer``, seguida del nombre de la acción.
    ```
     hacer nombreAccion;
    ```
  ##### Condicionales
  Estructura:
  ```
    si condicion {
        sentencia | sentencias
    } sino {
        sentencia | sentencias
    }
  ```
  ##### Condicion
  Permiten hacer comparaciones entre valores con los operadores

## Especificaciones semánticas:
- ``rutina`` define el programa principal
- las variables pueden ser reutilizadas y modificadas, deben declararse ante de utilizarse
- ``hacer accion;`` no retorna valores
- ``mostrar("texto")`` imprime mensaje en pantalla
- ``si condicion {...}`` evalúa una condición lógica si es verdadera, ejecutan el bloque correspondiente


## EJEMPLOS
```
rutina ejemploVariable inicio

definir nombre como "Magali";
mostrar("Bienvenida");
mostrar(nombre);

fin
```

```
rutina energia inicio

definir energia como 5;

si (energia > 3) {
    mostrar("Puedo estudiar");
} sino {
    mostrar("Mejor descansar");
}

fin
```

```
rutina rutinaDiaria inicio

definir dia como "lunes";
definir energia como 2;

mostrar("Inicio del día");

si (dia == "lunes") {
    mostrar("Hoy hay obligaciones");

    si (energia > 3) {
        hacer estudiar;
    } sino {
        mostrar("Poca energía");
    }

} sino {
    mostrar("Día tranquilo");
}

mostrar("Fin del día");

fin
```
