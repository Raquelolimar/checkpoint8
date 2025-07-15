
<img src= "https://github.com/user-attachments/assets/44ccfa40-935c-4551-b097-4480cca4e420" alt="titulo" width="700">




# **BLUCLES EN JAVASCRIPT**  

<img src ="https://github.com/user-attachments/assets/13c8951b-c08c-4ff7-a419-5372bb197464" alt = "js" width= "600">

Los bucles ofrecen una forma rápida y sencilla de hacer algo repetidamente. Puedes pensar en un bucle como un juego en el que dices a alguien que dé X pasos en una dirección y luego Y pasos en otra.  

Hay muchos diferentes tipos de bucles, pero esencialmente, todos hacen lo mismo: repiten una acción varias veces.


En JavaScript, como en otros lenguajes, vamos a prestar atención a los bucles. Una de la forma más común de usar estos bucles es que JavaScript recorre colecciones de datos.  
  

En JavaScript los bucles (loops) son utilizados para realizar tareas repetitivas con base en una condición. Las condiciones típicamente devuelven true (verdadero) o false(falso) al ser evaluados. El bucle continuará ejecutándose hasta que la condición devuelva false.  

## **for in**  

Permite obtener los índices de una estructura en cada iteración.

~~~ 
var players = [
    'Pedri',
    'Gabi',
    'Raphina',
    'Lamine'
];

for (player in players) {
  console.log(players[player]);
}
~~~  

Esto nos devolvería los cuatro nombres de nuestros jugadores.

   Pedri<br>
   Gabi<br>
   Raphina<br>
   Lamine  

 
Aquí player no representa el valor, representa el índice. Si dijéramos solo console.log (player) nos daría como resultado:

[ '0' ]<br>
[ '1' ]<br>
[ '2' ]<br>
[ '3' ]  

 

  



## **for** 

 
![Captura de pantalla 2025-07-08 174518](https://github.com/user-attachments/assets/ca84f1a1-f4b1-48b2-8671-550e018ef571)

El bucle **_for_** se utiliza para repetir una o más instrucciones un determinado número de veces. De entre todos los bucles, el **_for_** se suele utilizar cuando sabemos seguro el número de veces que queremos que se ejecute.

La sintaxis de **_for_** es que dentro y entre paréntesis hay que incluir una expresión completa con tres argumentos (un valor inicial, una condición y una expresión final o acción). Ponemos tres expresiones y una declaración final. 

El primer elemento dentro del bucle se ejecuta solamente al empezar la iteración.

 

En el siguiente ejemplo recorremos un array que contiene varias letras y mostramos en la consola tanto la letra como el índice de la iteración actual.  



~~~
const letras = ['a', 'b', 'c', 'd', 'e'];

for (let i = 0; i < letras.length; i++) {
  
  // Muestra la letra actual
  console.log(letras[i]);

  // Muestra el índice actual
  console.log(i);
}
~~~  
Esto nos daría como resultado.  

a<br>
0<br> 
b<br>
1<br>
c<br>
2<br>
d<br>
3<br>
e<br>
4  
  

Primero ponemos una variable que se usará durante el bucle, luego una condición que significa que queremos que el bucle continúe hasta que no se cumpla la condición y finalmente un incrementador.  

Otro ejemplo con la lista de jugadores de antes dentro de la variable players:
~~~
var players = [
    'Pedri',
    'Gabi',
    'Raphina',
    'Lamine'
];
~~~  



Creamos otra variable:  


~~~
for var i = 0
~~~  


Dentro de ella creamos una condición ( i tiene que ser menor que la longitud de la lista players)  Es el elemento que se debe cumplir para que continúe la ejecución del bucle.

~~~
for var i= 0; i<players.length;
~~~  

Esta condición al repetirse con cada iteración, comprobará si es verdadera. Si es así continuará y en cuanto sea falso saldrá del bucle.  

La longitud de nuestra lista es 4. Con el bucle recorremos toda la lista hasta que "i" (que empieza en 0) sea mayor o igual que la longitud de los jugadores. Mientras que "i" sea menor que 4 continuará.  

Para que cambie nos falta un elemento que será el incrementador ("i ++). Con cada iteración, cada vez que pasamos por el bucle ("i" empieza en 0), primero empieza en cero, la siguiente vez será uno, si todo sigue siendo cierto seguirá... hasta que "i" sea igual o mayor de 4 (que es la longitud de nuestra lista). El último elemento sirve para indicar los cambios que queramos ejecutar en las variables cada vez que termina la iteración del bucle, antes de comprobar si se debe seguir ejecutando. 

~~~
for (var i= 0; i<players.length; i ++) {
   console.log(players[i]);
}
~~~  


Puedes interrumpir el bucle utilizando la sentencia _break_. Además, también puedes saltar a la siguiente iteración del bucle mediante la sentencia _continue_. 

Este bucle es muy potente, ya que en una sola línea podemos indicar muchas cosas distintas y muy variadas, lo que permite una rápida configuración del bucle y una versatilidad enorme.  

## **forEach**  

Es un bucle más funcional, se llama a una colección y da la posibilidad de colocar dentro un objeto, o dentro de una función.  

El método **forEach()** ejecuta la función indicada una vez por cada elemento de la colección (array) y en orden.  

No hay forma de detener o cortar un bucle **forEach()** que no sea lanzar una excepción.  

Utilizando bucle **for** tradicional para recorrer una colección (array) sería así:  

~~~
const numeros = [1, 2, 3];
  for (i=0; i<numeros.length; i ++) {
  console.log(numeros[i]);
}
~~~  

Ahora, ¿porqué es diferente **forEach()** ?  

El método **forEach()**, como ya hemos dicho, también se utiliza para recorrer una colección pero utiliza una función diferente al clásico bucle **for**.  

**ForEach()** pasa una función anónima para cada elemento del array.  

~~~
numeros.forEach(function() {
  //código
});
~~~  

La función se ejecutará para cada elemento. Debe tomar al menos un parámetro que represente los elementos del array.  

~~~
numeros.forEach(function(número) {
  console.log(número);
});
~~~  

También podemos hacerlo con la función flecha para simplificar código.  

~~~
numeros.forEach(function(número => console.log(número));
~~~  

El resultado sería el mismo. 

1<br>
2<br>
3
 

    
En el ejemplo de `players = [ "Pedri", "Gabi", "Raphina", "Lamine"]`  


~~~
players.forEach(function(element) {
   console.log(element);

});
~~~  

## **While** 

Este bucle (y el siguiente que vamos a analizar **_do while_**) no es tan popular. Se utiliza mucho menos que los otros bucles.  
 
Este bucle no tiene el mismo tipo de configuración que tiene un bucle **_for_** tradicional, donde puedes poner la variable dentro de la propia expresión de la función.  

Ahora tendríamos que declarar la variable fuera `var i= 0;`. Puedes llamar a tu variable como quieras. 

Al declarar la variable fuera del bucle puedes tener acceso a ella siempre que quieras, incluso en otros momentos de tu programa. Aunque esto no es algo que seguramente quieras hacer de manera habitual.   

Una vez declarada la variable crear el bucle **_while_** es muy similar (su sintaxis) a crear un condicional con el bucle **_for_**.<br>  

Vamos a seguir con nuestro ejemplo de jugadores.  



~~~
var players = [
    'Pedri',
    'Gabi',
    'Raphina',
    'Lamine'
];

var i=0;
while(i<players.length) {
  console.log(players[i])
};
~~~  

Coge el índice porque en este caso "i" está funcionando como índex.  

Si ejecutamos esto así, lanzará un bucle infinito porque no tenemos nada que cambie el valor de "x".  

Recordar que con el tradicional bucle **_for_** el último elemento era un incrementador, así que ahora también tenemos que crear manualmente un incrementador después de `players[i]`.  

~~~
var i=0;
while(i<players.length) {
  console.log(players[i]; i ++)
};
~~~
  

Así, cada vez que pase por el bucle va a aumentar, va a volver a subir a `while`, va a comprobar si es menor que la longitud de la variable "players" ( que como ya sabíamos era 4) y si es correcto va a seguir adelante. Tan pronto como el resultado sea igual o mayor que 4 se detendrá la ejecución.  

El resultado es el mismo que antes.  

* Después del primer pase:<br>
   Pedri<br>
   Gabi<br>
   Raphina<br>
   Lamine  
 
* Después del segundo pase:<br>
   Gabi<br>
   Raphina"<br>
   Lamine 

* Después del tercer pase:<br>
   Raphina<br>
   Lamine  

## **do while**  

La sintaxis para usar este bucle es similar al anterior **_while_** pero al revés. Primero ponemos la variable y justo después "do". La parte donde ponemos el bucle **_while_** iría al final del código, después de la expresión, fuera del bucle, detrás del incrementador.  

Donde antes teníamos "while" ahora sólo ponemos "do". Esto va a dar un comportamiento algo diferente. Con el bucle **_do_** la condición se comprueba después de la iteración (después de **_while_**). El bucle **_while_** al contrario comprueba primero la condición.  

~~~
var i=0;
do {
  console.log(players[i]); i ++;
}while(i<players.length)
~~~  

Esto funciona de la misma forma que antes. Pero si pondríamos que la variable sea igual a 23 (recordar que sólo tenemos 4) nos va a dar "undefined".  

~~~
var i=23;
do {
  console.log(players[i]); i ++;
}while(i<players.length)
~~~  

`undefined`  

Si pondríamos esto en un bucle **_while_** no nos imprimiría nada.  

~~~
var i=23;
while(i<players.length) {
  console.log(players[i]); i ++;
};
~~~

**_while_** comprueba primero la condición.  

Con el bucle **_do while_** siempre se pasará por el programa al menos una vez. Este bucle hace algo que ninguna puede hacer porque puede ejecutar y garantizar que se ejecutará al menos una vez.  

Un ejemplo bueno es en programas de juegos, donde al construirlo quieres que por lo menos el proceso se ejecute una vez y si sigue ganando puede comprobarlo en las condiciones "while" y seguir adelante.  

# **DIFERENCIAS ENTRE CONST, LET, VAR**  

## **VAR**  


Tenemos diferentes tipos de variables en JavaScript. Hace años sólo teníamos que preocuparnos por la palabra clave "**var**" y después de ella poner el nombre que quisiéramos darle a la variable. Las declaraciones "var" eran las que mandaban antes de llegar al JavaScript moderno. Sin embargo, hay problemas asociados a las variables declaradas con var. Por eso fue necesario que surgieran nuevas formas de declarar variables. Esto provocó que "var" se convirtiera en una variable global y empezamos a tener algunos problemas. 

~~~
var saludar = "hey hola";
function nuevaFuncion() {
  var hola= "hola";
~~~  

"Saludar" tiene ámbito global porque existe fuera de la función, mientras que "hola" tiene ámbito local (no podemos acceder a ella fuera de la función).  

~~~
console.log(hola)
~~~  

Nos daría error. Hola is not defined. Porque "hola" no está disponible fuera de la función.  

Las variables con **_var_** se pueden volver a declarar y modificar . Podemos hacer esto dentro del mismo ámbito y no obtendremos error.  

~~~
var saludar ="hey hola";
var saludar="dice hola también";
~~~     

Si quieres redefinir saludar, se puede convertir en un problema cuando no te das cuenta de que la variable saludar ha sido definida antes.  


Puede que accidentalmente cambies el valor en algún lado del programa y se actualiza ese valor. Pero otra parte del programa esperaba que no se hubiera actualizado. (Esto causa muchos errores). las declaraciones "var" eran las que mandaban. Sin embargo, hay problemas asociados a las variables declaradas con **_var_**.  
Si has utilizado saludar en otras partes de tu código, puede que te sorprenda la salida que puedes obtener. Esto probablemente causará muchos errores en tu código. Por eso son necesarios _**let y const**_.  

## **LET**  

**_Let_** es ahora preferible para la declaración de variables. Es una mejora de las declaraciones con **_var_**. También resuelve el problema que  acabamos de ver con "var".  

**_Let_** no contamina el espacio de ámbito global. Es más específico que **_var_**.  

Sólo estará disponible en la función en la que se pone, no puede aparecer en otros lugares.  
**_Let_** puede modificarse pero no volver a declararse. A diferencia de _**var**_, una variable _**let**_ no puede ser re-declarada dentro de su ámbito.  

Esto funciona:  

~~~
let saludar = "dice Hola";
    saludar = "dice Hola también";
~~~  

Esto nos dará error:  

~~~
    let saludar = "dice Hola";
    let saludar = "dice Hola tambien"; // error: Identifier 'saludar' has already been declared
~~~  

Aquí tampoco tendremos error porque ambas instancias son tratadas como variables diferentes, ya que tienen ámbitos diferentes.  

~~~
 let saludar = "dice Hola";
    if (true) {
        let saludar = "dice Hola tambien";
        console.log(saludar); // "dice Hola también"
    }
    console.log(saludar); // "dice Hola"
~~~  
   
  

Este hecho hace que **_let_** sea una mejor opción que **_var_**. Cuando se utiliza **_let_**, no hay que preocuparse de sí se ha utilizado un nombre para una variable antes, puesto que una variable solo existe dentro de su ámbito.  

## **CONST**  

Las variables que van asociadas a **_const_** mantienen valores constantes.  

Al igual que las declaraciones **let**, solamente se puede acceder a las declaraciones **_const_** dentro del bloque en el que fueron declaradas.  

No se puede actualizar ni volver a declarar. **_Const_** debe ser inicializada en el momento de la declaración.  

~~~
 const saludar = {
        mensaje: "dice Hola",
        datos: 2
    }
console.log(saludar);
~~~
 
Como no queremos siempre tener la capacidad de redefinir nuestras variables **_const_** es muy adecuado. Nos da herramientas más útil que los otros.  

Vamos a ver un ejemplo poniendo primero **_let_** para ver la diferencia. 

~~~
let city= "Vitoria";
  console.log(city); // Vitoria

city = "Bilbao";
  console.log(city);  
~~~  

Nos da los dos resultados.   

Vitoria<br>
Bilbao  

Poniendo **_const_** arriba en vez de **_let_** sólo devuelve "Vitoria", aunque tratemos de enviar algo a `console.log` no funciona.  

# **FUNCIÓN FLECHA**  

<img src="https://github.com/user-attachments/assets/7aa5ae80-0d24-4e6a-bf1a-eca8b9426843" alt ="flecha" width= "600">

Las funciones de flecha se pueden usar de la misma manera que las expresiones de función. Es una versión más corta y efectiva. Nos dan el mismo resultado que las expresiones de función pero es una de las cosas más importantes de aprender en JavaScript moderno. Por lo que es una forma nueva y muy popular actualmente.  


<img src= "https://github.com/user-attachments/assets/ff881e81-1d37-467e-9c83-31bca38fe337" alt= "función" width= "600">

La forma más sencilla de utilizarlas y su sintaxis (el signo de "igual más el signo de "mayor que" ) :  

~~~
holaMundo= () => {console.log('empezamos');}
holaMundo();
~~~  

Esto nos dará como resultado `empezamos`.  

La función flecha siempre tiene que estar almacenada dentro de una variable y se ejecuta de inmediato. Al poner la función flecha el código que vayamos a incluir dentro tiene que estar entre corchetes {}. Luego llamamos a "holaMundo" de la misma forma que llamamos a una función.  

Las funciones con flecha son como funciones anónimas, en lugar de añadir el nombre de la función, sólo ponemos los paréntesis "()" seguidos de una flecha y seguido de lo que queremos ejecutar.  

~~~
primerNombre = pNombre => {console.log(pNombre.toUpperCase());}
primerNombre ("Ibai");
~~~  

primerNombre es la función y pasamos un único argumento, la flecha y dentro de los corchetes el argumento.  

Toman los parámetros a la izquierda de =>, los evalúan y devuelven la expresión del lado derecho.  

Esto nos dará como resultado: "IBAI".

Si hay más de un argumento tienen que estar dentro de paréntesis()  

~~~
nombreCompleto = (pNombre, uNombre) => {console.log(`${pNombre} ${uNombre}`);
   nombreCompleto("Ibai", "Gonzalez");
~~~  

Una función flecha no es más que otra manera de definir una función.  

Nos dará como resultado: "Ibai, Gonzalez".  

# **DECONSTRUCCIÓN DE VARIABLES** 

Es una herramienta nueva en JavaScript, permite trabajar con colecciones, poder cortar elementos de ellas, almacenarlos en variables.  

Deconstrucción es la capacidad de intercambiar valores de variables. Antes había que crear variables temporales para simplemente cambiar los roles de las variables. Ahora hay un modo de implementar esta tarea de manera mucho más rápida que antes.

~~~
let jugador1 = "Alba";
let jugador2 = "Ibai".  
~~~ 

LO que queremos hacer es cambiar los roles de estas variables. 


<img src= "https://github.com/user-attachments/assets/ee33f4fd-e7df-4c05-82e0-ab9bc40dfdb7" alt = "intercambio jugadores" width= "600">

Una vez que asignamos un nombre a la variable persona1 no se podría intercambiar.  

Como hemos dicho, antes se creaban variables temporales:  

~~~
let tempJugador1= "Alba";
let tempJugador2= "Ibai";
~~~  

Veamos como queda nuestro código primero sin usar las variables temporales.
~~~
jugador1 = jugador2
jugador2= jugador1

console.log(´
  jugador1 : ${jugador1}
  jugador2 : ${jugador2}
´)
~~~  

El resultado que nos daría esto es que `jugador1: "Ibai" y jugador2 : "Ibai" `. Esto no es lo que buscabamos.   

Lo que hemos echo aquí es que hemos asignado al jugador 1 el rol del jugador 2 (que era Ibai) y luego al jugador 2 que era Ibai le hemos asignado el rol del jugador 1 al que acababamos de asignar Ibai. Por lo tanto ahora Ibai es jugador1 y jugador2.  

La forma de arreglar esto es con las  variables temporales.  

~~~
let tempJugador1= "Alba";
let tempJugador2= "Ibai";
~~~  

~~~
jugador1 = tempJugador1;
jugador2 = tempJugador2;
~~~  

El jugador 1 iría a la variable temporal 1 y el jugador 2 a la variable temporal 2. Tenemos este paso intermedio. Cada jugador toma el valor de la variable temporal y así ya no se colapsan.  


Pero lo que queremos es cambiar los roles, por lo tanto:  

~~~
jugador1 = tempJugador2;
jugador2 = tempJugador1;
~~~  

Ahora sí tendríamos que el jugador1 sea "Ibai" y el segundo sea "Alba"  

jugador1: "Ibai"
jugador2: "Alba".  

Con JavaScript moderno nos vamos a deshacer de mucho de este código. No se necesita. Sólo tenemos que poner entre corchetes [] el código que queremos intercambiar.  

~~~
[jugadro1, jugador2] = [jugador2, jugador1]
~~~
Así es como se pueden intercambiar valores, esto es la "**_deconstrucción de variables_**". En una sola línea de código hemos cambiado los roles intercambiando sus valores.  

Resultado es el mismo de antes:  
jugador1: "Ibai"
jugador2: "Alba".  


<img width="600" alt="Captura de pantalla 2025-07-10 124604" src="https://github.com/user-attachments/assets/8c2233d1-2f27-44d6-97ab-7fc7b264be06" />  

La desestructuración hace que tu código sea mucho más limpio y fácil de leer, permite extraer valores de arrays u objetos y asignarlos a nuevas variables de una manera más concisa y legible.  

Ejemplo nuevo utilizando matrices. La definimos como "ganadoresLiga" que contiene tres valores de cadena "Barcelona", "Madrid", "Bilbao".  

<img width="600" alt="Captura de pantalla 2025-07-10 140128" src="https://github.com/user-attachments/assets/97e8751e-ed42-495d-a02b-f05631306b4d" />


~~~

const ganadoresLiga = ["Barcelona", "Madrid", "Bilbao"];
const [campeón] = ganadoresLiga;
console.log("El campeón es:", campeón);
~~~  

El resultado sería:  

~~~
El campeón es: Barcelona
~~~  

`const [campeón] = ganadoresLiga;` Aquí creamos la deconstrucción. Lo que ponemos en el lado izquierdo (campeón) le estamos diciendo a JavaScript que tome el primer elemento de nuestra matriz "ganadoresLiga". Y así asigna el valor a una nueva variable constante llamada "campeón". Los demás elementos del conjunto ("Madrid", "Bilbao") son simplemente ignorados en esta desestructuración. La desestructuración permite extraer fácilmente solo los valores específicos que se necesitan de un array. Hace que el código sea limpio y fácil de leer. 






# **OPERADOR DE EXTENSIÓN EN JAVASCRIPT**  

Es una herramienta muy poderosa. Se puede usar en muchos de los marcos de JavaScript más populares.   

La sintaxis es `...` (tres puntos seguidos por algún tipo de palabra)

El operador de extensión (spread operator) en JavaScript es una característica súper útil introducida en ES6 que te permite expandir un elemento iterable (como un array o una cadena) en lugares donde se esperan cero o más argumentos (para llamadas a funciones) o elementos (para literales de array) o pares clave-valor (para literales de objeto). 

1. Con Arrays  

Es uno de los usos más comunes. Se puede usar para copiar arrays, concatenar arrays, añadir elementos..  

  
* Creamos una copia:  


~~~
const numeros1= [1, 2, 3];
const numerosCopia = [...numeros1]; 

console.log(numerosCopia);
console.log(numeros1=== numerosCopia); // false (son arrays diferentes)
~~~  
Nos da la copia [1, 2, 3] aunque al ser una copia no tienen el mismo código de situación en el programa. Cada array tiene su referencia única.  

Si haríamos esto utilizando **_slice_**  

~~~
const numeros1= numerosCopia.slice();
console.log(numeros1);
~~~  

Nos da: <br>  

[ 1, 2, 3 ]  

Es una manera adecuada de copiar una colección pero ahora se usa el operador de extensión que es lo ideal. Hacen exactamente lo mismo pero actualmente se usa el operador. Son dos formas de conseguir el mismo resultado.  

 
* Añade elementos  

Antes se podía usar "push" para agregar elementos en una matriz, nos daría lo siguiente `[1, 2, 3 , [23, 10]]. Agregaba otra matriz dentro de la primera. Empuja una nueva matriz porque JavaScript no entendía que quieres añadirla.  
~~~
let numeros1 = [1, 2, 3];
let otros = [23, 10];
console.log(numeros1.push(otros));
~~~  


 Por eso aparece el operador de programación (...) colocado delante de la variable, encuentra los elementos nuevos y los agrega a la matriz.
~~~
let numeros1 = [1, 2, 3];
let otros = [23,10];
const numeros = [...numeros1, ...otros];
console.log(numeros);
~~~ 

Nos dará [ 1, 2, 3, 23, 10 ]  

* Argumentos de función  

Tenemos una serie de valores y queremos ver cual es el mayor. (Vamos a usar la biblioteca Math.max). Si ponemos una matriz con una serie de números y usamos el operador de extensión, va a tomar cada elemento de la matriz y lo convierte en argumento de una función.  

Tenemos una matriz `[2,4,6,90,230]` y la almacenamos en "total" . Si ponemos el operador, lo que hace JavaScript es que toma todo lo que está en la colección y lo convierte en un conjunto de elementos. (Pasa de ser `...[2,4,6,90,230]` a ser `2,4,6,90,230`. Ya no pasamos un sólo argumento de función, estamos pasando cinco enteros.  

~~~
const total = [2, 4, 6, 90, 230];
console.log(Math.max(...total)); 
~~~  

Nos da como resultado "230".   

Si haríamos esto sin el "operador" nos daría un resultado nulo. Porque antes JavaScript entendía que esto era un argumento de función (es una matriz) no un número. Por eso daría "null". 
~~~
const total = [2, 4, 6, 90, 230];
console.log(Math.max(total));
~~~  

Nos da "NaN".  

* Como trabaja el operador de programación con la deconstrucción de objetos.  

Vamos a crear un objeto con una serie de elementos. Son jugadores de fútbol, titulares y suplentes. 

<img src = "https://github.com/user-attachments/assets/7b069055-0d84-4185-afac-06782627605a" alt = "banquillo" width = "600">  

Vamos a poner dos delanteros y dos suplentes pero no sabemos el número determinado de suplentes que va a tener el equipo.  

~~~
const equipo = {
  delantero : "Iniesta",
  defensa: "Puyol",
  suplente_1 : "Messi",
  suplente_2 : "Pique"
};
~~~  

Los corchetes aquí nos indican que se va a realizar la deconstrucción y esto es específico de objetos.

Hemos dicho que va a haber un número variable de suplentes. No sabemos exactamente cuántos. Es una regla que va a cambiar. Aquí el **_operador de extensión _** nos va a ayudar mucho para realizar la deconstrucción.  

~~~
const {delantero, defensa,...suplentes} = equipo;
~~~  

Ponemos suplentes en el operador porque no sabemos cuántos va a haber, no es específico como el delantero y el defensa. LO que hace JavaScript es que al ver el operador se da cuenta que nos referimos a cualquier número de suplentes, buscará todo lo que queda y lo pondrá en otro objeto.  

~~~
console.log(delantero) // Nos dará "Iniesta".
console.logCdefensa) // Nos dará "Puyol".
console.log(suplentes) // Nos dará Object {
                                      suplente_1 : "Messi",
                                      suplente_2 : "Pique"
~~~  

Delantero y defensa tienen sus propios valores.  
Suplentes se convierte en un nuevo objeto que contiene las propiedades suplente_1 y suplente_2 con sus respectivos valores.  

Este patrón es muy útil para extraer propiedades específicas de un objeto mientras se agrupa el resto de las propiedades en un solo objeto, lo que es común en la manipulación de datos y la gestión de estados.

Es una de las formas más comunes de usar argumentos de función cuando no sabes cuantas vas a tener y necesitas extraerlos y almacenarlos dentro de una variable.   

Vamos a ver otro ejemplo para aclarar bien lo que hace el **_operador_**.  

Tenemos un libro y vamos a dar información sobre él.  

<img width="600" alt="Captura de pantalla 2025-07-10 141006" src="https://github.com/user-attachments/assets/96e27ae2-1cec-4235-af7b-0eb8beb827d1" />


~~~
const libro = {
   titulo: " Todo muere",
   autor: "Juan Gómez Jurado",
   editorial: "Anna Puig",
   publicación : 2024
};
const {titulo, autor,...otrosDatos} = libro;
console.log(titulo);
console.log(autor);
console.log(otrosDatos);
~~~  

Primero definimos el objeto "libro" con sus propiedades. `const {titulo, autor,...otrosDatos}` es la desestructuración.
El título y el autor van a ser variables específicas ( no van a cambiar). Pero en otrosDatos no sabemos el número exacto de elementos que queremos añadir por lo que lo añadimos con el **_operador_**. Éste recoge todas las propiedades restantes, editorial y publicación y las agrupa en un nuevo objeto llamado "otroDatos".  

El resultado será:  

~~~
 Todo muere
Juan Gómez Jurado
{ editorial: 'Anna Puig', 'publicación': 2024 }
~~~  

# **PROGRAMACIÓN ORIENTADA A OBJETOS**  

Queremos construir algo, en lugar de pensar en cada línea de código por separado, la **_POO_** (programación orientada a objetos) te da una forma de organizar todo. Es un estilo de programación donde todo se organiza alrededor de elementos (_**objetos**_).  

Cada "objeto" tiene una serie de características que lo definen (**datos**. Un coche tiene un color, marca,..) . También tiene un comportamiento (**acciones**). Esto es lo que el objeto puede hacer ( un coche puede acelerar, frenar..).  

En lugar de tener listas de datos, y funciones separadas la _**POO**_ junta los datos con las acciones todo dentro del objeto.  

La **_POO_** te ayuda a crear programas pensando en objetos del mundo real(personas, coches...) cada uno con sus características y sus habilidades. Haciendo el código más organizado y fácil de entender. 

Las versiones antiguas de JavaScript no tenían los componentes de programación orientados a objetos. Las versiones modernas han implementado clases. Una **_clase_** es una lista de definiciones que dicen exactamente como debe comportarse la clase. Se pondrán los atributos para que pueda describir lo que se supone que hace la clase y el comportamiento que va a tener.  

Un ejemplo es cuando tenemos una clase de usuario, cada vez que un nuevo usuario entra al sitio y se registra, el programa va a mirar en la clase de usuario.  

Va a ver como debe comportarse ese usuario y luego le llevan al siguiente paso (tenemos clase de usuario, tiene un nombre de usuario, apellidos, que página quiere ver el usuario...) Lo que el programa va a hacer es que va a crear una instancia de un objeto con ese y va a ser el objeto con el que en realidad va a trabajar.  

Se utilizan funciones como clases. Las clases están compuestas de toda clase de cosas.  

* Las clases son plantillas para crear objetos, que a la vez, son instancias de esas clases.
* Las clases pueden heredar propiedades y métodos de otras clases.
* Polimorfismo. Los objetos pueden tomar diferentes formas dependiendo del contexto.
* Encapsulación. Los objetos ocultan su implementación y exponen solo lo necesario.  
Intentemos ver un ejemplo. Queremos tener a un perro en nuestro código. Según la **_POO_** , un perro va a tener características(datos) y puede realizar acciones(comportamiento). 

Primero creamos el objeto perro:  

~~~
class Perro {
  
  constructor(nombre, raza) {
    this.nombre = nombre; 
    this.raza = raza;    
  }
~~~  

Es comno si iríamos a construir un "perro". Esto define que cualquier perro va a tener su nombre y su raza.

El constructor se ejecuta cuando creamos un nuevo "Perro". Y el código con "this" nos da las características. El nombre y la raza van a ser propios de cada nuevo perro. Cada nueva instanciación de la clase Perro. Con la _** instanciación**_ (que es una palabra clave muy importante en JavaScript) lo que hacemos es decirle a la clase que queremos crear algo que coincida con sus datos, nombre y raza. (Un perro que se llame Zuri y sea un Bichón Maltes u otro perro  que se llame Linda y sea un Pastor Alemán...)

Ahora vamos a poner una acción que el perro puede hacer.  

~~~
  ladrar() {
    console.log(`${this.nombre} dice: guau`);
  }

}
~~~  

Creamos el objeto "miPerro" a partir de la clase "Perro". Tiene sus propios datos.

~~~
const miPerro = new Perro("Zuri", "Bichón Maltes");
console.log(`Mi perro se llama ${miPerro.nombre} y es un ${miPerro.raza}.`);
~~~  

Con esto creamos un objeto real llamado "miPerro". Y con new Perro queremos decirle a la clase Perro que instanciamos un nuevo Perro con sus respectivos datos.

También podemos dar un método. Cada objeto realiza la acción con sus propios datos. En este caso, `Zuri ladra`.

~~~
miPerro.ladrar();    
~~~  

Esto nos dará como resultado `Mi perro se llama Zuri y es un Bichón Maltes`. `Zuri dice: guau`.

Los conceptos básicos de la programación orientada a objetos es que tenemos una clase, con objetos (que son instancias individuales) que tienen sus propios datos y comportamientos.  

En JavaScript hay mucha superposición, haremos con las clases cosas igual que lo que haríamos con funciones porque en este lenguaje todo es una función, todo es un objeto.  

<img width="600" alt="Captura de pantalla 2025-07-11 134235" src="https://github.com/user-attachments/assets/37fe521f-bdbb-4648-97f0-903d9a4b30a1" />


Una de las cosas más importantes de la **_POO_** es que después de crear nuestra clase, tenemos que incluir la **_función constructor_**. Esta ejecuta todos los procesos que queramos. **_Constructor_** es una palabra clave reservada en las clases. No se requiere obligatoriamente pero es muy común, ya que es difícil que se cree una clase y no queramos hacer algo con ella enseguida. **_Constructor_** realiza las tareas básicas que queremos hacer cada vez que instanciamos una clase nueva. Porque una clase por sí sola no es nada, no podemos hacer nada con ella. Sólo nos da un conjunto de reglas y pautas para desarrollar objetos.  

Otro ejemplo distinto. Tenemos una clase instructor que va a tener una "función constructor" en la que incluímos "nombre" ( este "nombre" se ingresará siempre que creemos un nuevo instructor. Es parte de la clase cuando se cree una nueva, por eso tenemos que ponerlo en "This.name".  

Este "name" referencia el mismo elemento dentro del objeto. Pero "this.name" referencia a la instancia del "instructor"(la clase en sí).  

Cada vez que cambiemos de instancia, cambiaremos el "nombre" que se ingresará en un nuevo objeto.  

~~~
class Instructor {
   constructor ({name}) {
   this.name= name;
   }
}
~~~  

Vamos a crear un nuevo instructor con sus propios datos.  

~~~
const Ibai = new Instructor ({name: "Ibai Olivenza"})
console.log(Ibai);
~~~  

Tenemos una variable llamada "Ibai" que es igual a instructor nuevo y dentro de ella metemos un objeto y los datos de la función constructor que era "name". Cuando programas algo nuevo debemos ingresar ese objeto(name).  

"Ibai" es un objeto que se considera una instancia de la clase "instructor".   

Esto nos daría como resultado : `Instructor { name: 'Ibai Genial' }`.   

Si pondríamos `console.log(Ibai.name);` Nos daría: `Ibai Olivenza`.  

 


    

# **PROMESA EN JAVASCRIPT**  

Las **_promesas_** son la forma en que JavaScript maneja las cosas que no suceden al instante. Un ejemplo claro son cuando cargas datos en internet (tarda un poco en decirte si puedes seguir o si los datos no son correctos), pero tienes la garantía de que en el futuro (enseguida) recibirás una respuesta. Ya sea exitosa o rechazada. Las **_promesas_** tienen que ver específicamente con la experiencia de usuario.  

Si consultas algo en internet y la página va lenta, el usuario tiene que esperar más de lo normal o volver a la página a cargar.. esto es una mala experiencia. Para evitar que esto ocurra podemos utilizar **_promesas_**.  

El sistema en el que trabajan es 50/50. El 50% del tiempo se gastará pensando si la situación funciona y la promesa regresa con una respuesta y el otro 50% se gasta edificando que proceso quieres que ocurra si sale error.  

Una _**promesa**_ es un objeto que representa la eventual finalización o fallo, de una operación asincrónica. Representan un valor que podría estar disponible ahora, en el futuro o nunca.   

Vamos a ver un ejemplo en la vida real. Pedimos una hamburguesa a domicilio. Cuando haces el pedido estas creando una **_promesa_**. Le dices al restaurante lo que quieres y este te da la promesa de que te lo llevará a tu casa. La hamburguesa todavía no está hecha pero hay un compromiso de que llegará.  

* Pendiente (pending). Es el estado inicial. (La hamburguesa todavía no está echa).  

* Cumplida(fulfilled). Todo ha salido bien, la hamburguesa ha llegado a tu casa. Tenemos un resultado exitoso.  

* Rechazada(rejected). La operación salió mal. No había repartidores disponibles y no te van a mandar la hamburguesa.  

JavaScript simula este ejemplo de compromiso.   

<img width="600" alt="Captura de pantalla 2025-07-12 025821" src="https://github.com/user-attachments/assets/bc830c29-f287-4cf9-84ed-8859a8d6cd25" />

~~~
function pedirHamburguesa() {
  return new Promise((resolver, rechazar) => {
    setTimeout(() => {
         return("genial...")
    }, 2000); // Esto indica que vamos a esperar 2 segundos para ver el resultado.
  });
}
    

~~~  

New Promise toma los dos argumentos (resolver y rechazar) y usamos una función flecha de indicador. Al tener dos argumentos, se espera que si la promesa funciona da una cosa y sino se espera que muestre algún tipo de error.  

Le tenemos que decir al programa que nos de algo devuelta, ya sea exitoso o si hay error.  

Con setTimeout que es una función de indicador, estamos mostrando que nuestra expectativa de lo que va a ocurrir no será inmediatamente. Tardará 2 segundos en ejecutarse.

~~~
console.log("Haciendo el pedido de hamburguesa...");

pedirHamburguesa()
  .then((mensajeDeExito) => {
    console.log("¡Genial!", mensajeDeExito);
  })
  .catch((mensajeDeError) => {
    console.error("¡Ups!", mensajeDeError);
  });

console.log("Esperando la hamburguesa...");  // Esto se ejecuta INMEDIATAMENTE 
~~~  
Esto nos devuleve `Esperando la hamburguesa...`.

Las **_promesas_** se crean con el constructor Promise que acepta una función con dos argumentos: resolver, rechazar. Luego utilizamos los métodos **_then()_**(se ejecuta cuando la promesa se resuelve, se cumple) y **_cath()_**(se ejecuta cuando la promesa se rechaza, se produce un error y recibimos el motivo del rechazo como argumento). 

Vamos a ver otro ejemplo. Tenemos una función que podemos traducir como saludo durmiente. Ponemos "new promise" con los dos argumentos de resuelto y rechazado. Si la promesa funciona nos da una cosa, (en este caso "Hello...") y si no nos dará error (Too sleety...").  

Colocamos nuestra clave configurar interrupción (setTimeout) que nos ayuda a que lo que pongamos dentro de ese código se ejecutará. O para resolver la promesa con éxito o para darnos un errr. Por eso tenemos dos escenarios distintos con "setTimeout". 

Por último tenemos el tiempo, 2000. Esto nos dice que el programa tardará 2 segundos en ejecutarse.  No lo hace automáticamente.  

~~~
let sleepyGreeting = new Promise((resolve, reject) => {
    setTimeout(() => {
        resolve("hello...")
        
    }, 2000);
    setTimeout(() => {
        reject(Error("Too sleepy..."))
    }, 2000);
});
~~~  
Ahora ponemos nuestro saludo "sleepyGreeting" y tenemos que utilizar las palabras reservadas en JavaScript **_then_** y _**catch**_.  

La palabra clave **_then_** accede a los datos que son un tipo de elemento específico en este caso. Cada vez que regrese una promesa nos va a dar la cadena del principio, es decir "hello...". Este es nuestro dato.  

Si todo sale bien recibiremos los datos y tendremos acceso a ellos.  

Y por último tenemos el rechazo, el error. "Catch" significa que atrapa el error.  

Datos es a luego (data =>then) como error es a anzuelo (err=>catch)
~~~
sleepyGreeting
    .then(data => {
        console.log(data);
    })

    .catch(err => {
        console.error(err);
    });  

~~~   
Si ejecutamos todo, tardará dos segundos en darnos el resultado.  


Esto nos devuelve `hello...`.


# **ASYNC Y AWAIT**  

En JavaScript las tareas son asincronimas. No ocurren instantáneamente. La tarea se inicia y el programa continúa ejecutando otras cosas mientras que espera que la operación asincronima termine. 

El problema más importante al que se enfrentan estas dos herramientas es la "devolución de llamadas".   


Incluso con las **_promesas_**, el código seguía siendo difícil de leer cuando hay que encadenar muchas operaciones asíncronas consecutivas.  

Aquí es donde aparecen dos herramientas especialmente útiles. **_Async_** y **_await_**. No añaden nueva funcionalidad fundamental, sino que proporcionan una forma mucho más elegante y legible de escribir código asíncrono. Son especialmente útiles cuando se trabaja con operaciones que pueden tardar un tiempo en completarse. Te permiten escribir código asíncrono de una manera que parece síncrona, haciéndolo mucho más legible y fácil de mantener que las cadenas de .then() y .catch() de las Promesas.

### **ASYNC**  
Se utiliza para declarar una función asíncrona. Cuando la llamamos SIEMPRE devuelve una promesa. Esta se resuelve cuando la función se completa.  

Permite usar **_await_**. Una función marcada con **_async_** es la única que puede usar la palabra clave "await" dentro de su código.  

### **AWAIT**   

Pausa la ejecución hasta que la "promesa" se resuelva. Nos permite hacer el proceso "Promise.then" de forma más eficiente.  

Cuando pones _**await **_ delante de una Promesa, JavaScript pausa la ejecución de la función _**async**_ hasta que esa Promesa se resuelva o se rechace.  



Nos dan ventajas, como construir un código más sencillo y legible. Permiten escribir código asincrono de manera más lineal y fácil de entender.  

Menos callbacks . Ya no es necesario anidar callbacks(funciones que se ejecutan después de que otra haya terminado su tarea) para manejar operaciones asíncronas.   

Mejor manejo de errores.  

Resumen:  

_**async**_ convierte una función en una "función especial" que sabe cómo manejar Promesas.

_**await**_ solo se puede usar dentro de esas funciones async. Lo que hace es pausar la función async hasta que la Promesa que tiene al lado termine.  

~~~
function obtenerDatosTardios() {
  return new Promise(resolve => {
    setTimeout(() => {
      resolve("¡Datos obtenidos después de un retraso!");
    }, 2000); 
  });
async function mostrarDatos() {
  console.log("1. Iniciando la operación...");
~~~  

Ahora vamos a poner **_await_** que va a pausar la ejecución de la función "mostrarDatos", hasta que la promesa se resuelva. 

~~~
  const mensaje = await obtenerDatosTardios();

  console.log("2. Mensaje recibido.");

  console.log("3. La función 'mostrarDatos' ha terminado.");
}

~~~  

Ahora llamamos a la función.  

~~~
mostrarDatos();

console.log("4. Este mensaje aparece inmediatamente...");
~~~  

Este mensaje (4) aparecerá antes que el mensaje "2" y "3", porque 'mostrarDatos' es asíncrona y permite que el resto del código se ejecute. 
Esto nos dará:  

~~~
1. Iniciando la operación...
4. Este mensaje aparece inmediatamente.
2. Mensaje recibido.
3. La función 'mostrarDatos' ha terminado.
~~~


Vamos a mostrar otro ejemplo. Vamos a construir una variable con una función flecha sin argumentos y dentro pondremos una promesa con un temporizador.  



~~~
const registro= () => {
  return new Promise((resolve, reject) => {
  setTimeout(() => {
  resolve("Usuario registrado...");
  } , 2000);
 });
}
~~~  

Esto realmente nos valdría para comunicarse con una base de datos y devolver información del usuario.  


<img width="600" alt="Captura de pantalla 2025-07-14 230005" src="https://github.com/user-attachments/assets/3bce79c7-bb6a-4fa2-aaaf-ea5c8a64a0f8" />  



Esta será la función de registro, devuelve una promesa y nos ejecutamos ningún rechazo.  

Pero antes de que un usuario se registre hay que actualizar su cuenta.  

~~~
const actualizarCuenta= () => {
  return new Promise((resolve, reject) => {
  setTimeout(() => {
  resolve("Actualizando último registro...");
  } , 2000);
 });
}
~~~  

Esta es una función para actualizar la cuenta. Como puedes ver, es prácticamente idéntica a la anterior.  

Esto es lo que se comunicaría a la base de datos. Por lo tanto, ambas funciones necesitan suceder de manera secuencial. Si actualizar cuenta ocurre antes del registro, nos daría error. Primero hay que pasar los datos del registro y verificarlos antes de actualizar su cuenta.  

Por este motivo son útiles **_async y await_** . Vamos a crear la función que tiene que empezar con la palabra **_aysnc_** y luego la declaración que vayamos a dar ( que este caso será "actividades de registro"). Como es una función normal dentro pondremos la variable "devolver registro" y la igualamos a **_await_** registro.  

~~~
async function actividadesRegistro () {
  const devolverRegistro= await registro();
  }
console.log(devolverRegistro);
~~~  

Esto llama a la primera función que hemos creado. Al poner **_await_** le estamos diciendo que no haga nada hasta que la "promesa" se haya completado.  

Cuando se complete nos dará `Usuario registrado...`. Nos daría datos como el nombre. apellido, mail...  

Ahora tendríamos que llamar a la función para que esto se lleve acabo.  

~~~
actividadesRegistro();
~~~  

Esto nos devolvería `Usuario registrado...`.  

Ahora hay que hacer lo mismo para la segunda función (actualizar cuenta).  

~~~
const devolverActualizarCuenta = await actualizarCuenta();
console.log(devolverActualizarCuenta);
~~~  

Hemos creado una especie de lista para ver cuando queremos que estos procesos ocurra y el orden.  

Primero aparecerá `Usuario registrado...` y dos segundos después aparecerá ` Actualizar cuenta...`.  

No podemos actualizar una cuenta antes de que un usuario inicie sesión. 

También puede darse el caso que quieras que todo se ejecute a la vez, en lugar de que uno ocurra y luego el otro). Para eso existen los **_cierres_** .  

Al poner **_aysnc y await_** en un programa y combinarlos con los **_cierres_** podemos controlar cuando se ejecutan todos los procesos.  

Para realizar esto, lo único que hay que hacer es crear argumentos dentro de la función.  

~~~
async function actividadesRegistro(registro, actualizarCuenta){
 const devolverRegistro=  await M;
  console.log(devolverRegistro);
 const devolverActualizarCuenta= await actualizarCuenta;
   console.log(devolverActualizarCuenta);
~~~  

En la función hemos añadido los dos argumentos que necesitamos y en la herramienta **_await_** simplemente podemos poner cualquier letra o palabra, pero siempre sin paréntesis() porque ahora es un argumento, no una función.  

Ahora tenemos que llamar a la función para que nos dé un resultado.  

~~~
actividadesRegistro(registro(), actualizarCuenta());
~~~  

Vemos que aquí los argumentos se vuelven a convertir en funciones. Envolvemos todo en esas dos funciones. Como devuelven "promesas" se pueden tratar igual.  

Lo que van a hacer **_async y await_** es que envuelven todo el proceso y en lugar de esperar 2 segundos para ejecutar una y otros dos para la siguiente, no muestra nada en la pantalla hasta que los dos procesos estén completados.  
 
~~~
Usuario registrado...
Actualizando último registro...
¡Proceso completo!
~~~  




   


     







 

 

