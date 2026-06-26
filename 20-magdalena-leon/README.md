# pc-dis09214-2026-1-seccion-2

## Exámen


## Desigualdad de opinión

Autoras: Olivia Preece, Magdalena León.


## Descripción objetiva

El proyecto abarca la problemática de género sobre la atención a la cual se da a 
la opinión del hombre en comparación a la mujer. En muchos espacios la opinión de la mujer
suele ser juzgada, interrumpida o minimizada por la sociedad. En cambio la opinión del hombre 
siempre se toma en cuenta, se escucha y la mayoría de veces se felicita sin importar cual sea. 
Quisimos vizualizar este tema ya que se normaliza en nuestra sociedad actual 
y no se toma en cuenta. 

El estado 0 comienza con la pregunta ¿La opinión tiene género?, para cuestionarnos la 
problématica actual. Luego en el estado 1 se observa la boca de un hombre hablando, con un fondo 
verde para representar la validación, luego aparecen aplausos para destacar a un más la 
aprobación y el espacio seguro que se le da al hombre al momento de opinar. Después en el 
estado 2 se muestra la boca de la mujer, y detrás un color blanco, pero al momento de hacer 
mousePressed se genera un sonido molesto y figuras que interrumpen la opinión de la mujer.

Para la pantalla inicial quisimos plantear un preguntar que ocupara gran cantidad del canvas
para poder generar un impacto en el usuario. Luego en el estado 1 y 2 ocupamos colores segun 
las emociones que queriamos generar. También ocupamos imágenes de bocas para poder representar 
visualmente la voz u opinión del hombre y de la mujer además de figuras que aportaban (en el 
caso del hombre) o interrumpieran (en el caso de la mujer) las distintas experiencias. 

##   Descripción conceptual

La idea central del proyecto era realizar una experiencia en la cual el usuario pueda interactuar
respecto a la problemática y se logre transmitir la sensación de impotencia que vive la mujer al 
momento de hablar. De esta manera la representamos con colores llamativos y sonidos que puedan fuertes
para generar ese impacto. También instrucciones para facilitar e invitar a participar en la actividad.
Estos fueron nuestros principales objetivos al crear nuestro sistema.

La regla de oro para nuestro sistema fue ocupar el codigo de mousePressed, ya que crea una interación 
con el usuario y al mismo tiempo va cambiando los estados de la experiencia que queríamos lograr, ese fue uno 
de los pasos más importantes para crear la propuesta.

Esta lógica se relaciona con la problemática por que al hablar de la desigualdad de opinión se
muestran dos perspectivas completamente distintas de una misma situación. Por esto la idea era crear 
dos experiencias diferentes que generaran un cuestionamiento sobre las brecha de género.

## Input/Output y sistema  

En el sketch, los inputs principales son el teclado, el mouse y el tamaño de la ventana. El teclado cambia entre pantallas: inicio, pantalla Experiencia (hombre) y pantalla Experiencia2 (mujer). El mouse activa las interacciones cuando se mantiene presionado, y mouseX modifica el color verde del fondo usando map().  
Estos datos se procesan con la variable estado, condicionales, funciones propias, random(), frameCount, un array y un class. El código decide que pantalla mostrar, cuándo activar sonidos, cuándo mover imágenes y cuándo generar figuras aleatorias.  
El Output es la respuesta visual y sonora: en el inicio, aparece la pregunta, en la segunda pantalla (del hombre) aparecen ondas fluidas, aplausos y sonidos de validación, y en la pantalla 3 (de la mujer) aparecen las mismas ondas pero con interrupciones visuales, temblor de la boca y ésta también mucho mñas abierta como si estuviera gritando y un sonido de interrupción de fondo.


## Pensamiento computacional

El sistema funciona a partir de reglas simples, hay inputs mediante el teclado y el mouse, el código los procesa con variables, condicionales y funciones, y luego produce outputs visuales y sonoros. La variable estado controla que pantalla aparece y se cambian con las teclas, mientras que el clic activa las respuestas principales de cada experiencia.  
En el sistema de interactividad lo organizamos mediante estados, cada estado tiene instrucciones, 
y el código mousePressed va generando varias pantallas distintas con respuestas visuales y de 
sonido que corresponden a cada experiencia, esto le permite al usuario ir cambiando las situaciones.

## Referentes

Para los refentes visuales quisimos inspirarnos un poco en los afiches de la diseñadora 
Barbara Kruger.
Al inicio de la representación visual ocupamos letras grandes e impactantes, 
y en la pantalla de experiencia 2 ocupamos los colores rojos, blancos y negros, al igual que el 
uso del collage por el cual está diseñadora es tan reconocida en sus afiches. También su ideología
feminista se veía plasmada en sus obras, de esta manera va completamente ligado a lo 
que queremos demostar en nuestro proyecto.

















## Código examen P5js



//VARIABLES CREADAS
let sonidoInterrupcion; //Variable para guardar el sonido de interrupción
let sonidoAplausos; //Variable para guardar el sonido de aplausos

let estado = 0//Variable que guarda la pantalla actual: 0 inicio, 1 hombre 2 mujer

let foto1;//Variable para guardar la primera imagenn de la boca del hombre
let foto2;//Variable para guardar la segunda imagen de la boca del hombre 
let foto3;//Variale para guardar la primera imagen de la mujer
let foto4;//Variable para guardar la segunda imagen de la mujer

let ajusteFoto2Y = -20; //Ajusta la segunda imagen del hombre para que quede alineada con la primera y no se vea desfasado

let aplausos = [];// Array que guarda las partículas de aplausos 

let circulo = {//Objeto que guarda datos de un circulo
  x: 250,//Posicion horizontal del circulo
  y:250,//Posicion vertical del circulo
  d: 50 //Diametro del circulo
};


//CLASS: PARTICULAS DE APLAUSOS
class Aplausos {//class que funciona como un molde para crear cada aplauso
  constructor(){//Define cómo nace cada aplauso
    this.x = random(0,width);//Posicion horizontal aleatoria en todo el ancho del canvas
    this.y = random(-height,0);// Nace arriba de la pantalla según el alto del canvas 
    this.velocidad = random(2,5);// Velocidad de caida aleatoria
    this.tamaño = random(26,38);// Tamaño aleatorio del emoji
  }

  mover() {//Función que mueve cada particula
    this.y = this.y + this.velocidad;//Aumenta la posición Y para que los emojis de aplauso caigan hacia abajo
    if(this.y > height + 30) {//Si el aplauso sale por debajo de la pantalla
      this.y = random(-height / 2,0); //Vuelve a aparecer arriba según el alto del canvas 
      this.x = random(0,width);//Cambia su posicón horizontal
    }
  }

  mostrar(){//Función que muestra cada aplauso en la pantalla
    noStroke();//No tiene borde
    fill(0);//Color negro para el texto
    textSize(this.tamaño);//Tamaño del texto
    text ("👏",this.x,this.y);//Dibuja el emoji en su posición
  }
}


//PRELOAD: CARGA ARCHIVOS
function preload(){//Carga las imagenes y sonidos antes de que empiece el sketch
  foto1 = loadImage("bocaH1.png");//Carga la primera imagen de la boca del hombre
  foto2 = loadImage("bocaH2.png");//Carga la segunda imagen de la boca del hombre
  foto3 = loadImage("bocaM1.png");//Carga la primera imagen de la boca de la mujer
  foto4 = loadImage("bocaM2.png");//Carga la segunda imagen de la boca de la mujer 

  sonidoInterrupcion = loadSound("interrupcion.mp3");//Carga el sonido de interrupción en mp3 
  sonidoAplausos = loadSound("Aplausos.mp3");//Carga el sonido de aplausos en mp3

}


function setup() {
  createCanvas(windowWidth,windowHeight); //Crea canvas que se adapte al tamaño de la ventana 

  textAlign(CENTER,CENTER);//Centra el texto
  imageMode(CENTER);//Hace que las imágenes esten desde el centro

  
  for (let i = 0; i < 35; i++){//Bucle que se repite 35 veces
    aplausos.push(new Aplausos());//Crea una nueva partícula de aplauso y la guarda en el array
  }
}


function draw() {
  background(220);

  switch (estado){
      case 0://Si el estado vale 0
      pantallaInicio();//Muestra la pantalla de inicio
      break;//Termina este caso 

      case 1://Si el estado vale 1
      pantallaExperiencia();//Muestra la pantalla Experiencia (hombre)
      break;//Termina este caso

    case 2://Si el estado vale 2
      pantallaExperiencia2();//Muestra la pantalla Experiencia2 (mujer)
      break;//Termina este caso
  }
}

//ONDAS
function ondas() {//Función que dibuja ondas circulares 
  noFill();//Sin relleno
  stroke(0,150);//Líneas negras co transparencia 
  strokeWeight(2);//Grosor de las líneas 

  let radio = (frameCount * 3) % 250;//Con frameCount el radio cambia con el tiempo

  for ( let i = 0; i < 20; i ++) {//Bucle que repite 20 circulos
    ellipse(
      width/2,
      height/2,
      radio + i * 20,//Ancho de cada círculo va aumentando con cada repetición
      radio + i * 20);//Alto de cada círculo va aumentando con cada repetición
  }
}


//PANTALLA 0: INICIO
function pantallaInicio() {//Función propia que muestra la pantalla inicial
  background(0);//Color del fondo en valor RGB

  detenerSonidos();//Detiene cualquier sonido activo 

  fill(255);//Texto negro
  noStroke();//Sin borde

  textFont("Arial");//Tipografía 
  textStyle(BOLD);//Deja el texto en negrita
  textSize(70);//Tamaño del texto 

  //PRIMERA PARTE DEL TEXTO
 textAlign(LEFT,TOP);//Alinea el texto hacia la izquierda y desde arriba 
  text("¿LA",35,35);//Ubica el texto a 35 px del borde izquierdo y 35 px del borde superior
  //SEGUNDA PARTE DEL TEXTO
  textAlign(RIGHT,TOP);//Alinea el texto hacia la derecha y desde arriba 
  text("OPINIÓN", width - 35, height * 0.22)//Ubica el texto a 35 px del borde derecho y al 22% de la altura de la pantalla

  //TERCERA PARTE DEL TEXTO
  textAlign(LEFT,CENTER);//Alinea el texto hacia la izquierda y centrado verticalmente
  text("TIENE",35,height * 0.55);//Ubica el texto a 35 px del borde izquierdo y al 55% de la altura de la pantalla

  //CUARTA PARTE DEL TEXTO
  textAlign(RIGHT,BOTTOM);//Alinea el texto hacia la derecha y desde abajo
  text("GÉNERO?", width - 35, height - 35);//Ubica el texto a 35 px del borde derecho y 35 px sobre el borde inferior


//INSTRUCCIONES DEL INICIO
  fill(144,166,61);//Color verde para el texto 1en valor RGB
  textAlign(LEFT,BOTTOM);//Alinea el texto a la izquierda y desde abajo
  textStyle(NORMAL);//Texto normal 
  textSize(16);//Tamaño texto 
  text("Presiona 2 para comenzar",20, height-30);//Ubica el texto a 20 px del borde izquierdo y 30 px sobre el borde inferior

}


//PANTALLA HOMBRE
function pantallaExperiencia () {//Función propia que muestra la pantalla 2 (hombre)
  let verde = map(mouseX, 0, width,130,200);//map para que posicion del mouse se refleje en intensidad del color
  
  background(144,verde,61);//color verde que cambia según la posición del mouse

  if(sonidoInterrupcion.isPlaying()) {//Si el sonido de interrupcion esta sonando
    sonidoInterrupcion.stop();//Lo detiene para que no suene en la pantalla del hombre
  }

  if(mouseIsPressed) {//Si el mouse está presionado
    if(!sonidoAplausos.isPlaying()) {//Si los aplausos todavía no estan sonando
      sonidoAplausos.loop();//Reproduce los aplausos en loop
    }
  } else {//Si el mouse no esta presionado
    if(sonidoAplausos.isPlaying()) {//Si los aplausos están sonando
      sonidoAplausos.stop();//Detiene el sonido de aplausos
    }
  }

  //Se van alternando las dos imágenes de la boca del hombre
  if (frameCount % 30 < 15) {//Durante la primera mitad del ciclo muestra la primera imagen
    image(foto1, width/2, height/2, 300, 300);//Muestra la foto1 al centro
  } else {//Durante la segunda mitad del ciclo muestra la segunda imagen
    image(foto2, width/2, height/2 + ajusteFoto2Y, 300, 300); //muestra la foto2 ajustada en Y
  }
    
    ondas();//Dibuja las ondas encima de la boca

    if(mouseIsPressed) {//Si el mouse está presionado
      lluviaAplausos();//Muestra la lluvia de aplausos
    }

//INSTRUCCIONES PANTALLA 2
fill(0);//Color negro para el texto
noStroke();//Sin borde
textStyle(NORMAL);//Texto normal
textSize(16);//Tamaño texto
textAlign(LEFT,TOP);//Alinear arriba a la izquierda
text("Presiona clic para validar",35,35);//

fill(250,0,0);//Color rojo para el texto
  noStroke();//Sin borde
textAlign(RIGHT,BOTTOM);//Alinear abajo a la derecha
text("Presiona 3 para continuar",width-35, height-35);//
  
  }

  //LLUVIA APLAUSOS
  function lluviaAplausos() {//Función que recorre y activa todas las partículas de aplausos
    for (let i = 0; i < aplausos.length; i ++) {//Bucle que recorre todos los elementos guardados en el array aplausos
      aplausos[i].mover();//Ejecuta la función mover() de cada aplauso para que caiga hacia abajo
      aplausos[i].mostrar();//Ejecuta la función mostrar() de cada aplauso para dibujarlo en la pantalla
    }
  }


  
  //PANTALLA MUJER 
function pantallaExperiencia2() {//Función propia que muestra la pantalla 3 (mujer) 
  background(255,230,230);//Color rosado para el fondo en valor RGB
  
  if(sonidoAplausos.isPlaying()) {//Si el sonido de aplausos está sonando
    sonidoAplausos.stop();//Lo detiene para que no suene en la pantalla de la mujer
  }

  if(mouseIsPressed) {//Si el mouse está presionado
    background(255,0,0);//Cambia el fondo a rojo intenso

    if(!sonidoInterrupcion.isPlaying()) {//Si el sonido de interrupcion no está sonando
      sonidoInterrupcion.loop();//Reproduce el sonido de interrupcion en loop
    }

    //INTERRUPCIÓN
    interrupcionVisual();//Muestra las figuras de interrupción
  } else {//Si el mouse no está presionado
    if (sonidoInterrupcion.isPlaying()){//Si el sonido de interrupcion está sonando
      sonidoInterrupcion.stop();//Detiene el sonido de interrupción
    }
  }

  let movimientoX = 0;//Variable para mover la boca horizontal
  let movimientoY = 0;//Variable para mover la boca vertical

  if(mouseIsPressed) {//Si el mouse esta presionado 
    movimientoX = random(-16,16);//Genera movimiento aleatorio horizontal
    movimientoY = random(-16,16);//Genera movimiento aleatorio vertical
  }

  let imagenActual; // variable que guarda que imagen de la mujer se mostrará

//alterna entre las dos imagenes 
   if (frameCount % 30 < 15) {// cambia la imagen en un tiempo de 30 frames, 15 muestra foto3 y 15 la foto4
     imagenActual= foto3;//Selecciona la primera imagen de la mujer
   } else {//Durante la otra parte del tiempo muestra foto4
     imagenActual = foto4;//Selecciona la segunda foto de la mujer
   }

  image(
    imagenActual,//Imagen seleccionada por la condición anterior
    width/2 + movimientoX,//Posición horizontal centrada de la imagen
    height/2 + movimientoY,//Posición vertical centrada de la imagen
    330,330);//Ancho y alto de la imagen

  //ONDAS
  ondas();//Dibuja las ondas sobre la boca

//Instrucciones pantalla 3
  fill(0);//Color negro para el texto
  noStroke();//Sin borde
  textStyle(NORMAL);//Texto normal
  textSize(16);//Tamaño texto
  textAlign(LEFT,TOP);//Alinear esquina arriba a la izquierda
  text("Haz clic para interrumpir",35,35);//Indica 


  textAlign(RIGHT,BOTTOM);//Alinear abajo a la derecha
  text("Presiona r para volver al inicio", width-35,height-35);//
}

  //FIGURAS DE INTERRUPCIÓN
  //Rectangulos
  function interrupcionVisual() {//Función propia que dibuja los elementos visuales de interrupción
fill(255,0,0,70); //Color rojo transparentado 
    noStroke();//Sin borde
    rect(0,0,width,height);//Rectángulo que cubre toda la pantalla desde la esquina superior izqueirda

    fill(0);//Color negro para los rectángulos
    for (let i = 0; i < 7; i++) {//Bucle que repite 7 veces la creación de rectángulos 
      let x = random(width/2 -170, width/2 + 170);//posicion horizontal cerca del centro del canvas
      let y = random(height/2-130, height/2 +130);//posicion vertical cerca del centro del canvas
      let ancho = random(20,70);//Ancho aleatorio de cada rectángulo
      let alto = random(6,18);//Alto aleatorio de cada rectángulo

      rect(x,y,ancho,alto);//Dibuja cada rectñangulo negro en la posición y tamaño definidos arriba
    }

    //Circulos
    fill(255);//Color blanco para los círculos
    for (let i = 0; i < 18; i++) {//Bucle que repite 18 veces la creación de círculos
      let x = random(width/2 -160,width/2 +160); //Posicion horizontal cercana al centro del canvas
      let y = random(height/2 - 130, height/2 + 130); //Posicion vertical cercana al centro del canvas
      let tamaño = random(4,9);//Tamaño aleatorio para cada círculo

      ellipse(x,y,tamaño,tamaño);//Dibuja cada círculo blanco en la posición y tamaño definidos arriba
    }
  }

  //PARA DETENER SONIDOS
  function detenerSonidos() {//Función propia que sirve para apagar todos los sonidos del sketch
    if (sonidoInterrupcion.isPlaying()) {//Revisa si el sonido de interrupción está sonando
      sonidoInterrupcion.stop();//Si está sonando, lo detiene
    }

    if (sonidoAplausos.isPlaying()) {//Revisa si el sonido de aplausos está sonando
      sonidoAplausos.stop();//Si está sonando, lo detiene
    }
  }

  //CAMBIAR ESTADOS
  function keyPressed() {//Función que detecta cuando el usuario presiona una tecla
    if (key === '1' || key === 'r') {//Si se presiona la tecla 1 o la recla r
      estado=0;//Cambia al estado 0 (pantalla de inicio)
      detenerSonidos();//Detiene los sonidos al volver al inicio
    }

    if (key === '2') {//Si se presiona la tecla 2
      estado=1;//Cambia al estado 1 (pantalla Experiencia, hombre)
      detenerSonidos();//Detiene los sonidos
    }

    if (key=== '3') {//Si se presiona la tecla 3
      estado=2;//Cambia al estado 2 (pantalla Experiencia2, mujer)
      detenerSonidos();//Detiene los sonidos
    }
  }

  //ADAPTAR EL CANVAS A LA VENTANA
  function windowResized() {//Función que se activa cuando cambia el tamaño de la ventana
    resizeCanvas(windowWidth,windowHeight);//Ajusta el canvas si se cambia el tamaño de la ventana 
  }








