# Notas del capítulo 2

En este capítulo empezamos a ahondar en lo que sería una expresión y una sentencia o instrucción; palabras más, palabras menos, la expresión es un conjunto de valores y operadores que evalúan a un valor único. Un ejemplo sería una suma, tenemos 2 elementos (a y b) que pueden tener un valor y al sumarse, es decir, empleamos el operador suma (+), lo convertimos en una operación que al evaluarse da un valor único; por ejemplo: 3 + 5 = 8.

También, mencionamos que hay 2 palabras para declarar variables, let  y var; incialmente se usaba nada más el var. Sin embargo, ciertas particularidades en el uso de esa palabra reservada y diseño del lenguaje fueron subsanados al incorporar let. También hablamos de lo que es una declaración de la variable, que no es más que una instrucción para apartar un espacio en memoria y referenciándolo con un nombre de variable. Cabe destacar que la acción siguiente a eso puede ser la asignación, que es darle un dato con un tipo específico a ese espacio en memoria. Por sí misma, la asignación es una expresión también:

```javascript
let saludo; //Declaracion
saludo = 'Hola, mundo!'; //Asignacion
```

Una particularidad, es que se puede declarar e inicializar una variable de una vez, esto nos agiliza a la hora de escribir el código.
```javascript
let despedida = 'Chaolín';
```

Se menciona además, de las convenciones para nombrar variables, tenemos el "snake case", que es escribir palabras seguidas de guión bajo: nombre_usuario. Otra convención es el "camel case", que sería escribir cada palabra con la primera palabra en mayúscula exceptuando la inicial, esto simula a la joroba de un camello: usuarioApellido. Acorde a lo descrito en el libro esta es la convención más usada en JS.

Para cerrar el tema de la declaración e inicialización de una variable, en este capítulo se nos muestra una nueva palabra reservada "const" que nos sirve para declarar constantes. Al igual que en matemáticas, la idea es la misma: una constante es un valor que no cambia en el tiempo. Es decir, una vez declarada si valor permanece inmutable. Además, hay que declararla e iniciarla al mismo tiempo.

Luego, entramos en el terrenos de los números y las operaciones matemáticas que usan PEMDAS (parentesis, exponenciación, multiplicación y división, suma y resta) para el orden de las operaciones. Adicionalmente, se nos muestra maneras en la que aumentar o decrecer un valor numérico en varias maneras que JS tiene para realizar esta tarea.
```javascript
const constanteEjemplo = "Esta es una constante";
constanteEjemplo = 'Intenando cmabiar esto dara error' // esto dara un error cuando se ejecute 

let number_a = 4;
let number_b = 7;
let number_c = 3;


++number_a; // Esto aumenta el valor de esta variable en 1, pasaria a valer 5
numer_a++; // similar al anterior solo que el retorno inicial muestra el valor anterior y luego hace la suma
--number_b; // tambien podemos restar el valor en 1


number_c = number_c + 2; // podemos escribir una operación de esta manera para sumar 2 pero también...
n
lumber_c += 2; // Esto significa lo mismo de arriba y servira con cualquier signo de operacionet result = (number_a + number_b) / number_c) ** number_c
number_c /= 7;
console.log(result);
```

Luego, se hace mención del tipo de dato "string", en español, "cadena de texto". No es más que un conjuntos de caracteres encerrados entre comillas para denotar que es un texto, eso se aplica también a números que estén dentro de las comillas porque serán considerados parte de una cadena de texto. Las cadenas pueden ser escritas con comillas simples o comillas dobles.

Otra idea importante que se expone aquí es sobre el cónteo que hace javascript para los elementos dentro de una cadena de texto, estos pueden ser seleccionados específicamente tomando el nombre de la variable y encerrando entre correchetes el número de la posicióne a la que queremos referirnos dentro del texto. El conteo en JS empieza desde el número 0 para la primera posición y se incrementará en un valor para cada posición subsiguiente.


 El uso de un tipo de comillas o de otra es indiferente, de hecho, se pueden completementar porque existe una restricción en el uso de ellas. No se puede esar el mismo estilo de comillas 2 veces, a menos que usemos algo llamado "secuencias de escape" (lo veremos luego). Sin embargo, podemos usar ambos estilos de comillas para escribir textos en lenguajes que usen comillas simples dentro del texto o para evitar que erroneamente cerremos la cadena de texto antes de tiempo. Ejemplo:
```javascript
let cadenaDeTexto = 'Soy una cadena'

let posicionSegunda = posicionSegunda[1]

let errorEnTexto = 'I'm an error'' // aqui, salimos de la cadena de texto antes de tiempo

let usoMixto = "I'm an error" // Se usaron ambos tipos de comillas (en realidad, uno es un apóstrofo ) 
```
Así como se ha explicado en varias partes del libro. En Javascript, las estructura de datos que hemos aprendido hasta ahora son considerados objetos. Y, aunque no hemos entrado en el apartado sobre este tema, sí que se abordó la explicación de una función, que no es más que un fragmento de código que realiza alguna acción y que puede ser llamado para realizar dicha tarea, es decir, parecido a las variables, se le da asigna un nombre para poder hacer uso de ella.
Este uso es llamado "invocación" o "llamado" de la función; también se nos introduce el concepto de argumento, que serían datos que se pasan al función para que puedan hacer su trabajo.

Toda explicación sobre las funciones fue dada para cerrar la exposición de algo llamado métodos; palabras más, palabras menos, se refieren a una función que está atada a un objeto, es decir, a una variable que tiene funciones especiales relacionadas a su tipo de dato.

Los strings tienen varios tipos de métodos que podemos emplear para realizar alguna acción sobre esa cadena de texto; tenemos, entre muchos otros metodos a:

- slice: Este método toma una porción de la cadena de texto original, es decir que desde un punto inicial hasta uno final se recorta el texto deseado. Para ello, se escriben entre los paréntesis 2 argumento, ambos numéricos, que determinan la posición "desde" y "hasta" donde será recortada la cadena de texto.
- trim: Sirve para remover los caracteres en blanco de ambos lados de una cadena de texto; sin embargo, espacios dentro de la cadena quedan intactos
- toLowerCase: Toda la cadena de texto pasa a estar en minúsculas.L
 includes: Devuelve un valor (verdadero o falso)

- padStart: Le agrega una cantidad de caracteres al comienzo de una cadena de texto
- repeat: Devuelve una cadena de texto escrita x veces


```javascript
let cadenaDeTexto = ' Hola MUNDO   '

console.log(cadenaDeTexto.trim())
console.log(cadenaDeTexto.toLowerCase())
console.log(cadenaDeTexto.includes('Hola'))
console.log(cadenaDeTexto.padStart(4,'hello '))
console.log(cadenaDeTexto.repeat(3))

```