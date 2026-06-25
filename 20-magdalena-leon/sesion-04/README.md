# sesión 04 - 23/03
**Clase 4 pensamiento computacional**

***movimiento del mouse***

background(162, 0, 168); //poniendo el fondo antes se macha el fondo

fill(mouseX, mouseY, 51)//va cambiando el color del mouse 

ellipse(mouseX,mouseY,25,25);//circulo que se mueve segun el mouse

***crea tus propias variable***
**Declarar tu variable**

let circuloMorado=0;

**Inicializa tu variable**

circuloMorado = circuloMorado+1;

**Usa tu variable**

backround(200,200,200);

fill(200,200,200);

ellipse(circuloMorado,200.50,50);

**p5js**
let circuloMorado = 0;//declarar
 
  function setup() {
  createCanvas(400, 400);
}

function draw() {
  circuloMorado = circuloMorado +1/10;//inicializa tu variable
  
  
  background(143, 255, 51);
  noStroke()
  fill(255, 249, 51)
  
  
  ellipse(circuloMorado,200,50,50)//usar variable

  **Java script objects**

 Nos servira para organizar nuestro codigo de una forma adecuada y ordenada

 Es la forma de agrupar muchas variables dentro de una variable

 Es una estructura dde datos que t permite agrupar valores reelacionados bajo un mismo nombre,
 en lugar de tener muchas variables sueltas, los objetos funcionan como un

**random fuction**();
