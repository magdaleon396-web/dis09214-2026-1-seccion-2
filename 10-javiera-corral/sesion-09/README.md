# sesión 09 - 5/06

ESTADOS Y CÁMARA WEB  recuerda sacar pantallaso de los sketch y agregar de mejor manera los codigos 
- 

como crear sketch con diferentes estados: 

CREAR Y DEFINIR VARIABLE ESTADO 
-
1. Al principio de tu código (fuera de las funciones), debes crear una
variable que guarde en qué pantalla nos encontramos. Empezará en 0.

let estado = 0; // 0 = Inicio, 1 = Experiencia, 2 = Final


CONFIGURAR EL LIENZO (funtion setuo)
-

2. Creamos el lienzo de fondo donde va a ocurrir toda la magia.

CREAR LA ESTRUCTURA DEL ESTADP (function draw)
-

3. Aquí usamos un switch Dependiendo del valor de la variable estado, el programa dibujará una cosa u otra.

PROGRAMAR VISUALMENTE CADA ESTADO (funciones propias)
-
4. Ahora creamos las funciones que inventamos en el paso anterior. Cada una tendrá un diseño y un color diferente para que se note el cambio.


LA LÓGICA DEL CAMBIO Y EL REINICIO
-

5. Para pasar de un estado a otro y lograr que vuelva al comienzo, usamos la función mousePressed() Cada vez que hagas un clic, la variable aumentará. Si llega a 3 (después del estado 2), volverá a 0.


DIFERENTES MANERAS DE CAMBIAR ESTADOS
-
1. Interacción con el Teclado
2. Botones Reales en la Pantalla
3. Zonas de Clic (Botones dibujados con rect o ellipse)
4. Zonas de Clic (Botones dibujados con rect o ellipse)

codigo de ejemplo:

(arreglar depsues el formato del codigo) se me ovido como hacer esto en el compu mac 
let estado = 0;

function setup() {
  createCanvas(400, 400);
  textAlign(CENTER, CENTER);
}

function draw() {
  background(220);

  switch (estado) {
    case 0:
      pantallaInicio();
      break;
    case 1:
      pantallaExperiencia();
      break;
    case 2:
      pantallaFinal();
      break;
  }
}

function pantallaInicio() {
  background(135, 206, 250);
  fill(0);
  textSize(24);
  text("ESTADO 0: INICIO", width / 2, height / 2 - 20);
  textSize(16);
  text("Haz clic para continuar", width / 2, height / 2 + 20);
}

function pantallaExperiencia() {
  background(144, 238, 144);
  fill(0);
  textSize(20);
  text("ESTADO 1: EXPERIENCIA", width / 2, height / 2 - 20);
  
  // Interactividad extra en este estado
  fill(255, 100, 100);
  ellipse(mouseX, mouseY, 30, 30);
  
  fill(0);
  textSize(14);
  text("Mueve el mouse. Haz clic para avanzar.", width / 2, height / 2 + 40);
}

function pantallaFinal() {
  background(255, 182, 193);
  fill(0);
  textSize(24);
  text("ESTADO 2: FINAL", width / 2, height / 2 - 20);
  textSize(16);
  text("Haz clic para volver al inicio 🔄", width / 2, height / 2 + 20);
}


function mousePressed() {
  estado = estado + 1;
  
  if (estado > 2) {
    estado = 0;
  }
}

CÁMARA WEB
-

createCapture(VIDEO);
1. Crear la variable para la captura, declarar una
variable global que guardará el flujo de video de
tu cámara web.

2. Inicializar la cámara en el function setup()
utilizamos el comando especial
createCapture(VIDEO) esto le pedirá permiso
al navegador para encender la cámara del
computador. También definimos tamaño con
captura.size(x,y); y es muy importante
agregar captura.hide(); para que esconda el
video que HTML pone abajo por default.
3. Dibujar la cámara en el function draw()
usamos la función image(). p5.js toma cada cuadro
(frame) de la cámara y lo dibuja en el lienzo en
tiempo real.

ejemeplo de cámara:
let captura;

function setup() {
  createCanvas(640, 480);
  
  // Capturamos la cámara del computador
  captura = createCapture(VIDEO);
  captura.size(640, 480);
  captura.hide(); // Esconde el duplicado de HTML
  textAlign(CENTER);
}

function draw() {
  background(0);
  
  // Dibujamos la cámara en el lienzo
  image(captura, 0, 0, width, height);
  
  // Agregamos interactividad con el mouse y un filtro
  // map() convierte la posición del mouse en un rango de 0 a 1
  let umbralT = map(mouseX, 0, width, 0, 1, true);
  //let umbralP = map(mouseX, 0, width, 0, 10, true);
  
  // Aplica un efecto de alto contraste (Blanco y Negro) interactivo
  filter(THRESHOLD, umbralT);
  //filter(INVERT);
  //filter(GRAY);
  //filter(POSTERIZE,umbralP);
  //filter(BLUR,4);// cambiar valores
 
  
  
  // texto con instrucciones
  fill(255, 0, 0);
  noStroke();
  textSize(18);
  text("Mueve el mouse horizontalmente", width/2, height-20);
}
