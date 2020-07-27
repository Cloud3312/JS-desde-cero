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
Es poder concatenar cosas, es la conversión automática o implicita de valores de un tipo de dato a otro (Ejemplo: de cadena de texto a número) 
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
#### toFixed()
devuelve el numero con la cantidad de decimales redondeados que vos quieras 
let number = 5.966
number.toFixed(2) devuelve 5.97

#### parseInt(string, 10) y parseFloat(string, 10)
parseInt convierte un numero que esta en forma de string a un numero entero
parseFloat convierte un numero que esta en forma de string a un numero decimal

### Math
#### .floor()
Se le pasa un numero y redondea para abajo
Math.floor(20.6) //devuelve 20
#### .ceil()
Se le pasa un numero y redondea para arriba
Math.ceil(20.4) //devuelve 21
#### .round()
Se le pasa un numero y redondea dependiendo de si es mayor a 5 para arriba y si es menor a 5 para abajo
#### .random()
Devuelve un numero random

Para hacer un sorteo se podria hacer Math.ceil(Math.random()*20) y devuelve un numero random entero de entre 0 y 20

## Strings
### Propiedades
Una **Propiedad** es un valor que tiene un dato.Por ejemplo: caracteristicas como edad, pais,direccion

#### .lenght
Devuelve la cantidad de caracteres que tiene un String
`Hola`.lenght devuelve 4

### Metodos 
Un **Metodo** es una operacion que el dato puede realizar, por ejemplo: acciones como trabajar,programar, disenar.
Existen metodos sin parametros como:
#### .trim()
Lo que hace es sacarle los espacios en blanco del inicio y final del String, **NO LOS ESPACIOS QUE ESTAN ENTRE MEDIO**
`   Hola    `.trim() devuele `Hola`
#### .toUpperCase()
Transforma el string que le pasemos a mayusculas
`hola`.toUpperCase() devuelve `HOLA`

#### .toLoweCase 
Transforma el string que le pasemos a minusculas
`HOLA`.toLoweCase() devuelve `hola`

Estos pueden ser utilizados por ejemplo, para hacer un cuestionario

let answer = prompt(`Cual es la capital de Argentina?`).trim().toUpperCase()   // Abre una ventana en el navegador con esa pregunta
let message =  answer === `ARGENTINA` 
               ? `Excelente, acertaste`                                        
               : `Respuesta incorrecta`
alert(message)

Se pueden encontrar caracteres con:

#### .indexOf()
Indica la posicion del elemento a buscar dentro del String
`Hola como estas`.indexOf(`o`) devuelve 1, ya que comienza a buscar en la posicion 0 del String, -1 si no lo encuentra

#### .lastIndexOf()
Indica la posicion ultima de lo que queremos a buscar 
`Hola amigos`.lastIndexOf(`o`) devuelve 9

#### .includes()
Indica si el String dado incluye lo que se le haya pasado como parametro
`https://ed.team/blog`.includes(`blog`) denota True

#### .startsWith()
Indica si el String dado comienza con lo que se le pasa como parametro
`https://ed.team/blog`.startsWith(`https://ed.team`)     // Denota True

#### endsWith()
Indica si el String dado termina con lo que se le pasa como parametro
`https://ed.team/blog`.endsWith(`blog`)                 //Denota True

### Manipular strings con metodos 
#### .replace()
`Hola mundo`.replace(`mundo`, `Miguel`)      //Esto devuelve `Hola Miguel`

#### .split(separator,[cuantity])
Separa el string dado en partes.Tambien se puede pasar un string vacio como parametro y va a separalo en letras
`Alexys`.split(`e`)                         // Devuelve (2) ["Al", "xys"]

#### .substring(start,[end])
Extra el texto dependiendo de la posicion que le pasemos.Si se le pasa un numero negativo en [end] extrae hacia atras
`Hola mundo`.substring(2)    //Devuelve `la mundo`
`Hola mundo`substring(2,-1)   //Devuelve `Ho`
#### .substr(start,[end])
Comienza desde start, y termina en end, el start es la posicion y el end es la cantidad de caracteres a extraer.Si se le da un numero negativo extra desde el final
`Hola mundo`.substring(2,5)    //Devuelve `la mu`

#### .slice(start,[end])
Es lo mismo que substring, solo que se diferencia en valores negativos


## Clase 3 condicionales y ciclos
### if
#### Una linea
if (condicion) // Hacer algo

#### Con bloque
if(condicion){
    ...
}

#### Con mas de una condicion
if(condicion1){
  ...
} else if(condicion2){
  ...
}
  else(condicion3){
  ...
}
    
