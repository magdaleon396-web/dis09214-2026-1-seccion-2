SOLEMNE2 
-

PROBLEMÁTICA DE GÉNERO LLEVADA AL CÓDIGO 
-

*Julio Andree, Javiera Corral*
-
Para la solemne 2 de pensamiento computacional nos enfrentamos al desafío de seleccionar una problemática de género y transformar su significado y presencia a un sketch interactivo en la plataforma de P5.js. 
Nosotros como dupla decidimos trabajar con la problemática de  encasillar/ etiquetar a las personas según su apariencia. 

Encasillar / etiquetar personas según apariencias 
-
*Etiqueta (RAE): Calificación estereotipada y simplificadora.*

*Encasillar(RAE): Clasificar personas o hechos con criterios poco flexibles o simplistas.*

El problema con encasillar personas según su apariencia es la consecuencia de quitar o eliminar la diversidad y complejidad que posee el humano, remplazandola por etiquetas simples que promueven el pensamiento estereotipado de quienes nos perciben y de nosotros mismos.  Esto puede llevar a una crisis de identidad personal ya que al no sentirse de acuerdo con la etiqueta que otras personas te otorgan tendemos a sentir una desconexión con nuestro entorno y nosotros mismos.

las etiquetas en si no suelen ser del todo maliciosas pero al ser tan cerradas en su significado (gay, lesbiana, mujer, hombre, trans, etc.) resultan restrictivas y deshumanizantes. 

ejemplos:
-
pensar que una persona es mujer o usa pronombres femeninos solo por vestirse con vestidos y tener pelo largo o pensar que es hombre solo por vestir con pantalones y llevar el pelo estilizado de manera “masculina”.


<img width="273" height="272" alt="image" src="https://github.com/user-attachments/assets/6e405375-c861-4599-bd17-23b1362c5d50" />
<img width="424" height="281" alt="image" src="https://github.com/user-attachments/assets/b949ec00-25cf-4921-9924-c7474dcb8ae0" />


"La diversidad nos aporta riqueza en todos los sectores y ámbitos de nuestra vida. Sin embargo, en numerosas ocasiones, por simplificar tendemos a “etiquetar” a las personas dentro de una determinada categoría que los define de una manera concreta, a etiquetarlos con unas características inamovibles y concretas. Al actuar de esta manera, muchas veces inconsciente, no tenemos en cuenta que estamos limitando nuestra percepción de los demás, perdiéndonos toda la complejidad de las personas, sus matices y en definitiva, toda esa riqueza que aporta la diversidad."
*Fragmento extraído de:[divem.accem.es]( https://divem.accem.es/problema-encasillar-personas/)*

IDEA DEL SKETCH
-

*• Descripción objetiva*
-
¿Qué es el proyecto? 

Nuestro proyecto es un código creado en la plataforma de p5.js que tiene como función etiquetar individuos en diferentes identidades sexuales predeterminadas que pueden o no ser acertadas a la realidad.

¿Qué se ve en pantalla? 

la pantalla del sketch muestra la cámara del computador que detecta la cara del individuo frente a ella y le designa una bandera de la comunidad LGBTQ+. al aparecer la opción de la bandera trans la imagen será seguida por confeti que cae de manera oscilante sobre el lienzo mientras el texto "¡¡¡¡¡¡¡¡ES TRANS!!!!!!!!" aparece en la parte superior de la pantalla.

¿Qué elementos visuales aparecen? 

la cámara donde se aprecia la cara del usuario, la bandera LGBTQ+ que se posiciona sobre su frente, el texto que determina la identidad en un solo caso resultante (el de la bandera trans) y el confetti que celebra el resultado (el confetti solo aparece en el caso de que se muestra la bandera trans).

*• Descripción conceptual*
-
Idea central del proyecto y su relación con el sistema diseñado?

Para nuestro sketch nos centraremos en explorar la idea de determinación de identidad sexual tomando las características de diferentes etiquetas e implementarlas en una especie de selección aleatoria. el usuario deberá interactuar para ser encasillado en alguna categoría la cual puede o no ser acertada. la respuesta que dé el usuario al sketch demostrará nuestro pensar sobre la problemática tratada. 

Buscamos con el sketch hacer que el usuario se sienta minimizado a una sola identidad por culpa de un sistema invisible que no pueden controlar. Para esto pensamos implementar en nuestro sketch la cámara para detectar la cara del usuario y utilizando imágenes de las banderas de la comunidad LGBTQ+ seguidas por textos que reafirman la etiqueta seleccionada aleatoriamente por el programa el usuario tendrá el resultado pegado a su frente sin poder deshacerse de él dejando al usuario satisfecho o no con su resultado eso no importa ya que el código no está hecho para tener las emociones humanas en cuenta y el usuario llevará el peso internalizado de la etiqueta que se le asignó.

Para crear ese resultado decidimos crear un sketch algo cómico que demuestre diferentes banderas LGBTQ+ que representan las etiquetas que la sociedad le determina  de manera superficial o algo discriminatoria a cualquier ser humano sin importar su compleja personalidad e identidad, más allá de lo que se ve a simple vista. 

Para crear una sensación de aminorar el sentir o "pasa allevar" que un individuo encasillado puede experimentar se implementa en el código partículas de confeti que acompañan al resultado y le agregan un pequeño morbo a la deshumanización de etiquetar al usuario.

*• Referentes*
-
nuestra mayor inspiración fueron los filtros de tiktok que determinaban qué bandera LGBTQ+ era la persona en pantalla. la mayoría de veces representaban al usuario de manera errónea y en los videos se nos demostraba la emoción que el usuario posee al inicio cambiar. el usuario puede animarse, decaer o hasta indignarse por el resultado adquirido.

<img width="247" height="443" alt="image" src="https://github.com/user-attachments/assets/d2c9a284-76a1-478e-a476-f5c84ba3b766" />

<img width="253" height="449" alt="image" src="https://github.com/user-attachments/assets/34c2bb97-86c1-4cda-a387-33df6af95908" />



FaceMesh de la biblioteca ml5js : utilizamos este referente para lograr mapear la cara del sujeto.
[biblioteca ml5js](https://docs.ml5js.org/#/reference/facemesh?id=methods) 

<img width="355" height="311" alt="image" src="https://github.com/user-attachments/assets/49dfaff0-da30-412f-a70b-9e6654561eb1" />


[Código que se utilizó de base para el confeti](https://editor.p5js.org/aceschen/sketches/A1Yn7XDc8)

```
let confetti = [];

function setup() {
  createCanvas(400, 400);
  rectMode(CENTER);
  for (let i = 0; i < 100; i++) {
    let col = color(random(100, 255), random(100, 255), random(100, 255), random(120, 240));
    confetti[i] = new Confetto(random(width), random(0, 30), random(10, 20), col);
  }
}

function draw() {
  background(0);
  for (let c of confetti) {
    c.move();
    c.display();
  }
}

class Confetto {
  constructor(_x, _y, _s, _c) {
    this.x = _x;
    this.y = _y; 
    this.size = _s;
    this.color = _c;
    this.shape = round(random(0, 1));
    this.speed = random(0.5, 2);
    this.time = random(1, 100);
    this.amp = random(2, 30);
  }
  
  display() {
    push();
    noStroke();
    fill(this.color);
    translate(this.x, this.y);
    translate(this.amp*cos(this.time), this.amp*sin(this.time));
    rotate(this.time);
    scale(cos(this.time), sin(this.time));
    if (this.shape == 1) {
      ellipse(0, 0, this.size);      
    } else {
      rect(0, 0, this.size, this.size/2);
    }
    pop();
  }
  
  move() {
    this.y += this.speed;
    this.speed += 0.005;
    this.time += 0.05;
    if (this.y > height) {
      this.y = 0;
      this.speed = random(0.5, 2);
    }
  }
}
```
<img width="305" height="296" alt="image" src="https://github.com/user-attachments/assets/a9f9113a-2624-409e-9c4e-124ce91226bb" />


DIAGRAMA DE FLUJO
-
[link diagrama de flujo](https://canva.link/aw432ebcl03r7xk) 
<img width="1920" height="1080" alt="diagrama de flujo A_C" src="https://github.com/user-attachments/assets/a9796842-1bc0-4228-ae23-65988de64d0d" />


NUESTRO PROYECTO: label Maker
-
[Label Maker](https://editor.p5js.org/StarBerryChiscake/sketches/9coSmJDBw) 


``` 
let video; //Variable que guarda la cámara que vamos a utilizar.
let faceMesh; //Variable que guardar el modelo de IA (Facemesh) de ml5js.
let options = { maxFaces: 1, refineLandmarks: false, flipped: false }; // Configuración del reconocimiento facial, reconoce solo una cara (maxFaces), no busca detalles avanzados(refineLandmarks) y no voltea la imagen de la cámara (flipped).
let faces = []; //Base de datos donde la IA guardará las coordenas del rostro.
let imagenesBanderas = []; //Lista para guardar las imagenes que subimos a files.
let banderaSeleccionada; ////Variable que guardará la imagen de la bandera que se esta mostrando en la pantalla.
let confetti = []; // Lista para almacenar todas las partículas de confeti en una sola variable.
let cantidadConfeti = 100; // Cantidad de partículas que caerán en la pantalla.

function preload() {
  //Funcion para cargar los archivos antes de iniciar.
  faceMesh = ml5.faceMesh(options); //Inicializamos el modelo faceMesh de ml5js y dandole las configuraciones que guardamos en el let options.
  //Cargamos las banderas
  imagenesBanderas[0] = loadImage("banderalgbt.png");
  imagenesBanderas[1] = loadImage("banderal.png");
  imagenesBanderas[2] = loadImage("bandera3.png");
  imagenesBanderas[3] = loadImage("banderagay.png");
  imagenesBanderas[4] = loadImage("banderalesb.png");
}

function setup() {
  // Función que se ejecuta solo una.
  createCanvas(640, 480); //Crea un lienzo de 640 x 480.
  rectMode(CENTER);

  //Bucle (loop) que se va a repetir exactamente 100 veces (desde i = 0 hasta i = 99).
  for (let i = 0; i < cantidadConfeti; i++) {
    //Crea un color aleatorio para el confeti actual. Formato RGBA (Rojo, Verde, Azul, Alfa/Transparencia).
    let col = color(
      random(100, 255),
      random(100, 255),
      random(100, 255),
      random(120, 240)
    );
    confetti[i] = new Confetto(
      random(width),
      random(-50, 0),
      random(10, 20),
      col
    ); //En la posición i de nuestra lista, guardamos un "nuevo" objeto de la clase Confetto (que está definida más abajo). Le pasa cuatro datos al azar (Argumentos): Una posición X cualquiera dentro del ancho del lienzo (random(width)). Una posición Y inicial cerca del borde superior (random(0, 30)). Un tamaño entre 10 y 20 píxeles. El color(col) que acabamos de calcular.
  }
  video = createCapture(VIDEO); //Activa la cámara web del usuario.
  video.size(640, 480); //Configuramos la resolución del video para que coincida con el lienzo.
  video.hide(); // Sirve para ocultar el video original que p5js crea por defecto abajo del lienzo.
  faceMesh.detectStart(video, gotFaces); //Empezamos a decirle a ml5js que analice el video continuamente y cuando detecte un rostro llamará a la función "gotFaces" para darnos los datos.
  banderaSeleccionada = random(imagenesBanderas); //Con random se selecciona una bandera aleatoria de nuestra lista.
}

function gotFaces(result) {
  //Función de respuesta de la IA, result contiene toda la información que recopiló la IA de ml5js.
  faces = result; //Guardamos los resultados dentro de la variable faces para usarlas en nuestro draw.
}

function draw() {
  //Función Draw que se ejecuta a 60fps de forma continua.
  image(video, 0, 0, width, height); //Dibuja el video de la cámara en el lienzo cubriendo todo el espacio con width y height.

  if (banderaSeleccionada === imagenesBanderas[1]) {
    //Si el archivo de la banderaSeleccionada que se muestra es el que guardamos en la posición 1 ("banderal.png"), Si la condición se cumple, va hacía la configuración del confetti y  dibuja cada partícula en la pantalla.

    for (let c of confetti) {
      c.move();
      c.display();
    } //Bucle for, lee la lista de confetis uno por uno (llamando temporalmente c a cada uno) y les ordena hacer dos tareas que tienen definidas en su clase: Actualizar su posición (move()) y dibujarse en la pantalla (display()).

    //Texto en la pantalla.
    push(); // Aislamos los estilos del texto para que no afecten a otros dibujos.
    fill(255); // Color de la letra blanco.
    stroke(0); // Borde negro.
    strokeWeight(4); // Grosor del borde de la letra.
    textSize(42); // Tamaño de la letra.
    textAlign(CENTER, TOP); // Centra el texto horizontalmente y lo alinea desde el borde superior.
    text("¡¡¡¡¡¡¡¡ES TRANS!!!!!!!!", width / 2, 40); // Dibuja el texto en la mitad del ancho y a 40 píxeles de la parte superior.    
    square(90, 67,20); //Figura para hacer un cuadrado
    quad(560, 48, 548, 62, 560, 76, 572, 62); //Cuadrilatero para realizar un rombo.
    pop(); //Encapsular nuestra configuración para el texto.
  }

  for (let i = 0; i < faces.length; i++) { // let 1 es el primer valor que tiene el computador, al no haber nadie frente a la cámara i vale 0 y como 0 < 0(faces.length) la condición es false y no se ejecuta nada.Si hay alguien frente a la cámara i pasa a valer 1 y como 0 < 1(faces.length) la condición es verdadera y se ejecuta el programa.
    let face = faces[i]; // Toma el rostro que se está analizando de la lista faces y lo guarda en la variable face.

    if (face.keypoints && face.keypoints[9]) {
      //Determinamos la posición de la frente de la cara que según la biblioteca de ml5js se encuentra en el número 9.
      let xRostro = face.keypoints[9].x; //Creamos la variable let xRostro para guardar la posición horizontal de la cara. Con ".x" le pedimos al punto 9 su valor en el eje X; a cuántos pixeles de distancia se encuentra la frente desde el borde horizontal de la pantalla.
      let yRostro = face.keypoints[9].y; //Creamos la variable let yRostro para guardar la posición vertical de la cara. Con ".y" le pedimos al punto 9 su valor en el eje Y; a cuántos pixeles de distancia se encuentra la frente desde el borde vertical de la pantalla.

      let anchoBandera = 120; //Determinamos el ancho de nuestra bandera.
      let altoBandera = 80; //Determinamos el alto de nuestra bandera.

      image(
        banderaSeleccionada, //Dibujamos la bandera seleccionada sobre el video
        xRostro - anchoBandera / 2, //Desplazamos la imagen a la izquierda a la mitad de su ancho para que quede centrada en el eje x, al restarle la mitad la bandera se centra con el centro de nuestra frente.
        yRostro - 100, //Restamos 100 pixeles en el eje Y para que la bandera se posicione por encima de los ojos.
        anchoBandera, //Le asignamos el ancho ya definido en let anchoBandera
        altoBandera //le asignamos el alto ya definido en let altoBandera.
      );
    }
  }
}

function mousePressed() {
  banderaSeleccionada = random(imagenesBanderas); //Cada que el usuario de click el código muestra una bandera al azar.
}

//Configuración del confetti
class Confetto {
  //class: es una plantilla o molde para crear objetos. Te permite empaquetar variables (datos) y funciones (comportamientos) juntos. Define qué propiedades tiene cada confetti y qué debe hacer.
  constructor(x, y, s, c) {
    //This es una referencia al objeto actual en el que se está ejecutando el código. Permite diferenciar entre una variable global y la propiedad específica de un objeto individual.
    this.x = x; //Punto x del confetti.
    this.y = y; //Punto y del confetti.
    this.size = s; //Tamaño del confetti.
    this.color = c; // Color del confetti.
    this.shape = round(random(0, 1)); //Elige al azar si el confeti será un círculo o un rectángulo. random(0, 1) da un decimal como 0.3 o 0.7, y round() lo redondea al entero más cercano (o 0 o 1).
    this.speed = random(0.5, 2); //Define qué tan rápido va a caer hacia abajo el confeti.

    //Variables matemáticas para el balanceo estético.
    this.time = random(1, 100); //Contador que avanzará constantemente.
    this.amp = random(2, 30); //(amplitud) define qué tan amplio será el "vaivén" u oscilación horizontal y vertical del confeti al caer.
  }

  display() {
    //Apariencia del confetti.
    push(); //Inicio grupo de dibujo aislado.
    noStroke(); //Sin relleno.
    fill(this.color); //Relleno.
    translate(this.x, this.y); //Traslación de figura en x,y.
    translate(this.amp * cos(this.time), this.amp * sin(this.time)); //Desplaza un poco más el origen usando trigonometría. Al combinar el coseno (cos) y el seno (sin) con el tiempo que avanza, el confetti no cae en línea recta, sino que se mueve haciendo órbitas circulares o elípticas en el aire, imitando cómo flota el papel real.
    rotate(this.time); //Rotación del confetti sobre su propo eje usando el contador time.
    scale(cos(this.time), sin(this.time)); //Escala visual en los ejes x e y usando ondas mecánicas. Como el coseno y el seno oscilan entre -1 y 1, provoca un efecto visual muy genial donde el confeti parece "aplanarse" y "estirarse".
     
    if (this.shape == 1) {
      //Si la propiedad shape es igual a 1, dibuja un círculo (ellipse). Si no, dibuja un rectángulo (rect) cuya altura es la mitad de su ancho.
      ellipse(0, 0, this.size); //dibuja un circulo en las cordenadas 0,0 del tamaño de la propiedad size.
    } else {
      //de lo contrario
      rect(0, 0, this.size, this.size / 2); //dibuja una rectangulo con ancho size y altura size/2.
      
    } 
    pop(); //Fin grupo de dibujo aislado.
  }

  move() {
    //Movimiento del confetti.
    this.y += this.speed; //Aumenta la posición y del confeti según su velocidad actual, lo que hace que caiga hacia abajo.
    //fUNCIÓN MAP
    let gravedadDinamica = map(this.y, 0, height, 0.002, 0.015); //map toma la posición y (this.y) y la combierte a un valor de ravedad dinámica.
    this.speed += gravedadDinamica; 
    this.time += 0.05; //Velocidad de los giros del confeti.
    if (this.y > height) {
      //Si la propiedad this.y es mayor a la altura del canvas.
      this.y = random(-20, 0); //this.y es igual a 0.
      this.x = random(width);
      this.speed = random(0.5, 2); //this.speed es igual a un valor aleatorio entre 0,5 y 2
    }
  }
}
```

explicación de nuestro sistema:
-

• ¿Cuál es la regla de oro de tu sistema?

el codigo que creamos funciona en base al reconocimiento facial de el usuario que interactua con el programa y en base a ese reconocimeinto arroja una bandera lGBTQ+ al azar que representa la etiqueta que se le otorga al usuario en base a su "apariencia" (detectar rostro = etiqueta de identidad).

• ¿Cómo se relaciona esta lógica con la problemática de género elegida?

con esta logica podemos representar como la sociedad simplifica al usuario a un simple objeto para detectar visualmente y ser "juzgado" por su apariencia la cual despues es analizada y etiquetada, deshumanizando al usuario. 
• Input / Output y sistema

¿Qué datos entran? (INPUT) *reconocimiento facial del usuario y click a la pantalla.*
¿Qué respuesta visual producen? (OUTPUT) *se clasifica con una bandera LGBT al detectar tu rostro o cambia con el click del mouse.*

• Pensamiento computacional

Reglas que gobiernan el sistema (inputs, procesos, outputs)
Explicación del sistema de interactividad 
*el programa al detectar el rostro del usuario empieza a seleccionar una imagen de la bandera LGBT aleatoria la cual se queda pegada a la frente de este con la opcion de presionar el mouse y obtener otro resultado de imagen.*
