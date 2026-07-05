# Parseo - Lenguaje: Gestor de tareas  

## Objetivo  
Orientado a la representación de rutinas y acciones cotidianas 

---

## Alcance
- Registrar gastos e ingresos
- Permite el uso de variables para representar distintas cuentas/billeteras
- Implementa una única estructura condicional simple

---

## Especificaciones léxicas
#### Palabras reservadas 
`inicio`, `fin`, `gasto`, `ingreso`, `si`, `finsi`
#### Identificadores
Deben contener exclusivamente letras minúsculas y tener una longitud máxima estricta de 4 caracteres.
#### Constantes
Números enteros
#### Operadores
`=`, `>`
#### Símbolos especiales
`;`

---

## Especificaciones sintácticas
`<Biletera> := inicio <ListaSen> fin`  
`<ListaSen> := <Sentecia> <ListaSen>`  
`<Sentecia> := ID = NUM ;`  
`<Sentecia> := gasto ID NUM ;`  
`<Sentecia> := ingreso ID NUM ;`  
`<Sentecia> := si ID > NUM <ListaSen> finsi ;`

---

## Especificaciones semánticas:
- Al utilizar `gasto`, `ingreso` o `si`, verifica que el ID exista.
- `ID = NUM;` crea una cuenta nueva o actualiza el saldo del identificador
- La estructura condicional evalúa exclusivamente si el saldo actual de una cuenta es estrictamente mayor a una constante numérica.
- El `gasto` de un identificador no debe ser mayor al monto del mismo.

---

## Código

