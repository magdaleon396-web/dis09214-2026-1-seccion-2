# sesión 04 - 23/03
# Datos dinámicos {variables}  

## Posición del mouse  
#### mouse X; mouseY; 
Variables de sistema numérico que determinan la posición del mouse en las coordenadas X e Y.   
__Sintaxis:__ (mouseX, mouseY);  
__Ejemplo:__ ellipse(mouseX, mouseY, 100, 100);  

## Crea variables propias
Para declarar una variables dinamicas usamos __let__  y __const__ para variables constantes.  

## Javascript objects  
Nos servirá para organizar nuestro código de una forma adecuada y ordenada.  

Es la forma de agrupar muchas variables dentro de una variable.  

Es una estructura de datos que te permite agrupar valores relacionados bajo un mismo nombre. En lugar de tener muchas variables sueltas, los objetos funcionan como un conjunto que organiza la información mediante __pares de clave y valor__.  

Luego se accede a la información mediante notación de punto.  

## random(); function  
Su trabajo es devolver un número __aleatorio__ dentro de un rango que tú definas.  

*  __random():__ Si no pones nada, devuelve un número decimal entre 0 y 1.  
__ejemplo:__ random() da 0.4571.
*  __random (máximo):__ Devuelve un número decimal entre 0 y el máximo que elijas.  
__ejemplo:__ random(100) da un número entre 0 y 100.
*  __random (mínimo, máximo):__ Devuelve un número decimal entre esos dos valores.   
__ejemplo:__ random(20,50) da un número entre 20 y 50.

## (width, height);  
Variables integradas en p5, que corresponden a los valores definidos en el createCanvas.  

### (windowWidth, windowheight);  
variables integradas en p5, que permiten ajustar tamaño del lienzo al tamaño de la ventana del navegador. Se usan en el createCanvas.  

## map(); function 
Esta función nos permite convertir un valor de un rango a otro.  

En términos simples: toma un número que está en una "escala" y lo traduce proporcionalmenete a una "escala" nueva.  

*  __sintaxis:__ map(valor, min_original, max_original, min_nuevo, max_nuevo)  
*  __valor:__ La variable que quieres "mapear" (por ejemplo, mouseX).  
*  __min_original y max_original:__ El rango en el que se encuentra ese valor actualmente. 
*  __min_nuevo y max_nuevo:__ El rango al que lo quieres transformar.  


