# Sesión 05 - 17/04 Apuntes  
---
## Transformaciones & condicionales { IF - ELSE }  
### Transoformaciones:  
**¿Qué son los radianes?**  
Es la forma de medir los ángulos por defecto en vez de grados.  
Basicamente otra unidad de medida.  

#### Ángulos:  

*angleMode();*
p5.js usa RADIANES oara medir los ángulos.  
*angleMode(RADIANS);*
Se usa en function SETUP  
*angleMode(DEGREES);*  

**Hay que pensarlo como las agujas del reloj:**  
![Angulo](https://i.pinimg.com/736x/05/d4/2f/05d42f9b69602ceffd45f459e21d2bd1.jpg)

**Rotación:**  
rotate(); 
Siempre rotan alrededor del punto de origen(0,0)  
se recomienda usar translate();
en algunos casos con rectMode(CENTER);
**Sintaxis: rotate(valor radianes o en grados);**  
Ejemplo: rotate(20);  
**Transladar:**  
translate();  
Sirve para transladar el PUNTO DE ORIGEN(0,0) a otra coordenada de mi canvas.  
**Sintaxis: translate(x,y);**  
Ejemplo: translate(200,200);  

#### Guardar y restaurar:  
push();
pop();  
Funciones que trabajan juntas como un "sistema de memoria temporal" para el estilo y las transformaciones del lienzo.  
Sintaxis: push();
Sintaxis: pop();
#### Escala:
scale();  
La función scale() ajusta la escala del sistema de coordenadas actual por el factor especifico.  
Sintaxis: scale(x,y);  
Ejemplo: scale(2,2);  
### Condicionales:  
**Lógica condicional & expresión booleana:**  
- Expresión booleana: Una expresión booleana es cualquier enunciado, dato o instrucción que, al ser evaluado, solo puede arrojar uno de los dos posibles: *verdadero (True) o falso (False)*.
  Ejemplo: Si algún estudiante apaga por completo las luces de la sala, la profesora debe bailar.

**Para construir este tipo de expresiones se utilizan 3 tipos de elementos: OPERADORES**  
![operadores](https://i.pinimg.com/736x/5e/b3/57/5eb35708d21ab54527aaf33ba72a51c1.jpg)
![operadores](https://i.pinimg.com/736x/aa/7c/e7/aa7ce764c8f6be5d0e358b5b0aa3a12a.jpg)  
![operadores](https://i.pinimg.com/736x/74/2d/d1/742dd174d25e835bd7fedc2592bc438a.jpg)  

#### Ejemplos de operaciones de comparación:  
- *menor que < y mayor que >*: Al comparar números, el operador devuelve un booleano basado en la comapración matematica.  
Ejemplos:  
//menor que 2 < 3// devuelve true  
3 < 2 // devuelve false  
//mayor que 2 > 3// devuelve false  
3 > 2 // devuelve true  
- *Al comparar cadenas de texto, el operador compara carácter por cáracter basándose en su orden alfabetico.*  
Ejemplos:  
'b' < 'a'// devuelve false  
'b' < 'c'// devuelve true  
'abc' < 'aaa'// devuelve false porque 'b' no es menor que 'a'  
'abc' < 'abd'// devuelve true porque 'c' si es menor que 'd' 
- *menor o igual que: <= y mayor o igual que: >=* Similar a < y >, pero también devuelve true cuando ambos valores son iguales.  
Ejemplos:  
12 < 12// devuelve false  
12 <= 12// devuelve true  
- *Lo mismo se aplica a las cadenas de texto, comparando siempre su orden alfabético.*  
Ejemplos:  
'a' < 'a'// devuelve false, ya que la posición de ambas cadenas en el alfabeto es la misma, por lo tanto no son diferentes.  
'a' <= 'a'// devuelve true  

*Igual == y no igual !=*  
El operador igual == devuelve true cuando los operandos son iguales y false cuando no lo son, mientras que el no igual != devuelve true cuando los operados no son iguales y false cuando son iguales.  
Ejemplos:  
//número - número  
2==2 // devuelve true  
2!= 2 // deuvleve false  
(más ejemplos en el pdf de la clase)  

#### Ejemplos de operadores lógicos:  
**Operadores lógicos:**  
Los operadores lógicos se utilizan para comparar valores booleanos, y
existen tres operadores diferentes: AND &&, OR || y NOT !.  
**And &&:**  
*El operador AND devuelve true solo si los dos operandos son true; de lo
contrario, devuelve false. Por ejemplo:*  
let bool1 = true;  
let bool2 = false;  
console.log(bool1 && bool2); // imprimirá false  
**OR ||:**  
*A diferencia de AND, OR devuelve true cuando al menos uno de los
operandos es igual a true.*  
let bool1 = true;  
let bool2 = false;  
console.log(bool1 || bool2); // imprimirá true  

#### Sentencia condicional: IF-ELSE IF-ELSE  
La sentencia if es una estructura especial que existe en casi todos los lenguajes de programación; toma una condición  
–expresada como un booleano– y ejecuta unapieza de código contenida dentro de las llaves { }  
*If (condición) {ejecuta este código si es true}*  
Ejemplo: Si algún estudiante apaga por completo las luces de la sala, la profesora debe bailar.  
**If - else if - else:**  
La sentencia if puede complementarse con la sentencia else if, que añade condiciones de prueba complementarias
a la original, y con la sentencia else, que implica todos los casos que no cumplen con la condición original.  

*If (condición)*: {ejecuta este código si es true}  
*else if (condición 2)*: {ejecuta este código si es true}  
*else*: {ejecuta este código si ambas condiciones son falsas}  
Ejemplo: Si algún estudiante apaga por completo las luces de la sala, la profesora debe bailar.
Si no se cumple lo anterior SI la ayudante se levanta de su silla, la profesora debe cantar.
Y SI NO SE CUMPLEN NINGUNA DE LAS ANTERIORES, los estudiantes guardan silencio.  

**Encargo 04:**  
