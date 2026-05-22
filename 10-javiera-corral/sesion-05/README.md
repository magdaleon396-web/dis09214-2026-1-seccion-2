# sesión 05 - 17/04
TRANSFORMACIONES & {If - else} 🍰
-
Angulos, angleMode [video info](https://youtu.be/DMg-WRfNB60?si=M7ZQaqsv-Q1tpMuN) <img width="446" height="384" alt="image" src="https://github.com/user-attachments/assets/1283c066-eadc-4de9-81ab-02c628cdb917" /> movimiento como el de las agujas del reloj

Por defecto p5.js usa RADIANES para medir los ángulos.
angleMode(RADIANS)
Para cambiar a grados se usa esto en el fuction SETUP
angleMode(DEGREES) 

ROTACIÓN rotate(); 
-
rotate(valor radianes o en grados); ejemplo: rotate(20); [referencia](https://p5js.org/reference/p5/rotate/)  

  * Sirve para rotar elementos.
  * SIEMPRE ROTA ALREDEDOR DEL PUNTO DE ORIGEN (0,0)
  * Se recomienda usar con translate(); y en algunos casos con rectMode(CENTER);
  * [ejemplo](https://editor.p5js.org/PoliMujica/sketches/XFVDpysTg)

TRASLADAR translate();
-  
  * translate(x,y);
  * Sirve para trasladar el PUNTO DE ORIGEN (0,0) a otra cordenada de mi canvas.
  * [ejemplo](https://editor.p5js.org/PoliMujica/sketches/ddsUf63Oy)

GUARDAR Y RESTAURAR
-
push();
pop();
Funciones que trabajan juntas como un "sistema de memoria temporal" para el estilo y las transformaciones del lienzo.
[ejemplo](https://editor.p5js.org/PoliMujica/sketches/XmQz1O5p9)
[video transformaciones1](https://youtu.be/o9sgjuh-CBM?si=GyV5YpSujomNga9s)
[video transformacione2](https://youtu.be/pkHZTWOoTLM?si=ZewYIACFRYHmLx51)

ESCALA 
scale();
-
scale(x,y);
La función scale() ajusta la escala del sistema de coordenadas actual por el factor especificado. [ejemplo](https://editor.p5js.org/PoliMujica/sketches/Rxcg579Jx) <img width="206" height="206" alt="image" src="https://github.com/user-attachments/assets/2cda1fc7-30ab-4910-9a9e-ef10cc0b1f6a" />


CONDICIONALES 🍰
-
**LOGICA CONDICIONAL:** (como en probabilidad y estadisticas,slay)
EXPRESIÓN BOOLEANA
Una expresión booleana es cualquier enunciado, dato o instrucción que, al ser evaluado, solo puede arrojar uno de dos valores posibles: verdadero (True) o falso (False).
Elementos para construir estas expresiones:  
  
  * Operandos (o Valores): Son los datos básicos que se evalúan. Pueden ser:
     Variables: (como x, y o mouseX, mouseY, etc).
     Constantes o Literales: Valores fijos como 5, "Hola" o los mismos valores booleanos True y False.
 
  * Operadores de Comparación: Permiten contrastar dos valores.
    == (Igual a)
   != (Diferente de)
   > o < (Mayor o menor que)
   >= o <= (Mayor o igual / Menor o igual)
 
  * Operadores Lógicos: Sirven para combinar varias expresiones.
    AND (&&): Es verdadero solo si ambas partes son verdaderas
    OR (||): Es verdadero si al menos una de las partes es verdadera.
    NOT (!): Invierte el valor (si era verdadero, pasa a ser falso).

SENTENCIA CONDICIONAL
-
If - else if - else

La sentencia if es una estructura especial que existe en casi todos los lenguajes de programación; toma una condición –expresada como un booleano– y ejecuta una pieza de código contenida dentro de las llaves { }  
  * **If (condición) {ejecuta este código si es true}**

La sentencia if puede complementarse con la sentencia else if, que añade
condiciones de prueba complementarias a la original, y con la sentencia else, que implica todos los casos que no cumplen con la condición original. (Nota: puedes añadir tantas sentencias else if como desees). 
<img width="957" height="303" alt="image" src="https://github.com/user-attachments/assets/b6defc8e-e5dc-4a38-be9d-2e3ec399a6a6" />
<img width="416" height="295" alt="image" src="https://github.com/user-attachments/assets/c7bac807-b2c4-4fd5-aa36-e5c2ba32c891" />
[ejemplop5 cuadrado](https://editor.p5js.org/PoliMujica/sketches/ZxBqL-b9-)
[Ejemplop5 carita feliz](https://editor.p5js.org/PoliMujica/sketches/Vw-QeAsTu)

ENCARGO 4
-
Deben crear un Sketch LIBRE, que incluya:
- Varias figuras geométricas
- Rotación
- Translate
- Push Pop
- Scale
- Texto https://p5js.org/es/search/?term=text
- Imagen https://p5js.org/es/search/?term=image https://editor.p5js.org/PoliMujica/sketches/nm0fj2seC
- 2 sentencias condicionales completas (If - else if - else)

ENTREGA: Antes de la clase del viernes 24 de abril. (ENCARGO_04)[https://editor.p5js.org/StarBerryChiscake/sketches/l188b4i9p]
-
´´´
let = angl = 0;
let speed = 0.1;

function preload() {
  //para pregargar elementos
  estrellas = loadImage(`estrellas.png`); //imagenes
  canica = loadImage(`canica_arcoiris.png`);
  domo = loadImage(`domo_kun.jpg`);
  judas = loadImage(`judas.jpg`);
}

function setup() {
  createCanvas(500, 500);
  angleMode(DEGREES);
  rectMode(CENTER);
  imageMode(CENTER);
}


function draw() {
  background(255, 181, 217);

  //CONDICIONALES
  //si se presiona el mouse sale la imagen
  if (mouseIsPressed === true) {
    image(judas, 250, 250, 500, 500);
  } //pero si el mouse va a estas cordenadas se pone otra imagen (intente poner judas de lady gaga pero sonaba horrible asi que no pude 😔)
  else if (mouseX >= 240 && mouseY >= 299) {
    image(domo, 250, 250, 500, 500);
  } //y cuando nada de lo anterior suceda avanza con lo siguente
  else {
    angl = angl + 1; //angulos para rotar mis fuguras luego
    speed = speed + 0.2;
    noStroke();

    //TEXTO
    fill(251, 252, 202);
    textSize(14);
    text(`JAVIERA CORRAL H. 💋`, 330, 470);

    //IMAGEN DE ESTRELLAS
    push();
    translate(250, 250);
    rotate(speed);
    image(estrellas, 0, 0, 490, 490);
    pop();

    //CUADRADO NARANJA
    push();
    translate(250, 120);
    rotate(angl);
    fill(250, 176, 57);
    square(0, 0, 60);
    pop();

    textSize(30);
    text(`💖`, 230, 130);

    //CIRCULO ROSADO E IMAGEN DE CANICA
    push();
    translate(360, 190); //cambia punto de origen
    fill(252, 98, 160);
    circle(0, 0, 60);
    rotate(-angl); //rota la figura
    image(canica, 0, 0, 47, 47); //cargue una imagen
    pop();

    //TRIANGULO VERDE
    push();
    translate(120, 310);
    rotate(angl + angl);
    scale(1.2);
    fill(105, 255, 94);
    triangle(0, 0, 50, 0, 50, 50);
    pop();

    //RECTANGULO AMARILLO
    push();
    translate(100, 180);
    rotate(angl);
    scale(1.1);
    fill(247, 250, 77);
    rect(0, 0, 70, 40);
    pop();

    //CUADRADO AZUL
    push();
    translate(250, 370);
    rotate(angl + angl + angl);
    fill(94, 209, 255);
    square(0, 0, 56);
    pop();

    textSize(30);
    text(`🍰`, 230, 380);

    //rectangulo morado
    push();
    translate(360, 290);
    rotate(angl);
    fill(236, 94, 255);
    rect(0, 0, 70, 40);
  }
}

´´´
    


