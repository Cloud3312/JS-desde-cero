# JS-desde-cero
# 1 Clase 1 Introduccion a JavaScript
## 1.1 Variables

Las variables son definidas con:   
let + nombreDeLaVariable = valorADefinir(pueden ser un String,Boolean,Numero).
Es buena practica tener los nombreDeLaVariable en ingles.  
Ademas, en vez de escribir let en cada variable, se puede separar por comas, para ahorrar un poco de codigo.Los valores de las variables se pueden reasignar
Ej:

```
let number = 10,
    nombre = `Braian`,
    pais   = `Argentina`
```
Para ver lo que devuelve la variable, se puede utilizar la consola a traves de  
console.log(nombreDeLaVariable).

## 1.2 Constantes
Es un valor constante, es decir que no puede variar, se define con  
const + nombreDeLaConstante = valorADefinir 

## 1.3 Sintaxis: 
Para comentar utilizar // o /* */ , son utilizados para indicar que sucede en el programa UTILIZARLO ADECUADAMENTE SIN EXAGERAR.Tambien sirve para comentar codigo, es decir dejarlo sin utilizar.

## 1.4 Tipos de Datos 
## 1.4.1 Primitivos
### 1.4.2 Numeros
Son numeros: 1,70,600, 6.6,etc
### 1.4.3 String
Son definidos con  ``` `Comillas simples al reves o backtips` ``` , "Comillas dobles" , 'Comillas simples'.Es preferible utilizar con backtips ya que nos permiten hacer mas cosas como por ejemplo: concatenar   

``` let nombre = `Juan tiene ${number} anos` ```

### 1.4.4 Boolean 
Denotan un valor de verdad     
5 == 5 daria verdadero/true    
5 == `5` daria verdadero/true ya que JS asi    
7 == 8 daria falso/false     

### 1.4.5 Undefined 
Es cuando la variable no tiene ningun valor asignado o definido

### 1.4.6 Null
Es cuando la variable nunca fue creada 

### 1.4.7 Symbol()

### 1.4.8 typeof 
Devuelve el dato que le pasaste en forma de String  
``` let prueba = 3  ```
typeof data devuelve `object`

## 1.4.9 Compuestos 
### 1.4.10 Arrays 
Guardan mas de un valor por ejemplo ``` let numbers = [1,2,5,6.7] ``` son datos del mismo tipo

### 1.4.11 Object 
Es un tipo de dato que posee varios datos ya sea del mismo o diferente tipo
```
let data = {
    nombre: `Juan`,
    apellido: `Perez`,
    Edad: 21
}
```

# 2 Clase 2  Como funciona JavaScript?
JS  es dinamnicamente tipado, es decir que el interprete deduce que es cada dato.Ademas de que las variables se pueden reedefinir(reasignar,pasarle un nuevo valor)

## 2.1 Type coertion 
Es poder concatenar cosas, es la conversión automática o implicita de valores de un tipo de dato a otro (Ejemplo: de cadena de texto a número) 
true + 1 = 2  porque se considera a true como un 1 y a false como un 0
``` `Hola Mundo ` + 1 = `Hola Mundo 1` ```  
Pero si se utiliza la multiplicacion daria NaN not a number

## 2.2 Valor o referencia
Al usar un dato se lo puede usar por valor(number, boolean, String) o referencia(objeto y arrays)
A los que son por valor se los puede modificar, mientras que los de referencia no, es decir, permanecen igual
Ej:
``` 
let number  = 60    
let number2 = number  
number2 = 70  <- al ser un Number y estar pasado por valor number 1 no cambia
// Mientras que al  ser referencia cambian ambos valores
let number  = [1,3,4,5]    
let number2 = number
number2.push(6)             //.push anade un elemento al array 
number  = [1,3,4,5,6]
number2 = [1,3,4,5,6]
``` 
## 2.3 Operadores 
### 2.3.1 Asignacion 
Le asignan el valor a una variable
=, +=, -=, /=, *=

### 2.3.2 Comparacion (Binarios)
Comparan valores , devuelven un Boolean
==, ===, !=, !==, >, <, >=, <=   
5 == `5` devuelve True  
5 === `5` devuelve False, ya que === se enfoca en el tipo de valor y dato   
Es conveniente evitar la doble igualdad ya que puede generar problemas  
5 != `5` devuelve False ya que al ser un solo igual se centra solo en el valor, el != es distinto de  
5 !== `5` devuelve True ya que sucede lo mismo que el punto del triple igual  

### 2.3.3 Unarios 
typeof, ! (negacion)
!true devuelve False 
!0 devuelve True

### 2.3.4 Aritmeticos 
+, -, *, /, % (te da el resto de la division), ++, --.
++ y -- son post aumento y decremento, si se lo pone a la izquierda contaria como un pre decremento y aumento

### 2.3.5 Operador Ternario (3 Valores)
Funciona como un condicional, utiliza ? para que haga algo primero y si eso no se cumple hace lo que esta al lado de :
```
expresionQueDevuelveBoolean  
? valorSiEsTrue  
: valorSiEsFalse  
```

### 2.3.6 Operador Corto circuito
|| evalua el primer valor, si es verdadero te da el primero y si es falso te da el segundo  
&& evalua el primer valor, si es falso te da el primero, si es verdadero te da el segundo  

### 2.3.7 Numeros
#### 2.3.7.1 toFixed()
devuelve el numero con la cantidad de decimales redondeados que vos quieras   
```
let number = 5.966
number.toFixed(2)  //devuelve 5.97
``` 
#### 2.3.7.2 parseInt(string, 10) y parseFloat(string, 10)
parseInt convierte un numero que esta en forma de string a un numero entero  
parseFloat convierte un numero que esta en forma de string a un numero decimal  

### 2.3.8 Math
#### 2.3.8.1 .floor()
Se le pasa un numero y redondea para abajo    
Math.floor(20.6) //devuelve 20
#### 2.3.8.2 .ceil()
Se le pasa un numero y redondea para arriba  
Math.ceil(20.4) //devuelve 21
#### 2.3.8.3 .round()
Se le pasa un numero y redondea dependiendo de si es mayor a 5 para arriba y si es menor a 5 para abajo
#### 2.3.8.4 .random()
Devuelve un numero random  
Para hacer un sorteo se podria hacer   
Math.ceil(Math.random()*20)  //devuelve un numero random entero de entre 0 y 20

## 2.4 Strings
### 2.4.1 Propiedades
Una **Propiedad** es un valor que tiene un dato.Por ejemplo: caracteristicas como edad, pais,direccion

#### 2.4.1.1 .lenght
Devuelve la cantidad de caracteres que tiene un String  
```
`Hola`.lenght devuelve 4
```
### 2.4.2 Metodos 
Un **Metodo** es una operacion que el dato puede realizar, por ejemplo: acciones como trabajar,programar, disenar.  
Existen metodos sin parametros como:  
#### 2.4.2.1 .trim()
Lo que hace es sacarle los espacios en blanco del inicio y final del String, **NO LOS ESPACIOS QUE ESTAN ENTRE MEDIO**  
```
`   Hola    `.trim() //devuelve `Hola`
```
#### 2.4.2.2 .toUpperCase()
Transforma el string que le pasemos a mayusculas  
```
`hola`.toUpperCase() //devuelve `HOLA`
```
#### 2.4.2.3 .toLoweCase 
Transforma el string que le pasemos a minusculas    
```
`HOLA`.toLoweCase() //devuelve `hola`
```
Estos pueden ser utilizados por ejemplo, para hacer un cuestionario  
```
let answer = prompt(`Cual es la capital de Argentina?`).trim().toUpperCase()   // Abre una ventana en el navegador con esa pregunta
let message =  answer === `ARGENTINA` 
               ? `Excelente, acertaste`                                        
               : `Respuesta incorrecta`
alert(message)
```

Se pueden encontrar caracteres con:

#### 2.4.2.4 .indexOf()
Indica la posicion del elemento a buscar dentro del String
```
`Hola como estas`.indexOf(`o`) //devuelve 1, ya que comienza a buscar en la posicion 0 del String, -1 si no lo encuentra
```
#### 2.4.2.5 .lastIndexOf()
Indica la posicion ultima de lo que queremos a buscar 
```
`Hola amigos`.lastIndexOf(`o`) devuelve 9
```
#### 2.4.2.6 .includes()
Indica si el String dado incluye lo que se le haya pasado como parametro
```
`https://ed.team/blog`.includes(`blog`)     //denota True
```
#### 2.4.2.7 .startsWith()
Indica si el String dado comienza con lo que se le pasa como parametro
```
`https://ed.team/blog`.startsWith(`https://ed.team`)     // Denota True
```
#### 2.4.2.8 endsWith()
Indica si el String dado termina con lo que se le pasa como parametro
```
`https://ed.team/blog`.endsWith(`blog`)                 //Denota True
```
### 2.4.3 Manipular strings con metodos 
#### 2.4.3.1 .replace()
```
`Hola mundo`.replace(`mundo`, `Miguel`)      //Esto devuelve `Hola Miguel`
```
#### 2.4.3.2 .split(separator,[cuantity])
Separa el string dado en partes.Tambien se puede pasar un string vacio como parametro y va a separalo en letras
```
`Alexys`.split(`e`)                         // Devuelve (2) ["Al", "xys"]
```

#### 2.4.3.3 .substring(start,[end])
Extra el texto dependiendo de la posicion que le pasemos.Si se le pasa un numero negativo en [end] extrae hacia atras
```
`Hola mundo`.substring(2)    //Devuelve `la mundo`
`Hola mundo`substring(2,-1)   //Devuelve `Ho`
```
#### 2.4.3.4 .substr(start,[end])
Comienza desde start, y termina en end, el start es la posicion y el end es la cantidad de caracteres a extraer.Si se le da un numero negativo extra desde el final
```
`Hola mundo`.substring(2,5)    //Devuelve `la mu`
```
#### 2.4.3.5 .slice(start,[end])
Es lo mismo que substring, solo que se diferencia en valores negativos

# 3 Clase 3 condicionales y ciclos
## 3.1 if
### 3.1.1 Una linea
```
if (condicion) // Hacer algo
```
### 3.1.2 Con bloque
```
if(condicion){
    ...
}
```
### 3.1.3 Con mas de una condicion
```
if(condicion1){
  ...
} else if(condicion2){
  ...
}
  else(condicion3){
  ...
}
```
## 3.2 Condiciones multiples    
### 3.2.1 && (and)
Requiere que ambas condiciones den True

### 3.2.2 || (or)
Requiere que al menos una de True

### 3.2.3 Pequeno ejercicio
```
let age = parseInt(prompt(`dame tu edad`,10))
if(age){
    if(age > 18){
        alert(`Sos mayor de edad`)
    }
    else{
        alert(`Sos menor de edad, te faltan ` + (18-age) + ` anios` )
    }  
}
else{
    age = parseInt(prompt(`Tu edad debe ser un numero`,10))
}
```
## 3.3 Truthy and falsy values
### 3.3.1 Valores que te dan False en la condicion
- 0  
- ""  
- NaN  
- undefined  
- null  

### 3.3.2 Valores que te dan True en la condicion
- String no vacio  
- Numero diferente de cero  
- Arrays     
- Objetos  

## 3.4 switch

Cuando queremos comparar un valor con una serie de valores.Los ; son opcionales  
```
let valorAComparar = prompt(`Introduce un numero entre 1 y 3 `).toUpperCase().trim()
//trim evita los espacios, y toUpperCase pone todo en mayusculas, esto es para evitar errores
switch (valorAComparar){
    case `1`:
        alert(`Sos gracioso`)
        break;
    case `2`:
        alert(`Sos extrovertido`)
        break;
    case `3`:
        alert(`Sos feliz`)
        break;    
    default
        alert(`Por favor elige un numero del 1 al 3`)
        break;
}
```
## 3.5 Ciclos
### 3.5.1 Ciclo for 
Se declara una variable, mientras la condicion se cumple y luego un incremento
```
for(let i = 0; i <=100; i++){
    if(i % 5 === 0)console.log(i)
}
// Imprime todos los numeros que sean divisibles por 5, empieza preguntando por 0
// y en cada iteracion va aumentando en 1 gracias a i++
// en vez de aumentar uno en uno se puede hacer += n  numeros
```
#### 3.5.1.1 break y continue 
continue evitara esa iteracion, y break detendra el ciclo completo  

Con **continue** se evita la iteracion, en este caso se evita el multiplo de 5, aunque tambien se puede hacer   
i % 5 !== 0 que va a dar como resultado lo mismo  
```
for (let i = 0; i <= 50; i++){
    if(i % 5 === 0) continue
    console.log(i)         
}
// esta funcion devuelve los numeros entre 0 y 50 que no son multiplo de 5 
```

En este caso se utiliza **break** para detener la iteracion cuando n valga 5, esto devuelve los 5 primeros multiplos de 5  
```
let n = 0
for (let i = 1; i <= 50; i++){
    if(i % 5 === 0){
        console.log(i)
        n++
    }
    if(n >= 5) break    
}
```

### 3.5.2 Ciclo while 
Mientras la condicion que este en el while se cumpla se ejecuta el codigo  
```
let i = 0 
while(condicion){           //Condicion puede ser i<=10 para que siga el ciclo hasta que i valga 10
    console.log(i)
    i++
}
```

### 3.5.3 Ciclo do while
Primero realiza la accion, luego pregunta la condicion  
``` 
let password = "Capoeira"
let pass
do {
    pass = prompt("Ingrese su contrasena")
} while(pass !== password)
```
# 4 Clase 4 Funciones
## 4.1 Que es una funcion?
Una funcion es un pedazo de codigo reutilizable, en el que hay un conjunto de instrucciones  
input => funcion => output  
**input** son los argumentos  
El **output** es el valor que devuelve la funcion  
Las funciones sin valor de retorno devuelven undefined  

Para ejecutar una funcion:
```
nombreDeFuncion(argumento1,argumento2,argumento3)
nombreDeFuncion()
```
No siempre se requieren argumentos  

Una funcion puede ser metodo de un objeto  
```
objeto.nombreDeFuncion(argumentos)
`Hola Mundo`.slice(3)
```
## 4.2 Formas de declarar una funcion
### 4.2.1 Declaracion
```
function nombreFuncion(parametros){
    //instrucciones a dar
    return valor
}
``` 
Ejemplos:
```
function saludar(persona){
    return `Hola ${persona}`
}

function saludar(persona,sexo){
    return sexo === `m`
            ?   `Bienvenido a la pagina ${persona}`
            :   `Bienvenida a la pagina ${persona}`  
}

function saludar(persona,sexo){
    let saludo = sexo === "m"
                   ?  `Bienvenido`
                   :  `Bienvenida`
    return `${saludo} a la pagina ${persona}`               
    
}
```

### 4.2.2 Expresion
#### 4.2.2.1 con function(en desuso)     
```
var nombreDeFuncion = function() {          // YA NO SE USA
}
```
#### 4.2.2.2 funciones de flecha (recomendado desde ES6)
```
const nombreDeFuncion = (parametros) => {
    // instrucciones de la funcion
    return valor
}
```

**NO USAR LET PARA LAS FUNCIONES**
```
const saludar = (persona,sexo) => {
    return sexo === `m`
            ?   `Bienvenido a la pagina ${persona}`
            :   `Bienvenida a la pagina ${persona}`  
}
```
**Si la funcion de flecha retorna directamente un valor, sin instrucciones adicionales, la sintaxis se reduce**
const sumar = (a,b) => a + b 
