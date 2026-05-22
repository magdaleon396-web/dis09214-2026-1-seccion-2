# sesión 04 - 10/04

# Datos dinámicos  Variables  

### **Posición del mouse**

* Mouse X; Mouse Y

* Variable de sistema numérico que determinan la posición del mouse en las coordenadas x, y

Ejemplo: noStroke(); fill(247, 126, 193, 50); ellipse(mouseX, mouseY, 100, 100);  
No solo se puede usar en las figuras, si no que también en color, diámetros, etc.

___

## Variables integradas en p5.js

![Variables](https://github.com/user-attachments/assets/154177d4-38da-4cac-af54-6497ae35d04e)

![Variables2](https://github.com/user-attachments/assets/edf6466a-2031-4e00-9ba1-0dedf36de57d) 


___

## crea tus propias variables

1. Declarar tu variable
2. Inicializar tu variable
3. Usa tu variable

* Para declarar variables dinámicas podemos usar **let** para variables dinámicas y **const** para variables constantes.
* **OJO** antiguamente se usaba **var** en vez de **let**, se puede encontrar algunos tutoriales con var.

![Crear Variables](https://github.com/user-attachments/assets/1138ef89-0b1b-4390-b993-e09b2606fc78) 


___

## Javascript Objects

* Nos servirán para organizar nuestro código de una forma adecuada y ordenada.
* Es la forma de agrupar muchas variable dentro de una variable.
* Es una estructura de datos que permite agrupar valores relacionados bajo un mismo nombre. En lugar de tener muchas variables sueltas, los objetos funcionan como un "contenedor" que organiza la información mediante **pares de clave y valor**.
* Luego se accede a la información mediante notación de punto.

___

## random(); fuction

* Su trabajo es devolver un número **aleatorio** dentro de un rango que tú definas.

random(): Si no se pone nada, devuelve un número decimal entre 0 y 1
* Ejemplo: random() da 0.4571

random(máximo): Devuelve un número decimal entre 0 y el máximo que elijas.  
* Ejemplo: random(100) da un número entre 0 y 100.

random(mínimo, máximo): Devuelve un número decimal entre esos dos valores.
* Ejemplo: random(20, 50) da un número entre 20 y 50.

___

## width, height 

* Variables integradas en p5, que corresponden a los valores definidos en el createCanvas.

**(windowWidth, windowHeight);**  
* Variables integradas en p5, que permiten ajustar el tamaño del lienzo al tamaño de la ventana del navegador. Se usan en el createCanvas.

___

## map(); fuction 

* Esta función nos permite convertir un valor de un rango a otro.
* En términos simples se toma un número que está en una "escala" y lo traduce proporcionalmente a una "escala" nueva.

**Sintaxis:** map(valor, min_original, max_original; min_nuevo; max_nuevo) 

* valor: La variable que quieres "mapear" (por ejemplo, mouseX).  
* min_original y max_original: El rango en el que se encuentra ese valor actualmente.  
* min_nuevo y max_nuevo: El rango al que lo quieres transformar.

## Encargo de la clase
Hacer un duplicado del dibujo que entregue para la solemne y darle movimiento al dibujo en p5.js usando cada una de las variables y funciones que aprendimos durante esta clase:

* mouseX mouseY  
* let creado por mi  
* Javascript object  
* Random fuction  
* Width height  
* WindowWidth WindowHeight  
* Map función
