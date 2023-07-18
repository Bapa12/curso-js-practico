## Respuestas al Test de JavaScript

Recuerda que estas respuestas (o al  menos la mayoría) NO SON ABSOLUTAS. Es completamente válido (en la mayoría de casos) si tienes otras respuestas. Recuerda que podemos discutirlo en la sección de comentarios del curso. :D


## Variables y operaciones

### 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

- ¿Qué es una variable y para qué sirve?

Espacio reservado en memoria donde se puede guardar información, dependiendo de los tipos y estructuras de datos que soporte el lenguaje que se está utilizando.

- ¿Cuál es la diferencia entre declarar e inicializar una variable?

DECLARAR: es decirle a JS que se está creando una variable con su nombre.  
```js
let nombre;
```

INICIALIZAR: cuando se le asigna un valor a una variable. 
```js
let nombre = "Bapa";
```

REINICIALIZAR: cuando se le cambia el valor de una variable.
```js
let nombre = "Bapa";
nombre = "Loki";
```

* LET: permite cambiar el valor de las variables en el futuro.

EJEMPLO:
```js
let nombre = "Bapa";
nombre = "Loki";
console.log(nombre); // "Loki"
```

*CONST: no se puede cambiar su valor. Son variables cuyo valor siempre va a ser el mismo, es decir, son constantes. 

EJEMPLO:
```js
const apellido = "Caloguerea";
apellido = "Bozinovich";
console.log(apellido); // Uncaught TypeError
```

- ¿Cuál es la diferencia entre sumar números y concatenar strings?
- ¿Cuál operador me permite sumar o concatenar?

En las variables no sólo se pueden guardar valores fijos, si no, que también se pueden utilizar operadores como el de suma, resta, multiplicación, división, entre otros, para obtener un resultado dependiendo de otras variables.

EJEMPLO:
```js
let suma = 2 + 2 // 4
let sumaString = "Hola, " + "Loki"; // "Hola, Loki"
```

El operador que nos permite sumar o concatenar es +. Este operador nos permite sumar números cuando lo utilizamos con números, pero cuando se utiliza con strings lo que hace es unir (concatenar) ambos strings. 

### 2️⃣ Determina el nombre y tipo de dato para almacenar en variables la siguiente información:

- Nombre: String
- Apellido: String
- Nombre de usuario en Platzi: String
- Edad: Number
- Correo electrónico: String
- Mayor de edad: Boolean
- Dinero ahorrado: Number
- Deudas: Number

### 3️⃣ Traduce a código JavaScript las variables del ejemplo anterior y deja tu código en los comentarios.

```js
let name = "Loki";
let lastName = "Caloguerea";
let userName = "Loki31"
let age = 6;
let email = "loki.31@gmail.com";
let ofLegalAge = true;
let savedMoney = 500000;
let debt = 15000;
```

### 4️⃣ Calcula e imprime las siguientes variables a partir de las variables del ejemplo anterior:

- Nombre completo (nombre y apellido)

```js
let name = "Loki";
let lastName = "Caloguerea";
let fullName = name + " " + lastName;
console.log(fullName); // "Loki Caloguerea"
```
- Dinero real (dinero ahorrado menos deudas)

```js
let savedMoney = 500000;
let debt = 15000;
let actualMoney = savedMoney - debt;
console.log(actualMoney); // 485000
```

## Funciones

### 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

- ¿Qué es una función?

Las funciones permiten encapsular (guardar) bloques de código para reutilizarlos y ejecutarlos en el futuro.
Una función trabaja con parámetros y argumentos. 

```js
function fullName(name, lastName) {
    return name + " " + lastName;
} 

fullName("Loki", "Caloguerea");
```
Una función puede recibir parámetros para que dinámicamente cada vez que se llame a fullName no se tenga siempre el mismo name y lastName, si no, que luego del nombre de la función y entre paréntesis, se defina name y lastName, para que sean estos parámetros los que  se concatenen o ejecuten cualquier otra acción, dependiendo de lo que se le indica a la función que realice.

- ¿Cuándo me sirve usar una función en mi código?

Nos sirve cuando se tiene código repetido, cuando se tienen variables que son muy similares unas con otras o incluso cuando se tienen bloques completos de código que siempre hacen lo mismo una y otra vez, cambiando sólo ciertos valores que podrían ser parámetros o argumentos, que se pueden encapsular para reutilizar más de una vez en el futuro. 

También sirven para ordenar y mejorar la legibilidad del código. 

- ¿Cuál es la diferencia entre parámetros y argumentos de una función?

EJEMPLO
```js
function fullName(name, lastName) {
    return name + " " + lastName;
} 

fullName("Loki", "Caloguerea");
```
PARÁMETROS: son lo que recibe una función cuando se está creando. Es lo que va dentro de los paréntesis luego del nombre de la función. 

EJEMPLO: 
```js
function fullName(name, lastName) {
    return name + " " + lastName;
}
```

ARGUMENTOS: cuando se va a ejecutar una función, ésta no va a recibir parámetros, sino, que se le envían argumentos. 

EJEMPLO: 

```js
fullName("Loki", "Caloguerea");
```


### 2️⃣ Convierte el siguiente código en una función, pero, cambiando cuando sea necesario las variables constantes por parámetros y argumentos en una función:

```js
const name = "Juan David";
const lastname = "Castro Gallego";
const completeName = name + lastname;
const nickname = "juandc";

console.log("Mi nombre es " + completeName + ", pero prefiero que me digas " + nickname + ".");
```

```js
function fullName(name, lastName) {
    return name + " " + lastName;
}

function greeting(name, lastName, nickname) {
    const completeName = fullName(name, lastName);
    console.log("Mi nombre es " + completeName + ", pero prefiero que me digas " + nickname + ".");
} 

greeting("Loki", "Caloguerea", "Lokimaru");
// Mi nombre es Loki Caloguerea, pero prefiero que me digas Lokimaru.
```


## Condicionales

### 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

- ¿Qué es un condicional?

Forma en la que se ejecuta un bloque de código u otro dependiendo de alguna condición o validación. 

- ¿Qué tipos de condicionales existen en JavaScript y cuáles son sus diferencias?

*IF (ELSE IF y ELSE): permite realizar validaciones completamente distintas en cada validación o condicional. 

*SWITCH: permite agregar una variable o algo que se quiera validar y luego por medio de cases (casos) comenzar a preguntar si esa condición o esa variable cumple con cierta condición. En Switch todos los cases se comparan con la misma variable o condición que se define en el switch. 

- ¿Puedo combinar funciones y condicionales?

Sí, las funciones pueden encapsular cualquier bloque de código, incluyendo condicionales. 

### 2️⃣ Replica el comportamiento del siguiente código que usa la sentencia switch utilizando if, else y else if:

```js
const tipoDeSuscripcion = "Basic";

switch (tipoDeSuscripcion) {
   case "Free":
       console.log("Solo puedes tomar los cursos gratis");
       break;
   case "Basic":
       console.log("Puedes tomar casi todos los cursos de Platzi durante un mes");
       break;
   case "Expert":
       console.log("Puedes tomar casi todos los cursos de Platzi durante un año");
       break;
   case "ExpertPlus":
       console.log("Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año");
       break;
}
```

```js
const tipoDeSuscripcion = "Basic";

if(tipoDeSuscripcion == "Free") {
    console.log("Solo puedes tomar los cursos gratis");
} else if(tipoDeSuscripcion == "Basic") {
    console.log("Puedes tomar casi todos los cursos de Platzi durante un mes");
} else if(tipoDeSuscripcion == "Expert") {
    console.log("Puedes tomar casi todos los cursos de Platzi durante un año");
} else if(tipoDeSuscripcion == "ExpertPlus") {
    console.log("Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año");
} else {
    console.log("No tienes ningún tipo de suscripción");
}
```

### 3️⃣ Replica el comportamiento de tu condicional anterior con if, else y else if, pero ahora solo con if (sin else ni else if).

> 💡 Bonus: si ya eres una experta o experto en el lenguaje, te desafío a comentar cómo replicar este comportamiento con arrays y un solo condicional. 😏


## Ciclos

### 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

- ¿Qué es un ciclo?

Es la forma de ejecutar un bloque de código hasta que se cumpla cierta condición. Son similares a los condicionales, porque también están validando condiciones (realizando validaciones), pero lo ejecutan hasta que esa condición se cumpla. 

- ¿Qué tipos de ciclos existen en JavaScript?

*WHILE: realiza la validación antes de ejecutar la primera vez el bloque de código. Este ciclo hace una validación y luego se tiene el bloque de código, pero el bloque de código no está obligado a cambiar esa condición en algún momento para que pare el ciclo.  

EJEMPLO CICLO WHILE:
```js
let i = 0

while(i < 0) {
    // Código a ejecutar y agregar variable i++, i--, dependiendo de la variable (puede i, j, k, entre otros).
}
```

*FOR: automáticamente obliga a definir qué pasa al principio y al final de cada ejecución de código en el ciclo. Automáticamente pide que se inicialice una variable, que se defina algún momento en el que el ciclo debe terminar la validación como tal y además alguna variable que deba cambiar.  

EJEMPLO CICLO FOR:
```js
for (let i = 0; i < 5, i++) {
    // Código a ejecutar
}

// let i = 0 --> creación de la variable
// i < 5 --> validación (que cierta variable sea "true", "false", que sea "mayor", "menor", lo que se requiera.)
// i++ --> indica lo que se hace con esa primera variable que se creó. 
// En resumen: en el ejemplo, se le indica a una variable que empiece en 0 (cero), luego que ejecute el bloque de código hasta que la variable llegue a 4 y cada vez que se termine de ejecutar una vuelta del ciclo, se va a sumar 1 a esa variable que se creó al principio.  
```

*DO-WHILE: es igual al ciclo WHILE, pero DO-WHILE la primera vez no realiza la validación, primero ejecuta el código, luego realiza la validación y dependiendo de esa validación vuelve a ejecutar el ciclo. 

- ¿Qué es un ciclo infinito y por qué es un problema?

Es cuando la validación de los condicionales para terminar de ejecutar un ciclo nunca se cumple y termina toteando (dañando) la aplicación (e.j. cuando el navegador ya no puede más de tanta ejecución de ese bloque de código).  

- ¿Puedo mezclar ciclos y condicionales?

Sí, los ciclos de por sí ya son una especie de condicionales, sólo que se van a estar ejecutando hasta que ese condicional falle. Pero, tener un condicional que ayude a parar la ejecución del código, no impide tener otros condicionales.   

### 2️⃣ Replica el comportamiento de los siguientes ciclos for utilizando ciclos while:

```js
for (let i = 0; i < 5; i++) {
    console.log("El valor de i es: " + i);
}

for (let i = 10; i >= 2; i--) {
    console.log("El valor de i es: " + i);
}
```

```js
let i = 0;

while(i < 5) {
    console.log("El valor de i es: " + i);
    i++;
}
```

```js
let i = 10;

while(i >= 2) {
    console.log("El valor de i es: " + i);
    i--;
}
```

### 3️⃣ Escribe un código en JavaScript que le pregunte a los usuarios cuánto es `2 + 2`. Si responden bien, mostramos un mensaje de felicitaciones, pero si responden mal, volvemos a empezar.

> 💡 Pista: puedes usar la función prompt de JavaScript.

```js
let answer;

while (answer != '4') {
    let question = prompt('¿Cuánto es 2 + 2?');
    answer = question;
}
```

## Listas

### 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

- ¿Qué es un array?
- ¿Qué es un objeto?
- ¿Cuándo es mejor usar objetos o arrays?
- ¿Puedo mezclar arrays con objetos o incluso objetos con arrays?

### 2️⃣ Crea una función que pueda recibir cualquier array como parámetro e imprima su primer elemento.

### 3️⃣ Crea una función que pueda recibir cualquier array como parámetro e imprima todos sus elementos uno por uno (no se vale imprimir el array completo).

### 4️⃣ Crea una función que pueda recibir cualquier objeto como parámetro e imprima todos sus elementos uno por uno (no se vale imprimir el objeto completo).
