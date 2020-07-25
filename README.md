# JS-desde-cero
# Clase 1 Introduccion a JavaScript
## Variables

Las variables son definidas con: let + nombreDeLaVariable = valorADefinir(pueden ser un String,Boolean,Numero).
Es buena practica tener los nombreDeLaVariable en ingles.
Ademas, en vez de escribir let en cada variable, se puede separar por comas, para ahorrar un poco de codigo.Los valores de las variables se pueden reasignar
Ej: 
let number = 10,
    nombre = `Braian`,
    pais   = `Argentina`

Para ver lo que devuelve la variable, se puede utilizar la consola a traves de console.log(nombreDeLaVariable).

## Constantes
Es un valor constante, es decir que no puede variar, se define con const + nombreDeLaConstante = valorADefinir 

## Sintaxis: 
Para comentar utilizar // o /* */ , son utilizados para indicar que sucede en el programa UTILIZARLO ADECUADAMENTE SIN EXAGERAR.Tambien sirve para comentar codigo, es decir dejarlo sin utilizar.

## Tipos de Datos 
### Numeros
Son numeros: 1,70,600, 6.6,etc
### String
Son definidos con `Comillas simples al reves o backtips`, "Comillas dobles" , 'Comillas simples'.Es preferible utilizar con backtips ya que nos permiten hacer mas cosas 
como por ejemplo: concatenar 

let nombre = `Juan tiene ${number} a;os` 

#### Boolean 
Denotan un valor de verdad 
5 == 5 daria verdadero/true
5 == `5` daria verdadero/true ya que JS asi
7 == 8 daria falso/false 

### Undefined 
Es cuando la variable no tiene ningun valor asignado o definido

### Null
Es cuando la variable nunca fue creada 

### Symbol()

### Arrays 
Guardan mas de un valor por ejemplo let numbers = [1,2,5,6.7] son datos del mismo tipo

### Object 
Es un tipo de dato que posee varios datos ya sea del mismo o diferente tipo
let data = {
    nombre: `Juan`,
    apellido: `Perez`,
    Edad: 21
}

### typeof 
Devuelve el dato que le pasaste en forma de String
let prueba = 3
typeof data devuelve `object`

#Clase 2  Como funciona JavaScript?
