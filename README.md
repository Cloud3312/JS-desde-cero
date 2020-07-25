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
## Primitivos
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

### typeof 
Devuelve el dato que le pasaste en forma de String
let prueba = 3
typeof data devuelve `object`

## Compuestos 
### Arrays 
Guardan mas de un valor por ejemplo let numbers = [1,2,5,6.7] son datos del mismo tipo

### Object 
Es un tipo de dato que posee varios datos ya sea del mismo o diferente tipo
let data = {
    nombre: `Juan`,
    apellido: `Perez`,
    Edad: 21
}


#Clase 2  Como funciona JavaScript?
JS  es dinamnicamente tipado, es decir que el interprete deduce que es cada dato.Ademas de que las variables se pueden reedefinir(reasignar,pasarle un nuevo valor)

## Type coertion 
Es poder concatenar cosas 
true + 1 = 2  porque se considera a true como un 1 y a false como un 0
`Hola Mundo ` + 1 = `Hola Mundo 1`
Pero si se utiliza la multiplicacion daria NaN not a number

## Valor o referencia
Al usar un dato se lo puede usar por valor(number, boolean, String) o referencia(objeto y arrays)
A los que son por valor se lo puede modificar, mientras que los de referencia no, permanecen igual
Ej:
let number  = 60    
let number2 = number  
number2 = 70  <- al ser un Number y estar pasado por valor number 1 no cambia
Mientras que al  ser referencia cambian ambos valores
let number  = [1,3,4,5]    
let number2 = number
number2.push(6)
number  = [1,3,4,5,6]
number2 = [1,3,4,5,6]

## Operadores 
### Asignacion 
Le asignan el valor a una variable
=, +=, -=, /=, *=

### Comparacion (Binarios)
Comparan valores , devuelven un Boolean
==, ===, !=, !==, >, <, >=, <= 
5 == `5` devuelve True
5 === `5` devuelve False, ya que === se enfoca en el tipo de valor y dato 
Es conveniente evitar la doble igualdad ya que puede generar problemas
5 != `5` devuelve False ya que al ser un solo igual se centra solo en el valor, el != es distinto de 
5 !== `5` devuelve True ya que sucede lo mismo que el punto del triple igual

### Unarios 
typeof, ! (negacion)
!true devuelve False 
!0 devuelve True

### Aritmeticos 
+, -, *, /, % (te da el resto de la division), ++, --.
++ y -- son post aumento y decremento, si se lo pone a la izquierda contaria como un pre decremento y aumento

### Operador Ternario (3 Valores)
Funciona como un condicional, utiliza ? para que haga algo primero y si eso no se cumple hace lo que esta al lado de :
expresionQueDevuelveBoolean
? valorSiEsTrue
: valorSiEsFalse

### Operador Corto circuito
|| evalua el primer valor, si es verdadero te da el primero y si es falso te da el segundo
&& evalua el primer valor, si es falso te da el primero, si es verdadero te da el segundo

### Numeros
