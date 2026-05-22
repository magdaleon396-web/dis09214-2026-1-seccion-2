# sesión 06 - 14/04
# Solemne2  
---

# Miradas que Agobian  
### Autoras: Dafne Hernandez, Josefina Puña  

## Descripción del proyecto:  
### ¿Qué es?  
Es un sketch hecho en P5.js que tiene como objetivo visibilizar y reflexionar sobre el trato que reciben las mujeres en cuanto a la estética y los estándares de belleza impuestos por la sociedad. A través de elementos visuales e interactivos, se busca representar la presión constante que existe sobre la apariencia femenina, donde se espera que las mujeres mantengan una imagen “perfecta” e inalcanzable para ser aceptadas socialmente.
Esta exigencia crea inseguridades, frustración y la sensación de no ser suficientes, ya que los modelos de belleza suelen ser irreales e imposibles de alcanzar. El sketch evidencia cómo estas presiones afectan emocionalmente a las mujeres, influyendo en su autoestima y en la percepción que tienen de sí mismas. De esta forma, el proyecto utiliza el lenguaje visual y la programación creativa para transformar una problemática de género en una experiencia interactiva y reflexiva.  

### ¿Qué se ve en pantalla?  
En el sketch de 600 x 400 píxeles se puede apreciar principalmente una mujer en el centro con numerosos ojos a su alrededor que cambian de tamaño de manera random y textos de distintos colores aparecen de manera random detras de la chica. Al mantener presionado el mouse se ve la imagen de una chica agobiada, estresada y con una cadena al tobillo arrastrando el peso de la perfección, junto con un texto que refleja sus sentimientos más profundos.

### ¿Qué elementos visuales aparecen?  
Principalmente círculos y textos, también se pueden apreciar imágenes, diversas figuras geométricas (elipses, triángulos y cuadrados) y distintos colores.  

## Descripción conceptual  
### Idea central del proyecto y su relación con el sistema diseñado  
Los estándares de belleza en mujeres son sumamente exigentes e imposibles de lograr, la sociedad ha construido ideales de apariencia que generan una constante presión sobre el cuerpo y la imagen femenina. En este proyecto, esa presión es representada visualmente a través de ojos que observan a la mujer en el centro e incomodan constantemente al espectador, simbolizando la sensación de estar siendo juzgada de manera permanente por la sociedad. La mirada funciona como una metáfora de la vigilancia y crítica continua hacia la apariencia femenina, generando incomodidad y tensión dentro de la experiencia interactiva. Además, se incorporan textos con mensajes explícitos y frases comunes que suelen imponerse a las mujeres respecto a su físico, evidenciando cómo estas opiniones y exigencias se encuentran normalizadas en la vida cotidiana.  

### ¿Cuál es la regla de oro de tu sistema?  
Al mantener presionado el mouse se cambia a otra imagen con el mismo trasfondo.    

### ¿Cómo se relaciona esta lógica con la problemática de género elegida?  
El mantener presionado el mouse evoca la presión que se mantiene en las mujeres solamente por existir y no coincidir con los estandares de belleza dictados por la sociedad.  

##  Input / Output y sistema   
### ¿Qué datos entran?    
* El usuario mantiene presionado el mouse.  
* Círculos, cuadrados y textos generados por la función random.  
* El usuario mueve el mouse en Y.  

### ¿Cómo se procesan y transforman?  
El código detecta y transforma las acciones mediante:  
* Condicionales.  
* Loops.  
* Rotaciónes.  
* generacion random.  
* mapeos.  
* funciones propias.  

### ¿Qué respuesta visual producen? 
En respuesta a las distintas interacciones del usuario se genera:  
* La pantalla cambia en su totalidad (clic).  
* El color y el tamaño del borde del cuadrado cambia según la posición Y del mouse.  

## Pensamiento computacional  
### Reglas que gobiernan el sistema (inputs, procesos, outputs)  
Las reglas que gobiernan el sistema son:  
* Si el usuario presiona una tecla: Se añaden palabras.
* Si el usuario presiona el mouse: Se añade una nueva pantalla.
* Si mueve el mouse verticalmente: El cuadrado se agranda.  

### Explicación del sistema de interactividad  
El programa detecta las siguientes acciones (inputs): el movimiento del mouse en Y, los clics. Las interpreta (procesos) mediante condiciones, variables o cálculos y entrega una respuesta (output) visible en el sketch: cambia el contenido visual en la pantalla o cambia el color y tamaño del borde del cuadrado.  

## Referentes  
#### Corner Eyes de Margaret Keane (2004)  
Esta obra de la artista Margaret Keane (que tuvo conflictos sobre la autoría de sus obras con su marido)  muestra a tres mujeres con los ojos grandes mirando fijamente e incomodando al espectador. Nos basamos en esa incomodidad y presión que causan las miradas cuando estas están fijadas en nosotros.  

![corner eyes](https://www.keane-eyes.com/wp-content/uploads/2014/09/Corner-Eyes02-copy.jpeg)  

### Discurso película Barbie (2023)  
En este discurso dicho por la actriz America Ferrera se visibiliza todas las cosas que se le exigen a una mujer, sobre lo contradictorio y difícil que es siquiera intentar seguir los estándares impuestos por la sociedad.  

![Discurso Barbie](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSwCsnEQ3rsLDcF-zEyRYjwtSKs_Z6ersveWw&s)  

### La serie "Propped" de Jenny Saville (1992)  
La artista británica es conocida por sus enormes pinturas al óleo de cuerpos femeninos que escapan al canon de extrema delgadez. En "Propped" y otras obras, desafía la mirada masculina al mostrar la piel con pliegues, marcas de celulitis y proporciones reales, celebrando el cuerpo tal y como es.  

![Propped](https://miro.medium.com/0*mgCLMtGMiNAHAGNi)  

### "Terror of Beauty" de Sarah Amrani  
Su obra critica cómo los filtros y las calculadoras de belleza online, basados en cánones occidentales, presionan a las mujeres a modificar sus rostros, borrando su identidad y transformando el cuidado personal en una batalla constante por una perfección inalcanzable.  
![Terror of Beauty](https://static1.squarespace.com/static/5702ab9d746fb9634796c9f9/5702ad93b09f95bfee70b342/6746a1443cf669360434e10e/1752386795893/Strategy+of+Beautification+2018+C+Sarah+Amrani.jpeg?format=1500w)  

## Diagrama de flujo  
![Diagrama de flujo](https://github.com/Josefina130/solemne2/blob/main/Diagrama%20de%20flujo.png)  
[PDF Diagrama de flujo](https://github.com/Josefina130/solemne2/blob/main/_Diagrama%20de%20flujo.pdf)


## Código p5.js  

 ```  
let chica1; // Se crea la variable chica1
let chica2; // Se crea la variable chica2
let giroRect=0; // Se crea la variable giroRect y se le asigna el valor 0
let tamOjo; // Se crea la variable tamOjo
let tamPupila; // Se crea la variable tamPupila
let tamañoCuadrado ; // Se crea la variable tamañoCuadrado
let bordeCuadrado ; // Se crea la variable bordeCuadrado


function preload(){ // Se activa la función para pre cargar las imágenes
chica1 = loadImage ('girl1.png'); // Se carga la imagen con la variable chica1
chica2 = loadImage ('chica2.jpg'); // Se carga la imagen con la variable chica2
}

function setup() {
  createCanvas(600, 400);
  frameRate(20); // Se activa la velocidad de los frames por segundo, y se le asigna el valor 20
  //background(124, 39, 170);
}

function draw() {
  background(0);
  
textSize(10); // Se le añade el tamaño al texto
for (let x = 0; x <= width; x = x + 20) { // Mediante el cómando for, se crea la variable x y se le asigna el valor 0, si x es mayor o igual al ancho del lienzo, será igual a x + 20
for (let y = 0; y <= height; y = y + 5){ // Mediante el cómando for, se crea la variable y  se le asigna el valor 0, si y es mayor o igual al alto del lienzo, será igual a y + 5
fill(random(255),random(100),0); // Se le asigna un color aleatorio con el cómando random y rgb
text('Fea',x, y); //Se le añade el texto "Fea" y se crea un nested loop 
}
}
push();  //Se abre un estado de "capa"
rectMode(CENTER); // se activa la función para crear las figuras desde el centro
stroke(69,69,69,mouseY) //Se colorea el borde de gris
strokeWeight(bordeCuadrado);  //Se le asigna el tamaño al borde
translate(295,200); // Se traslada la figura desde el punto 295 y 200
rotate(giroRect*30); // Rota la figura según el ángulo 
fill(0) // Se rellena de color negro
square(0,0,tamañoCuadrado); //Se crea un cuadrado en las coordenadas 0 y 0
pop(); //Se cierra el estado de "capa"
  

giroRect = giroRect+1; // Se le asigna la velocidad a la que girará
tamañoCuadrado = random(100,250); //Se le asigna el valor al tamaño que varia de 100 a 250
bordeCuadrado = random(1,25); //Se le asigna el valor al borde que varia de 1 a 25
tamOjo = random(40,100) //Se le asigna el valor al tamaño del ojo que varia de 40 a 100
tamOjo2 = random(10,30); //Se le asigna el valor al tamaño del ojo 2 que varia de 10 a 30
tamPupila = random(30,50) //Se le asigna el valor al tamaño del ojo 2 que varia de 30 a 50
  
zonaOjos() // Se añade la función zonaOjos
zonaTexto() // Se añade la función zonaTexto
pantallaDos() // Se añade la función pantallaDos

function zonaOjos() { //Se activa la zonaOjos

noStroke() // Se quita los bordes a mis objetos 
fill(255); //Se rellenan de color blanco
  
triangle(40,60,60,50,60,70); // Se crea un triangulo en las coordenadas 40,60,60,50,60,70
triangle(90,60,70,50,70,70); // Se crea un triangulo en las coordenadas 90,60,70,50,70,70
ellipse(65,60,tamOjo,22);
  
ellipse(330,30,tamOjo,40);

triangle(500,50,520,40,520,60); // Se crea un triangulo en las coordenadas 500,50,520,40,520,60
triangle(560,50,540,40,540,60); // Se crea un triangulo en las coordenadas 560,50,540,40,540,60
ellipse(530,50,tamOjo,25); 
  
triangle(130,120,170,80,170,150); // Se crea un triangulo en las coordenadas 130,120,170,80,170,150
triangle(240,120,200,80,200,150); // Se crea un triangulo en las coordenadas 240,120,200,80,200,150
ellipse(185,115,tamOjo,80);

triangle(470,170,500,150,500,200); // Se crea un triangulo en las coordenadas 470,170,500,150,500,200
triangle(570,170,540,150,540,200); // Se crea un triangulo en las coordenadas 570,170,540,150,540,200
ellipse(520,175,tamOjo,60); // Se crea un ellipse en las coordenadas 520,175
  
ellipse(50,250,tamOjo,20); // Se crea un ellipse en las coordenadas 50,250

ellipse(110,330,tamOjo,45); // Se crea un ellipse en las coordenadas 110,330

triangle(190,370,210,350,210,380); // Se crea un triangulo en las coordenadas 190,370,210,350,210,380
triangle(260,370,240,350,240,380); // Se crea un triangulo en las coordenadas 260,370,240,350,240,380
ellipse(225,365,tamOjo,40); // Se crea un ellipse en las coordenadas 225,365

triangle(350,320,400,295,400,345); // Se crea un triangulo en las coordenadas 350,320,400,295,400,345
triangle(470,320,420,295,420,345); // Se crea un triangulo en las coordenadas 470,320,420,295,420,345
ellipse(410,320,tamOjo,55); // Se crea un ellipse en las coordenadas 410,320

ellipse(550,340,tamOjo,25); // Se crea un ellipse en las coordenadas 550,340
  
fill(0); // Se rellena de color negro los objetos
circle(80,65,tamOjo2); // Se crea un circulo en las coordenadas 80,65
circle(325,40,tamOjo2); // Se crea un circulo en las coordenadas 325,40
circle(510,55,tamOjo2); // Se crea un circulo en las coordenadas 510,55
circle(200,135,tamPupila); // Se crea un circulo en las coordenadas 200,135
circle(500,180,tamPupila); // Se crea un circulo en las coordenadas 500,180
circle(70,250,tamOjo2); // Se crea un circulo en las coordenadas 70,250
circle(130,325,tamPupila); // Se crea un circulo en las coordenadas 130,325
circle(225,355,tamOjo2); // Se crea un circulo en las coordenadas 225,355
circle(400,310,tamPupila); // Se crea un circulo en las coordenadas 400,310
circle(530,335,tamOjo2);  // Se crea un circulo en las coordenadas 530,335
  
imageMode(CENTER); //Se situa la imagen desde el centro
image(chica1,300,200,350,300); //Se coloca la imagen en las coordenadas 300,200
}

function zonaTexto(){ //Se activa la zonaTexto
if (keyIsPressed){ // Se genera una condicional: Si se presiona una tecla se cumplirá lo siguiente
let x , y // Se crean las variables x e y
let x1 , y1 // Se crean las variables x1 e y1
let x2 , y2 // Se crean las variables x2 e y2

x = random(width) / 2; // Se le asigna el valor aleatorio, que vaya por el ancho y se divide en 2
y = random (height) / 2; // Se le asigna el valor aleatorio, que vaya por el alto y se divide en 2
x1 = random(width) / 2; // Se le asigna el valor aleatorio, que vaya por el ancho y se divide en 2
y1 = random(height) / 2; // Se le asigna el valor aleatorio, que vaya por el alto y se divide en 2
x2 = random(width) / 3; // Se le asigna el valor aleatorio, que vaya por el ancho y se divide en 3
y2 = random(height) / 3; // Se le asigna el valor aleatorio, que vaya por el alto y se divide en 3

textSize(25); // Se le asigna un tamaño al texto
fill(255); // Este se rellena de color blanco
text('Subiste de peso?',x,y); // Se añade el texto "Subiste de peso?" en las coordenadas de x e y
fill(255, 0, 0); // // Este se rellena de color rojo
text('Hay chicas mejores',x1,y); // Se añade el texto "Hay chicas mejores" en las coordenadas de x1 e y1
fill(0); // Este se rellena de color negro
text('No entras en el estándar',x2,y2) // Se añade el texto "No entras en el estándar" en las coordenadas de x2 e y2
} // Se cierra la condicional
}

function pantallaDos() { // Se activa la pantallaDos

if (mouseIsPressed) { // Se genera una condicional: Si se presiona el mouse se cumplirá lo siguiente
background(255); // Se le asigna un color al fondo, de color blanco
textSize(25) // Se le asigna el tamaño al texto
stroke(255); //Se le asigna el color del borde
text('Presa de la perfección',180,70) // Se le añade el texto "Presa de la perfección" en las coordenadas 180,70
imageMode(CENTER); //Se situa la imagen desde el centro
image(chica2,300,290,150,270); //Se coloca la imagen en las coordenadas 300,300

fill(0); // Se rellena de color negro
rect(0,120,width,40); // Se crea un rectangulo en las coordenadas 0 y 120 y que tenga el mismo ancho del canvas
fill(255) // Se rellena de color blanco
text('Y tal vez algún día seré aceptada',115,145) // Se le añade el texto "Y tal vez algún día seré aceptada" en las coordenadas 115,145
} // Se cierra la condicional
}



}


 ```  

## [Sketch p5.js](https://editor.p5js.org/kitcaaatt/sketches/JSuVu-QnC)  
