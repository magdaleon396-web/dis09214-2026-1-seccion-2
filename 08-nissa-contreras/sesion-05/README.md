# sesión 04 - 17/04

# **Radios**  

* Radius- Radian
* Es una medida que se usa en geometría. Es cuando el ángulo de afuera mide lo mismo que el ángulo del circulo.
* Un ángulo forma un radian cuando el alguno de la circunferencia es igual a su radio.

![Radian](https://github.com/user-attachments/assets/c734de5c-003a-424b-ae65-a6bd43137a4e) 


___

## **Ángulos** angleMode();

* Por defecto p5.js usa radiantes para medir los ángulos.
* angleMode (RADIANS)
* Para cambiar a grados se usa esto en el fuction SETUP
* angleMode (DEGREES)

* Hay que pensarlo como se mueven las agujas del rejos:
    * TWO_PI 360°
    * PI 180°
    * HALF_PI 90°
    * QUARTER_PI 45°

![Ángulos](https://github.com/user-attachments/assets/87d480b3-5cca-436e-96ed-bdf7c53637b6) 


___
 
## **Rotación** rotate();

* Sirve para rotar elementos.
* Siempre rota desde el punto de origen (0,0)
* Se recomienda usar con traslante(); y en algunos casos con rectMode();


## **Traslate** translate();

* Sirve para trasladar el punto de origen (0,0) a otra coordenada de mi canvas.


## **Guardar y restaurar** push(); pop();

* Funciones que trabajan juntas como un "sistema de memoria temporal" para el estilo y las transformaciones del lienzo.
* Es para comenzar una variable y encerrarlo en una "capa" y no altera las demás.
* Si quiero que un objeto gire en el sentido contrario le pongo un menos y los valores se vuelven negativos.


## **Escala** scale();

* La función scale() ajusta la escala del sistema de coordenadas actual por el factor especificado.


___

# **Condicionales**

## **Expresion Boleana**

* Una expresión booleana es cualquier enunciado, dato o instrucción que, al ser evaluado, solo puede arrojar uno de dos valores posibles: verdadero (True) o falso (False).
    * Ejemplo: Si algún estudiante apaga por completo las luces de la sala, la profesora debe bailar.

 Para construir este tipo de expresiones se utilizan 3 tipos de elementos:

**Operandos (o valores):**
Son los datos básicos que se evalúan. Pueden ser:
Variables: (como x,y o mouseX, MouseY, etc).

Constantes o Literales: Valores fijos como 5, "Hola" o los mismos valores booleanos True y False.

**Operadores de Comparación:**
Permiten contrastar dos valores.  
* == (Igual a)
* != (Diferente de)
* > o < (Mayor o menor que)
* >= o <= (Mayor o igual / Menor o igual)

**Operadores Lógicos:**
Sirven para combinar varias expresiones.  
* AND (&&): Es verdadero solo si ambas partes son verdaderas.
* OR (||): Es verdadero si al menos una de las partes es verdadera.
* NOT (!): Invierte el valor (si era verdadero, pasa a ser falso).


___

**Ejemplo de comparaciones** 

menor que < y mayor que >
* Al comparar números, el operador devuelve un booleano basado en la comparación matemática.  
EJEMPLOS

* menor que
2 < 3 // devuelve true
3 < 2 // devuelve false

* mayor que
2 > 3 // devuelve false
3 > 2 // devuelve true

menor o igual que: <= y mayor o igual que: >  
* Similar a < y >, pero también devuelve true cuando ambos valores son iguales.  
EJEMPLOS

12 < 12 // devuelve false
12 <= 12 // devuelve true


___

**Ejemplos de operadores lógicos** 

**Operadores lógicos**  
Los operadores lógicos se utilizan para comparar valores booleanos, y existen tres operadores diferentes: AND &&, OR || y NOT !.

**AND &&**
El operador AND devuelve true solo si los dos operandos son true; de lo contrario, devuelve false. Por ejemplo:  
EJEMPLO:  
let bool1 = true;  
let bool2 = false;  

**OR ||**  
A diferencia de AND, OR devuelve true cuando al menos uno de los operandos es igual a true.  
EJEMPLO:  
let bool1 = true;  
let bool2 = false;  
console.log(bool1 || bool2); // imprimirá true

**NOT !**  
El operador NOT devuelve el opuesto del valor booleano actual.  
EJEMPLO:  
let bool1 = true;  
console.log(bool1); // imprime true  
console.log(!bool1); // imprime false


___

## **Sentencia condicional**  
If - else if - else

* La sentencia if es una estructura especial que existe en casi todos los lenguajes de programación; toma una condición –expresada como un booleano– y ejecuta una pieza de código contenida dentro de las llaves { }

If (condición) {ejecuta este código si es true}  
* Si algún estudiante apaga por completo las luces de la sala, la profesora debe bailar.

* La sentencia if puede complementarse con la sentencia else if, que añade condiciones de prueba complementarias a la original, y con la sentencia else, que implica todos los casos que no cumplen con la condición original. Puedes añadir tantas sentencias else if como desees). If (condición) {ejecuta este código si es true}  
else if (condición 2) {ejecuta este código si es true}  
else {ejecuta este código si ambas condiciones son falsas}


___

## Encargo 4  
Crear un sketch libre que contenga:

* Varias figuras geométricas
* Rotación
* Translate
* Push Pop
* Scale
* Texto
* Imagen
* 2 sentencias condicionales completas (If - else if - else)
