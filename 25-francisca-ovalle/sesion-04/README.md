# Sesión 04 - 10/04 Apuntes
---
## Variables  
Introduciremos el movimiento en P5.js, hay variables que son constantes y otras que van fluctuando, hay algunas variables que vienen intregradas o¿y otras que se pueden crear.

#### Pocisión del mouse:  
*Variable de sistema numerico* que determinan las pocisiones de x,y.   
**Sintaxis: (mouseX,mouseY)**
Ejemplo: (ellipse(mouseX,mouseY,100,100)

#### Apuntes mouseX, mouseY:
- Si se coloca el background en setup, no quedará estela, si se pone el draw pintará el fondo.
- mouseX y mauseY se puede usar en las figuras, en el color, tamañao, diametro, pocisión, etc.

### Variables integradas en P5.js:  
***Teclado:***
*key:* Te dice la ultima tecla presionada  
*keyCode*: Guarda un número que representa las teclas especiales  
*keylsPressed:* Indica si hay alguna tecla presionada actualmente  
***Tiempo:***  
*frameCount:* Cantidad de cuadros transcurridos desde el inicio  
*deltaTime:* Tiempo en milisegundos entre el cuadro actual y el anterior  
***Ventana:***  
*windowWidth:* Ancho total de la ventana del navegador  
*windowHeight*: Alto total de la ventana del navegador  
*focused*: Indica si la ventana del sketch tiene el foco activo  

### Crear tus propias variables:  
1. Declarar tu variable
2. Inicializar tu variable
3. Usa tu varible

#### Para declarar la variable podemos usar:  
- let : Variables dinámicas
- const : Variables constantes
#### Apuntes de let:  
- Cuando son palabras distintas no se pone espacios si no, letras mayusculas para diferenciar las palabras.  
- Arriba del funtion setup y draw.  

### JavaScript Objects:
Organizar nuestro codigo de forma adecuada y ordenada.
Agrupa mucha variables dentro de la variable, estructura de datos que te permite agrupar, valores relacionados bajo un mismo nombre, el lugar de tener muchas variables sueltas, los obj funcionan como contenedor, en donde se organiza la info mediantes pares de >**clave y valor.**  

#### random fuction():  
Devuelve un **numero aleatorio** dentro del rango que se defina.  
*random(); Si no pones nada, devuelve un número decimal entre 0 y 1*  
Ejemplo: random() da 0.4571
*random(máximo); Devuelve un número decimal entre 0 y el máximo que elijas*  
Ejemplo: random() da un número entre 0 y 100
*random(mínimo,máximo); Devuelve un número decimal entre esos dos valores*  
Ejemplo: random(20,50) da un número entre 20 y 50  

#### (width,height);  
Variables integradas en p5, que corresponden a los valores definidos en el createCanvas.  
#### (windowWidth,windowHeight);  
Variables integradas en p5, que permiten ajustar el tamaño del lienzo al tamaño de la ventana del navegador. Se usan en el createCanvas.  

#### map(); function  
Esta función nos permite convertir un valor de un rango a otro.  
En términos simples: toma un número que está en una escala y lo traduce proporcionalmente a una escala nueva.  
**Sintaxis: map(valor, min_original,max_original,min_nuevo,max_nuevo)**  
*Valor*: La variable que quieres "mapear"(por ejemplo, mouseX).  
*min_original y max_original*: El rango que se encuentra en ese valor actualmente.  
*min_nuevo y max_nuevo*: El rango al que lo quieres transformar.

### Encargo 03: 
[![encargo 03](https://i.pinimg.com/736x/dd/6b/e4/dd6be478c7fcd08d5438c5f512577419.jpg)](https://editor.p5js.org/francisca.ovalle/sketches/4CTLaq6i7)
